<!-- .slide: data-background-gradient="linear-gradient(to bottom right, #f1881c, #ffffff)" -->

# Python Plus

Q-highschool / Les 2: Kwaliteit van code

***

## Vandaag

- Huiswerk bespreken: MoSCoW
- PEP 8: leesbare Python-code
- Tips voor een goede projectstart
- Werken aan je project

***

## Huiswerk: MoSCoW

Vertel aan je buurman/buurvrouw:

- Wat is je project-idee?
- Wat zijn je **Must haves**?

Notes:
Bespreken in tweetallen, daarna paar voorbeelden plenair.

---

## MoSCoW

| Prioriteit | Betekenis |
|------------|-----------|
| **M**ust have | Zonder dit is je project niet af |
| **S**hould have | Zou er graag in willen |
| **C**ould have | Leuk als het lukt |
| **W**on't have | Bewust buiten scope |

Notes:
Uitleg van de MoSCoW-methode als ze die nog niet kennen.

***

## PEP 8

De officiële stijlgids voor Python-code

---

## Waarom PEP 8?

- Code lees je vaker dan je schrijft
- Anderen moeten je code kunnen begrijpen
- Professionele standaard

---

## PEP 8: de belangrijkste regels

<div class="columns">
<div>

**Naamgeving**
- variabelen: `snake_case`
- functies: `snake_case`
- klassen: `PascalCase`
- constanten: `UPPER_CASE`

</div>
<div>

**Opmaak**
- 4 spaties per inspringing
- Maximaal 79 tekens per regel
- Spaties rondom `=` in assignments

</div>
</div>

---

## PEP 8 in VS Code

Installeer de **Flake8** of **Pylint** extensie:

1. Open Extensions (Ctrl+Shift+X)
2. Zoek "Flake8"
3. Installeer

Notes:
Demo: laat de extensie een fout markeren en leg uit wat het betekent.

***

## Leesbare code

---

## Goede namen

```python
# ❌ Niet leesbaar
x = 42
def f(a, b):
    return a * b

# ✅ Leesbaar
max_pogingen = 42
def bereken_oppervlak(breedte, hoogte):
    return breedte * hoogte
```

---

## Comments

```python
# Bereken het gemiddelde van de lijst
totaal = sum(scores)
gemiddelde = totaal / len(scores)
```

- Leg het **waarom** uit, niet het **wat**
- Niet elke regel hoeft een comment

Notes:
Goede comments zijn schaars maar waardevol. Code zegt wat er gebeurt, comments zeggen waarom.

***

## Tips voor je project

- Maak kleine, overzichtelijke functies
- Één functie = één taak
- Begin simpel, voeg daarna features toe
- Commit regelmatig!

---

## Aan de slag!

- Open je project in VS Code
- Begin met de **Must haves**
- Vraag hulp als je vastloopt

Notes:
Rondlopen voor individuele gesprekken over projectkeuze.
