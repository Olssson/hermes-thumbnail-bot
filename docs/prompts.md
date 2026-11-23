# Gotowe prompty

## Przygotowanie miniatury dla konkretnego SKU

> Pracuj tylko na wierszu SKU `<SKU>` z pliku `<KATALOG_CSV>` i zdjęciach, które wskazałem. Wypisz potwierdzone cechy produktu i przygotuj prompt do miniatury e-commerce. Zachowaj proporcje, kolor, oznaczenia i rzeczywistą zawartość zestawu. Nie dodawaj cech ani akcesoriów, których nie potwierdzają materiały. Jeśli brakuje zdjęć lub opisu, zgłoś brak zamiast zgadywać.

## Dostosowanie konfiguracji do własnego katalogu

> Adapt this repository to my catalog. Ask for the SKU, title, description and image column names, input directory, output directory, and target dimensions. Use a supported image-generation API or a local generator if I explicitly select one; otherwise produce prompts and keep export local. Do not automate ChatGPT Web, import browser sessions, or copy credentials. Keep secrets out of Git. Start with one SKU and verify the exported file and its dimensions before enabling batch processing.

Zobacz [konfigurację katalogu i przepływ pracy](catalog-web.md).
