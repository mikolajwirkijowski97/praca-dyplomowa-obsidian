
# Podstawowe Pojęcia

## Złożoności
- **Złożoność Czasowa** - określa jak szybko algorytm działa w funkcji rozmiaru danych wejściowych. Jest to miara liczby operacji elementarnych wykonywanych przez algorytm.
- **Złożoność pamięciowa** - określa ile pamięci zużywa algorytm w funkcji rozmiaru danych wejściowych. Jest to miara pamięci zużywanej podczas wykonywania alorytmu.
- **Złożoność obliczeniowa** - Uogólnienie, obejmujące dwie powyższe złożoności.

## Notacja Asymptotyczna 

- **Duże O** - Ograniczenie z góry. Mówimy że funkcja f(n) jest O(g(n)), jeśli istnieją stałe c > 0 i n0 >= 0 takie, że dla wszytkich n >= n0, 0 <= f(n) <= c*g(n)
- **Duże Omega** - Ograniczenie z dołu. Funkcja f(n) jest Ω(g(n)) jeśli c·g(n) ≤ f(n)
- **Notacja Θ (duże Theta)** - dokładne ograniczenie. Mówimy, że funkcja f(n) jest Θ(g(n)), jeśli f(n) jest zarówno O(g(n)) jak i Ω(g(n)). Oznacza to, że f(n) rośnie dokładnie tak szybko jak g(n).
- **Notacja o (małe o)** - ścisłe ograniczenie z góry. Mówimy, że f(n) jest o(g(n)), jeśli dla każdego c > 0 istnieje n₀ ≥ 0 takie, że dla wszystkich n ≥ n₀, 0 ≤ f(n) < c·g(n). Oznacza to, że f(n) rośnie wolniej niż g(n).
- **Notacja ω (małe omega)** - ścisłe ograniczenie z dołu. Mówimy, że f(n) jest ω(g(n)), jeśli dla każdego c > 0 istnieje n₀ ≥ 0 takie, że dla wszystkich n ≥ n₀, 0 ≤ c·g(n) < f(n). Oznacza to, że f(n) rośnie szybciej niż g(n).
## Przykładowe algorytmy o danej złożoności

- $O(1)$ - Tablica haszowana, po prostu dostęp do tablicy
- $O(\log n)$ - Binary Search
- $O(n)$ - Przeszukiwanie liniowe
- $O(n \log n)$ - Merge sort
- $O(n^2)$ - Bubble sort
- $O(2^n)$ - Rekurencyjny algorytm na ciąg Fibonacciego