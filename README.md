# MachineLearning_UFC
Model ML pisany w Jupyter Lab - Przewidywanie wyniku walk pomiędzy dwoma zawodnikami.

1. Problem badawczy:
    • Projekt ma na celu stworzenie modelu do przewidywania wyników walk w zawodach UFC na podstawie dostępnych danych o zawodnikach.
    • Wykorzystano dane zawarte w pliku CSV, a następnie przetworzono je i zbudowano model klasyfikacyjny.
2. Przetwarzanie danych (UFCDataProcessor):
    • Wczytanie danych z pliku CSV do obiektu DataFrame.
    • Usunięcie wierszy, w których kluczowe kolumny zawierają wartości null.
    • Zastąpienie zerowych wartości w niektórych kolumnach średnią wartością danej kolumny.
    • Usunięcie wierszy, w których dowolna kolumna (spoza kluczowych) ma wartość null.
    • Uzupełnienie brakujących wartości w kolumnie 'stance' wartością 'brak'.
    • Utworzenie kolumny 'stance_number' na podstawie mapowania wartości 'stance'.
    • Podział kolumny 'name' na 'name' i 'surname'.
    • Uporządkowanie kolumn w odpowiedniej kolejności.
    • Wyświetlenie przetworzonego DataFrame.
3. Analiza danych (UFCDataAnalyzer):
    • Charakterystyka statystyczna danych, identyfikacja nierównowag klas.
    • Statystyki wybranych kategorii, np. częstotliwość występowania poszczególnych postaw ('stance').
    • Statystyki atrybutów, takie jak skuteczność uderzeń czy skuteczność takedownów.
    • Statystyki wielowymiarowe, w tym macierz korelacji.
4. Model klasyfikacyjny (RandomForestClassifier):
    • Wybór cech do modelu na podstawie analizy danych.
    • Przygotowanie danych, standaryzacja cech.
    • Podział danych na zbiór treningowy i testowy.
    • Zbudowanie modelu RandomForestClassifier z optymalnymi parametrami.
    • Trenowanie modelu na danych treningowych.
    • Kalibracja modelu.
    • Ocena modelu na zbiorze testowym.
    • Dodatkowo, stworzenie interakcji między cechami dla dodatkowej analizy i ulepszenia modelu.
5. Przewidywanie wyników pojedynków:
    • Użytkownik podaje dane dwóch zawodników (imię, nazwisko) do przewidzenia wyniku pojedynku.
    • Jeśli dane są dostępne dla obu zawodników, model przewiduje prawdopodobieństwo zwycięstwa każdego z nich.
    • Wyświetlenie przewidywanego zwycięzcy i jego prawdopodobieństwa.
6. Uzasadnienie wyboru modelu:
    • RandomForestClassifier został wybrany ze względu na zdolność do radzenia sobie z różnymi typami danych oraz efektywne radzenie sobie z problemami klasyfikacyjnymi.
    • Kalibracja modelu pozwala na uzyskanie bardziej wiarygodnych prawdopodobieństw przewidywań.
7. Uzyskane wyniki:
    • Model został oceniony na zbiorze testowym, a dokładność wyniosła około X%. (Wartość dokładności zostanie uzyskana po wykonaniu kodu).
    • Przewidywanie wyników pojedynków jest możliwe po podaniu danych dwóch zawodników.
8. Wnioski:
    • Model jest przygotowany do przewidywania wyników walk w UFC na podstawie dostępnych danych.
    • Analiza statystyczna i wielowymiarowa pozwoliła zrozumieć charakterystykę danych.
    • Przyjęty model klasyfikacyjny może nie być optymalny.
    • Interakcje między cechami mogą poprawić zdolności modelu do przewidywania wyników.


Kacper Nowicki, Jakub Wawrzyniak CDV 02.02.2024
