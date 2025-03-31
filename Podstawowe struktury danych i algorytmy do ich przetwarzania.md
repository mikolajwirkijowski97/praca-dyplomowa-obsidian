
## Tablice (Arrays)

- **Charakterystyka:** Ciągły blok pamięci, stały czas dostępu O(1)
- **Złożoność:**
    - Dostęp: $O(1)$
    - Wstawianie/usuwanie na końcu: $O(1)$ amortyzowany
    - Wstawianie/usuwanie w środku: $O(n)$
- **Algorytmy:** wyszukiwanie liniowe $O(n)$, binarne $O(\log n)$ (dla posortowanych)

## Listy (Lists)

- **Lista jednokierunkowa:** Węzły zawierają dane i wskaźnik do następnego
- **Lista dwukierunkowa:** Węzły zawierają dane i wskaźniki do poprzedniego/następnego
- **Złożoność:**
    - Dostęp: $O(n)$
    - Wstawianie/usuwanie na początku: $O(1)$
    - Wstawianie po znanym węźle: $O(1)$

## Stosy (Stacks)

- **Charakterystyka:** LIFO (Last In, First Out)
- **Operacje:** push/pop/peek $O(1)$
- **Zastosowania:** sprawdzanie nawiasów, wywołania funkcji, odwracanie

## Kolejki (Queues)

- **Charakterystyka:** FIFO (First In, First Out)
- **Operacje:** enqueue/dequeue $O(1)$
- **Zastosowania:** BFS, buforowanie, szeregowanie zadań

## Drzewa (Trees)

- **Drzewo binarne:** Każdy węzeł ma najwyżej dwóch potomków
- **BST (Binary Search Tree):** Lewe poddrzewo < węzeł < prawe poddrzewo
    - Operacje: $O(h)$ gdzie h to wysokość
- **Drzewa zrównoważone:** AVL, Red-Black, B-Trees - operacje $O(\log n)$
- **Przechodzenie:** pre-order, in-order, post-order, level-order

## Grafy (Graphs)

- **Reprezentacje:** macierz sąsiedztwa $O(V^2)$, lista sąsiedztwa $O(V+E)$
- **Algorytmy:**
    - BFS: kolejka, $O(V+E)$, najkrótsze ścieżki w grafie nieważonym
    - DFS: stos/rekurencja, $O(V+E)$, wykrywanie cykli
    - Dijkstra: $O((V+E)\log V)$, najkrótsze ścieżki w grafie ważonym
    - Kruskal/Prim: $O(E\log V)$, minimalne drzewo rozpinające

## Tablice mieszające (Hash Tables)

- **Charakterystyka:** Mapowanie klucz-wartość przez funkcję mieszającą
- **Złożoność:** $O(1)$ średnio, $O(n)$ najgorszy przypadek
- **Kolizje:** łańcuchowanie, adresowanie otwarte
- **Zastosowania:** słowniki, cache, indeksowanie

## Kopce (Heaps)

- **Charakterystyka:** Drzewo binarne z właściwością kopca (rodzic większy/mniejszy od dzieci)
- **Operacje:** insert/extract min/max $O(\log n)$, build heap $O(n)$
- **Zastosowania:** heapsort, kolejki priorytetowe, algorytm Dijkstry

## Drzewa trie (Prefix Trees)

- **Charakterystyka:** Optymalizacja dla ciągów znaków, wspólne prefiksy
- **Złożoność:** $O(m)$ gdzie m to długość ciągu
- **Zastosowania:** słowniki, autouzupełnianie

## Struktury disjoint-set (Union-Find)

- **Charakterystyka:** Zarządzanie rozłącznymi zbiorami
- **Operacje:** find/union $O(\alpha(n))$ - prawie stała złożoność
- **Zastosowania:** algorytm Kruskala, wykrywanie cykli w grafie

## B-drzewa i B+-drzewa

- **Charakterystyka:** Zrównoważone drzewa wyszukiwań, wiele kluczy w węźle
- **Zastosowania:** bazy danych, systemy plików
- **Złożoność:** wszystkie operacje $O(\log n)$

## Skip listy

- **Charakterystyka:** Wielopoziomowe listy z "przeskokami"
- **Złożoność:** $O(\log n)$ średnio dla operacji wyszukiwania/wstawiania/usuwania
- **Zastosowania:** alternatywa dla zrównoważonych drzew