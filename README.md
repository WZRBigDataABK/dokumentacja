1. Charakterystyka oprograowania
   
a) Nazwa skrócona: Dashboard Inwestora

b) Nazwa pełna: Dashboard Inwestora Giełdy Nasdaq

c) Opis: Dashboard inwestora ma za zadanie ułatwić użytkownikowi poszukiwanie informacji o interesującej go spółce. Aplikacja daje możliwość wyszukania dowolnej spółki notowanej na amerykańskiej giełdzie Nasdaq, oraz wyświetla najważniejsze z punktu widzenia inwestora informacje takie jak: statystyki opisowe (wartość minimalna, maksymalna, mediana i średnia) dla cen zamknięcia oraz dopasowane do nich interaktywne wykresy. Poonadto oblicza stopę zwrotu dla cen zamknięcia i również generuje wykres pozwalający na wizualizację zjawiska w horyzoncie ostatnich 100 dni.

2) Prawa autorskie
   
a) Autorzy: Hajduk Bartosz, Kucińska Agata, Piekarski Jakub

b) Warunki licencyjne: Dane wykorzystane w aplikacji pochodzą z serwisu Aplpha Vantage, któr udziela licencji na instalowanie, użytkowanie, dostęp, wyświetlanie oraz uruchamianie oprogramowania na urządzeniach komputerowych lub mobilnych, które są w posiadaniu lub pod kontrolą użytkownika. Korzystanie z aplikacji jest możliwe jedynie w celach osobistych oraz niekomercyjnych. 

# Wymagania
|  Funkcjonalność    | Wymagania      | Kategoria         |
|--------------------|----------------|-------------------|
|Połączenie z API zawierającym dane z NASDAQ    | Wymagane       | funkcjonalne      |
|Wyszukiwarka firm NASDAQ    | Wymagane       | funkcjonalne      |
|Statystyki opisowe i pozycyjne (mediana, średnia)      | Wymagane       | funkcjonalne      |
|Wykres Boxplot    | Wymagane       | funkcjonalne      |
|Wykresy Violin    | Przydatne     | funkcjonalne      |
|Wykres linii dla stopy zwrotu z wolumenu    | Wymagane       | funkcjonalne      |
|Histogram stopy zwrotu dla ceny zamknięcia    | Przydatne       | funkcjonalne      |
|Histogram stopy zwrotu dla wolumenu   | Wymagane       | funkcjonalne      |
|Podsumowanie statystyk stóp zwrotu    | Wymagane       | funkcjonalne      |
|Interaktywność wykresów    | Przydatne       | funkcjonalne      |
|Wykresy linii trendu    | Wymagane       | funkcjonalne      |
|GUI    | Wymagane       | funkcjonalne      |
|System obsługuje jednego użytkownika jednocześnie    | Wymagane       | pozafunkcjonalne      |
|Obsługa w środowisku Windows                         | Wymagane       | pozafunkcjonalne      |
|System posługuje się danymi od dnia poprzedniego     | Wymagane       | pozafunkcjonalne      |
|Prognozy   | opcjonalne       | funkcjonalne      |
|Zapisywanie portfela użytkownika | opcjonalne       | funkcjonalne      |
|Obliczanie ryzyka dla portfela użytkownika | opcjonalne       | funkcjonalne      |



