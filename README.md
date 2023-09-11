# Python+ Syllabus 

Deze syllabus maakt gebruik van Jupyter Book. Alle inhoudelijke bestanden staan in de map *syllabus*:

- *_config.yml* is de configuratie van dit "boek". Je moet daar in elk geval de titel aanpassen! Verder zijn in de meeste gevallen geen wijzigingen nodig, maar lees de comments vooral even door.
- *_toc.yml* is de inhoudsopgave, waarin alle bestanden waaruit de syllabus bestaat op een rijtje worden gezet. Dit bestand bepaalt de volgorde van de hoofdstukken en elk bestand dat niet in de lijst voorkomt, wordt ook geen onderdeel van de syllabus.
- *index.md* is de "homepagina" van deze syllabus (want die staat bij `root` in *_toc.yml*) met de gebruikelijke introductiedingen en een aantal belangrijke zaken.
- De rest van de bestanden vormen de inhoud van de syllabus.

## Benodigdheden

- Een recente versie van Python

## De syllabus bouwen

Zorg eerst dat je alle vereiste dependencies geïnstalleerd hebt:

```sh
pip install --user -r requirements.txt
```

Vervolgens kun je de syllabus bouwen met:

```sh
jupyter-book build syllabus
```

De homepagina staat dan in *syllabus\\_build\html\index.html*.

### Voor Pieter, omdat hij niks kan onthouden

#### First time build

```bash
git clone https://github.com/qhinf/syllabi.git
cd syllabi
git submodule init
git status
git add .
git commit -m "met een boodschap"
git push
git submodule update --remote
```

En dan wachten maar.

#### Na een update van de syllabus

```bash
cd syllabi
git submodule update --remote
git add .
git commit -m "grote boodschap"
git push
git submodule update --remote
```

En dan wachten maar.
