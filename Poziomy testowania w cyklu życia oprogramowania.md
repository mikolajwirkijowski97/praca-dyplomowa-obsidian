# Poziomy testowania w cyklu życia oprogramowania

W procesie wytwarzania oprogramowania testowanie odgrywa kluczową rolę w zapewnianiu jakości i niezawodności produktu końcowego. Proces testowania jest zorganizowany w hierarchiczną strukturę poziomów, z których każdy ma określone cele, zakres i moment wykonania w cyklu życia oprogramowania. Cztery główne poziomy testowania to: testy jednostkowe, testy integracyjne, testy systemowe oraz testy akceptacyjne.

## Testy jednostkowe (modułowe)

Testy jednostkowe koncentrują się na weryfikacji pojedynczych komponentów oprogramowania w izolacji od pozostałych części systemu. Ich celem jest upewnienie się, że każdy moduł poprawnie realizuje przypisane mu funkcje zgodnie z wymaganiami.

Te testy są zazwyczaj przeprowadzane przez autorów kodu lub innych programistów pracujących nad projektem. Stanowi to pewne wyzwanie, ponieważ twórcy oprogramowania mogą nieświadomie powielać te same błędy myślowe w kodzie i testach, lub zakładać wiedzę, której nie posiadają końcowi użytkownicy.

Dobrą praktyką jest stosowanie podejścia TDD (Test Driven Development), w którym najpierw tworzy się testy, a dopiero potem implementuje funkcjonalność. Pozwala to na lepsze zrozumienie wymagań i tworzenie bardziej testowalnego kodu.

Typowe defekty wykrywane na tym poziomie to wycieki pamięci, błędy wykonania oraz brak walidacji danych wejściowych. Procesy testów jednostkowych często nie są sformalizowane, jednak ich zaniedbanie może prowadzić do nawarstwiania się problemów na wyższych poziomach testowania.

## Testy integracyjne

Testy integracyjne weryfikują poprawną współpracę między modułami lub systemami. Ich głównym celem jest sprawdzenie komunikacji między komponentami, a także interakcji z systemem operacyjnym, sprzętem czy usługami zewnętrznymi. Na tym etapie rozpoczyna się również badanie wydajności oraz identyfikacja potencjalnych luk bezpieczeństwa.

Istnieją różne strategie prowadzenia testów integracyjnych:

- Strategia skokowa (big-bang integration) - wszystkie komponenty są integrowane jednocześnie, co wiąże się z wysokim ryzykiem niepowodzenia, ale jest szybsze
- Strategia przyrostowa, która może być realizowana:
    - Wstępująco (bottom-up) - zaczynając od najniższych poziomów hierarchii komponentów
    - Zstępująco (top-down) - zaczynając od najwyższych poziomów architektury systemu

Testy integracyjne często wymagają tworzenia zaślepek (stubs) i atrap (mocks) do symulowania zachowania komponentów, które nie są jeszcze dostępne lub są trudne do skonfigurowania w środowisku testowym.

## Testy systemowe

Testy systemowe oceniają kompletny, zintegrowany system pod kątem zgodności z wymaganiami funkcjonalnymi i niefunkcjonalnymi. Przeprowadza się je w środowisku jak najbardziej zbliżonym do produkcyjnego, aby symulować rzeczywiste warunki użytkowania.

Od wyników testów systemowych zależy, czy oprogramowanie nadaje się do pełnienia zamierzonych funkcji biznesowych. Optymalnie testy te powinny być wykonywane przez odrębny zespół testerów, aby zapewnić świeże spojrzenie i obiektywną ocenę produktu.

Testy systemowe obejmują szereg podkategorii:

- Testy funkcjonalne - weryfikujące zgodność z wymaganiami funkcjonalnymi
- Testy wydajnościowe - sprawdzające szybkość, skalowalność i stabilność systemu pod obciążeniem
- Testy regresyjne - zapewniające, że nowe zmiany nie wpłynęły negatywnie na istniejące funkcjonalności
- Testy bezpieczeństwa - identyfikujące potencjalne luki i zagrożenia
- Testy instalacji - weryfikujące poprawność procesu instalacji i konfiguracji
- Testy interfejsu użytkownika - oceniające użyteczność i zgodność z założeniami projektowymi

## Testy akceptacyjne

Testy akceptacyjne stanowią końcowy etap procesu testowania i potwierdzają, że system działa zgodnie z umową, oczekiwaniami klienta oraz obowiązującymi przepisami. Są one przeprowadzane z udziałem klientów i docelowych użytkowników, co pozwala na weryfikację, czy produkt rzeczywiście spełnia potrzeby biznesowe.

Na tym etapie zakłada się, że oprogramowanie jest już wolne od większości błędów, a głównym celem jest zbudowanie zaufania klienta do produktu. W ramach testów akceptacyjnych często organizuje się demonstracje funkcjonalności oraz uruchamia testy alfa (w kontrolowanym środowisku) i beta (z udziałem szerszej grupy użytkowników).

Wynikiem testów akceptacyjnych może być:

- Przyjęcie systemu
- Odrzucenie systemu
- Akceptacja warunkowa, wymagająca wprowadzenia określonych poprawek

## Zależności między poziomami testowania

Poziomy testowania tworzą piramidę, w której każdy kolejny poziom opiera się na wynikach poprzednich. Wczesne wykrywanie i usuwanie defektów na niższych poziomach (testy jednostkowe, integracyjne) znacząco redukuje koszty i czas naprawy błędów, które w przeciwnym razie ujawniłyby się na wyższych poziomach lub w środowisku produkcyjnym.

Skuteczne testowanie na wszystkich poziomach jest kluczowym elementem zapewnienia jakości oprogramowania i wpływa bezpośrednio na satysfakcję użytkowników końcowych oraz powodzenie projektu informatycznego.

Piramida - 
Unit Tests
Component Tests
Integration Tests
E2E Tests
Acceptance Tests