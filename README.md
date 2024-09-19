Hej Dominik tutaj znajdziesz opis zadania. Podstawowym użyciu z Git'a możesz poczytać: https://www.flynerd.pl/2018/02/github-dla-zielonych-pierwsze-repozytorium.html

Zadanie:
W repozytorium znajdzesz dwa pliki:
- products.xml (plik jest spakowany ponieważ nie wszedłby do repozytorium)
- productsAllegro.csv

Twoim zadaniem będzie przetworzenie tych dwóch plików w taki sposób aby powstał wynikowy plik csv w następującej postaci:

| data | kod | ean | cena netto | cena allegro |
|------| --- | --- | ---------- | ------------ |

- pole *data* -> dowolny format daty zawierający dzień, miesiąc, rok, godziny, minuty (data generowania tabeli)
- pole *kod* -> to kod produktu pobrany z pliku productsAllegro.csv
- pole *cena netto* -> cena netto dla produktu o danym kodzie pobrana z pliku products.xml
- pole *cena allegro* -> cena produktu pobrana z pliku productsAllegro.csv

1. Dla każdego wpisu z pliku productsAllegro.csv należy znaleść odpowiadającą cenę netto z pliku products.xml
2. Powyższa tabelka powinna być posortowana najpierw po dacie a później po kolumnie kod. Chcemy uzyskać efekt, że wpisy w tabeli są posortowane według daty i wszystkie produkty z tym samym kodem są obok siebie
3. Skrypt powinien się wywoływac w następujący sposób:  ```python nazwa_pliku_wynikowego.csv products.xml productsAllegro.csv```
4. Jeśli plik ```nazwa_pliku_wynikowego.csv``` już istnieje to idealnie by było nie nadpisywac go w pełni a dopisać z nową datą przetwarzania kolejne wiersze pliku i posortować go według reguły wyżej. W ten sposób uzyskamy historię zmian cen na allegro oraz w hurtowni.
