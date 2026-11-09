# 08. Bezpieczeństwo i wymagania prawne (Polska / UE)

> To nie jest porada prawna — zebrane najważniejsze wymagania do projektu/strony.

## 1. Bezpieczeństwo techniczne
- **HTTPS** (certyfikat SSL/TLS, np. darmowy Let's Encrypt) na całej stronie, przekierowanie z http.
- Aktualny CMS, wtyczki, motywy (WordPress — najczęstsza przyczyna włamań to nieaktualne wtyczki).
- Silne hasła + logowanie dwuetapowe do panelu.
- Walidacja danych z formularzy po stronie serwera (nie tylko w przeglądarce).
- Ochrona formularzy przed spamem.
- Kopie zapasowe (automatyczne, przechowywane poza serwerem).
- Nagłówki bezpieczeństwa (np. Content-Security-Policy, X-Content-Type-Options, HSTS).
- Nie ujawniać błędów serwera użytkownikowi.

## 2. RODO — dane osobowe
- **Polityka prywatności** (link w stopce i przy formularzach), zawiera m.in.:
  - kto jest administratorem (nazwa, adres, kontakt, ewentualnie IOD),
  - cele i podstawy prawne przetwarzania,
  - jakie dane, jak długo przechowywane, komu przekazywane (np. hosting, Google),
  - przekazywanie poza EOG,
  - prawa użytkownika (dostęp, sprostowanie, usunięcie, sprzeciw itd.) i prawo skargi do **UODO**,
  - informacje o cookies i profilowaniu.
- Formularze: tylko niezbędne dane, klauzula informacyjna, **checkboxy zgód niezaznaczone domyślnie**, osobne zgody na różne cele (np. newsletter osobno).
- Newsletter: zalecany double opt-in (potwierdzenie e-mailem).

## 3. Cookies — baner zgody
- Podstawa w Polsce: **Prawo komunikacji elektronicznej** (od 10.11.2024 zastąpiło w tym zakresie Prawo telekomunikacyjne) + RODO.
- Model **opt-in**: cookies analityczne i marketingowe dopiero **po zgodzie**. Niezbędne (techniczne) — bez zgody.
- Przyciski **„Akceptuj” i „Odrzuć” równie widoczne** (nie chowaj odrzucania w ustawieniach).
- Możliwość wyboru kategorii (niezbędne / analityczne / marketingowe).
- Łatwe wycofanie zgody (np. ikonka/link „Ustawienia cookies” w stopce).
- Baner dostępny z klawiatury, nie zasłania całej strony na telefonie i nie zakrywa fokusu (WCAG 2.4.11).
- Google Consent Mode v2 — jeśli używasz narzędzi Google.

## 4. Dostępność jako obowiązek prawny
- Podmioty publiczne: ustawa o dostępności cyfrowej (2019) → WCAG 2.1 AA + **deklaracja dostępności**.
- Sklepy i wybrane usługi: **Europejski Akt o Dostępności** (polska ustawa z 26.04.2024, obowiązuje od **28.06.2025**) — szczegóły w 04_dostepnosc_WCAG.md.

## 5. Sklep internetowy — dodatkowo
- **Regulamin** sklepu (dane sprzedawcy, procedura zamówienia, płatności, dostawa, reklamacje, odstąpienie od umowy w 14 dni).
- Przycisk zamówienia z jasną informacją o obowiązku zapłaty: np. „Zamawiam i płacę”.
- Ceny brutto; przy promocjach — **najniższa cena z 30 dni przed obniżką** (dyrektywa Omnibus).
- Informacja o weryfikacji opinii (czy opinie pochodzą od kupujących).
- Formularz odstąpienia od umowy, dane kontaktowe sprzedawcy.

## 6. Prawa autorskie
- Licencje na zdjęcia, fonty, ikony, muzykę, wideo.
- Umowa z wykonawcą strony — przeniesienie praw autorskich do projektu i kodu.
