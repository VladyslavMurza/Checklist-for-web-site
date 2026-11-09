# Mapowanie źródeł

Każda informacja z materiałów przypisana do źródła, z oceną wiarygodności. Wersja do przeglądania na GitHubie — ta sama treść jest w pliku `15_mapowanie_zrodel.xlsx` (z filtrami). Pełna lista źródeł: [`10_zrodla.md`](../docs/10_zrodla.md).

**Zmapowanych informacji:** 93 · **Źródeł:** 54 · 🟢 wysoka: 73 · 🟡 średnia: 16 · 🔴 niska: 4

## Kryteria oceny

| Ocena | Kiedy |
|---|---|
| 🟢 Wysoka | Źródło pierwotne (standard W3C, dokumentacja Google/Apple, akt prawny) lub organizacja publikująca badania (NN/g, Baymard, GOV.UK, CXL) |
| 🟡 Średnia | Blog firmy lub portalu branżowego — uznany, ale źródło wtórne lub częściowo promocyjne |
| 🔴 Niska | Brak jednego źródła — zasada praktyczna, opisywana jako konwencja |

## Spis

- [01. Struktura strony](#01-struktura-strony)
- [02. UX i funkcjonowanie](#02-ux-i-funkcjonowanie)
- [03. Responsywność (RWD)](#03-responsywność-rwd)
- [04. Dostępność (WCAG)](#04-dostępność-wcag)
- [05. Design wizualny](#05-design-wizualny)
- [06. Wydajność](#06-wydajność)
- [07. SEO](#07-seo)
- [08. Bezpieczeństwo i prawo](#08-bezpieczeństwo-i-prawo)
- [09. Testowanie](#09-testowanie)
- [11. Marketing i konwersja](#11-marketing-i-konwersja)
- [12. CTA](#12-cta)
- [13. Analityka](#13-analityka)

## 01. Struktura strony

Plik: `01_struktura_strony.md`

| Nr | Temat | Informacja | Źródło | Wiarygodność | Uwagi |
|---|---|---|---|---|---|
| 1 | Architektura informacji | Projekt zaczyna się od celu, grupy docelowej i mapy strony (sitemap) | [S08] [NN/g — Homepage Design: 5 Fundamental Principles](https://www.nngroup.com/articles/homepage-design-principles/) | 🟢 Wysoka |  |
| 2 | Header | Logo w lewym górnym rogu, klikalne, prowadzi do strony głównej | [S08] [NN/g — Homepage Design: 5 Fundamental Principles](https://www.nngroup.com/articles/homepage-design-principles/) | 🟢 Wysoka |  |
| 3 | Header | Menu główne w przewidywalnym miejscu, proste nazwy | [S06] [NN/g — 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) | 🟢 Wysoka | Heurystyka 4: spójność i standardy |
| 4 | Header | Sticky header nie może zasłaniać elementu z fokusem | [S03] [WCAG 2.2](https://www.w3.org/TR/WCAG22/) | 🟢 Wysoka | Kryterium 2.4.11 |
| 5 | Treść | Ludzie skanują tekst wzrokiem (wzorzec F) | [S10] [NN/g — F-Shaped Pattern of Reading](https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content/) | 🟢 Wysoka |  |
| 6 | Semantyczny HTML | Atrybut lang="pl" w znaczniku html | [S01] [WCAG 2.0 (rekomendacja W3C)](https://www.w3.org/TR/WCAG20/) | 🟢 Wysoka | Kryterium 3.1.1 |
| 7 | Semantyczny HTML | Link „Przejdź do treści” (pomijanie bloków) | [S01] [WCAG 2.0 (rekomendacja W3C)](https://www.w3.org/TR/WCAG20/) | 🟢 Wysoka | Kryterium 2.4.1 |
| 8 | Semantyczny HTML | Nagłówki H1–H6 w logicznej hierarchii, prawdziwe listy i etykiety | [S01] [WCAG 2.0 (rekomendacja W3C)](https://www.w3.org/TR/WCAG20/) | 🟢 Wysoka | Kryterium 1.3.1 |
| 9 | Zasada 3 kliknięć | Ważne treści nie głębiej niż 2–3 poziomy | [S51] Praktyka branżowa (brak jednego źródła) | 🔴 Niska | Brak potwierdzenia w badaniach — NN/g podważa sztywną „zasadę 3 kliknięć”; opisać jako orientacyjną |
| 10 | Footer | Użytkownicy przewijają do stopki celowo (kontakt, info o firmie) lub w ostateczności | [S53] [NN/g — Web Page Footers 101: Design Patterns](https://www.nngroup.com/articles/footers/) | 🟢 Wysoka |  |
| 11 | Footer | Linki użytkowe w stopce każdej strony: kontakt, obsługa klienta, polityka prywatności, regulamin | [S53] [NN/g — Web Page Footers 101: Design Patterns](https://www.nngroup.com/articles/footers/) | 🟢 Wysoka |  |
| 12 | Footer | Powtórzenie nawigacji (doormat) na długich stronach i na telefonie | [S53] [NN/g — Web Page Footers 101: Design Patterns](https://www.nngroup.com/articles/footers/) | 🟢 Wysoka |  |
| 13 | Footer | Mapa strony w stopce: cała do ok. 25 podstron, w dużych serwisach link do osobnej | [S53] [NN/g — Web Page Footers 101: Design Patterns](https://www.nngroup.com/articles/footers/) | 🟢 Wysoka |  |
| 14 | Footer | Elementy zaufania (opinie, nagrody) w stopce | [S53] [NN/g — Web Page Footers 101: Design Patterns](https://www.nngroup.com/articles/footers/) | 🟢 Wysoka |  |
| 15 | Footer | Nie zwijać treści stopki w domyślnie zamknięty akordeon | [S53] [NN/g — Web Page Footers 101: Design Patterns](https://www.nngroup.com/articles/footers/) | 🟢 Wysoka |  |
| 16 | Footer | Tylko potrzebne elementy, grupowanie z nagłówkami, spójne nazwy | [S54] [Uxcel — Footers best practices](https://app.uxcel.com/lessons/footers-best-practices-643) | 🟡 Średnia |  |
| 17 | Footer | Zapis na newsletter w stopce — stale widoczny, nienachalny | [S54] [Uxcel — Footers best practices](https://app.uxcel.com/lessons/footers-best-practices-643) | 🟡 Średnia |  |
| 18 | Footer | Link „Ustawienia cookies” — wycofanie zgody równie łatwe jak udzielenie | [S46] [RPMS — Czy Twoja strona www spełnia wymagania RODO? Checklista](https://rpms.pl/czy-twoja-strona-www-spelnia-wymagania-rodo-checklista-2025/) | 🟡 Średnia |  |
| 19 | Footer | Kontrast tekstu w stopce min. 4.5:1 | [S01] [WCAG 2.0 (rekomendacja W3C)](https://www.w3.org/TR/WCAG20/) | 🟢 Wysoka | Kryterium 1.4.3 |

## 02. UX i funkcjonowanie

Plik: `02_UX_i_funkcjonowanie.md`

| Nr | Temat | Informacja | Źródło | Wiarygodność | Uwagi |
|---|---|---|---|---|---|
| 20 | UX | 10 heurystyk użyteczności Nielsena | [S06] [NN/g — 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) | 🟢 Wysoka |  |
| 21 | Formularze | Placeholder nie zastępuje etykiety pola (label) | [S11] [NN/g — Placeholders in Form Fields Are Harmful](https://www.nngroup.com/articles/form-design-placeholders/) | 🟢 Wysoka |  |
| 22 | Formularze | Atrybut autocomplete w polach z danymi osobowymi | [S02] [WCAG 2.1](https://www.w3.org/TR/WCAG21/) | 🟢 Wysoka | Kryterium 1.3.5 |
| 23 | Formularze | Błędy opisane tekstem z podpowiedzią poprawy | [S01] [WCAG 2.0 (rekomendacja W3C)](https://www.w3.org/TR/WCAG20/) | 🟢 Wysoka | Kryteria 3.3.1 i 3.3.3 |
| 24 | Animacje | Uwzględnianie prefers-reduced-motion | [S15] [web.dev — Learn Design: Typography](https://web.dev/learn/design/typography/) | 🟢 Wysoka |  |
| 25 | Karuzele | Automatycznie przewijane karuzele ukrywają treść i irytują | [S12] [NN/g — Auto-Forwarding Carousels Annoy Users](https://www.nngroup.com/articles/auto-forwarding/) | 🟢 Wysoka |  |
| 26 | Pop-upy | Natrętne pop-upy szkodzą (szczególnie na telefonie) | [S29] [Google — Interstitials and dialogs](https://developers.google.com/search/docs/appearance/avoid-intrusive-interstitials) | 🟢 Wysoka |  |
| 27 | CTA | Rozmiar dotykowy min. 24×24 px wg WCAG 2.2 AA | [S03] [WCAG 2.2](https://www.w3.org/TR/WCAG22/) | 🟢 Wysoka | Kryterium 2.5.8 |

## 03. Responsywność (RWD)

Plik: `03_responsywnosc_RWD.md`

| Nr | Temat | Informacja | Źródło | Wiarygodność | Uwagi |
|---|---|---|---|---|---|
| 28 | RWD | Tag viewport width=device-width, initial-scale=1 | [S14] [web.dev — Responsive web design basics](https://web.dev/articles/responsive-web-design-basics) | 🟢 Wysoka |  |
| 29 | RWD | Nie blokować powiększania (user-scalable=no) | [S16] [DevToolbox — Responsive Web Design Best Practices 2026](https://devtoolbox.dedyn.io/blog/responsive-design-best-practices) | 🟡 Średnia | Wynika też z WCAG 1.4.4 (S01) |
| 30 | RWD | Google indeksuje wersję mobilną strony (mobile-first indexing) | [S24] [Google — Mobile-first Indexing Best Practices](https://developers.google.com/search/docs/crawling-indexing/mobile/mobile-sites-mobile-first-indexing) | 🟢 Wysoka |  |
| 31 | RWD | Breakpointy 640/768/1024/1280/1536 px; ustawiać tam, gdzie psuje się treść | [S16] [DevToolbox — Responsive Web Design Best Practices 2026](https://devtoolbox.dedyn.io/blog/responsive-design-best-practices) | 🟡 Średnia | Wartości to konwencja frameworków (Tailwind) |
| 32 | Typografia | Płynna typografia z clamp() | [S15] [web.dev — Learn Design: Typography](https://web.dev/learn/design/typography/) | 🟢 Wysoka |  |
| 33 | Typografia | Długość linii 50–75 znaków | [S21] [Baymard — Readability: The Optimal Line Length](https://baymard.com/blog/line-length-readability) | 🟢 Wysoka | Poprawiono w plikach 03 i 05 (wcześniej 45–75) |
| 34 | Obrazy | srcset/sizes, <picture>, width i height przeciw skakaniu | [S14] [web.dev — Responsive web design basics](https://web.dev/articles/responsive-web-design-basics) | 🟢 Wysoka |  |
| 35 | Dotyk | Cel dotykowy 44×44 pt (Apple) | [S31] [Apple — UI Design Dos and Don'ts](https://developer.apple.com/design/tips/) | 🟢 Wysoka |  |
| 36 | Dotyk | Cel dotykowy 48×48 dp (Android/Google) | [S32] [Android Accessibility Help — Touch target size](https://support.google.com/accessibility/android/answer/7101858) | 🟢 Wysoka |  |
| 37 | Dotyk | Działanie w orientacji pionowej i poziomej | [S02] [WCAG 2.1](https://www.w3.org/TR/WCAG21/) | 🟢 Wysoka | Kryterium 1.3.4 |
| 38 | Reflow | Brak poziomego przewijania przy 320 px szerokości | [S02] [WCAG 2.1](https://www.w3.org/TR/WCAG21/) | 🟢 Wysoka | Kryterium 1.4.10 |

## 04. Dostępność (WCAG)

Plik: `04_dostepnosc_WCAG.md`

| Nr | Temat | Informacja | Źródło | Wiarygodność | Uwagi |
|---|---|---|---|---|---|
| 39 | WCAG | Wersje: 2.0 (2008), 2.1 (2018), 2.2 (2023) | [S03] [WCAG 2.2](https://www.w3.org/TR/WCAG22/) | 🟢 Wysoka |  |
| 40 | WCAG | WCAG 2.0: 61 kryteriów (25 A, 13 AA, 23 AAA) | [S01] [WCAG 2.0 (rekomendacja W3C)](https://www.w3.org/TR/WCAG20/) | 🟢 Wysoka |  |
| 41 | WCAG | Usunięcie 4.1.1 Parsowanie w WCAG 2.2 | [S03] [WCAG 2.2](https://www.w3.org/TR/WCAG22/) | 🟢 Wysoka |  |
| 42 | WCAG | Zasady POUR: postrzegalność, funkcjonalność, zrozumiałość, solidność | [S01] [WCAG 2.0 (rekomendacja W3C)](https://www.w3.org/TR/WCAG20/) | 🟢 Wysoka |  |
| 43 | WCAG | Kontrast tekstu 4.5:1, duży tekst 3:1 | [S01] [WCAG 2.0 (rekomendacja W3C)](https://www.w3.org/TR/WCAG20/) | 🟢 Wysoka | Kryterium 1.4.3 |
| 44 | WCAG | Powiększenie tekstu do 200% | [S01] [WCAG 2.0 (rekomendacja W3C)](https://www.w3.org/TR/WCAG20/) | 🟢 Wysoka | Kryterium 1.4.4 |
| 45 | WCAG | Pełna obsługa klawiaturą, brak pułapki | [S01] [WCAG 2.0 (rekomendacja W3C)](https://www.w3.org/TR/WCAG20/) | 🟢 Wysoka | Kryteria 2.1.1 i 2.1.2 |
| 46 | WCAG | Widoczny fokus | [S01] [WCAG 2.0 (rekomendacja W3C)](https://www.w3.org/TR/WCAG20/) | 🟢 Wysoka | Kryterium 2.4.7 |
| 47 | WCAG | Kontrast elementów nietekstowych 3:1 | [S02] [WCAG 2.1](https://www.w3.org/TR/WCAG21/) | 🟢 Wysoka | Kryterium 1.4.11 |
| 48 | WCAG | Komunikaty o stanie ogłaszane czytnikom | [S02] [WCAG 2.1](https://www.w3.org/TR/WCAG21/) | 🟢 Wysoka | Kryterium 4.1.3 |
| 49 | WCAG | Nowe kryteria 2.2: fokus niezasłonięty, rozmiar celu, dostępne logowanie itd. | [S03] [WCAG 2.2](https://www.w3.org/TR/WCAG22/) | 🟢 Wysoka |  |
| 50 | WCAG | Objaśnienia kryteriów w praktyce | [S04] [How to Meet WCAG (Quick Reference)](https://www.w3.org/WAI/WCAG22/quickref/) | 🟢 Wysoka |  |
| 51 | WCAG | Zestawienie kryteriów w formie checklisty | [S05] [BrowserStack — WCAG Compliance Checklist](https://www.browserstack.com/guide/wcag-compliance-checklist) | 🟡 Średnia | Tylko pomocniczo — weryfikować z W3C (S01–S04) |
| 52 | Prawo | Podmioty publiczne: ustawa o dostępności cyfrowej, deklaracja dostępności | [S48] [gov.pl — Dostępność cyfrowa](https://www.gov.pl/web/dostepnosc-cyfrowa) | 🟢 Wysoka |  |
| 53 | Prawo | EAA od 28.06.2025 obejmuje sklepy internetowe; mikroprzedsiębiorcy wyłączeni z usług | [S47] [Shoper — Polski Akt o Dostępności a sklepy](https://www.shoper.pl/learn/artykul/polski-akt-o-dostepnosci-wplynie-na-sklepy-internetowe) | 🟡 Średnia |  |

## 05. Design wizualny

Plik: `05_design_wizualny.md`

| Nr | Temat | Informacja | Źródło | Wiarygodność | Uwagi |
|---|---|---|---|---|---|
| 54 | Design | Siatka 12/8/4 kolumny, odstępy w systemie 8 px | [S51] Praktyka branżowa (brak jednego źródła) | 🔴 Niska | Konwencja (m.in. Material Design) — opisać jako praktykę |
| 55 | Design | Zasada kolorów 60-30-10 | [S51] Praktyka branżowa (brak jednego źródła) | 🔴 Niska | Zasada praktyczna bez badań — opisać jako konwencję |
| 56 | Design | Maksymalnie 2 kroje pisma | [S51] Praktyka branżowa (brak jednego źródła) | 🔴 Niska | Zasada praktyczna |

## 06. Wydajność

Plik: `06_wydajnosc.md`

| Nr | Temat | Informacja | Źródło | Wiarygodność | Uwagi |
|---|---|---|---|---|---|
| 57 | Wydajność | Progi: LCP ≤ 2.5 s, INP ≤ 200 ms, CLS ≤ 0.1 (75. percentyl) | [S18] [corewebvitals.io — Core Web Vitals](https://corewebvitals.io/core-web-vitals) | 🟡 Średnia | Te same progi w dokumentacji Google (S17) |
| 58 | Wydajność | Core Web Vitals jako wskaźniki jakości strony (definicja Google) | [S17] [web.dev — Web Vitals](https://web.dev/articles/vitals) | 🟢 Wysoka |  |
| 59 | Wydajność | INP zastąpił FID w Core Web Vitals (2024) | [S19] [web.dev — INP is officially a Core Web Vital](https://web.dev/blog/inp-cwv-launch) | 🟢 Wysoka | 12 marca 2024 |
| 60 | Wydajność | TTFB dobrze ≤ 0.8 s | [S20] [web.dev — Time to First Byte (TTFB)](https://web.dev/articles/ttfb) | 🟢 Wysoka |  |
| 61 | Wydajność | FCP dobrze ≤ 1.8 s | [S17] [web.dev — Web Vitals](https://web.dev/articles/vitals) | 🟢 Wysoka | Wartość do potwierdzenia na web.dev/articles/fcp |
| 62 | Wydajność | Lazy loading, WebP/AVIF, width/height na obrazach | [S14] [web.dev — Responsive web design basics](https://web.dev/articles/responsive-web-design-basics) | 🟢 Wysoka |  |

## 07. SEO

Plik: `07_SEO.md`

| Nr | Temat | Informacja | Źródło | Wiarygodność | Uwagi |
|---|---|---|---|---|---|
| 63 | SEO | Unikalny title i meta description | [S25] [Google — Influencing Title Links](https://developers.google.com/search/docs/appearance/title-link) | 🟢 Wysoka | Google nie podaje limitu znaków — 60/155 to praktyka branżowa (długość widoczna w wynikach) |
| 64 | SEO | Meta description — zachęcający opis strony | [S26] [Google — How to Write Meta Descriptions](https://developers.google.com/search/docs/appearance/snippet) | 🟢 Wysoka |  |
| 65 | SEO | Przyjazne adresy URL (słowa, myślniki) | [S27] [Google — URL Structure Best Practices](https://developers.google.com/search/docs/crawling-indexing/url-structure) | 🟢 Wysoka |  |
| 66 | SEO | Sitemap, linkowanie wewnętrzne, dane strukturalne, opisowe alty | [S28] [Google — SEO Starter Guide](https://developers.google.com/search/docs/fundamentals/seo-starter-guide) | 🟢 Wysoka |  |
| 67 | SEO | HTTPS i doświadczenie strony a wyniki wyszukiwania | [S30] [Google — Understanding Page Experience](https://developers.google.com/search/docs/appearance/page-experience) | 🟢 Wysoka |  |

## 08. Bezpieczeństwo i prawo

Plik: `08_bezpieczenstwo_i_prawo.md`

| Nr | Temat | Informacja | Źródło | Wiarygodność | Uwagi |
|---|---|---|---|---|---|
| 68 | Bezpieczeństwo | Najczęstsze zagrożenia aplikacji webowych, walidacja po stronie serwera | [S50] [OWASP Top 10](https://owasp.org/www-project-top-ten/) | 🟢 Wysoka |  |
| 69 | RODO | Polityka prywatności: administrator, cele, podstawy, prawa, skarga do UODO | [S44] [Rozporządzenie RODO (UE) 2016/679](https://eur-lex.europa.eu/legal-content/PL/TXT/?uri=CELEX:32016R0679) | 🟢 Wysoka | Art. 13 RODO |
| 70 | RODO | Formularze: niezaznaczone checkboxy, osobne zgody, dokumentowanie zgód | [S46] [RPMS — Czy Twoja strona www spełnia wymagania RODO? Checklista](https://rpms.pl/czy-twoja-strona-www-spelnia-wymagania-rodo-checklista-2025/) | 🟡 Średnia |  |
| 71 | Cookies | Zgoda na cookies (oprócz niezbędnych) — Prawo komunikacji elektronicznej | [S45] [Prawo komunikacji elektronicznej (Dz.U. 2024 poz. 1221)](https://eli.gov.pl/eli/DU/2024/1221/ogl/pol) | 🟢 Wysoka | Art. 399 PKE; S46 podaje nieaktualną nazwę ustawy |
| 72 | Cookies | Opt-in, równie widoczny przycisk „Odrzuć”, łatwe wycofanie zgody | [S46] [RPMS — Czy Twoja strona www spełnia wymagania RODO? Checklista](https://rpms.pl/czy-twoja-strona-www-spelnia-wymagania-rodo-checklista-2025/) | 🟡 Średnia |  |
| 73 | Sklep | Najniższa cena z 30 dni przed obniżką (Omnibus) | [S49] [Prawo.pl — Wdrożenie dyrektywy Omnibus](https://www.prawo.pl/prawo/wdrozenie-dyrektywy-omnibus-kontroluje-uokik,519298.html) | 🟡 Średnia | Warto potwierdzić na uokik.gov.pl |

## 09. Testowanie

Plik: `09_testowanie_i_narzedzia.md`

| Nr | Temat | Informacja | Źródło | Wiarygodność | Uwagi |
|---|---|---|---|---|---|
| 74 | Testy | Automaty wykrywają część problemów dostępności (najlepsze narzędzie 41%, wszystkie razem 71%) | [S33] [GOV.UK — What we found when we tested tools…](https://accessibility.blog.gov.uk/2017/02/24/what-we-found-when-we-tested-tools-on-the-worlds-least-accessible-webpage/) | 🟢 Wysoka | Poprawiono w pliku 09: najlepsze narzędzie 41%, wszystkie razem 71% |
| 75 | Testy | Test z 3–5 użytkownikami wykrywa większość problemów | [S13] [NN/g — Why You Only Need to Test with 5 Users](https://www.nngroup.com/articles/why-you-only-need-to-test-with-5-users/) | 🟢 Wysoka | NN/g: 5 użytkowników ≈ 85% problemów |

## 11. Marketing i konwersja

Plik: `11_marketing_i_konwersja.md`

| Nr | Temat | Informacja | Źródło | Wiarygodność | Uwagi |
|---|---|---|---|---|---|
| 76 | Marketing | Większość użytkowników wychodzi w 10–20 s; propozycja wartości w 10 s | [S07] [NN/g — How Long Do Users Stay on Web Pages?](https://www.nngroup.com/articles/how-long-do-users-stay-on-web-pages/) | 🟢 Wysoka |  |
| 77 | Marketing | 5 zasad strony głównej NN/g | [S08] [NN/g — Homepage Design: 5 Fundamental Principles](https://www.nngroup.com/articles/homepage-design-principles/) | 🟢 Wysoka |  |
| 78 | Marketing | Hierarchia zaufania — nie żądać za dużo za wcześnie | [S09] [NN/g — Hierarchy of Trust](https://www.nngroup.com/articles/commitment-levels/) | 🟢 Wysoka |  |
| 79 | Marketing | Lejek TOFU/MOFU/BOFU i treści na każdym etapie | [S41] [Semrush — Marketing Funnel](https://www.semrush.com/blog/marketing-funnel/) | 🟡 Średnia |  |
| 80 | Landing page | Budowa landing page, message match, jeden cel | [S34] [CXL — How to Build a High-Converting Landing Page](https://cxl.com/blog/how-to-build-a-high-converting-landing-page/) | 🟢 Wysoka |  |
| 81 | Landing page | Prosty język: 11.1% vs 5.3% konwersji | [S34] [CXL — How to Build a High-Converting Landing Page](https://cxl.com/blog/how-to-build-a-high-converting-landing-page/) | 🟢 Wysoka | Dane Unbounce cytowane przez CXL |
| 82 | Zaufanie | Co buduje i co zabija wiarygodność | [S35] [CXL — Website Credibility: 39-Point Checklist](https://cxl.com/blog/website-credibility-killers) | 🟢 Wysoka |  |
| 83 | Zaufanie | Rodzaje dowodu społecznego | [S36] [CXL — Social Proof](https://cxl.com/blog/is-social-proof-really-that-important/) | 🟢 Wysoka |  |
| 84 | E-commerce | Średnio ok. 70% porzuconych koszyków + powody | [S22] [Baymard — Cart Abandonment Rate Statistics](https://baymard.com/blog/cart-abandonment-rate) | 🟢 Wysoka |  |
| 85 | E-commerce | Checkout: zalecane 7–8 pól formularza | [S22] [Baymard — Cart Abandonment Rate Statistics](https://baymard.com/blog/cart-abandonment-rate) | 🟢 Wysoka |  |
| 86 | E-commerce | Zakupy bez konta, koszty widoczne wcześnie | [S23] [Baymard — Checkout UX Guide](https://baymard.com/blog/checkout-flow-ux-optimization) | 🟢 Wysoka |  |
| 91 | Marketing | Porady CRO: jak zwiększyć konwersję | [S38] [Unbounce — How to increase conversion rates](https://unbounce.com/conversion-rate-optimization/how-to-increase-conversion-rate/) | 🟡 Średnia |  |

## 12. CTA

Plik: `12_CTA.md`

| Nr | Temat | Informacja | Źródło | Wiarygodność | Uwagi |
|---|---|---|---|---|---|
| 87 | CTA | „Call to value”, pierwsza osoba (+90% w teście ContentVerve), kolor tylko dla CTA | [S37] [Unbounce — CTA Buttons That Convert](https://unbounce.com/conversion-rate-optimization/cta-buttons-that-convert/) | 🟡 Średnia | Wynik jednego testu — nie uogólniać |
| 88 | CTA | Akcja + korzyść, ta sama nazwa oferty, testy A/B, above the fold | [S39] [HubSpot — Checklist for Compelling CTAs](https://blog.hubspot.com/marketing/call-to-action-optimization-ht) | 🟡 Średnia |  |
| 89 | CTA | Przykłady CTA i ich analiza | [S52] [CXL — Call to Action Examples & Why They (Don't) Work](https://cxl.com/blog/call-to-action/) | 🟢 Wysoka |  |
| 90 | CTA | Projektowanie przycisków (wygląd, stany) | [S40] [Smashing Magazine — How To Design Better Buttons](https://www.smashingmagazine.com/2016/11/a-quick-guide-for-designing-better-buttons/) | 🟡 Średnia |  |

## 13. Analityka

Plik: `13_analityka_i_testy.md`

| Nr | Temat | Informacja | Źródło | Wiarygodność | Uwagi |
|---|---|---|---|---|---|
| 92 | Analityka | Parametry UTM, wielkość liter ma znaczenie | [S42] [Google Analytics Help — URL builders (UTM)](https://support.google.com/analytics/answer/10917952) | 🟢 Wysoka |  |
| 93 | Analityka | Kluczowe zdarzenia (key events) w GA4 | [S43] [Google Analytics Help — Key events](https://support.google.com/analytics/answer/12844695) | 🟢 Wysoka |  |
