(hoofdstuk_structuur)=

# Professionele uitstraling geven

(bestandsstructuur)=

## Bestandsstructuur

Wanneer je net begint met programmeren, dan zijn je codebestanden vaak niet langer dan 100 tot 200 regels code. Dat past nog prima in één enkel bestand en is nog overzichtelijk ook. Wanneer je een groter project gaat schrijven, dan neemt het aantal regels code toe. Om dit overzichtelijk te houden, is het verstandig om je code over verschillende bestanden te verdelen. Stel dat je een applicatie maakt, die gebruik maakt van een database. Dan is het een verstandig idee om alle code, die voor de communicatie met de database-server zorgt, in een apart `.py`-bestand te zetten. 



Wanneer je bijvoorbeeld een game programmeert of een AI traint, dan heb je ook ondersteunenden bestanden nodig. Zoals afbeeldingen of templates. Deze bestanden zul je ook bereikbaar moeten hebben voor je code. Om nu alles in één map te gooien en zo een grote vergaarbak met 30 bestanden te hebben is onoverzichtelijk. En dat kan weer zorgen voor fouten in je code. Dus het hebben van een overzichtelijke bestandsstructuur is belangrijk voor de kwaliteit van je code. Deze structuur laat je terugkomen in je Git-repo. Maar hoe ziet een goeie bestandsstructuur er nu uit? Daar ga je in de onderstaande opdracht achter komen.

:::{exercise} Projectstructuur

**Doel**: Deze opdracht helpt je begrijpen hoe bestanden en mappen georganiseerd zijn binnen verschillende open source Python projecten.

1. Kies een project uit de lijst {ref}`projecten_lijst`
1. Verken de structuur van het project op GitHub. Noteer hoe de mappen en bestanden zijn georganiseerd, welke soorten bestanden er zijn, en wat hun functies lijken te zijn (bijvoorbeeld: broncode, documentatie, tests, configuratiebestanden, ...)
1. Maak een visuele representatie (zoals een mindmap of een diagram) van de projectstructuur
1. Schrijf een kort verslag waarin je de projectstructuur beschrijft en specifieke kenmerken benoemt zoals de aanwezigheid van een `README`, `LICENSE`, `.gitignore`, en `setup.py` bestanden. Zet je visuele representatie van de projectstructuur in dit verslag.
1. Zet je verslag (inclusief visuele representatie) in je GitHub-repo voor dit vak.

:::

(projecten_lijst)=

### Professionele projecten in Python

