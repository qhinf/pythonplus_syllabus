# Eindopdracht Python+

## Wat ga je maken

Je hebt aan het begin van de cursus een keuze gemaakt wat je wil maken. Dit kan van alles zijn, zolang je het maar in de programmeertaal Python schrijft, versie 3.5 of hoger. Het doel van je project is dat je leert om een groter programma te schrijven in Python. Er komen nogal wat extra uitdagingen kijken bij het schrijven van een lang programma. Hieronder krijg je te zien waar op gelet wordt bij het beoordelen van je werk.

## Wat lever je in?

Je levert een zip-bestand van je Github repo aan in je Q-Highschoolportfolio. In dat zip-bestand staat de volledige directory-structuur van je project. Het is niet erg wanneer je niet weet hoe je dat moet doen, vraag dan even hulp van een medeleerling of de docent.

:::{warning} 
1. Geen zip-file van je project in de Q-Highschool portfolio is geen resultaat!
2. Wel een zip-file, maar enorme verschillen tussen de zip-file en je Github-repo is ook geen resultaat!
:::


De **deadline** voor het inleveren van je product is **{{ deadline }}**, het _eerste_ inlevermoment. Je mag je eindproduct natuurlijk eerder inleveren. Mocht je nu in tijdsnood komen en het eerste inlevermoment niet halen, dan kun je uitstel aanvragen. Doe dit vóór {{ deadline_uitstel_aanvragen }} met een mailtje aan je {{ docent }}: _{{ docent_email }}_. Je krijgt dan uitstel tot {{ deadline_uitstel }}.

## Checklist voordat je inlevert
- [ ] Zijn alle bestanden aanwezig?
  - [ ] Je Python-code
  - [ ] Alle ondersteunende bestanden (config-files, afbeeldingen, enz.)
  - [ ] Een `README` in Markdown (.md)
  - [ ] Installatie handleiding in de `README`
  - [ ] Een `requirements.txt`
- [ ] Heb je alle bestanden in je GitHub-repo gecommit en gepushed? 

## Beoordeling

| Criterium | Omschrijving | Maximale score |
|--|--|--|
| [Specificatie](les_1) | Er is een MoSCoW-document aanwezig en bevat een realistische, zinvolle specificatie van je programma. | 20 pt |
| Implementatie | Je hebt de *Must*-onderdelen van je MoSCoW-document uitgeprogrammeerd en in je programma zitten | 20 pt | 
| [Code leesbaarheid](les_2) | Je code voldoet volledig aan de PEP8 guidelines</br>Je maakt gebruik van zinnige variabele namen</br>Je code is voorzien van zinvolle commentaren | 30 pt |
| [Code correctheid](les_3) | Er zitten geen syntax errors of enorme bugs in je code | 10 pt |
| [Project structuur](les_4) | Je code heb je in verschillende Python-bestanden op logische wijze georganiseerd. Inclusief steunbestanden, zoals afbeeldingen. Je hebt een *requirements.txt*  in je repo staan, zodat andere programmeurs gemakkelijk je code kunnen  draaien. | 10 pt|
| [GitHub](les_1) | Je hebt de link naar je Github-repo tijdens de les met de docent gedeeld en op  het moment van inleveren is je code volledig gesynchroniseerd met de code, die je met de zip-file ingeleverd hebt. | 10 pt |

Wanneer je werk beoordeeld wordt, dan volgt de docent de door jou geschreven installatie-handleiding. 

Je kunt een totaal van 100 punten behalen voor je eindopdracht. Je eindcijfer voor de module is het aantal punten gedeeld door 10.

## Code kopieren
Je mag externe bronnen gebruiken als hulp bij het maken van je spel, want daar kun je veel van leren. Je mag ook stukjes code overnemen, maar die moet je wel uitgebreid van commentaar voorzien om uit te leggen wat die code doet (minstens 1 regel commentaar per regel code!) en in commentaar de bron vermelden. De bron vermelden betekent dat je een link naar de exacte bron toevoegt, dus "uit een video op YouTube" is geen bronvermelding! Een link naar de code is minimaal wat we verwachten. Indien de code via persoonlijke communicatie gedeeld, vermeld dan minstens de naam van de persoon en jouw relatie tot die persoon. Gebruik `# BRON:` om duidelijk aan te geven dat dit een bronvermelding is en zodat wij het makkelijk terug kunnen vinden. Bijvoorbeeld:

```python
# BRON: https://rosettacode.org/wiki/Reverse_words_in_a_string#Python
# Draai de volgorde van woorden in elke regel van de variabele tekst om, 
# dus deze twee regels worden dan:
# om, tekst variabele de van regel elke in woorden van volgorde de Draai
# dan: worden regels twee deze dus
# Eerst wordt de tekst per regel gesplitst, en loopen we over elke regel
for line in text.split("\n"):
    # Elke regel splitsen we dan bij elke spatie (dat is standaard met split)
    # en met [::-1] word dan die lijst van woorden omgedraaid. " ".join plakt
    # de woorden weer aan elkaar met spaties ertussen en dat wordt geprint.
    print(" ".join(line.split()[::-1]))
```

Ook code uit ChatGPT en andere chatbots dien je van een bronvermelding te voorzien. Zet dan ook de prompt die je hebt gebruikt in je commentaar.

Het is uitdrukkelijk niet de bedoeling dat je grote blokken code of het hele spel kopieert. In dat geval zien we het als plagiaat en zullen we daar ook naar handelen. Voor diegenen die dit ingewikkeld vinden: meer dan 5 regels code is een groot blok.



