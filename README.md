# school-project

Jednoduchá **Django** aplikácia (školský/učebný projekt).

## Inštalácia

```bash
# 1. Vytvor a aktivuj virtuálne prostredie
python -m venv venv
source venv/Scripts/activate      # Windows (Git Bash)
# source venv/bin/activate        # Linux / macOS

# 2. Nainštaluj závislosti
pip install -r requirements.txt

# 3. Nastav premenné prostredia
cp .env.example .env
# vyplň DJANGO_SECRET_KEY (vygeneruj ho príkazom v .env.example)

# 4. Priprav databázu
python manage.py migrate
```

## Spustenie

```bash
python manage.py runserver
```

Testovací endpoint:

- http://127.0.0.1:8000/school/hello-world/
- admin: http://127.0.0.1:8000/admin/ (najprv `python manage.py createsuperuser`)

## Štruktúra

```
school_project/   # konfigurácia projektu (settings, urls, wsgi/asgi)
school_app/        # aplikácia (views, urls, models)
manage.py          # správcovský nástroj Django
```

## Bezpečnosť

`SECRET_KEY` a ďalšie citlivé nastavenia sa načítavajú z `.env` (mimo gitu).
Databáza `db.sqlite3` a `__pycache__` sa necommitujú.