| Naam          | Wat is het      | Omschrijving                                                 | Link                                                         |
| ------------- | --------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Django        | Web framework   | Django is een hoogwaardig webframework voor Python dat het mogelijk maakt snel webapplicaties te ontwikkelen met een minimum aan code. Het volgt het model-template-view (MTV) architectuurpatroon. | [Django GitHub](https://github.com/django/django)            |
| Flask         | Web framework   | Flask is een micro webframework voor Python, gebaseerd op Werkzeug en Jinja 2. Het is lichtgewicht en modulair, waardoor het eenvoudig is om met behulp van extensions uit te breiden. | [Flask GitHub](https://github.com/pallets/flask)             |
| Pandas        | Data verwerking | Pandas is een open source, BSD-gelicentieerde bibliotheek die high-performance, eenvoudig te gebruiken datastructuren en data analyse tools biedt voor de programmeertaal Python. | [Pandas GitHub](https://github.com/pandas-dev/pandas)        |
| Scrapy        | Web scraper     | Scrapy is een open source en collaboratief framework voor het extraheren van de gegevens die je nodig hebt van websites. In een snelle, eenvoudige, maar uitbreidbare manier. | [Scrapy GitHub](https://github.com/scrapy/scrapy)            |
| Matplotlib    | Grafisch        | Matplotlib is een uitgebreide bibliotheek voor het creëren van statische, geanimeerde en interactieve visualisaties in Python. Het biedt een object-georiënteerde API voor het embedden van plots in applicaties. | [Matplotlib GitHub](https://github.com/matplotlib/matplotlib) |
| Calibre       | App             | Calibre is een krachtige en eenvoudig te gebruiken e-boekmanager. Het kan gebruikt worden om e-boeken te organiseren, converteren, en uploaden naar e-readers, naast vele andere functies. | [Calibre GitHub](https://github.com/kovidgoyal/calibre)      |
| Audacity      | App             | Audacity is een gratis, open-source, cross-platform audiobewerkingssoftware. Het stelt gebruikers in staat om audio op te nemen en te bewerken. | [Audacity GitHub](https://github.com/audacity/audacity)      |
| Anki          | App             | Anki is een programma dat helpt bij het onthouden van informatie voor de lange termijn. Het maakt gebruik van flashcards en het spaced repetition systeem. | [Anki GitHub](https://github.com/ankitects/anki)             |
| KeePassXC     | App             | KeePassXC is een cross-platform wachtwoordbeheerder die gebruikers in staat stelt hun wachtwoorden veilig op te slaan in een versleutelde database. Het is ontworpen met veiligheid en eenvoud in gebruik als prioriteit. | [KeePassXC GitHub](https://github.com/keepassxreboot/keepassxc) |
| Spyder        | App             | Spyder is een krachtige wetenschappelijke omgeving geschreven in Python, voor Python, en ontworpen door en voor wetenschappers, ingenieurs en data-analisten. Het biedt een geïntegreerde ontwikkelomgeving (IDE) met geavanceerde bewerkings-, test-, debug-, en profileringsfuncties. | [Spyder GitHub](https://github.com/spyder-ide/spyder)        |
| Deluge        | App             | Deluge is een lichtgewicht, Free Software, cross-platform BitTorrent-client. Het biedt een rijke set aan functies, is volledig gratis en zonder advertenties. | [Deluge GitHub](https://github.com/deluge-torrent/deluge)    |
| PySolFC       | Game            | PySolFC is een verzameling van meer dan 1000 solitaire kaartspellen. Het is een fork van het originele PySol Solitaire. | [PySolFC GitHub](https://github.com/shlomif/PySolFC)         |
| Frets on Fire | Game            | Frets on Fire is een muziek-/ritmegame waarin spelers een gitaarcontroller of het toetsenbord gebruiken om muziek te spelen. Het doel is om noten te spelen die op het scherm verschijnen en zo muziektracks succesvol uit te voeren. | [Frets on Fire GitHub](https://github.com/skyostil/fretsonfire) |

## Een goede README

Als je een project begint in Python, is een van de eerste dingen die je moet doen het maken van een README.md-bestand. Dit bestand helpt anderen (en jezelf) om snel te begrijpen waar jouw project over gaat, hoe ze het kunnen installeren, gebruiken en eraan kunnen bijdragen. Hier zijn enkele stappen en tips om een effectieve README.md te schrijven. Je schrijft je README.md in een opmaak, die Markdown genoemd wordt. 

### 1. Titel en Beschrijving

Begin je README.md met een duidelijke en pakkende titel voor je project. Onder de titel plaats je een korte beschrijving die uitlegt wat je project doet en waarom het nuttig is.

**Voorbeeld:**

```markdown
# SuperCool Python Project

Dit project is een eenvoudige tool om afbeeldingen om te zetten naar ASCII-kunst. Het is bedoeld om te laten zien hoe je met Python en bibliotheken als Pillow en NumPy kunt werken.
```

### 2. Inhoudsopgave

Een inhoudsopgave helpt lezers om snel door je README te navigeren, vooral als het een langer document is. Gebruik markdown-links om naar verschillende secties in je README te verwijzen.

**Voorbeeld:**

```markdown
## Inhoudsopgave
1. [Installatie](#installatie)
2. [Gebruik](#gebruik)
3. [Features](#features)
4. [Bijdragen](#bijdragen)
5. [Licentie](#licentie)
```

### 3. Installatie

In dit gedeelte leg je uit hoe anderen jouw project kunnen installeren. Zorg ervoor dat je stapsgewijze instructies geeft. Als er externe afhankelijkheden zijn, vermeld deze dan ook.

**Voorbeeld:**

````markdown
## Installatie

1. Clone deze repository naar je lokale machine:
    ```bash
    git clone https://github.com/jouwgebruikersnaam/supercool-python-project.git
```
2. Navigeer naar de projectdirectory:
    ```bash
    cd supercool-python-project
    ```
3. Installeer de vereiste dependencies:
    ```bash
    pip install -r requirements.txt
    ```

> **Opmerking:** Zorg ervoor dat je Python en pip hebt geïnstalleerd.
````

### 4. Gebruik

Geef voorbeelden van hoe je project gebruikt kan worden. Je kunt codefragmenten en screenshots toevoegen om het duidelijker te maken.

**Voorbeeld:**

````markdown
## Gebruik

Na het installeren van de dependencies, kun je de tool gebruiken door het volgende commando uit te voeren:

```bash
python convert_to_ascii.py path/to/image.jpg
```

Het resultaat wordt opgeslagen in dezelfde directory als het bronbestand.
````

### 5. Features

Licht de belangrijkste kenmerken van je project toe. Dit geeft lezers een idee van wat ze kunnen verwachten en waarom jouw project nuttig is.

**Voorbeeld:**

```markdown
## Features

- Converteert afbeeldingen naar ASCII-kunst
- Ondersteuning voor meerdere afbeeldingsformaten (JPEG, PNG, etc.)
- Makkelijk aanpasbare ASCII-tekenset
```

### 6. Bijdragen

Moedig anderen aan om bij te dragen aan je project. Leg uit hoe ze bugmeldingen kunnen indienen, nieuwe features kunnen voorstellen of code kunnen bijdragen.

**Voorbeeld:**

````markdown
## Bijdragen

Bijdragen zijn altijd welkom! Volg deze stappen om bij te dragen:

1. Fork deze repository.
2. Maak een nieuwe branch voor jouw feature of bugfix:
    ```bash
    git checkout -b feature/nieuwe-feature
```
3. Commit je wijzigingen:
    ```bash
    git commit -m "Voeg nieuwe feature toe"
    ```
4. Push naar de branch:
    ```bash
    git push origin feature/nieuwe-feature
    ```
5. Open een Pull Request.
````

### 7. Licentie

Geef aan onder welke licentie je project valt. Dit is belangrijk voor juridische duidelijkheid over hoe jouw code gebruikt mag worden.

**Voorbeeld:**

```markdown
## Licentie

Dit project is gelicenseerd onder de MIT License. Zie het [LICENSE](LICENSE) bestand voor meer informatie.
```

Het schrijven van een goede README.md is een belangrijke stap in het ontwikkelen van een softwareproject. Het maakt je project toegankelijker en aantrekkelijker voor anderen om te gebruiken en eraan bij te dragen. Vergeet niet om je README regelmatig bij te werken als je project verandert.

