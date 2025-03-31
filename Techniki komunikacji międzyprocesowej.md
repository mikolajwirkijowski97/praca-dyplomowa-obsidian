## Komunikacja oparta na plikach

Najprostsza metoda IPC polega na zapisywaniu i odczytywaniu danych z plików na współdzielonym nośniku. Jest uniwersalna i wspierana przez wszystkie systemy operacyjne. Chociaż jest prosta w implementacji, może być nieefektywna przy częstej wymianie informacji ze względu na narzut operacji dyskowych. Dodatkowo, przy jednoczesnym dostępie kilku procesów do jednego pliku mogą wystąpić problemy z niespójnością danych, jeśli nie zastosuje się odpowiednich mechanizmów synchronizacji.

## Sygnały (Signals)

Sygnały stanowią asynchroniczny mechanizm powiadomień, powszechnie wykorzystywany w systemach UNIX. Kiedy proces otrzymuje sygnał, tymczasowo wstrzymuje normalne wykonanie, aby obsłużyć zdarzenie. Popularne przykłady to SIGINT (sygnał przerwania wywołany przez Ctrl+C) czy SIGKILL (sygnał zakończenia procesu). Sygnały są odpowiednie do prostych powiadomień, ponieważ przekazują jedynie swój typ, bez dodatkowych danych. Proces może implementować własne procedury obsługi sygnałów, definiując specyficzne reakcje na różne ich rodzaje.

## Gniazdka (Sockets)

Gniazdka zapewniają dwukierunkowy kanał komunikacyjny między procesami, zarówno na tym samym komputerze, jak i w sieci. Mogą działać przy użyciu różnych protokołów – TCP oferuje niezawodną komunikację zorientowaną na połączenie, a UDP szybszą, lecz mniej pewną transmisję. Gniazdka lokalne (Unix domain sockets) optymalizują wydajność dla procesów na tej samej maszynie, unikając zbędnego narzutu protokołów sieciowych. Gniazdka są bardzo wszechstronne i stanowią podstawę większości komunikacji sieciowej, w tym architektury klient-serwer, na której opiera się internet.

## Kolejki komunikatów (Message Queues)

Kolejki komunikatów tworzą asynchroniczny kanał, gdzie procesy mogą umieszczać i pobierać wiadomości. Takie podejście rozdziela nadawców od odbiorców, pozwalając im działać niezależnie bez bezpośredniej synchronizacji. Kolejki zapewniają trwałość – wiadomości pozostają dostępne do momentu ich jawnego pobrania, co zwiększa odporność systemu na awarie. Sprawdzają się w scenariuszach równoważenia obciążenia oraz przy rozsyłaniu informacji do wielu procesów odbiorczych. Nowoczesne implementacje obejmują kolejki POSIX, RabbitMQ czy Apache Kafka dla systemów rozproszonych.

## Potoki (Pipes)

Potoki tworzą jednokierunkowy przepływ danych między procesami. Występują w dwóch odmianach:

1. Potoki nienazwane (anonymous pipes) łączą powiązane procesy (zazwyczaj relacje rodzic-dziecko) i istnieją tylko podczas działania połączonych procesów. Są powszechnie używane w środowiskach wiersza poleceń do łączenia operacji, np. `komenda1 | komenda2`.
2. Potoki nazwane (named pipes, FIFO) istnieją jako specjalne pliki w systemie plików i pozwalają na komunikację między niepowiązanymi procesami. Utrzymują się do momentu jawnego usunięcia.

Potoki są zorientowane strumieniowo, co czyni je idealnymi do sekwencyjnego przetwarzania danych, ale mniej odpowiednimi do losowego dostępu do informacji.

## Semafory (Semaphores)

Semafory to prymitywy synchronizacji regulujące dostęp do współdzielonych zasobów. Utrzymują licznik, który procesy mogą zwiększać lub zmniejszać, przy czym operacje blokują się, gdy określone warunki nie są spełnione. Semafory występują w dwóch głównych formach:

1. Semafory binarne funkcjonują jako mutexy (mutual exclusion locks), pozwalając tylko jednemu procesowi na dostęp do zasobu w danym momencie.
2. Semafory zliczające pozwalają na określoną liczbę jednoczesnych dostępów do zasobu.

Choć nie są zaprojektowane głównie do wymiany danych, semafory są niezbędne do koordynacji zachowania procesów i zapobiegania warunkom wyścigu w scenariuszach z pamięcią współdzieloną.

## Pamięć współdzielona (Shared Memory)

Pamięć współdzielona ustanawia region RAM, do którego może bezpośrednio uzyskać dostęp wiele procesów. Technika ta oferuje najwyższą wydajność wymiany danych, ponieważ po utworzeniu współdzielonego regionu nie jest wymagane pośrednie kopiowanie ani interwencja jądra systemu. Jednakże ta wydajność wiąże się ze zwiększoną złożonością, ponieważ programiści muszą implementować jawne mechanizmy synchronizacji (zazwyczaj przy użyciu semaforów lub mutexów) w celu zapobiegania problemom z jednoczesnym dostępem. Pamięć współdzielona jest szczególnie wartościowa dla aplikacji wymagających transferu danych o wysokiej przepustowości między procesami, takich jak przetwarzanie multimediów czy obliczenia naukowe.

## Zdalne wywołania procedur (RPC)

Zdalne wywołania procedur abstrahują złożoność komunikacji międzyprocesowej, sprawiając, że zdalne wywołania funkcji wyglądają jak lokalne. Gdy proces inicjuje RPC, podstawowy system zajmuje się pakowaniem parametrów, transmisją do zdalnego procesu, wykonaniem i zwrotem wyników. Takie podejście upraszcza rozwój aplikacji rozproszonych, ukrywając szczegóły komunikacji. Implementacje obejmują tradycyjne protokoły RPC, Java RMI oraz nowoczesne warianty jak gRPC, JSON-RPC czy XML-RPC. Systemy RPC zazwyczaj zawierają mechanizmy odkrywania usług oraz wsparcie dla uwierzytelniania i szyfrowania.

## Przekazywanie komunikatów (Message Passing)

Frameworki przekazywania komunikatów zapewniają ustrukturyzowaną komunikację poprzez jawnie zdefiniowane wiadomości. W przeciwieństwie do strumieniowego charakteru potoków, przekazywanie komunikatów zachowuje granice dyskretnych wiadomości i zazwyczaj obsługuje większe ilości danych niż sygnały. Technika ta może być implementowana synchronicznie (gdzie nadawca czeka na potwierdzenie) lub asynchronicznie (gdzie nadawca kontynuuje wykonanie natychmiast). Systemy przekazywania komunikatów często zawierają możliwości routingu i mogą wspierać różne wzorce komunikacji wykraczające poza prostą wymianę punkt-punkt. Nowoczesne implementacje obejmują MPI dla obliczeń o wysokiej wydajności oraz frameworki modelu aktora, jak Akka.