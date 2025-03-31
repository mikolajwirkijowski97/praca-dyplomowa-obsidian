## Model RGB

Model RGB jest najpowszechniej stosowanym modelem barw w grafice komputerowej, stosowanym praktycznie we wszystkich urządzeniach elektronicznych z wyświetlaczami. Jest to model addytywny, w którym kolory powstają przez nakładanie na siebie trzech barw podstawowych: czerwonej (Red), zielonej (Green) i niebieskiej (Blue).

Intensywność każdej z barw składowych wyrażana jest najczęściej w zakresie od 0 do 255 (8 bitów na kanał) lub od 0 do 1. Przykładowo, kolor czarny reprezentowany jest jako (0, 0, 0), a biały jako (255, 255, 255).

Model RGB można przedstawić geometrycznie jako sześcian, w którym trzy podstawowe osie reprezentują intensywność poszczególnych barw. W jednym rogu sześcianu znajduje się czerń, a w przeciwległym – biel.

Model RGB działa dobrze w urządzeniach wyświetlających, które wykorzystują fizyczne źródła światła RGB umieszczone blisko siebie. Ludzkie oko nie jest w stanie rozróżnić poszczególnych punktów świetlnych z odpowiedniej odległości, co tworzy wrażenie jednolitego koloru.

Pomimo swojej powszechności, model RGB ma ograniczoną użyteczność dla ludzi ze względu na nieintuicyjny sposób mieszania kolorów i trudność w przewidywaniu rezultatów zmian poszczególnych składowych.

## Model CMY i CMYK

Model CMY składa się z trzech kolorów: niebieskozielonego (Cyan), różowofioletowego (Magenta) i żółtego (Yellow). Jest to model subtraktywny, co oznacza, że kolory powstają przez odejmowanie (pochłanianie) światła, a nie przez jego dodawanie jak w przypadku RGB.

CMYK rozszerza model CMY o czarny komponent (blacK), stąd nazwa CMYK. Dodanie czarnego pigmentu wynika z praktycznych niedoskonałości w uzyskiwaniu głębokiej czerni przez samo nakładanie C, M i Y, które w rzeczywistych warunkach daje raczej odcień ciemnobrązowy.

Model CMYK jest powszechnie stosowany w druku, gdzie kolory nakładane są na biały papier. Każdy z nakładanych pigmentów pochłania (odejmuje) część światła odbijanego od papieru, tworząc zamierzony kolor.

Wprowadzenie czarnego pigmentu ma także uzasadnienie ekonomiczne – drukowanie dużych obszarów czarnego tekstu czy grafiki z użyciem tylko trzech barw podstawowych byłoby kosztowne i nieefektywne.

Model CMYK ma pewne ograniczenia, takie jak mniejsza paleta barw w porównaniu z RGB oraz zależność od jakości podłoża i pigmentów.

## Modele HSV, HSB i HSL

Modele HSV (Hue, Saturation, Value), HSB (Hue, Saturation, Brightness) i HSL (Hue, Saturation, Lightness) również są przekształceniami modelu RGB, ale w sposób, który znacznie lepiej odpowiada ludzkiemu postrzeganiu kolorów. Składają się z trzech parametrów:

1. **Hue (odcień)** – kolor bazowy, wyrażany najczęściej jako kąt w zakresie 0-360 stopni.
2. **Saturation (nasycenie)** – intensywność koloru, od bladego (0%) do intensywnego (100%).
3. **Value/Brightness/Lightness (jasność)** – ilość światła, od ciemnego (0%) do jasnego (100%).

Modele te można przedstawić geometrycznie jako walec (HSL), pojedynczy stożek (HSV) lub podwójny stożek (HSL). W reprezentacji walcowej, na przykład, oś walca reprezentuje jasność, odległość od osi to nasycenie, a kąt wokół osi oznacza odcień.

Dzięki temu, że parametry w tych modelach mają bardziej intuicyjne znaczenie dla człowieka, są one często wykorzystywane w aplikacjach graficznych jako interfejs do wyboru kolorów, nawet jeśli wewnętrznie program operuje na modelu RGB.