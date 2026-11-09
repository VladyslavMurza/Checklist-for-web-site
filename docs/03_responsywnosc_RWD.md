# 03. Responsywność (RWD) — dopasowanie do różnych urządzeń

## 1. Podstawy
- **RWD (Responsive Web Design)** — jedna strona, która płynnie dopasowuje układ do szerokości ekranu.
- **Mobile first** — najpierw CSS dla telefonu, potem `@media (min-width: …)` dodaje układ dla większych ekranów.
  Dlaczego: większość ruchu to telefony, a Google indeksuje wersję mobilną (mobile-first indexing).
- Obowiązkowy tag w `<head>`:
  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1">
  ```
  ⚠️ NIE dodawaj `user-scalable=no` ani `maximum-scale=1` — blokuje powiększanie, łamie WCAG.

## 2. Breakpointy (punkty przełamania)

Typowe wartości (np. Tailwind / Bootstrap):

| Nazwa | Szerokość | Urządzenie (orientacyjnie) |
|---|---|---|
| bazowy | < 640 px | telefony (projektuj od ok. 360 px, min. 320 px) |
| sm | ≥ 640 px | duże telefony, poziomo |
| md | ≥ 768 px | tablety pionowo |
| lg | ≥ 1024 px | tablety poziomo, małe laptopy |
| xl | ≥ 1280 px | laptopy, monitory |
| 2xl | ≥ 1536 px | duże monitory |

- Zasada: **breakpoint tam, gdzie „psuje się” treść**, a nie pod konkretny model telefonu.
- W Figmie zwykle robi się 3 makiety: **mobile 360/375/390 px, tablet 768 px, desktop 1440 px** (treść max ~1200–1320 px szerokości).

```css
/* mobile first */
.grid { display: grid; grid-template-columns: 1fr; gap: 16px; }

@media (min-width: 768px)  { .grid { grid-template-columns: repeat(2, 1fr); } }
@media (min-width: 1024px) { .grid { grid-template-columns: repeat(3, 1fr); } }
```

## 3. Płynny układ
- Jednostki względne: `%`, `rem`, `em`, `vw`, `fr` zamiast sztywnych `px` dla szerokości.
- **Flexbox** (układ w jednym kierunku: menu, rzędy kart) i **CSS Grid** (siatki, całe układy).
- `max-width` dla kontenera treści, np. `max-width: 1200px; margin: 0 auto; padding: 0 16px;`.
- Długość linii tekstu: ok. **50–75 znaków** (czytelność, wg Baymard Institute) → `max-width: 65ch`.
- **Container queries** (`@container`) — komponent dopasowuje się do szerokości rodzica, a nie ekranu (obsługa we wszystkich nowoczesnych przeglądarkach).

## 4. Płynna typografia
```css
html { font-size: 100%; } /* 16px, szanuje ustawienia użytkownika */
h1 { font-size: clamp(1.75rem, 1.2rem + 2.5vw, 3rem); }
body { font-size: clamp(1rem, 0.95rem + 0.25vw, 1.125rem); line-height: 1.5; }
```
- Tekst podstawowy min. **16 px** na telefonie (mniejszy → iOS powiększa formularze przy kliknięciu).
- Rozmiary czcionek w `rem`, nie w `px` — żeby działało powiększanie tekstu w przeglądarce.

## 5. Obrazy i multimedia
```css
img, video { max-width: 100%; height: auto; }
```
- Zawsze atrybuty `width` i `height` w `<img>` → brak „skakania” strony (CLS).
- `srcset` + `sizes` — przeglądarka pobiera obraz w rozmiarze pasującym do ekranu.
- `<picture>` — inny kadr na telefon / formaty AVIF → WebP → JPG.
- `loading="lazy"` dla obrazów poniżej pierwszego ekranu (ale NIE dla głównego zdjęcia hero).
- Wideo: responsywny kontener `aspect-ratio: 16 / 9;`.

## 6. Dotyk i telefony
- Cele dotykowe min. **44×44 px** (Apple), **48×48 dp** (Google/Material), z odstępem ~8 px. Minimum WCAG 2.2 AA: 24×24 px.
- Brak hover na telefonie — nic ważnego nie może być dostępne *tylko* po najechaniu myszką.
- Ważne akcje w zasięgu kciuka (dół ekranu na dużych telefonach).
- Działa w orientacji pionowej i poziomej (WCAG 2.1: 1.3.4).
- Numery telefonów jako linki `tel:`, e-maile jako `mailto:`.
- Tabele na telefonie: przewijanie poziome w kontenerze lub zamiana na karty.
- Brak przewijania całej strony w poziomie (WCAG 1.4.10 Reflow — strona działa przy szerokości 320 px).

## 7. Co się zmienia między wersjami (przykład)

| Element | Telefon | Tablet | Desktop |
|---|---|---|---|
| Menu | hamburger | hamburger lub pełne | pełne poziome |
| Kolumny kart | 1 | 2 | 3–4 |
| Hero | tekst nad zdjęciem / pod | obok lub nad | tekst obok zdjęcia |
| Stopka | kolumny jedna pod drugą (bez zwijania w akordeon) | 2 kolumny | 4 kolumny |
| Formularz | pola na całą szerokość | 1–2 kolumny | 2 kolumny |

## ⚠️ Typowe błędy
- Projekt tylko na desktop, potem „ściskanie” na telefon.
- Za mały tekst i przyciski zbyt blisko siebie.
- Obrazy 4000 px ładowane na telefonie.
- Elementy wychodzące poza ekran (poziomy scroll).
- Blokowanie zoomu.
- Testowanie tylko w trybie „device” w przeglądarce, bez prawdziwego telefonu.
