### FAT (File Allocation Table)

FAT to jeden z najstarszych systemów plików, wywodzący się z MS-DOS. Istnieje w kilku wariantach: FAT12, FAT16 i FAT32, gdzie liczby oznaczają liczbę bitów używanych do adresowania bloków. Główne cechy systemu FAT:

- Prosta struktura z tabelą alokacji plików przechowującą informacje o lokalizacji danych
- Pliki i foldery zajmują pierwszą wolną lokalizację na dysku
- Ograniczone atrybuty plików (tylko READONLY, HIDDEN, SYSTEM, ARCHIVAL)
- Brak mechanizmu uprawnień
- Maksymalny rozmiar pojedynczego pliku wynosi 4 GB
- Nazwy plików ograniczone do 8 znaków w oryginalnej implementacji

### NTFS (New Technology File System)

NTFS to zaawansowany system plików opracowany przez Microsoft, który zastąpił FAT w nowszych wersjach systemu Windows. Charakteryzuje się następującymi cechami:

- Wszystkie pliki, katalogi i metadane są opisane w MFT (Master File Table)
- Wspiera nazwy plików zakodowane w Unicode UTF-16, do 255 znaków
- Oferuje szyfrowanie (EFS - Encrypting File System)
- Posiada mechanizm księgowania (journaling), który chroni przed błędami zapisu
- Implementuje system praw dostępu oparty na listach kontroli dostępu (ACL)
- Obsługuje kompresję danych w locie
- Wspiera transakcyjność operacji
- Teoretycznie pozwala na pliki o rozmiarze do 16 eksabajtów

Interesującą funkcją NTFS jest możliwość dodawania do plików alternatywnych strumieni danych (Alternative Data Stream), które pozwalają przechowywać dodatkowe informacje niewidoczne w standardowych narzędziach.

### Ext4 (Fourth Extended Filesystem)

Ext4 to system plików powszechnie używany w systemach Linux, oparty na alokacji indeksowej. Jego główne cechy to:

- Bloki są grupowane w "grupy bloków" dla efektywnego zarządzania
- Informacje o plikach przechowywane są w i-węzłach (inodes)
- Wykorzystuje strukturę superbloku, który zawiera metadane systemu plików
- Wspiera dowiązania symboliczne (skróty do plików) i twarde (odniesienia do tego samego i-węzła)
- Oferuje wysoką wydajność i odporność na fragmentację
- Umożliwia przechowywanie plików w ciągłych obszarach (extents)
- Jest wstecznie kompatybilny z ext2 i ext3

System plików ext4 wykorzystuje zaawansowane techniki indeksowania, gdzie i-węzeł zawiera wskaźniki bezpośrednie oraz pośrednie (1, 2 i 3 poziomowe), co pozwala efektywnie adresować zarówno małe jak i duże pliki.