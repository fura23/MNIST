# Struktura przestrzeni MNIST w reprezentacji PCA + QDA

## Opis projektu
Projekt stanowi rozwiązanie zadania akademickiego dotyczącego analizy struktury zbioru MNIST w przestrzeni zredukowanej metodą PCA oraz modelowanej za pomocą QDA.

Celem projektu jest zbadanie, jak cyfry 0-9 są rozmieszczone w przestrzeni cech po redukcji wymiarowości, które klasy są do siebie najbardziej podobne w sensie statystycznym oraz czy te podobieństwa przekładają się na rzeczywiste błędy klasyfikacji.

## Zakres analizy
W projekcie wykonano następujące elementy:
- podział danych MNIST na zbiór treningowy i testowy,
- redukcję wymiarowości za pomocą PCA,
- dopasowanie klasyfikatora QDA w przestrzeni PCA,
- wyznaczenie średnich i macierzy kowariancji dla każdej klasy,
- obliczenie macierzy odległości Bhattacharyya pomiędzy parami cyfr,
- analizę wpływu liczby składowych PCA na separowalność klas,
- porównanie odległości między klasami z macierzą pomyłek klasyfikatora,
- wizualizację danych w przestrzeni 2D/3D po PCA.

## Wykorzystane metody
### PCA
PCA (Principal Component Analysis) służy do redukcji wymiarowości danych wejściowych. W przypadku MNIST pozwala przejść z 784 wymiarów do mniejszej liczby składowych, zachowując możliwie dużo informacji o zmienności danych.

### QDA
QDA (Quadratic Discriminant Analysis) modeluje każdą klasę jako osobny wielowymiarowy rozkład normalny o własnej średniej i macierzy kowariancji. Dzięki temu możliwe jest badanie podobieństwa klas nie tylko przez klasyfikację, ale także przez analizę parametrów rozkładów.

### Odległość Bhattacharyya
Odległość Bhattacharyya została wykorzystana do pomiaru podobieństwa pomiędzy parami rozkładów normalnych odpowiadających poszczególnym cyfrom. Małe wartości oznaczają silne nakładanie się klas, a duże wartości wskazują na lepszą separowalność.

## Zawartość repozytorium
- `README.md` — opis projektu,
- `raport.pdf` — końcowy raport z analizą i interpretacją wyników,
- `notebook.ipynb` — notatnik Jupyter zawierający kod i wyniki,
- `notebook.html` — eksport notatnika do formatu HTML.

## Wymagania
Projekt został przygotowany w Pythonie z użyciem bibliotek:
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `scipy`


## Wyniki analizy
W projekcie analizowano:
- które pary cyfr mają najmniejsze odległości Bhattacharyya,
- jak zmienia się separowalność klas wraz ze wzrostem liczby składowych PCA,
- czy klasy podobne statystycznie są częściej mylone przez klasyfikator QDA,
- jak wygląda struktura danych MNIST w przestrzeni 2D i 3D po redukcji PCA.

## Wnioski
Projekt pozwala porównać teorię i praktykę klasyfikacji:
- teoria: podobieństwo klas mierzone odległością między rozkładami,
- praktyka: rzeczywiste pomyłki klasyfikatora na zbiorze testowym.

Analiza pokazuje, w jakim stopniu geometryczna i probabilistyczna struktura danych MNIST wpływa na trudność rozpoznawania poszczególnych cyfr.

## Autor
Projekt wykonany w ramach zadania akademickiego z modeli analizy danych.

## License
This project is provided for viewing, downloading, running, and private modification only.
Redistribution, republication, commercial use, and claiming authorship or ownership are prohibited without prior written permission from the author.
