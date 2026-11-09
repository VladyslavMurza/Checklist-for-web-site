# 04. Dostępność — WCAG 2.0 (oraz zmiany w 2.1 i 2.2)

## 1. Co to jest WCAG
- **WCAG** (Web Content Accessibility Guidelines) — standard W3C, jak robić strony dostępne dla osób z niepełnosprawnościami (wzroku, słuchu, ruchu, poznawczymi) — ale w praktyce wygodniejsze dla wszystkich.
- Wersje: **2.0 (2008)** → **2.1 (2018, +17 kryteriów, głównie mobile i słabowidzący)** → **2.2 (2023, +9 kryteriów; usunięto 4.1.1 Parsowanie)**. Każda nowsza wersja zawiera poprzednią.
- Poziomy: **A** (minimum), **AA** (standard wymagany prawnie w UE/Polsce), **AAA** (najwyższy, rzadko wymagany w całości).
- WCAG 2.0 ma 61 kryteriów sukcesu: 25 × A, 13 × AA, 23 × AAA.
- ⚠️ Prawo w Polsce/UE wymaga dziś **WCAG 2.1 AA** (przez normę EN 301 549) — więc warto robić co najmniej 2.1 AA, nawet jeśli zadanie mówi o 2.0.

## 2. Cztery zasady — POUR

| Zasada | Po polsku | Pytanie kontrolne |
|---|---|---|
| **P**erceivable | Postrzegalność | Czy każdy może odebrać treść (zobaczyć / usłyszeć / przeczytać czytnikiem)? |
| **O**perable | Funkcjonalność | Czy da się wszystko obsłużyć (klawiaturą, dotykiem, bez pośpiechu)? |
| **U**nderstandable | Zrozumiałość | Czy treść i działanie są zrozumiałe i przewidywalne? |
| **R**obust | Solidność | Czy działa w różnych przeglądarkach i z technologiami asystującymi? |

## 3. Kryteria WCAG 2.0 — poziom A i AA (to trzeba spełnić)

### 1. Postrzegalność
| Nr | Poziom | Kryterium | W praktyce |
|---|---|---|---|
| 1.1.1 | A | Treść nietekstowa | `alt` dla obrazów z treścią; dekoracyjne `alt=""`; ikony-przyciski z opisem |
| 1.2.1 | A | Tylko audio / tylko wideo (nagrane) | Transkrypcja lub opis |
| 1.2.2 | A | Napisy (nagrane) | Napisy w filmach z dźwiękiem |
| 1.2.3 | A | Audiodeskrypcja lub alternatywa | Opis tego, co widać w filmie |
| 1.2.4 | AA | Napisy (na żywo) | Napisy w transmisjach |
| 1.2.5 | AA | Audiodeskrypcja (nagrane) | Audiodeskrypcja do wideo |
| 1.3.1 | A | Informacje i relacje | Prawdziwe nagłówki H1–H6, listy, tabele z `<th>`, `<label>` w formularzach |
| 1.3.2 | A | Zrozumiała kolejność | Kolejność w kodzie = logiczna kolejność czytania |
| 1.3.3 | A | Właściwości zmysłowe | Nie: „kliknij zielony przycisk po prawej” |
| 1.4.1 | A | Użycie koloru | Kolor nie może być jedynym nośnikiem informacji (np. błąd = kolor + ikona + tekst) |
| 1.4.2 | A | Kontrola odtwarzania dźwięku | Dźwięk > 3 s musi dać się zatrzymać |
| 1.4.3 | AA | **Kontrast (minimum)** | Tekst **4.5:1**; duży tekst (≥ 24 px lub ≥ 18.66 px pogrubiony) **3:1** |
| 1.4.4 | AA | Zmiana rozmiaru tekstu | Powiększenie do **200%** bez utraty treści |
| 1.4.5 | AA | Obrazy tekstu | Tekst jako tekst, nie jako obrazek (wyjątek: logo) |

### 2. Funkcjonalność
| Nr | Poziom | Kryterium | W praktyce |
|---|---|---|---|
| 2.1.1 | A | **Klawiatura** | Wszystko działa klawiszami Tab / Shift+Tab / Enter / Spacja / strzałki / Esc |
| 2.1.2 | A | Brak pułapki klawiaturowej | Z każdego elementu (np. okna modalnego) da się wyjść |
| 2.2.1 | A | Dostosowanie czasu | Limity czasu można wydłużyć/wyłączyć |
| 2.2.2 | A | Pauza, stop, ukrycie | Karuzele, animacje > 5 s — przycisk pauzy |
| 2.3.1 | A | Max 3 błyski na sekundę | Brak migotania (ryzyko ataku padaczki) |
| 2.4.1 | A | Pomijanie bloków | Link „Przejdź do treści”, landmarki |
| 2.4.2 | A | Tytuł strony | Unikalny `<title>` na każdej podstronie |
| 2.4.3 | A | Kolejność fokusu | Tab przechodzi w logicznej kolejności |
| 2.4.4 | A | Cel linku (w kontekście) | Zrozumiałe linki, nie „kliknij tutaj” |
| 2.4.5 | AA | Wiele sposobów | Min. 2 sposoby dotarcia do podstrony (menu + wyszukiwarka / mapa strony) |
| 2.4.6 | AA | Nagłówki i etykiety | Opisowe nagłówki i etykiety pól |
| 2.4.7 | AA | **Widoczny fokus** | Wyraźna ramka fokusu — nigdy `outline: none` bez zamiennika |

