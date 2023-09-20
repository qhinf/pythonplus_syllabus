# Les 2: Leesbare code

## Tijdens de les

- Bespreken huiswerk opdracht MosCoW.
- PEP8 Guidelines en leesbare code
- Tips voor een goede start van je project
- Tijd voor werken aan je project en individuele gesprekken over keuze eindopdracht

## Na de les

- Weet je hoe je Python-code volgens de PEP8 guidelines moet schrijven en hoe je dit in PyCharm doet.
- Weet je hoe leesbare code eruit ziet.
- Heb je een start gemaakt met je project.

## Leesbare code

### PEP8 Guidelines

Wanneer je een boek leest, verwacht je ook dat je niet alleen een leesbaar lettertype hebt, maar ook dat er een bepaalde structuur in het boek zit. Hoofdstukken, punten, komma's, lijstjes en al die andere zaken. Deze structuur zorgt ervoor dat je sneller kan begrijpen wat er staat. Het bevordert de leesbaarheid. Bij het lezen van programmeercode is het precies hetzelfde. Je hebt bij Basis van Programmeren met Python een start gemaakt met programmeren en mogelijk niet heel erg gelet op de leesbaarheid. Dat is op zich niet erg. Maar wanneer je met andere mensen gaat samenwerken, dan is de leesbaarheid van je code erg belangrijk. Want je wil natuurlijk dat andere mensen ook kunnen begrijpen wat je bedacht en geschreven hebt. Het schrijven van leesbare code heeft niet alleen nu met samenwerken. Wanneer je je eigen code na een half jaar nog eens terugleest, dan ben je jezelf dankbaar wanneer je leesbare code hebt geschreven.

Voor Python zijn er richtlijnen voor het schrijven van leesbare code. Deze richtlijnen heten de PEP8 Guidelines. Je kunt ze [hier](https://peps.python.org/pep-0008/) vinden.

In de les ga je deze richtlijnen lezen en bespreken.

### Leesbare code

Wanneer je je code helemaal volgens de PEP8 Guidelines opgesteld hebt, dan is er nog een extra toevoeging, die je code leesbaarder maakt. *Commentaar*. In Python is dat een `#` voor je regel code.

Het volgende tekst is een aanpassing van https://kinsta.com/blog/python-comments/

#### Inline commentaar

Wil je een kort commentaar leveren om een verheldering van een regel code, dan zet je deze op dezelfde regel als de code. Het commentaar geeft uitleg van de betekenis van die regel.

```python
rand = x + 10 # Maak een rand van 10px
```

#### Block commentaar

Wordt een regel code langer dan 79 karakters door een inline commentaar? Dan zet je het op meerdere regels. Dit heet een *block commentaar*. Dit klinkt ook logisch als je meer uitleg nodig hebt. Volgens de PEP8 richtlijnen plaats je een block commentaar vóór het codeblock.

```python
# Sorteer de lijst op de eerste letter, omdat 
# de groupby functie naar sequentiele data zoekt.
persons.sort(key=lambda x:x[0])
data = groupby(persons, key=lambda x:x[0])
```

#### Multi line commentaar

#### Docstring commentaar

#### TODO commentaar

#### Wat schrijf je dan in een commentaar?

### Zo ziet het er uit
