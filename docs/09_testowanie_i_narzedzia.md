# 09. Testowanie i narzędzia

## 1. Kolejność testów przed oddaniem strony
1. **Treść** — literówki, aktualne dane, wszystkie linki działają.
2. **Responsywność** — telefon (pion/poziom), tablet, laptop, duży monitor; szerokość 320 px bez poziomego scrolla.
3. **Przeglądarki** — Chrome, Firefox, Safari (iPhone!), Edge.
4. **Klawiatura** — przejdź całą stronę samym Tab/Shift+Tab/Enter/Esc: czy widać fokus, czy kolejność logiczna, czy da się zamknąć menu i okna.
5. **Zoom** — powiększenie 200% i 400%: nic nie ucieka, nie nachodzi na siebie.
6. **Czytnik ekranu** — NVDA (Windows, darmowy), VoiceOver (iPhone/Mac), TalkBack (Android).
7. **Automatyczne testy dostępności** — WAVE, axe, Lighthouse.
8. **Wydajność** — PageSpeed Insights (osobno telefon i komputer).
9. **Formularze** — wysyłka, błędy, potwierdzenie, czy maile dochodzą.
10. **SEO** — tytuły, opisy, sitemap, podgląd w social media.
11. **Prawo** — polityka prywatności, cookies (czy przed zgodą nic się nie ładuje), regulamin.
12. **Test z użytkownikiem** — 3–5 osób wykonuje zadanie (np. „znajdź cenę i wyślij zapytanie”) — wychodzi ~80% problemów.

⚠️ Automaty wykrywają tylko część problemów z dostępnością. W teście GOV.UK (2017) najlepsze pojedyncze narzędzie wykryło ok. 41% barier, a wszystkie narzędzia razem ok. 71% — testy ręczne są konieczne.

## 2. Narzędzia (darmowe)

| Cel | Narzędzie |
|---|---|
| Wydajność + dostępność + SEO | **Lighthouse** (Chrome DevTools → zakładka Lighthouse), **PageSpeed Insights** (pagespeed.web.dev) |
| Dostępność | **WAVE** (wave.webaim.org), **axe DevTools** (rozszerzenie), Accessibility Insights |
| Kontrast | WebAIM Contrast Checker, w Figmie plugin Stark / Contrast |
| Responsywność | Chrome DevTools → Device Mode (Ctrl+Shift+M), Responsively App, prawdziwe telefony |
| Walidacja HTML | validator.w3.org |
| Linki | Dead Link Checker, Screaming Frog (do 500 adresów za darmo) |
| SEO | Google Search Console, Rich Results Test |
| Bezpieczeństwo | SSL Labs (ssllabs.com/ssltest), securityheaders.com |
| Czytniki ekranu | NVDA, VoiceOver, TalkBack |
| Projekt | Figma (Auto Layout, Variables, prototyp), FigJam (sitemap, user flow) |

## 3. Proces projektowania (od zera do strony)
1. Brief: cel, grupa docelowa, konkurencja.
2. Architektura informacji: sitemap, user flow.
3. Wireframe (low-fi) → test z osobą.
4. Moodboard, style (kolory, fonty), komponenty.
5. Mockup hi-fi: mobile + tablet + desktop.
6. Prototyp klikany, test.
7. Kodowanie (HTML semantyczny → CSS mobile first → JS).
8. Testy (lista wyżej).
9. Publikacja: domena, hosting, HTTPS, Search Console, analityka.
10. Utrzymanie: aktualizacje, kopie zapasowe, poprawki wg danych.
