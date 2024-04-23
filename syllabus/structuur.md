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
| Frets of Fire | Game            | Frets on Fire is een muziek-/ritmegame waarin spelers een gitaarcontroller of het toetsenbord gebruiken om muziek te spelen. Het doel is om noten te spelen die op het scherm verschijnen en zo muziektracks succesvol uit te voeren. | [Frets on Fire GitHub](https://github.com/skyostil/fretsonfire) |

## Readme.md