# Wymagania
| Kod |  Funkcjonalność    | Wymagania      | Kategoria         |
|--------------------|----------------|-------------------|
|FD-001|Połączenie z API zawierającym dane z NASDAQ    | Wymagane       | funkcjonalne      |
|FD-002|Wyszukiwarka firm NASDAQ    | Wymagane       | funkcjonalne      |
|FD-003|Statystyki opisowe i pozycyjne (mediana, średnia,      | Wymagane       | funkcjonalne      |
|FD-004|Wykres Boxplot    | Wymagane       | funkcjonalne      |
|FD-005|Wykresy Violin    | Przydatne     | funkcjonalne      |
|FD-006|Wykres linii dla stopy zwrotu z wolumenu    | Wymagane       | funkcjonalne      |
|FD-007|Histogram stopy zwrotu dla ceny zamknięcia    | Przydatne       | funkcjonalne      |
|FD-008|Histogram stopy zwrotu dla wolumenu   | Wymagane       | funkcjonalne      |
|FD-009|Podsumowanie statystyk stóp zwrotu    | Wymagane       | funkcjonalne      |
|FD-010|Interaktywność wykresów    | Przydatne       | funkcjonalne      |
|FD-011|Wykresy linii trendu    | Wymagane       | funkcjonalne      |
|FD-012|GUI    | Wymagane       | funkcjonalne      |
|FD-013|System obśługuje jednego użytkownika jednocześnie    | Wymagane       | pozafunkcjonalne      |
|FD-014|Obsługa w środowisku windows                         | Wymagane       | pozafunkcjonalne      |
|FD-015|System posługuje się danymi od dnia poprzedniego     | Wymagane       | pozafunkcjonalne      |
|FD-016|Prognozy   | opcjonalne       | funkcjonalne      |
|FD-017|zapisywanie portfela użytkownika | opcjonalne       | funkcjonalne      |
|FD-018|obliczanie ryzyka dla portfela użytkownika | opcjonalne       | funkcjonalne      |


# Dokumentacja Architektury Oprogramowania

## Architektura Rozwoju

### Stos Technologiczny
| Nazwa                          | Przeznaczenie                    | Numer Wersji |
|--------------------------------|-----------------------------------|--------------|
| Python                         | Język programowania backendu     | 3.11         |
| Flask                          | Framework do budowy aplikacji    | 2.3.2        |
| Alpha Vantage API              | Dostarczanie danych giełdowych   | 1.0.0        |
| Pandas                         | Przetwarzanie danych             | 2.1.1        |
| Matplotlib                     | Tworzenie wykresów statycznych   | 3.8.0        |
| Plotly                         | Tworzenie interaktywnych wykresów| 5.16.0       |
| HTML/CSS                       | Frontend aplikacji               | -            |

### Narzędzia Programistyczne
- **Visual Studio Code (1.83.1)**: Edytor kodu źródłowego z wsparciem dla języków i frameworków.
- **Git (2.42.0)**: System kontroli wersji do zarządzania kodem.
- **Pip (23.2.1)**: Menedżer pakietów Python do instalowania zależności.
- **Postman (10.15.0)**: Testowanie żądań API (opcjonalnie).
- **Google Colab**: Środowisko testowe dla skryptów Python.

---

## Architektura Uruchomieniowa

### Stos Technologiczny
| Nazwa                          | Przeznaczenie                    | Numer Wersji |
|--------------------------------|-----------------------------------|--------------|
| Python                         | Wykonywanie kodu backendu        | 3.11         |
| Flask                          | Hostowanie aplikacji             | 2.3.2        |
| Alpha Vantage API              | Pobieranie danych giełdowych     | 1.0.0        |
| Pandas                         | Operacje na danych               | 2.1.1        |
| Matplotlib                     | Wyświetlanie wykresów statycznych| 3.8.0        |
| Plotly                         | Wyświetlanie wykresów interaktywnych| 5.16.0     |
| HTML/CSS                       | Wyświetlanie frontendu           | -            |

### Narzędzia Wykonywania
- **Visual Studio Code (1.83.1)**: Wygodne środowisko do obsługi i uruchamiania aplikacji.
- **Serwer lokalny Flask**: Uruchamianie aplikacji w środowisku lokalnym.
- **Przeglądarka internetowa**: Wyświetlanie aplikacji (np. Google Chrome, Firefox).
- **System operacyjny**: Windows/Linux/MacOS kompatybilny z Python 3.11.

---

## Opis Systemu

### Funkcjonalności
1. Wyszukiwanie danych giełdowych na podstawie symbolu akcji.
2. Wyświetlanie tabeli z danymi historycznymi akcji (otwarcie, zamknięcie, wolumen).
3. Generowanie statystyk opisowych (średnia, mediana, odchylenie standardowe, itp.).
4. Wyświetlanie wykresów:
   - Statycznych (cena zamknięcia, wolumen).
   - Interaktywnych (histogram, boxplot, violin plot, stopy zwrotu).
5. Responsywny interfejs użytkownika zbudowany przy użyciu HTML i CSS.

---

## Wymagania Systemowe
1. Python 3.11 z zainstalowanymi bibliotekami:
   - Flask (2.3.2)
   - Alpha Vantage (1.0.0)
   - Pandas (2.1.1)
   - Matplotlib (3.8.0)
   - Plotly (5.16.0)
2. Przeglądarka internetowa do uruchomienia interfejsu aplikacji.
3. Połączenie internetowe do komunikacji z API Alpha Vantage.
4. Edytor kodu, np. Visual Studio Code (1.83.1).

---

