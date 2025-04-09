## INSTRUKCJA OBSŁUGI ŚRODOWISK

#### Jak postawić środowisko z samą bazą danych

1. Potrzebne pliki .env czyli w tym przypadku to będzie `.env-db` przekopiować do folderu devops
2. Włączyć środowisko za pomocą komendy `docker-compose -f docker-compose-db.yaml up`. Podczas wywoływania komendy należy znajdować się w folderze w którym znajduje się `docker-compose`

##### Uwagi
- Baza danych nie ma podpiętego `volume` co oznacza że przy każdej inicjalizacji będą się tam znajdować tylko pliki testowe z repozytorium `DB`. Jeśli będzie potrzebne środowisko z `volume` proszę o kontakt

#### Jak postawić środowisko backend z bazą
1. Potrzebne pliki .env czyli w tym przypadku to będzie `.env-db` oraz `.env-backend` przekopiować do folderu devops
2. Włączyć środowisko za pomocą komendy `docker-compose -f docker-compose-backend.yaml up`. Podczas wywoływania komendy należy znajdować się w folderze w którym znajduje się `docker-compose`