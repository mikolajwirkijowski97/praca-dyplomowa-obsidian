## Wprowadzenie

Modele przetwarzania w Internecie definiują sposoby organizacji, dystrybucji i realizacji zadań obliczeniowych oraz zarządzania danymi w środowisku sieciowym. Wraz z rozwojem technologii internetowych i rosnącymi wymaganiami aplikacji, ewoluowały one od prostych, scentralizowanych struktur do złożonych, rozproszonych systemów. Niniejsze opracowanie przedstawia główne modele przetwarzania wykorzystywane we współczesnym Internecie, ich charakterystykę, zastosowania oraz zalety i ograniczenia.

## Model klient-serwer

Model klient-serwer stanowi fundament większości współczesnych usług internetowych. Opiera się na podziale funkcji między dwa typy podmiotów: klientów, którzy wysyłają żądania usług lub zasobów, oraz serwery, które przetwarzają te żądania i zwracają odpowiedzi.

Charakterystyka modelu klient-serwer:

- Jasny podział ról między klientami (zwykle aplikacje użytkowników) a serwerami (systemy przetwarzające i udostępniające zasoby)
- Komunikacja oparta na standardowych protokołach (HTTP, FTP, SMTP)
- Możliwość implementacji zarówno w wersji scentralizowanej (wszystkie usługi na jednym serwerze), jak i rozproszonej (różne usługi na różnych serwerach)

Model klient-serwer można rozwinąć do architektury wielopiennej, gdzie funkcje systemu są podzielone na odrębne, niezależnie działające warstwy (piętra). Typowym przykładem jest architektura trójpiętrowa, składająca się z:

- Warstwy prezentacji (interfejs użytkownika)
- Warstwy logiki biznesowej (przetwarzanie danych i implementacja reguł biznesowych)
- Warstwy danych (przechowywanie i zarządzanie danymi)

Dzięki takiemu podziałowi możliwe jest skalowanie poszczególnych warstw niezależnie od siebie, co zwiększa elastyczność i wydajność systemu. Model ten dominuje w aplikacjach internetowych, od prostych stron WWW po złożone systemy transakcyjne.

### Model Peer-to-Peer (P2P)

W modelu P2P wszystkie uczestniczące węzły (komputery) są równorzędnymi partnerami, pełniącymi jednocześnie rolę klientów i serwerów. Charakterystyczne cechy tego modelu to:

- Decentralizacja - brak centralnego serwera zarządzającego siecią
- Rozproszenie danych między wszystkimi uczestnikami
- Samoorganizacja - system działa nawet przy zmiennej liczbie aktywnych węzłów
- Odporność na awarię pojedynczych węzłów

Model P2P jest powszechnie wykorzystywany w systemach wymiany plików (BitTorrent), komunikacji (IRC) czy dystrybucji treści (np. dystrybucja obrazów Linuxa przez sieci peer-to-peer). Stanowi on efektywne rozwiązanie dla aplikacji wymagających wysokiej skalowalności i odporności na awarie, jednocześnie minimalizując potrzebę centralnej infrastruktury.