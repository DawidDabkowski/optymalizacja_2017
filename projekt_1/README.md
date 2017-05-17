# Pivot Rules

Rozważamy następującą listę reguł wyboru zmiennych:

* `LARGEST COEFFICIENT`. Wybór zmiennej o największym wspołczynniku funkcji celu;
* `LARGEST INCREASE`. Wybór zmiennej, który prowadzi do największego wzrostu funkcji celu;
* `STEEPEST EDGE`. Wybór zmiennej, który prowadzi do wierzchołka w kierunku najbliższym wektorowi `c` (gradientowi funkcji celu);
* `BLAND'D RULE`. Wybór zmiennej wchodzącej o najmniejszym indeksie; jeżeli jest wiele wyborów zmiennej wychodzącej, to wybór zmiennej wychodzącej o najmniejszym indeksie;
* `RANDOM EDGE`. Wybór losowy (prawdopodobieństwo jednostajne).

Zbadaj, jak wybór reguły wpływa na liczbę wykonywanych przez algorytm sympleks kroków.

Zbadaj co najmniej *osiem* reguł (uzupełniając powyższą listę o reguły własne, np `SMALLEST INCREASE`), w tym powyższe, na co najmniej *dziesięciu* problemach testowych.

## Implementacja własnych reguł w InteractiveLPProblem

[[pivot_steps.sage]]

Program zawiera implementacje dwóch reguł: wybór najmniejszej/największej leksykograficznie zmiennej wchodzącej (`lexicographical_min_entering` / `lexicographical_max_entering`) i wybór najmniejszej/największej leksykograficznie zmiennej wychodzącej (`lexicographical_min_leaving`/`lexicographical_max_leaving`).

Regułę wybiera się w funkcjach `my_entering`, `my_leaving`.

[[testy/]]

Badany problem podaje się w formacie `.lp`. Treść problemu można wkleić bezpośrednio w kodzie lub odczytać z pliku (wymaga to odkomentowania odpowiedniego fragmentu kodu). W katalogu można znaleźć kilka przykładowych problemów.

