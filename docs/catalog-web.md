# Katalog produktów → prompt → ChatGPT w przeglądarce → miniatura

To publiczny wariant procesu produkcyjnego. **Hermes przygotowuje instrukcję dla konkretnego produktu; generowanie odbywa się ręcznie w ChatGPT Web.** Skill nie jest integracją z kontem ChatGPT i nie kieruje tam automatycznie plików. Kod produkcyjny automatyzował przeglądarkę za pomocą Playwright; nie ma go w publicznym profilu. Nie kopiuj sesji, cookies ani firmowych katalogów. Zobacz [warunki OpenAI dla Europy](https://openai.com/policies/eu-terms-of-use/).

1. Zainstaluj [profil i skill](../README.md#instalacja), wybierz model w Hermesie i otwórz sesję z `-s catalog-thumbnail`. To oddzielna konfiguracja od logowania w witrynie ChatGPT.
2. W katalogu roboczym umieść swój CSV, np. z kolumnami `sku,nazwa,opis,zdjecia`. W ostatniej kolumnie możesz podać nazwy zdjęć lokalnych lub linki; nie udostępniaj całego katalogu, jeśli wystarczy jeden wiersz. Wskaż Hermesowi dokładny SKU i pliki referencyjne. Otwórz sesję w katalogu projektu zgodnie z README.
3. Przykładowe polecenie: „Dla SKU DEMO-001 przeczytaj wiersz z `katalog.csv`, wypisz wybrane zdjęcia i przygotuj prompt do ChatGPT Web. Nie wysyłaj żadnych plików.” Sprawdź, że prompt używa właściwego opisu i nie dopisuje części ani cech.
4. Otwórz [chatgpt.com](https://chatgpt.com/) w swojej przeglądarce i zaloguj się samodzielnie. Dodaj zatwierdzone zdjęcia, wklej prompt, wygeneruj wariant i pobierz wynik przez interfejs ChatGPT. Nie przekazuj Hermesowi danych logowania. Do samego testu eksportu wystarczy zdjęcie z repo.
5. Zapisz pobrany plik lokalnie, wskaż go Hermesowi i poproś o porównanie z referencjami oraz eksport według [ustawień renderowania](workflow.md). Jeśli sesja nie ma narzędzia do oglądania obrazów, porównaj je samodzielnie. Przed publikacją sprawdź etykiety, kolory i zawartość zestawu.

Tryb automatyczny wymaga osobnego, wspieranego interfejsu generowania obrazów. Publiczny profil nie zawiera takiego połączenia ani automatycznego pobierania z ChatGPT Web.
