# Bijlage: GitHub en PyCharm

In deze cursus is het verplicht Git te gebruiken. Hiermee houd je online de versies van je software bij. Ook kunnen wij als begeleiders makkelijk met je meekijken en je vorderingen zien. Uiteindelijk moet je een zip-file van je software vanuit GitHub maken en deze inleveren in je Q-highschool portfolio/inleverbakje. Deze handleiding bestaat uit twee delen. Je kunt kiezen om deel 1 te volgen of deel 2 te volgen. Het resultaat van de instructie is bij allebei hetzelfde. In de les gebruiken we deel 1 van de instructie.

1. Als eerste een repository in Git aanmaken en die koppelen aan PyCharm.
2. Als eerste een project in PyCharm aanmaken en die koppelen aan je GitHub.

## Wat is GitHub?

GitHub is een online platform om versies van je software bij te kunnen houden. Het Git-protocol is in 2005 door de bedenker van Linux, Linus Torvalds gepubliceerd. Hij heeft het gemaakt om het samenwerken in een software team en het bijhouden van de verschillende versies van software mogelijk te maken. Ondertussen is het Git-protocol de standaard bij software ontwikkelaars. Bijna alle Open Source projecten hebben een git-repo.

Binnen Git gebeurt alles in een repository of _repo_. Dit is de plek waar alle bestanden van je project zich bevinden. Met commando's als `git commit -a`, `git clone` of `git push`  kun je in GitHub met meerdere mensen samenwerken aan hetzelfde project. Zonder dat je bestanden op en neer hoeft te mailen of samen te voegen. In deze module werk je volledig in Git.

Waar staan de bestanden? Op de site van GitHub en op je computer. Met git-commando's kun je ervoor zorgen dat de bestanden op GitHub en op je computer gesynchroniseerd blijven.

## Eerst Git, dan PyCharm

1. Als je het nog niet hebt: maak een account aan op [GitHub](https://github.com).
2. Maak een private repository aan. Geef deze een begrijpelijke naam.
3. Voeg je docenten toe aan je Git-project, zodat we je voortgang kunnen zien en mee kunnen denken. Dit kan bij _Instellingen -> Collaborators -> Add people (by username)_. Voeg hier {{ docent }} toe.
4. Gefeliciteerd, je hebt nu je een Git-repo aangemaakt. Deze 'leeft' alleen nog maar op GitHub.
5. Kijk even rond in je repo.
6. Klik uiteindelijk op het groene knopje <span style='font-family: sans-serif; background-color:green; color: white;'><> Code</span>.
7. Kopieer de url die daar staat. Die ziet er ongeveer als volgt uit:
   `https://github.com/qhinf/pythonplus_syllabus.git`
8. Het wordt nu tijd om naar PyCharm te gaan.
9. Mocht je nog projecten geopend hebben, sluit deze allemaal.
10. Wanneer er geen projecten meer geopend zijn, krijg je drie keuzes. Een nieuw project aanmaken, een oud project openen of 'Get from VCS'. Kies voor deze laatste optie.
11. Plak nu de url, die je bij stap 7 gekopieerd hebt in dit veld.
12. Klik op Ok en de rest gaat vanzelf.
13. Mogelijk zal PyCharm je nog vragen om de git-tools te installeren. Doe dit.

## Eerst PyCharm, dan Git

Voor dit deel heb je al een Git-account nodig en heb je ook de `git`-gereedschappen geïnstalleerd op je laptop. Wanneer de `git`-gereedschappen niet op je laptop staan, dan zal PyCharm hier vanzelf melding van maken en ze voor je installeren. Dit neemt wat tijd in beslag.

1. Maak een nieuw project aan zoals uitgelegd in {doc}`Bijlage_nieuwproject`.
2. Klik op _Version Control_
3. Klik op _Share Project On_
4. Klik op *Github*
5. Geef de repository een herkenbare en duidelijke naam.<br>Kies voor *private*<br>Remote laat je staan zoals het is
   Geef bij *Description* een korte beschrijving van je project.<br>Klik op **Share**
6. Je krijgt een nieuw venster te zien met 'Add Files For Initial Commit' als titel.<br>Klik op *Add*
7. Als het goed is krijg je nu een melding 'Succesfully shared project on GitHub'.

Neem nu maar eens kijkje in je GitHub via je browser. Je ziet nu je kersverse Python project, gemaakt in PyCharm, in je GitHub staan.

## Code commit en push

Stel dat je een stuk code hebt afgeschreven. De code werkt en heeft een deel van de functionaliteit van je project afgerond. Of je bent gewoon even klaar met werken en wil stoppen. Dan is het verstandig om je code met GitHub te synchroniseren.

1. Sla eerst alle bestanden op met de toetscombinatie Ctrl-S
2. Klik in de linkerbalk van PyCharm op het icoontje dat eruit ziet als een lijntje met een bolletje.
3. Je ziet nu een overzicht van welke bestanden gewijzigd zijn ten opzichte van de vorige keer dat je een synchronisatie hebt uitgevoerd. Deze bestanden moet je eerst 'committen'. Dit doe je door alle gewijzigde bestanden te selecteren. Dit kun je handig doen door het hokje links naast *Changes* aan te vinken. 
4. Elke commit moet een boodschap bevatten. In die boodschap schrijf je kort wat er gewijzigd is. Bijvoorbeeld iets als: "De gameloop aangepast zodat audio op de achtergrond afspeelt" of "een bug met het besturen van Mario met de pijltjestoetsen verholpen".<br>
5. Klik op *Commit and Push*
6. Je krijgt een nieuw venster te zien. Klik hier op weer op *Push*

Neem nu maar eens kijkje in je repo op GitHub. Dan zie je dat je zojuist geschreven code in je repo op GitHub staat. Handig!

:::{Tip}
Wanneer je een deel van je code 'af' hebt of wanneer je stopt met werken voor deze dag, doe een *Commit & Push*! Zo raak je je code niet zo snel kwijt en hoef je plotseling een week werk te synchroniseren wanneer je docent {{ docent }} weer eens naar je code wil kijken 😉
:::