### 3. Zrozumiałość
| Nr | Poziom | Kryterium | W praktyce |
|---|---|---|---|
| 3.1.1 | A | Język strony | `<html lang="pl">` |
| 3.1.2 | AA | Język części | Fragment w innym języku: `<span lang="en">` |
| 3.2.1 | A | Po otrzymaniu fokusu | Fokus nie wywołuje niespodziewanych zmian |
| 3.2.2 | A | Podczas wprowadzania danych | Wybór z listy nie przeładowuje strony bez ostrzeżenia |
| 3.2.3 | AA | Spójna nawigacja | Menu w tym samym miejscu i kolejności |
| 3.2.4 | AA | Spójna identyfikacja | Te same funkcje tak samo nazwane (ikona szukania zawsze „Szukaj”) |
| 3.3.1 | A | Identyfikacja błędów | Błąd opisany tekstem |
| 3.3.2 | A | Etykiety lub instrukcje | Każde pole z etykietą, format podany (np. DD.MM.RRRR) |
| 3.3.3 | AA | Sugestie korekty błędów | Podpowiedź jak naprawić |
| 3.3.4 | AA | Zapobieganie błędom (prawne, finansowe) | Podsumowanie i potwierdzenie przed zamówieniem/płatnością |

### 4. Solidność
| Nr | Poziom | Kryterium | W praktyce |
|---|---|---|---|
| 4.1.1 | A | Parsowanie *(usunięte w 2.2)* | Poprawny HTML, unikalne `id` |
| 4.1.2 | A | Nazwa, rola, wartość | Własne komponenty (menu, zakładki, akordeon) z poprawnym ARIA; lepiej natywne elementy HTML |

## 4. Co doszło w WCAG 2.1 (A/AA) — warto spełnić
| Nr | Poziom | Kryterium | W praktyce |
|---|---|---|---|
| 1.3.4 | AA | Orientacja | Działa pionowo i poziomo |
| 1.3.5 | AA | Cel pola | `autocomplete` w polach z danymi osobowymi |
| 1.4.10 | AA | **Reflow** | Przy 320 px szerokości (= zoom 400%) brak poziomego przewijania |
| 1.4.11 | AA | Kontrast elementów nietekstowych | Ramki pól, ikony, fokus — min. **3:1** |
| 1.4.12 | AA | Odstępy w tekście | Układ nie psuje się przy zwiększonych odstępach liter/linii |
| 1.4.13 | AA | Treść po najechaniu/fokusie | Tooltipy: da się zamknąć (Esc), najechać na nie, nie znikają same |
| 2.1.4 | A | Skróty jednoklawiszowe | Można je wyłączyć/zmienić |
| 2.5.1 | A | Gesty | Gesty wielopalcowe/ścieżki mają prostą alternatywę (przyciski) |
| 2.5.2 | A | Anulowanie wskazania | Akcja przy puszczeniu palca, nie przy dotknięciu |
| 2.5.3 | A | Etykieta w nazwie | Nazwa dostępna zawiera widoczny tekst przycisku |
| 2.5.4 | A | Aktywacja ruchem | Potrząsanie telefonem — ma alternatywę |
| 4.1.3 | AA | Komunikaty o stanie | „Dodano do koszyka” ogłaszane przez czytnik (`role="status"` / `aria-live`) |

## 5. Co doszło w WCAG 2.2 (A/AA)
| Nr | Poziom | Kryterium | W praktyce |
|---|---|---|---|
| 2.4.11 | AA | Fokus niezasłonięty | Sticky header/baner cookies nie zakrywa elementu z fokusem |
| 2.5.7 | AA | Przeciąganie | Drag & drop ma alternatywę kliknięciem |
| 2.5.8 | AA | **Rozmiar celu (minimum)** | Klikalne elementy min. **24×24 px** (lub odpowiedni odstęp) |
| 3.2.6 | A | Spójna pomoc | Kontakt/pomoc zawsze w tym samym miejscu |
| 3.3.7 | A | Zbędne ponowne wpisywanie | Nie każ wpisywać tych samych danych drugi raz (np. „adres jak do dostawy”) |
| 3.3.8 | AA | Dostępne uwierzytelnianie | Logowanie bez testów pamięci/zagadek; pozwól wklejać hasło i używać menedżera haseł |

## 6. Szybka ściąga dla projektanta (Figma)
- Kontrast sprawdzaj pluginem (np. Stark, A11y – Color Contrast Checker) lub na webaim.org/resources/contrastchecker.
- Projektuj **stan fokusu** dla każdego interaktywnego elementu.
- Nie przekazuj informacji samym kolorem (status: kolor + ikona + tekst).
- Etykiety pól widoczne nad polem, nie tylko placeholder.
- Rozmiar tekstu podstawowego ≥ 16 px, interlinia ≥ 1.5.
- Oznacz w makiecie kolejność nagłówków (H1, H2…) i kolejność Tab.
- Opisz alt-y dla kluczowych obrazów w notatkach do makiety.

## 7. Prawo (Polska / UE) — w skrócie
- **Ustawa o dostępności cyfrowej stron internetowych i aplikacji mobilnych podmiotów publicznych (2019)** — urzędy, szkoły, uczelnie: WCAG 2.1 AA + **deklaracja dostępności**.
- **Europejski Akt o Dostępności (EAA)** → polska ustawa z 26.04.2024 — od **28 czerwca 2025** dotyczy m.in. **sklepów internetowych**, bankowości, e-booków, biletów. Wyłączeni mikroprzedsiębiorcy (< 10 osób i ≤ 2 mln € obrotu) — ale tylko w zakresie usług.
  Obowiązki: dostępny proces zakupu i płatności, informacja o dostępności, deklaracja/informacja o dostępności, obsługa skarg. Kary do 10-krotności przeciętnego wynagrodzenia (max 10% obrotu).
