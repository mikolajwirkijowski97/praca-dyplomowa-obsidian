## 1. Model kaskadowy (wodospadowy)

Jest to klasyczny, sekwencyjny model wytwarzania oprogramowania.

**Charakterystyka:**

- Jasno zdefiniowane i uporządkowane fazy
- Przejście do kolejnej fazy dopiero po zakończeniu poprzedniej
- Dokładne badanie wymagań przed rozpoczęciem prac

**Fazy:**

1. Planowanie
2. Analiza wymagań
3. Projektowanie
4. Implementacja
5. Testowanie
6. Wdrożenie
7. Utrzymanie

**Zalety:**

- Prosty i łatwy w zarządzaniu
- Jasno określone granice między fazami
- Dobra dokumentacja

**Wady:**

- Brak elastyczności wobec zmieniających się wymagań
- Trudności w zrównoleglaniu prac
- Produkt końcowy dostępny dopiero po ukończeniu całego procesu

## 2. Model V

Rozszerzona wersja modelu kaskadowego, która dodaje odpowiadające fazy testowania.

**Fazy:**

1. Opracowanie wymagań ↔ Testy akceptacyjne
2. Analiza ↔ Testy systemowe
3. Projektowanie architektury ↔ Testy integracyjne
4. Implementacja komponentów ↔ Testy jednostkowe

**Zalety:**

- Wysoka jakość produktu
- Łatwiejsze utrzymanie
- Wczesne wykrywanie błędów

**Wady:**

- Duży narzut pracy i rozbudowana dokumentacja
- Słabo radzi sobie ze zmiennymi projektami
- Niewystarczające skupienie na weryfikacji przez klienta

## 3. Modele iteracyjne

### 3.1. Model iteracyjny w czystej postaci

**Charakterystyka:**

- System jest rozwijany w wielu iteracjach
- Każda iteracja dostarcza nowe funkcjonalności
- Każda wersja jest planowana, implementowana, testowana i konsultowana z klientem

**Zalety:**

- Zmniejszenie ryzyka związanego ze zmieniającymi się wymaganiami
- Większe zaangażowanie klienta
- Możliwość równoległej pracy nad różnymi elementami

**Wady:**

- Może wydawać się chaotyczny
- Narzut organizacyjny związany z planowaniem iteracji

### 3.2. Model spiralny

Połączenie modelu kaskadowego z iteracyjnym.

**Charakterystyka:**

- Cykliczne przechodzenie przez fazy: planowanie, analiza ryzyka, implementacja, testowanie
- Każdy cykl zaczyna się od identyfikacji celów i alternatyw
- Mocny nacisk na analizę ryzyka

**Zalety:**

- Systematyczna i uporządkowana praca
- Obniżenie ryzyka niepowodzenia
- Możliwość zaangażowania klienta przy każdej nowej wersji

**Wady:**

- Często przekracza budżet i czas
- Wymaga surowego nadzoru
- Konieczność tworzenia obszernej dokumentacji

### 3.3. Model przyrostowy

**Charakterystyka:**

- Każda dodana funkcjonalność jest w 100% gotowa
- System jest zawsze w pełni sprawny, choć niekompletny
- Wymaga możliwości podziału systemu na niezależne podsystemy

**Zalety:**

- Możliwość prezentowania działającego systemu w dowolnym momencie
- Elastyczność wobec zmieniających się wymagań
- Stały dostęp klienta do kolejnych wersji

### 3.4. Model prototypowy

**Charakterystyka:**

- Budowanie prototypów zamiast pełnej implementacji
- Prezentowanie klientowi makiet, animacji, częściowych implementacji
- Zbieranie feedbacku przed rozpoczęciem właściwego wytwarzania

**Zalety:**

- Zaangażowanie klienta i szybki feedback
- Identyfikacja wymagań przez demonstrację
- Walidacja koncepcji przed pełną implementacją

**Wady:**

- Klient może być niechętny finansowaniu prototypów
- Czasochłonność
- Ryzyko przenoszenia prototypowych rozwiązań do produkcji

## 4. Model komponentowy

**Charakterystyka:**

- Wykorzystanie istniejących komponentów z wcześniejszych projektów
- Modyfikacja i integracja gotowych elementów
- Testowanie integracyjne komponentów

**Zalety:**

- Szybkie i tanie wytwarzanie
- Elastyczność wobec zmian wymagań
- Ponowne wykorzystanie sprawdzonych rozwiązań

**Wady:**

- Ograniczona przydatność do wysoce spersonalizowanych projektów
- Nadmiarowy kod, który może nie być wykorzystywany
- Wymaga dobrej dokumentacji i testów komponentów

## 5. Metodyki zwinne (Agile)

Choć nie wymienione bezpośrednio w treści, warto wspomnieć również o tych popularnych obecnie podejściach:

**Przykłady:**

- Scrum
- Kanban
- Extreme Programming (XP)
- Feature-Driven Development (FDD)

**Charakterystyka:**

- Iteracyjne i przyrostowe podejście
- Skupienie na współpracy z klientem i adaptacji do zmian
- Regularne dostarczanie działającego oprogramowania

**Zalety:**

- Elastyczność wobec zmieniających się wymagań
- Szybkie dostarczanie wartości biznesowej
- Bliska współpraca z klientem

**Wady:**

- Trudności w oszacowaniu całkowitego czasu i kosztu projektu
- Wymaga zaangażowania klienta
- Może być wyzwaniem w dużych, formalnych organizacjach