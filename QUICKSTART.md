# Demo bez konta i klucza

Wymagania: ImageMagick 6 (`convert`) lub 7 (`magick`). W katalogu repo uruchom:

```sh
magick=convert
command -v magick >/dev/null && magick=magick
output=$(mktemp -d)
"$magick" demo/case-kd4082-kd2100/KD4082_01.jpg -auto-orient -resize '1080x1080>' -background white -gravity center -extent 1200x1200 -strip "$output/thumbnail.jpg"
printf '%s\n' "$output/thumbnail.jpg"
```

Otwórz wypisany plik: to nowy JPEG 1200 × 1200 z rzeczywistego zdjęcia produktu. Nie jest to generator kompozycji AI. Jeśli chcesz uruchomić również profil Hermes, przejdź do [instalacji skilla](README.md#instalacja).
