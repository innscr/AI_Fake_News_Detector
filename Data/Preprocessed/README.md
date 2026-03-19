
Ten etap projektu odpowiada za przygotowanie danych tekstowych do modelu wykrywającego fake newsy. Notebook zajmuje się wczytaniem danych, ich czyszczeniem oraz podziałem na zbiory treningowe i testowe.

#### Kroki przetwarzania danych

#### 1. Wczytanie i połączenie danych

Dane są ładowane przy użyciu pandas

Dodawana jest kolumna label

Zbiory są łączone w jeden DataFrame

#### 2. Czyszczenie danych

Usuwane są:

- brakujące wartości (NaN)

- duplikaty

#### 3. Czyszczenie tekstu

Zaimplementowana funkcja clean_text() wykonuje:

- zamianę tekstu na małe litery

- usunięcie linków (URL)

- usunięcie liczb

- usunięcie znaków specjalnych i interpunkcji

- redukcję nadmiarowych spacji

#### 4. Filtrowanie danych

Usuwane są bardzo krótkie teksty (< 50 znaków)

#### 5. Podział na zbiory

Dane są dzielone na:

- zbiór treningowy (80%)

- zbiór testowy (20%)

Z użyciem:

train_test_split

zachowania proporcji klas (stratify=y)
