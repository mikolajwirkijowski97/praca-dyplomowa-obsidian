## Wstęp do projektowania baz danych

Modelowanie bazy danych to fundamentalny proces, który poprzedza jej faktyczną implementację. Aby prawidłowo zaprojektować bazę danych, należy najpierw zrozumieć cel jej powstania i określić, jakie dane będzie przechowywać oraz jak będą one ze sobą powiązane. Dobry projekt powinien być niezależny od konkretnej implementacji systemu zarządzania bazą danych (DBMS), co pozwala na elastyczność i łatwiejszą migrację w przyszłości.

Proces ten zaczyna się od projektowania logicznego, które można przeprowadzić przy użyciu diagramów ERD (Entity-Relationship Diagram) w narzędziach typu CASE (Computer Aided System Engineering), jak Oracle Designer czy Enterprise Architect.

## Reguły i zasady projektowania

### Encje (tabele/relacje)

Punktem wyjścia jest identyfikacja potrzebnych encji, czyli obiektów, które będą reprezentowane w bazie danych. Encje te stają się tabelami w modelu relacyjnym. Każda encja powinna:

- Mieć jednoznaczną nazwę, która odzwierciedla jej zawartość
- Zawierać odpowiedni zestaw atrybutów (kolumn), które przechowują dane o pojedynczym rekordzie
- Reprezentować jeden spójny koncept (np. Klient, Zamówienie, Produkt)

### Klucze

Klucze są fundamentalnym elementem w relacyjnych bazach danych, zapewniającym unikalność rekordów i umożliwiającym tworzenie powiązań między tabelami:

1. **Klucz główny (primary key)** - atrybut lub zestaw atrybutów, który jednoznacznie identyfikuje rekord w tabeli:
    - Klucz prosty - składa się z jednej kolumny
    - Klucz złożony - składa się z wielu kolumn
2. **Klucz kandydujący** - atrybut, który potencjalnie może pełnić rolę klucza głównego, ponieważ zawiera unikalne wartości
3. **Klucz obcy (foreign key)** - atrybut, który odnosi się do klucza głównego w innej tabeli, tworząc powiązanie między tabelami

W praktyce często zaleca się stosowanie kluczy sztucznych (ID), które oferują następujące korzyści:

- Pozostają niezmienne, co zabezpiecza integralność danych
- Przyspieszają operacje (szczególnie wstawiania i wyszukiwania)
- Są prostsze w zarządzaniu niż klucze złożone

### Związki (asocjacje)

Po zdefiniowaniu encji, określa się związki między nimi. Związki te charakteryzują się:

- **Licznością** - określa, ile obiektów jednego typu może być powiązanych z obiektem drugiego typu (1:1, 1
    
    , M
    
    )
- **Opcjonalnością/obowiązkowością** - czy związek musi istnieć dla każdego rekordu
- **Stopniem** - ile encji uczestniczy w związku:
    - Unarny - związek tabeli z samą sobą (np. Pracownik → Przełożony)
    - Binarny - łączy dwie encje
    - Ternarny - łączy trzy encje (np. w związku wiele-do-wielu z tabelą pośredniczącą)
    - N-arny - łączy n encji

Implementacja związków wymaga dodania kluczy obcych, które wskazują na klucze główne w powiązanych tabelach.

## Optymalizacja logiki - normalizacja bazy danych

Po stworzeniu podstawowego projektu, należy zweryfikować jego zgodność z wymaganiami i przeprowadzić normalizację, aby uniknąć anomalii CUD (Create, Update, Delete):

### Pierwsza postać normalna (1NF)

- Każda tabela musi mieć klucz główny
- Każda kolumna powinna być atomowa (nie zawierać list czy grup wartości)
- Nie można mieć grup kolumn reprezentujących podobne informacje
- Kolejność wierszy i kolumn jest nieistotna

### Druga postać normalna (2NF)

- Musi spełniać warunki 1NF
- Każda kolumna niebędąca częścią klucza musi być w pełni zależna od całego klucza głównego
- Kolumny muszą opisywać tylko to, co bezpośrednio dotyczy encji reprezentowanej przez tabelę

### Trzecia postać normalna (3NF)

- Musi spełniać warunki 2NF
- Kolumny muszą bezpośrednio zależeć od klucza głównego, nie mogą być zależne od siebie nawzajem
- Eliminuje zależności przechodnie (np. jeśli kolumna C zależy od B, a B zależy od klucza A, to C powinno być w innej tabeli)

Oprócz normalizacji, należy przestrzegać podstawowych zasad integralności:

- Klucze główne nigdy nie mogą zawierać wartości NULL
- Klucze obce muszą wskazywać na istniejące klucze główne lub być NULL (jeśli związek jest opcjonalny)

## Przykłady systemów zarządzania bazami danych

Popularne silniki relacyjnych baz danych to:

- Microsoft SQL Server
- Oracle Database
- MySQL
- PostgreSQL

Każdy z nich oferuje różne funkcjonalności i optymalizacje, ale podstawowe zasady modelowania pozostają takie same.

Dobrze zaprojektowana baza danych nie tylko prawidłowo przechowuje dane, ale także umożliwia ich efektywne pozyskiwanie, modyfikowanie i analizowanie, co jest kluczowe dla funkcjonowania współczesnych systemów informatycznych.