### 1. Klasyfikacja pikselowa

Każdy piksel klasyfikowany jest niezależnie od innych, wyłącznie na podstawie jego wartości spektralnych.

### 2. Klasyfikacja obiektowa (OBIA - Object-Based Image Analysis)

Obraz najpierw dzielony jest na segmenty (obiekty) składające się z grup pikseli, a następnie klasyfikowane są całe obiekty, a nie pojedyncze piksele. Metoda ta uwzględnia nie tylko wartości spektralne, ale również kształt, teksturę, kontekst i relacje przestrzenne między obiektami.

## Zastosowania klasyfikacji obrazów satelitarnych

- Tworzenie map pokrycia terenu i użytkowania ziemi
- Monitorowanie zmian środowiskowych (wylesianie, pustynnienie)
- Ocena szkód po klęskach żywiołowych
- Planowanie przestrzenne i urbanistyczne
- Monitorowanie upraw i prognozowanie plonów
- Kartowanie zasobów naturalnych

W klasyfikacji pokrycia terenu na podstawie obrazów satelitarnych najczęściej wykorzystuje się światło z zakresu bliskiej podczerwieni (NIR - Near Infrared). Ten zakres spektralny jest szczególnie cenny z kilku powodów:

Bliska podczerwień (NIR, około 700-1100 nm) jest niezwykle efektywna w odróżnianiu typów roślinności i ocenie ich stanu zdrowotnego. Zdrowa roślinność silnie odbija promieniowanie w zakresie NIR, podczas gdy absorbuje większość światła widzialnego (zwłaszcza czerwonego). Ta właściwość pozwala na obliczanie wskaźników wegetacji, takich jak NDVI (Normalized Difference Vegetation Index).

Oprócz NIR, kluczowe zakresy spektralne używane w klasyfikacji pokrycia terenu to:

- Światło czerwone (620-700 nm) - używane w kombinacji z NIR do obliczania NDVI i innych wskaźników wegetacji, pomaga odróżnić tereny z roślinnością od obszarów bez roślinności.
- Światło niebieskie (450-520 nm) i zielone (520-600 nm) - przydatne do analizy środowisk wodnych, rozróżniania typów gleb i budynków.
- Średnia podczerwień (SWIR - Short Wave Infrared, 1100-3000 nm) - wykorzystywana do identyfikacji zawartości wilgoci w glebie i roślinności oraz rozróżniania typów minerałów i skał.