# 13. Analityka i testy — skąd wiadomo, że strona zarabia

„Czego nie mierzysz, tego nie poprawisz.” Bez analityki nie wiadomo, które elementy działają.

## 1. Co mierzyć (KPI)

| Wskaźnik | Co mówi |
|---|---|
| **Użytkownicy / sesje** | Ile osób odwiedza stronę |
| **Źródła ruchu** | Skąd przychodzą: Google, reklamy, social media, bezpośrednio, polecenia |
| **Współczynnik konwersji** | Jaki % odwiedzających wykonuje cel |
| **Kluczowe zdarzenia (key events)** | Wysłanie formularza, klik w telefon, zakup, zapis na newsletter |
| **Współczynnik zaangażowania** | Czy ludzie coś robią na stronie, czy od razu wychodzą |
| **Strony wejścia i wyjścia** | Gdzie zaczynają i na której stronie uciekają |
| **CTR CTA** | Ile osób klika przycisk |
| **Porzucenia koszyka** | Ile osób przerywa zakup (sklep) |
| **Koszt pozyskania klienta (CAC)** i **ROI** | Czy reklama się opłaca |
| **Średnia wartość zamówienia (AOV)** | Ile średnio wydaje klient |

## 2. Narzędzia

| Cel | Narzędzie |
|---|---|
| Statystyki strony | **Google Analytics 4** (darmowe), Matomo, Plausible (prostsze, przyjazne prywatności) |
| Zarządzanie kodami śledzącymi | Google Tag Manager |
| Widoczność w Google | **Google Search Console** |
| Zachowanie użytkowników | **Microsoft Clarity** (darmowe: mapy cieplne, nagrania sesji), Hotjar |
| Szybkość | PageSpeed Insights |
| Zgody cookies | CMP (np. Cookiebot, CookieYes) + Google Consent Mode v2 |

⚠️ Narzędzia śledzące uruchamiaj **dopiero po zgodzie** użytkownika (cookies — plik 08).

## 3. GA4 — podstawy
- W GA4 cele nazywają się **„kluczowe zdarzenia” (key events)** — oznaczasz zdarzenie (np. `generate_lead`, `purchase`) jako kluczowe.
- Typowe zdarzenia: wyświetlenie strony „Dziękujemy”, wysłanie formularza, klik `tel:` / `mailto:`, zakup.

## 4. Linki UTM — skąd przyszedł klient

Dopisujesz parametry do linku w kampanii, a GA4 pokazuje, która kampania przyniosła wynik.

```
https://twojastrona.pl/oferta?utm_source=instagram&utm_medium=social&utm_campaign=zima_2026
```

| Parametr | Znaczenie | Przykład |
|---|---|---|
| `utm_source` | skąd (serwis) | `instagram`, `newsletter`, `google` |
| `utm_medium` | kanał | `social`, `email`, `cpc` |
| `utm_campaign` | nazwa kampanii | `zima_2026` |
| `utm_content` | wersja kreacji / który link | `baner_gora` |
| `utm_term` | słowo kluczowe (reklamy płatne) | `tuning_rajdowy` |

Zawsze dodawaj co najmniej `utm_source`, `utm_medium`, `utm_campaign`. Wielkość liter ma znaczenie (`Google` ≠ `google`) — pisz wszystko małymi literami.
Generator: Google Campaign URL Builder.

## 5. Testy A/B i optymalizacja (CRO)

Proces:
1. **Dane** — gdzie ludzie uciekają? (GA4, mapy cieplne, nagrania sesji)
2. **Hipoteza** — „Jeśli skrócimy formularz z 7 do 3 pól, więcej osób go wyśle, bo…”
3. **Test A/B** — połowa ruchu widzi wersję A, połowa B. Zmieniaj **jedną rzecz** naraz.
4. **Wystarczająco danych** — test trwa min. 1–2 pełne tygodnie i do uzyskania wiarygodnego wyniku (mała strona = mało ruchu = testy trudne; wtedy lepiej testy z użytkownikami).
5. **Wdrożenie** zwycięzcy i kolejny test.

Co warto testować: nagłówek, tekst CTA, długość formularza, zdjęcie hero, kolejność sekcji, cenę/ofertę.

Przy małym ruchu (typowo w małej firmie): zamiast A/B — **testy z 3–5 użytkownikami** (NN/g), analiza nagrań w Clarity, ankieta „Co Cię powstrzymuje przed zakupem?”.

## 6. Raport (np. co miesiąc)
- Ruch i źródła → co się zmieniło?
- Konwersje i CR → rośnie czy spada?
- Top strony i strony z największymi wyjściami.
- Co poprawiamy w następnym miesiącu.

## Źródła
- Google Analytics Help — URL builders (UTM): https://support.google.com/analytics/answer/10917952
- Google Analytics Help — Create or modify key events: https://support.google.com/analytics/answer/12844695
- Google Analytics Help — Tutorial: Set up a key event: https://support.google.com/analytics/answer/12966437
- CXL — How to Build a High-Converting Landing Page (testowanie): https://cxl.com/blog/how-to-build-a-high-converting-landing-page/
- HubSpot — Conversion funnel: https://blog.hubspot.com/marketing/conversion-funnel
