# PIESKI-UW IO project

## Opis projektu
Projekt obejmuje zbieranie i analizowanie danych dotyczących adopcji zwierząt w warszawskim schronisku **Na Paluchu**

Aplikacja będzie opierała się na frameworku Django

## Fragmenty projektu
### Zbieranie danych 
Zbieranie danych ze strony odbywać się za pomocą webscraper'a zapisanego w python.
- Zbieranie danych i zapis w bazie danych sql za pomocą api django do baz danych ze strony schroniska: https://napaluchu.waw.pl/zwierzeta/znalazly-dom/
- Testowanie poprawności zbieranych danych za pomocą testów django i lokalnej kopii fragmentu strony za pomocą testów django
- Aktualizowanie danych poprzez ręczne wywołanie webscraper'a lub automatyczne wykonywanie np raz dziennie
- Zbieranie danych wykorzysta bibliotekę requests i beautiful soup

### Django
- Backend bazy danych
- Generowanie i udostępnianie stron umożliwiających wizualizacje zebranych danych
- Podstawa do testów
- Przechowywanie danych w bazie sqlite(domyślna używana przez django) lub w postgresql

### Analiza danych
- Dane analizowane w python za pomocą bibliotek takiej jak numpy i przechowywane w bazie danych dostarczanej przez django

### Wizualizacja danych
- Wyświetlanie danych zebranych oraz możliwość filtrowania ich według różnych kryteriów
- Wykresy analizujące czas przebywania zwierzęcia w schronisku w zależności od ich wieku, masy ciała, rasy, płci
- Najczęstsze zwierzęta trafiające do schronisk w zależności od podobnych kryteriów.
- Mapa wyświetlająca najczęstsze miejsca w których zostały znalezione zwierzęta za pomocą biblioteki leaflet.js oraz danych dotyczących mapy dostarczanych przez openstreetmaps
- Wszelkie wykresy będą wyświetlane przy użyciu biblioteki chart.js