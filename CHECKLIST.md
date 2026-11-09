# ✅ Checklista strony internetowej — zasada 80/20

26 punktów, które dają największy efekt. Wybrane z ponad 90 zasad opisanych w [`docs/`](docs/) według trzech kryteriów:

1. **Wpływ na wynik:** czy bez tego klient odejdzie, nie zrozumie oferty albo nie wykona akcji?
2. **Wymóg:** czy wymaga tego standard (WCAG 2.1 AA) albo prawo (RODO, cookies)?
3. **Siła źródła:** czy potwierdzają to badania lub oficjalna dokumentacja (patrz [mapowanie źródeł](zrodla/15_mapowanie_zrodel.md))?

> 💡 Na GitHubie kratek w pliku nie da się klikać. Aby odhaczać punkty, skopiuj treść do nowego **Issue** albo pobierz plik i wpisuj `[x]`.

---

## 1. Cel i struktura

- [ ] **Jeden główny cel strony** (np. zapytanie o wycenę) jest określony przed projektowaniem, a każda sekcja do niego prowadzi. → [11](docs/11_marketing_i_konwersja.md)
- [ ] **Prosta nawigacja:** logo prowadzi do strony głównej, w menu 5–7 zrozumiałych pozycji, ten sam układ na każdej podstronie. → [01](docs/01_struktura_strony.md)
- [ ] **Stopka:** kontakt, polityka prywatności, regulamin, „Ustawienia cookies”, powtórzona nawigacja; na telefonie nie zwinięta w akordeon. → [01](docs/01_struktura_strony.md)

## 2. Pierwszy ekran i CTA

- [ ] **W 10 sekund wiadomo, co oferujesz:** nagłówek H1 mówi o korzyści dla klienta, a nie „Witamy na stronie”. → [11](docs/11_marketing_i_konwersja.md)
- [ ] **Jedno główne CTA na pierwszym ekranie:** czasownik + korzyść („Odbierz wycenę w 24 h”), kolor zarezerwowany tylko dla CTA. → [12](docs/12_CTA.md)
- [ ] **CTA powtórzone na końcu strony**, obok opinii lub innego dowodu zaufania. → [12](docs/12_CTA.md)
- [ ] **Dowody zaufania:** prawdziwe opinie, realizacje, pełne dane firmy, widoczny kontakt. → [11](docs/11_marketing_i_konwersja.md)
- [ ] **Krótki formularz:** tylko niezbędne pola, widoczne etykiety (nie placeholder), błędy opisane tekstem z podpowiedzią. → [02](docs/02_UX_i_funkcjonowanie.md)

## 3. Responsywność

- [ ] **Mobile first:** makiety co najmniej dla telefonu (360–390 px), tabletu (768 px) i desktopu (1440 px). → [03](docs/03_responsywnosc_RWD.md)
- [ ] **Tag viewport** `width=device-width, initial-scale=1`, bez blokowania powiększania. → [03](docs/03_responsywnosc_RWD.md)
- [ ] **Brak poziomego przewijania** przy szerokości 320 px. → [03](docs/03_responsywnosc_RWD.md)
- [ ] **Przyciski i linki łatwe do kliknięcia palcem:** zalecane 44×44 px, minimum 24×24 px. → [03](docs/03_responsywnosc_RWD.md)
- [ ] **Czytelny tekst:** min. 16 px, interlinia ok. 1.5, linia 50–75 znaków. → [03](docs/03_responsywnosc_RWD.md)

## 4. Dostępność (WCAG)

- [ ] **Kontrast:** tekst min. 4.5:1, duży tekst i elementy interfejsu min. 3:1. → [04](docs/04_dostepnosc_WCAG.md)
- [ ] **Klawiatura:** całą stronę da się obsłużyć klawiszem Tab, a fokus jest zawsze wyraźnie widoczny. → [04](docs/04_dostepnosc_WCAG.md)
- [ ] **Teksty alternatywne i etykiety:** `alt` dla obrazów, `label` dla pól, `lang="pl"`. → [04](docs/04_dostepnosc_WCAG.md)
- [ ] **Semantyczna struktura:** jeden H1, nagłówki po kolei, znaczniki `header`, `nav`, `main`, `footer`. → [01](docs/01_struktura_strony.md)
- [ ] **Kolor to nie jedyny sygnał:** błąd lub status = kolor + ikona + tekst. → [04](docs/04_dostepnosc_WCAG.md)

## 5. Szybkość

- [ ] **Lekkie obrazy:** WebP/AVIF, właściwy rozmiar, atrybuty `width`/`height`, `loading="lazy"` poniżej pierwszego ekranu. → [06](docs/06_wydajnosc.md)
- [ ] **Core Web Vitals na telefonie:** LCP ≤ 2.5 s, INP ≤ 200 ms, CLS ≤ 0.1 (sprawdź w PageSpeed Insights). → [06](docs/06_wydajnosc.md)

## 6. Prawo i bezpieczeństwo

- [ ] **HTTPS** na całej stronie. → [08](docs/08_bezpieczenstwo_i_prawo.md)
- [ ] **RODO i cookies:** polityka prywatności, baner cookies z przyciskiem „Odrzuć” tak samo widocznym jak „Akceptuj”, zgody w formularzach domyślnie niezaznaczone. → [08](docs/08_bezpieczenstwo_i_prawo.md)
- [ ] **Sklep (jeśli dotyczy):** koszt dostawy widoczny wcześnie, zakup bez zakładania konta, krótki checkout. → [11](docs/11_marketing_i_konwersja.md)

## 7. SEO i pomiar

- [ ] **Każda podstrona ma unikalny `title` i meta description**, a adresy URL są czytelne (`/oferta/tuning-silnika`). → [07](docs/07_SEO.md)
- [ ] **Analityka mierzy cel strony** (np. wysłanie formularza jako kluczowe zdarzenie w GA4) i działa dopiero po zgodzie na cookies. → [13](docs/13_analityka_i_testy.md)

## 8. Test przed publikacją

- [ ] **Trzy testy:** strona sprawdzona na prawdziwym telefonie, narzędziami Lighthouse i WAVE oraz przez 3–5 osób, które wykonują zadanie (np. „wyślij zapytanie”). → [09](docs/09_testowanie_i_narzedzia.md)

---

**Wynik:** ___ / 26 &nbsp;·&nbsp; Strona: __________________ &nbsp;·&nbsp; Data: __________
