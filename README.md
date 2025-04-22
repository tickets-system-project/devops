## INSTRUKCJA OBSŁUGI ŚRODOWISK

#### Jak postawić środowisko z bazą danych oraz serwerem mailowym

1. Potrzebne pliki .env czyli w tym przypadku to będzie `.env-db` przekopiować do folderu devops
2. W folderze devops uruchomić następujące komendy:
    - `docker compose -f docker-compose-db.yaml down --remove-orphans`
    - `docker compose -f docker-compose-db.yaml up --pull always --force-recreate`

#### Jak postawić środowisko backend z bazą oraz serwerem mailowym
1. Potrzebne pliki .env czyli w tym przypadku to będzie `.env-db` oraz `.env-backend` przekopiować do folderu devops
2. W folderze devops uruchomić następujące komendy:
   - `docker compose -f docker-compose-backend.yaml down --remove-orphans`
   - `docker compose -f docker-compose-backend.yaml up --pull always --force-recreate`

### Uwagi
- Baza danych nie ma podpiętego `volume` co oznacza że przy każdej inicjalizacji będą się tam znajdować tylko pliki testowe z repozytorium `DB`. Jeśli będzie potrzebne środowisko z `volume` proszę o kontakt
- Obie komendy należy uruchomić za każdym razem kiedy chce się zaaktualizować obraz. Najlepiej wykonywać je po prostu za każdym razem.
- Serwer mailowy ma otwarty port `SMTP` na `1025`. Czy mail się wysłał można sprawdzić na `http://localhost:8025/`
