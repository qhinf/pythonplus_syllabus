<!-- .slide: data-background-gradient="linear-gradient(to bottom right, #f1881c, #ffffff)" -->

# Python Plus

Q-highschool / Les 5: Extra documenten

***

## Vandaag

- README.md – wat is het en waarom?
- Comments in je code
- requirements.txt
- Werken aan je project

***

## README.md

Het visitekaartje van je project.

---

## Wat staat er in een README?

- Wat doet je programma?
- Hoe installeer je het?
- Hoe gebruik je het?
- (Optioneel) Screenshots, voorbeelden

---

## Voorbeeld README

```markdown
# Mijn Spel

Een eenvoudig raadspel in Python.

## Installeren

```bash
pip install -r requirements.txt
```

## Uitvoeren

```bash
python main.py
```

## Hoe werkt het?

Raad het getal dat de computer heeft gekozen.
Je krijgt feedback of je te hoog of te laag zit.
```

Notes:
Laat een echte GitHub-pagina zien met een goede README als voorbeeld.

***

## Comments in je code

---

## Wanneer een comment?

```python
# ❌ Overbodig – de code zegt het al
getal = getal + 1  # tel 1 op bij getal

# ✅ Nuttig – legt het waarom uit
# Sla de vorige waarde op voor vergelijking later
vorige_waarde = getal
getal = getal + 1
```

---

## Docstrings

```python
def bereken_gemiddelde(cijfers: list) -> float:
    """
    Berekent het gemiddelde van een lijst met cijfers.

    Args:
        cijfers: lijst met getallen

    Returns:
        Het gemiddelde als float
    """
    return sum(cijfers) / len(cijfers)
```

Notes:
Docstrings zijn zichtbaar in VS Code als je over een functie hovert.

***

## requirements.txt

Welke externe packages gebruik jij?

---

## Aanmaken

```bash
pip freeze > requirements.txt
```

---

## Inhoud

```
requests==2.31.0
pygame==2.5.2
```

---

## Waarom?

Iemand anders kan jouw project dan installeren met:

```bash
pip install -r requirements.txt
```

Zie de bijlage *Requirements* in de syllabus.

***

## Checklist leesbaarheid

- ✅ README.md aanwezig en ingevuld
- ✅ Functies hebben duidelijke namen
- ✅ Nuttige comments op lastige plekken
- ✅ requirements.txt up to date
- ✅ Git is up to date

***

## Aan de slag!

- Schrijf of verbeter je README.md
- Maak een requirements.txt
- Voortgangsgesprekken: kom even langs

Notes:
Individuele voortgangsgesprekken. Wie is er klaar, wie heeft nog hulp nodig?
