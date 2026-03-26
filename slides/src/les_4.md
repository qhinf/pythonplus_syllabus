<!-- .slide: data-background-gradient="linear-gradient(to bottom right, #f1881c, #ffffff)" -->

# Python Plus

Q-highschool / Les 4: Structuur van je project

***

## Vandaag

- Bestanden en mappen
- Functies: klein en gefocust
- Gegevens bijhouden
- Opdracht: bestandsstructuur
- Werken aan je project

***

## Waarom structuur?

Een groot programma in één bestand wordt al snel onoverzichtelijk.

<!-- .element: class="fragment" -->

Splits je code op in **logische stukken**.

<!-- .element: class="fragment" -->

Notes:
Vergelijk het met een boek: hoofdstukken en paragrafen maken het leesbaar.

---

## Bestandsstructuur

```
mijn_project/
├── main.py          # startpunt
├── spel.py          # spellogica
├── speler.py        # spelerklasse
├── data/
│   └── scores.json  # opgeslagen data
└── README.md        # uitleg
```

---

## Eén bestand = één onderwerp

- `main.py` – start het programma
- `utils.py` – hulpfuncties
- `config.py` – instellingen

Notes:
Laat een voor-na-voorbeeld zien met een klassiek monolithisch bestand vs. gesplitst.

***

## Functies

---

## Kleine functies

```python
# ❌ Te groot
def verwerk_alles():
    # 100 regels code...

# ✅ Klein en gefocust
def lees_invoer():
    ...

def bereken_resultaat(invoer):
    ...

def toon_uitvoer(resultaat):
    ...
```

---

## De "één taak"-regel

Een goede functie doet **één ding** en doet dat goed.

Als je een functie moeilijk kunt benoemen, doet hij waarschijnlijk te veel.

***

## Gegevens bijhouden

---

## In het geheugen

```python
scores = []

def voeg_score_toe(naam, punten):
    scores.append({"naam": naam, "punten": punten})
```

Verdwijnt als het programma stopt.

---

## Opslaan in een bestand

```python
import json

def sla_scores_op(scores, bestandsnaam):
    with open(bestandsnaam, "w") as f:
        json.dump(scores, f)

def laad_scores(bestandsnaam):
    with open(bestandsnaam, "r") as f:
        return json.load(f)
```

---

## Andere opties

- **CSV** – eenvoudige tabellen (`csv` module)
- **JSON** – geneste data (`json` module)
- **SQLite** – als je écht veel data hebt (`sqlite3` module)

***

## Opdracht: bestandsstructuur

Bekijk je eigen project:

1. Welke onderdelen kun je uit `main.py` halen?
2. Maak een plan: welk bestand krijgt welke code?
3. Voer de splitsing uit

Zie de syllabus: opdracht *Bestandsstructuur*

Notes:
Geef 15-20 minuten voor de opdracht. Rondlopen voor vragen.

***

## Aan de slag!

- Doe de opdracht bestandsstructuur
- Voortgangsgesprekken: kom even langs

Notes:
Individuele voortgangsgesprekken. Let op: wie loopt achter?
