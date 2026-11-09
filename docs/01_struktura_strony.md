# 01. Struktura strony internetowej

## 1. Architektura informacji (zanim zaczniesz rysować)

- **Cel strony** — co ma osiągnąć (sprzedaż, kontakt, informacja, portfolio).
- **Grupa docelowa** — kto wchodzi i czego szuka (persony).
- **Mapa strony (sitemap)** — drzewo podstron, np.:
  ```
  Strona główna
  ├── O nas
  ├── Oferta / Usługi
  │   ├── Usługa 1
  │   └── Usługa 2
  ├── Realizacje / Portfolio
  ├── Blog / Aktualności
  ├── FAQ
  └── Kontakt
  (+ Polityka prywatności, Regulamin, Deklaracja dostępności)
  ```
- **Zasada 3 kliknięć** (orientacyjna) — ważne treści nie głębiej niż 2–3 poziomy.
- Nazwy w menu proste i zrozumiałe („Oferta”, nie „Nasze rozwiązania synergii”).
- **User flow** — ścieżka użytkownika od wejścia do celu (np. strona główna → oferta → formularz → podziękowanie).
- **Wireframe** (szkielet bez kolorów) → **mockup** (wygląd) → **prototyp** (klikany, np. w Figmie).

## 2. Elementy każdej podstrony (anatomia strony)

### Header (nagłówek)
- Logo w lewym górnym rogu, klikalne → prowadzi do strony głównej.
- Główne menu (zwykle 5–7 pozycji, nie więcej).
- Najważniejsze CTA (np. „Umów się”, „Koszyk”), wyszukiwarka jeśli treści jest dużo.
- Na telefonie: menu „hamburger” (☰) z czytelną etykietą / `aria-label="Menu"`.
- Opcjonalnie przyklejony (sticky) — ale nie może zasłaniać fokusu i treści (WCAG 2.2: 2.4.11).

### Hero / sekcja powitalna (strona główna)
- Nagłówek H1 — jasno mówi, co oferujesz.
- Krótki opis (1–2 zdania) + główny przycisk CTA.
- Wyraźne zdjęcie/grafika, ale lekka (szybkość!).

### Treść główna (`<main>`)
- Sekcje z nagłówkami H2, H3 w logicznej kolejności (nie przeskakiwać poziomów).
- Krótkie akapity, listy, wyróżnienia — ludzie skanują wzrokiem (wzorzec F i Z).
- Dowody zaufania: opinie, logotypy klientów, realizacje, liczby.
- Okruszki (breadcrumbs) na głębszych podstronach: `Start > Oferta > Usługa 1`.

### Footer (stopka)

**Po co jest stopka (NN/g):** użytkownicy przewijają na dół celowo, gdy szukają kontaktu, informacji o firmie, social mediów, albo w ostateczności, gdy nie znaleźli czegoś wyżej. Stopka to „druga szansa” na przekonanie klienta i wskazanie mu kolejnego kroku. Jest na każdej podstronie i rzadko szkodzi użyteczności, więc warto ją dobrze zaprojektować.

**Co powinno być w stopce:**
- **Linki użytkowe (zawsze):** kontakt, obsługa klienta, polityka prywatności, regulamin. NN/g zaleca je w stopce każdej strony.
- **Dane kontaktowe:** adres, telefon (`tel:`), e-mail (`mailto:`), godziny otwarcia, ewentualnie mapa.
- **Linki prawne:** polityka prywatności, regulamin, **„Ustawienia cookies”** (łatwe wycofanie zgody), **deklaracja dostępności**.
- **Powtórzenie głównej nawigacji (doormat navigation):** przydaje się na długich stronach, zwłaszcza na telefonie, bo nie trzeba wracać na górę.
- **Mapa strony:** w małym serwisie (do ok. 25 podstron) można pokazać całą, w dużym tylko 1–2 poziom + link do osobnej mapy strony.
- **Social media i zapis na newsletter:** stopka jest na każdej stronie, więc zapis jest stale widoczny, a przy tym nienachalny (Uxcel).
- **Elementy zaufania:** opinie, nagrody, certyfikaty, loga płatności i dostawców (sklep). Szczególnie ważne dla małych/nowych firm.
- **CTA na końcu strony:** np. „Umów bezpłatną wycenę” tuż nad stopką. Kto doczytał do końca, często jest gotowy działać.
- © rok, nazwa firmy, NIP (sklep / firma).

