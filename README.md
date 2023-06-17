# Wtyczka

Spis treści
=======================

1. Funkcjonalność wtyczki
2. Wymagania systemowe 
3. Wymagane oprogramowanie 
4. Instalacja i uruchomienie 
5. Wady programu


=======================

1. Funkcjonalność wtyczki


Wtyczka posiada następujące funkcje:
- Obliczanie pola powierzchni metodą Gaussa między co najmniej trzema
  wybranymi punktami z możliwością wyboru jednostki pola (m2, hektary, ary)
- Obliczanie przewyższenia między dwoma wybranymi punktami.
- Wyświetlenie liczby zaznaczonych punktów.
- Wyczyszczenie okna wynikowego.
- Jest to wtyczka przydatna głównie podczas prac geodezyjnych, znacznie ułatwia i przyspiesza proces obliczeniowy.


=======================

2. Wymagania systemowe 

Program został napisany, z myślą o pracy na komputerach lub laptopach posiadających system operacyjny Windows.

=======================

3. Wymagane oprogramowanie 

Do uruchomienia programu potrzebne będzie środowisko python w wersji 3.8

Instalacja wtyczki wtyczki odbywa się w oprogramowaniu geoinformacyjnym Qgis wersja 3.22.6

Wygląd zewnętrzny wtyczki został stworzony w programie Qt Designer


=======================

4. Instalacja i uruchumienie

 Instalacja wtyczki:

 1. Otwarcie programu Qgis i wybranie z paska narzędzi opcji "Wtyczki"
 2. W oknie "Wtyczki" należy wybrać pierwszą opcję - "Zarządzaj wtyczkami", wyskoczy wówczas nowe okno 
 i z pasku po lewej stronie należy wybrać opcję "Instaluj z pliku ZIP"
 3. Wybranie pliku ZIP, który zawiera wtyczkę do zainstalowanie i kliknięcie opcji "Zainstaluj wtyczkę"
 4. Gdy proces instalacji przebiegnie prawidłowo wyskoczy komunikat  "Wtyczka zainstalowana pomyślnie"
 5. Wtyczka jest zlokalizowana na pasku narzędzi obok Plugin Builder (użytkownik widzi ikonę nadaną wtyczce)


Uruchomienie wtyczki:

Przed użyciem wtyczki należy zaimportować odpowiednie warstwy ( u nas warstwa „xy2000” oraz "xy92" ), w tym celu użytkownik wykonuje następujące kroki:

1. Wybranie z paska narzędzi opcji „Warstwa”.
2. Następnie z rozwiniętego paska wybieranie opcji „Dodaj warstwę tekstową CSV”.
3. Z zakładek zlokalizowanych po lewej stronie zakładek wybranie opcji „CSV” i zaimportowanie wybranej warstwy, po uprzednim zaznaczeniu w oknie „Format pliku” opcji Tab, Średnik, Przecinek.

4. Kliknięcie opcji „Dodaj”. Zaimportowana warstwa powinna się znaleźć w oknie „Warstwy” znajdującym się po lewej stronie programu.

Po zaimportowaniu warstw można sprawdzić działanie wtyczki.

1. Kliknięcie ikony wtyczki znajdującej na paska narzędzi
Chcąc obliczyć przewyższenia między 2 punktami, należy:
- wybrać za pomocą opcji „Zaznacz obiekty” tylko 2 punkty z wybranej warstwy 
2. Wybranie w oknie wtyczki przycisk „ Oblicz przewyższenie” 
3. Wynik obliczeń jest widoczny w oknie znajdującym się po lewej stronie wgranej wtyczki, wynik zostaje podany w metrach

W przypadku zaznaczenia na warstwie większej ilości punktów w oknie „Wynik” ukazuje się komunikat „Nieprawidłowa liczba punktów! Wybierz 2 punkty!”.

Jest to spowodowane faktem, że wtyczka liczy przewyższenia między tylko 2 wybranymi punktami.

W sytuacji, gdy użytkownik chce obliczyć pole powierzchni powinien:

1. Kliknąć w oknie wtyczki przycisk „Wyczyść okno”, tej opcji należy użyć, jeśli wyniki poprzednich obliczeń są widoczne w oknie wyników.

2. Wybrać za pomocą opcji „Zaznacz obiekty” minimum 3 punkty z wybranej warstwy.
   
3. Dokonać wyboru w jakiej jednostce pola chce otrzymać wynik i zaznaczyć wybraną, możliwe opcje:
-metry kwadratowe
-ary
-hektary

4. Kliknąć w oknie wtyczki przycisk  „Oblicz pole powierzchni”.
   
6. Wynik obliczeń w wybranej jednostce jest widoczny w oknie wynikowym .
   
W przypadku zaznaczenia zbyt małej liczby punktów ukaże się komunikat „ Nieprawidłowa liczba punktów! Wybierz minimum 3 punkty”

Wtyczka daje również możliwość wykazania ile punktów z warstwy zostało zaznaczonych, służy do tego przycisk w oknie wtyczki „Pokaż liczbę zaznaczonych obiektów”. 
Ilość punktów zostaje pokazana w oknie wynikowym.


=======================

5. Wady programu
   
-Wtyczka działa poprawnie przy jedenej aktywnej wartwie

-Program nie działa na wszystkich wersjach qgisa i pythona
