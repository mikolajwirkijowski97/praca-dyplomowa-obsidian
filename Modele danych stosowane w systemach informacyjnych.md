Modele (7) można podzielić na generacje :
- proste
	- model prosty
- klasyczne
	- hierarchiczny (lata 60)
	- sieciowy (lata 70)
	- relacyjny (lata 70)
- semantyczne
	- wielowymiarowy
	- obiektowy (około 85)
	- obiektowo-relacyjny

## 2.1 Model prosty, z ang. Flat, czyli płaski.

Ciężko nazwać go prawdziwym modelem ponieważ jest trywialny w swojej istocie.
Polega na przechowywaniu danych w postaci pojedynczych, zwykłych plików np. tekstowych, 
albo jakiś arkuszy.

Rekordy są odzwierciedlone w wierszach, a ich poszczególne atrybuty są kolumnami.
Nie ma tu miejsca na wiązanie elementów ze sobą w relacje, wszystko jest proste.
Dane mogą się tutaj duplikować i często wyszukiwanie jakiejś istotnej informacji może być trudne.

Format takiego pliku zazwyczaj sprowadza się do oddzielania kolumn jakimś znakiem specjalnym, a wiersze 
trafiają za znakiem nowej linii.



## 2.2 Model hierarchiczny

Tak jak wspomniałem wcześniej był popularny bardzo dawno temu, obecnie można go pewnie znaleźć tylko w bardzo starych systemach - legacy.

Jego budowa przypomina strukturę drzewa, czyli każdy potomek ma tylko jednego rodzica/węzeł nadrzędny,
a rodzic może mieć wiele węzłów potomnych.
To co jest nietypowe dla drzewa, to to, że nie rodzic wskazuje na potomków, 
lecz to potomkowie wskazują na rodzica.

Kolejnym następstwem takiej struktury jest to, że kiedy chcemy usunąć jakiś rekord nadrzędny, to
wiąże się to z usunięciem wszystkich jemu podrzędnych rekordów. 
Nie możemy również wstawiać rekordów gdziekolwiek - każdy rekord musi mieć rekord nadrzędny i 
mieć taki sam typ.

Hierarchia była zależna od fizycznej kolejności zapisanych rekordów (aby dostać się do węzła liścia, 
należało przejść całą trasę do niego - czyli sekwencyjny, !!! chyba nieprawda - powolny dostęp!!!)

Za przykład modelu hierarchicznego może posłużyć tutaj rejestr systemu Windows albo 
struktura katalogów na dysku.



## 2.3 Model sieciowy

Od modelu hierarchicznego odróżnia go przede wszystkim to, że pozwala na posiadanie wielu rodziców.
Taka właściwość dała mu dużo większą eleastyczność w odzwierciedleniu rzeczywistości.
Ze względu na tę cechę nie jest już struktury drzewiastej tylko grafem (cykle są dozwolone).

Charakterystyczne dla niego były 2 elementy/budulce: rekordy i zbiory.
Rekordy przechowywały pola na dane, a zbiory opisywały relację jeden-do-wielu między rekordami.
Ten jeden był właścicielem, a "wielu" to tzw. "członkowie". 

Biorąc pod uwagę możliwość posiadania wielu rodziców pozwalało to na systuację, w której
jeden rekord był na raz właścicielem wielu zbiorów (czyli miał swoje dzieci) 
oraz był członkiem wielu zbiorów (bo mógł mieć kilku rodziców)

Koniec końców oba poprzednie modele zostały wyparte przez model relacyjny.



## 2.4 Model relacyjny

Rzecz jasna opiera swoje działanie na pojęciu relacji. 
Oznacza to tyle, że wykorzystujemy tabele do reprezentowania jakiś danych o wspólnych cechach/atrybutach
Np. Każdy produkt ma swoją cenę

Tabela taka składa się z krotek i kolumn. Kolejność krotek nie ma tu znaczenia, a kolumny są 
po prostu atrybutami.

Każda relacja (tabela) posiada klucz główny (primary key), który sprawia, że krotka jest unikatowa.
Oczywiście można wykorzystywać kombinację kilku atrybutów, wtedy mówi się o kluczu złożonym.

Aby skutecznie powiązać ze sobą 2 tabele w relację potrzebujemy drugiego klucza - tzw. klucza obcego,
który wskazuje na klucz główny w innej tabeli.

W tym modelu bardzo istotna jest integralność tabel.
Tzn. nie powinniśmy dopuścić do sytuacji w której:
- klucz główny jest wartością NULL
- klucz obcy wskazuje na nieistniejący rekord w innej tabeli

Do operacji na modelu relacyjnym wykorzystuje się algebrę relacyjną, czyli takie operacje jak:
- suma
- różnica
- iloczyn kartezjański

Plus dochodzą do tego operacje zaprojektowane do modelu relacyjnego:
- selekcja
- przecięcie, część wspólna
- złączenia

Powszechnie wykorzystuje się do tego język SQL (Structured Query Language).
