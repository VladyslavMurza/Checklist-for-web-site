# 05. Design wizualny

## 1. Siatka i odstępy
- Siatka kolumn: desktop **12 kolumn**, tablet **8**, telefon **4** (Layout Grid w Figmie).
- Marginesy boczne: telefon 16–24 px, desktop wg kontenera (np. max 1200 px).
- System odstępów oparty na **8 px** (4, 8, 16, 24, 32, 48, 64…) — spójność.
- Wyrównanie elementów do siatki, dużo „białej przestrzeni” (whitespace).
- W Figmie: **Auto Layout** + ustawione Constraints → łatwe przeniesienie na RWD.

## 2. Typografia
- Maks. **2 kroje pisma** (np. jeden do nagłówków, jeden do tekstu).
- Skala typograficzna (np. 16 / 20 / 24 / 32 / 40 / 48 px) — zawsze te same rozmiary.
- Tekst podstawowy 16–18 px, interlinia 1.5, długość linii 50–75 znaków (Baymard).
- Tekst do lewej (nie justowany na stronach — „rzeki” spacji).
- Fonty webowe: max 2–3 grubości, format WOFF2, `font-display: swap`.

## 3. Kolory
- Paleta: **kolor główny (brand)**, akcent (CTA), neutralne (tła, tekst), semantyczne (sukces – zielony, błąd – czerwony, ostrzeżenie – żółty/pomarańczowy, info – niebieski).
- Zasada **60-30-10** (60% tło/neutralny, 30% kolor drugorzędny, 10% akcent).
- Kontrasty zgodne z WCAG (4.5:1 tekst, 3:1 elementy UI).
- Czysta czerń #000 na bieli może męczyć — często używa się ciemnoszarego (#1a1a1a – #222).
- Opcjonalnie tryb ciemny (`prefers-color-scheme`).
- W Figmie: kolory jako **Variables / Styles**, nie wpisywane ręcznie.

## 4. Hierarchia wizualna
- Najważniejsze = największe, najbardziej kontrastowe, najwyżej.
- Rozmiar, grubość, kolor, odstęp — narzędzia do wskazania ważności.
- Test „zmrużonych oczu”: czy po rozmyciu nadal widać, co najważniejsze i gdzie jest CTA?

## 5. Spójność — mini design system
- Komponenty: przycisk (warianty + stany), pole formularza, karta, menu, stopka, modal, alert.
- Każdy komponent ze stanami: default / hover / focus / active / disabled / error.
- Ikony z jednej rodziny (ten sam styl i grubość linii).
- Zaokrąglenia, cienie, obramowania — jednolite w całym projekcie.
- Zdjęcia w jednym stylu (kolorystyka, kadrowanie).

## 6. Grafika i obrazy
- Wysoka jakość, ale zoptymalizowane (patrz 06_wydajnosc.md).
- Ikony i logo jako **SVG**.
- Prawa do zdjęć/fontów/ikon (licencje!) — darmowe źródła: Unsplash, Pexels, Google Fonts.
- Favicon (+ ikona dla urządzeń Apple / PWA).

## ⚠️ Typowe błędy
- Za dużo kolorów i fontów.
- Każdy przycisk wygląda inaczej.
- Szary jasny tekst na białym tle (za słaby kontrast).
- Brak odstępów — wszystko „sklejone”.
- Projekt w Figmie bez Auto Layout i stylów → trudny do przeniesienia do kodu.
