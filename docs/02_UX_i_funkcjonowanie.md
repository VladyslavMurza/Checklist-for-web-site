# 02. UX — jak strona ma funkcjonować

## 1. 10 heurystyk użyteczności Jakoba Nielsena (Nielsen Norman Group)

| # | Heurystyka | Co to znaczy na stronie www |
|---|---|---|
| 1 | Widoczność stanu systemu | Loader przy ładowaniu, komunikat „Wysłano”, aktywna pozycja w menu podświetlona, licznik w koszyku |
| 2 | Zgodność z rzeczywistością | Język użytkownika, znane ikony (🛒 koszyk, 🔍 szukaj), bez żargonu |
| 3 | Kontrola i swoboda | Przycisk „Wstecz/Anuluj”, łatwe zamknięcie okna (X + Esc), usuwanie z koszyka |
| 4 | Spójność i standardy | Te same przyciski wyglądają i działają wszędzie tak samo; konwencje (logo lewo-góra, koszyk prawo-góra) |
| 5 | Zapobieganie błędom | Walidacja pól na bieżąco, potwierdzenie przed usunięciem, podpowiedzi formatu |
| 6 | Rozpoznawanie zamiast przypominania | Widoczne opcje, podpowiedzi, ostatnio oglądane, breadcrumbs |
| 7 | Elastyczność i efektywność | Skróty dla zaawansowanych, filtry, autouzupełnianie, logowanie przez Google |
| 8 | Estetyka i minimalizm | Tylko potrzebne informacje, dużo „oddechu”, brak zbędnych ozdobników |
| 9 | Pomoc w rozpoznaniu i naprawie błędów | Komunikat po ludzku: „Podaj e-mail w formacie jan@przyklad.pl”, a nie „Błąd 422” |
| 10 | Pomoc i dokumentacja | FAQ, czat, kontakt łatwo dostępny |

## 2. Nawigacja
- Użytkownik zawsze wie, gdzie jest (aktywny stan w menu, breadcrumbs, tytuł strony).
- Menu w tym samym miejscu na każdej podstronie (WCAG 3.2.3).
- Linki opisowe: „Zobacz cennik”, a nie „Kliknij tutaj”.
- Linki wyglądają jak linki (podkreślenie lub wyraźny kolor + nie tylko kolor).
- Wyszukiwarka przy dużej liczbie treści.
- Przycisk „do góry” na długich stronach.

## 3. Przyciski i CTA (call to action)
- Jedno główne CTA na sekcję, wyróżnione kolorem; drugorzędne — mniej widoczne (outline).
- Tekst-czasownik: „Zamów”, „Pobierz cennik”, „Umów jazdę testową”.
- Stany przycisku: **domyślny, hover, focus, active (wciśnięty), disabled, loading**.
- Rozmiar dotykowy min. 44×44 px (zalecane), min. 24×24 px wg WCAG 2.2 AA.

## 4. Formularze
- Każde pole ma widoczną etykietę `<label>` (placeholder to NIE etykieta).
- Tylko niezbędne pola — każde dodatkowe obniża konwersję.
- Oznaczenie pól wymaganych (*) + wyjaśnienie, co oznacza gwiazdka.
- Odpowiedni typ pola: `type="email"`, `type="tel"` → na telefonie właściwa klawiatura.
- `autocomplete` (np. `autocomplete="email"`) — WCAG 2.1 (1.3.5).
- Komunikaty błędów przy polu, tekstem (nie tylko czerwonym kolorem), z podpowiedzią jak poprawić.
- Po wysłaniu: wyraźne potwierdzenie.
- Zabezpieczenie przed spamem bez trudnych CAPTCHA (np. honeypot, niewidoczna weryfikacja).
- Zgody RODO: checkboxy niezaznaczone domyślnie.

## 5. Stany i informacja zwrotna
- Ładowanie (spinner / skeleton), pusty stan („Brak wyników — spróbuj…”), błąd, sukces.
- Animacje krótkie (150–300 ms), wspierające zrozumienie, nie ozdobne.
- Szanuj `prefers-reduced-motion` — wyłączaj animacje dla osób, które tego chcą.

## 6. Treść (content)
- Najważniejsze informacje na górze (odwrócona piramida).
- Krótkie zdania, proste słowa, listy punktowane.
- Aktualne dane kontaktowe, ceny, daty.
- Zdjęcia własne zamiast stockowych, gdy to możliwe.

## 7. Zaufanie (wiarygodność)
- Prawdziwe dane firmy, NIP, adres.
- Opinie klientów (prawdziwe!), certyfikaty, portfolio.
- Kłódka HTTPS, polityka prywatności, regulamin.
- Profesjonalny wygląd, brak literówek i niedziałających linków.

## ⚠️ Typowe błędy
- Wyskakujące okienka (pop-up) od razu po wejściu, szczególnie na telefonie.
- Automatyczne odtwarzanie wideo z dźwiękiem.
- Karuzela (slider) z ważną treścią — mało kto klika dalsze slajdy.
- Przyciski bez stanu hover/focus.
- Formularz, który po błędzie czyści wszystkie wpisane dane.
