# Jak ma wyglądać i działać strona internetowa — baza wiedzy

Materiał zebrany jako podstawa do późniejszej checklisty (stan: listopad 2026).

## Pliki

| Plik | Temat |
|---|---|
| 01_struktura_strony.md | Z czego składa się strona: header, nawigacja, treść, stopka, architektura informacji |
| 02_UX_i_funkcjonowanie.md | Jak strona ma działać: 10 heurystyk Nielsena, formularze, CTA, stany |
| 03_responsywnosc_RWD.md | Dopasowanie do telefonów, tabletów i komputerów |
| 04_dostepnosc_WCAG.md | WCAG 2.0 (+ co doszło w 2.1 i 2.2), kontrast, klawiatura, alt |
| 05_design_wizualny.md | Typografia, kolory, siatka, spójność (design system) |
| 06_wydajnosc.md | Szybkość ładowania, Core Web Vitals, obrazy |
| 07_SEO.md | Widoczność w Google: meta, nagłówki, adresy URL, mapa strony |
| 08_bezpieczenstwo_i_prawo.md | HTTPS, RODO, cookies, Europejski Akt o Dostępności |
| 09_testowanie_i_narzedzia.md | Czym i jak sprawdzać stronę przed oddaniem |
| 10_zrodla.md | Linki do źródeł |
| 11_marketing_i_konwersja.md | Strona ma zarabiać: cel, lejek, propozycja wartości, landing page, zaufanie, koszyk |
| 12_CTA.md | Wezwanie do działania: typy, tekst, wygląd, rozmieszczenie, testy |
| 13_analityka_i_testy.md | KPI, GA4, linki UTM, testy A/B |
| 14_zrodla_marketing_polecane.md | Źródła polecane przez designerów i marketerów |

## Najważniejsze w 10 punktach

1. Użytkownik w kilka sekund ma wiedzieć: **gdzie jest, co tu jest, co może zrobić**.
2. Stały, przewidywalny układ: logo → menu → treść → stopka, na każdej podstronie tak samo.
3. **Mobile first** — najpierw projekt na telefon, potem rozszerzanie na większe ekrany.
4. Tag `<meta name="viewport" content="width=device-width, initial-scale=1">` — bez niego RWD nie działa.
5. Kontrast tekstu min. **4.5:1** (duży tekst 3:1) — WCAG AA.
6. Cała strona obsługiwana **samą klawiaturą**, z widocznym fokusem.
7. Każdy obrazek z treścią ma **alt**, każde pole formularza ma **label**.
8. Szybkość: **LCP < 2.5 s, INP < 200 ms, CLS < 0.1**.
9. HTTPS, polityka prywatności, baner cookies z równorzędnym „Odrzuć”.
10. Testy na prawdziwych urządzeniach + automatyczne (Lighthouse, WAVE, axe).
