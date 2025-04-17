## INSTRUKCJA OBSŁUGI ŚRODOWISK

#### Jak postawić środowisko z samą bazą danych

1. Potrzebne pliki .env czyli w tym przypadku to będzie `.env-db` przekopiować do folderu devops
2. W folderze devops uruchomić następujące komendy:
    - `docker compose -f docker-compose-db.yaml down --remove-orphans`
    - `docker compose -f docker-compose-db.yaml up --pull always --force-recreate`

#### Jak postawić środowisko backend z bazą
1. Potrzebne pliki .env czyli w tym przypadku to będzie `.env-db` oraz `.env-backend` przekopiować do folderu devops
2. W folderze devops uruchomić następujące komendy:
   - `docker compose -f docker-compose-backend.yaml down --remove-orphans`
   - `docker compose -f docker-compose-backend.yaml up --pull always --force-recreate`

### Uwagi
- Baza danych nie ma podpiętego `volume` co oznacza że przy każdej inicjalizacji będą się tam znajdować tylko pliki testowe z repozytorium `DB`. Jeśli będzie potrzebne środowisko z `volume` proszę o kontakt
- Obie komendy należy uruchomić za każdym razem kiedy chce się zaaktualizować obraz. Najlepiej wykonywać je po prostu za każdym razem.