**Jak ją zaprojektować:**
- Tylko potrzebne elementy, pogrupowane w kolumny z nagłówkami (np. „Oferta”, „Firma”, „Pomoc”, „Kontakt”).
- Te same nazwy co w menu i na podstronach (nie „Kontakt” w menu i „Napisz do nas” w stopce).
- Hierarchia: nagłówki kolumn wyróżnione rozmiarem/grubością; nieuporządkowana stopka jest ignorowana.
- Kontrast tekstu min. 4.5:1, także na ciemnym tle stopki (częsty błąd: szary tekst na ciemnoszarym).
- Linki z odpowiednim odstępem, łatwe do kliknięcia palcem (min. 24×24 px, zalecane 44×44 px).
- W kodzie: znacznik `<footer>`, linki w listach `<ul>`, nawigacja w stopce jako `<nav aria-label="Stopka">`.

**Na telefonie:**
- Kolumny ustawione jedna pod drugą (desktop 4 kolumny → tablet 2 → telefon 1).
- ⚠ **Nie zwijaj treści stopki w akordeon domyślnie zamknięty.** NN/g podaje przykład, w którym taki akordeon sprawił, że ludzie nie znajdowali informacji. Lepiej skrócić stopkę niż ją chować.
- Telefon i e-mail jako klikalne linki.
- Sticky elementy (baner cookies, sticky CTA) nie mogą zasłaniać stopki ani fokusu.

**Typowe błędy w stopce:**
- Za dużo linków bez grupowania („ściana linków”).
- Brak kontaktu i linku do polityki prywatności.
- Nieaktualny rok © (sygnał, że strona jest zaniedbana).
- Zbyt słaby kontrast i małe linki.
- Nieskończone przewijanie (infinite scroll), przez które do stopki nie da się dojść. Wtedy NN/g zaleca np. „mini-stopkę” z boku.

### Strony obowiązkowe / pomocnicze
- Kontakt (formularz + dane + mapa).
- Strona 404 — przyjazna, z linkiem do strony głównej i wyszukiwarką.
- Strona „Dziękujemy” po wysłaniu formularza.
- Polityka prywatności, regulamin (sklep), deklaracja dostępności.

## 3. Semantyczny HTML (struktura w kodzie)

```html
<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Nazwa podstrony | Nazwa firmy</title>
  <meta name="description" content="Opis do 155 znaków">
</head>
<body>
  <a href="#main" class="skip-link">Przejdź do treści</a>
  <header>
    <nav aria-label="Główna nawigacja">…</nav>
  </header>
  <main id="main">
    <h1>Jeden H1 na stronę</h1>
    <section>…</section>
    <article>…</article>
  </main>
  <aside>…</aside>
  <footer>…</footer>
</body>
</html>
```

- `lang="pl"` — czytnik ekranu czyta po polsku (WCAG 3.1.1).
- Używaj `<button>` dla akcji, `<a>` dla przejścia na inną stronę — nie `<div onclick>`.
- Jeden `<h1>` na stronę, nagłówki po kolei.
- Link „Przejdź do treści” (skip link) — omija menu przy nawigacji klawiaturą (WCAG 2.4.1).

## ⚠️ Typowe błędy
- Za dużo pozycji w menu, niejasne nazwy.
- Różny układ menu na różnych podstronach.
- Brak linku do strony głównej w logo.
- Brak strony 404 i strony „dziękujemy”.
- Nagłówki wybierane „bo ładnie wyglądają”, a nie według hierarchii.
