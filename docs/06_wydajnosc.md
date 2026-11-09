# 06. Wydajność — szybkość strony

Wolna strona = ucieczka użytkownika i gorsza pozycja w Google.

## 1. Core Web Vitals (Google) — progi

Mierzone dla **75% odwiedzin** (75. percentyl), osobno dla telefonu i komputera.

| Wskaźnik | Co mierzy | Dobrze | Do poprawy | Źle |
|---|---|---|---|---|
| **LCP** – Largest Contentful Paint | Kiedy załaduje się największy element (zwykle zdjęcie hero / nagłówek) | ≤ 2.5 s | 2.5–4 s | > 4 s |
| **INP** – Interaction to Next Paint | Jak szybko strona reaguje na kliknięcie/dotyk (od 2024 zastąpił FID) | ≤ 200 ms | 200–500 ms | > 500 ms |
| **CLS** – Cumulative Layout Shift | Czy elementy „skaczą” podczas ładowania | ≤ 0.1 | 0.1–0.25 | > 0.25 |

Pomocnicze: TTFB (czas odpowiedzi serwera, dobrze ≤ 0.8 s), FCP (pierwsza treść, dobrze ≤ 1.8 s).

## 2. Jak poprawić

### Obrazy (zwykle największy problem)
- Formaty **WebP / AVIF**, JPG jako zapas.
- Właściwy rozmiar (nie 4000 px do miniatury), kompresja (Squoosh, TinyPNG).
- `srcset` / `sizes`, `loading="lazy"` poniżej pierwszego ekranu.
- Obraz hero: bez lazy, można dodać `fetchpriority="high"`.
- `width` i `height` (lub `aspect-ratio`) → brak skakania (CLS).

### Kod
- Minifikacja CSS/JS, usunięcie nieużywanego kodu.
- JS z `defer` / `async`, nie blokuje renderowania.
- Mniej zewnętrznych skryptów (czaty, trackery, widgety).
- Fonty: WOFF2, `font-display: swap`, preload głównego fontu, mało wariantów.

### Serwer
- Kompresja (gzip / Brotli), cache przeglądarki, HTTP/2 lub HTTP/3.
- CDN dla plików statycznych.
- Dobry hosting.

### Stabilność układu (CLS)
- Rezerwowanie miejsca na obrazy, reklamy, banery, embedy.
- Nie wstawiać treści nad już widoczną treścią (np. baner wsuwający się z góry).

## 3. Orientacyjny budżet
- Waga strony głównej najlepiej < 1–2 MB.
- Obraz hero < 200 KB.
- Liczba zapytań jak najmniejsza.

## ⚠️ Typowe błędy
- Wideo w tle na telefonie.
- Ciężkie slidery i biblioteki animacji dla jednego efektu.
- Niezoptymalizowane zdjęcia prosto z aparatu.
- Wiele fontów i grubości.
