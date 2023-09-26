# Je Python project

In deze module ga je een groter project in Python uitwerken. Soms kan het ingewikkeld zijn om te bedenken wat je wil maken. Wanneer je al weet wat je wil maken, dan kun je de volgende sectie overslaan en verder gaan bij de sectie {ref}`moscow`.

## Project ideeën

Hieronder is een lijst van project ideeën en onderwerpen waar je met Python mee uit de voeten kan. Kijk door deze lijst en voel waar je enthousiast van wordt! Mogelijk is dat het onderwerp of idee, waar je iets mee wil.

| Onderwerp         | Onderdelen                                                   |
| ----------------- | ------------------------------------------------------------ |
| Games             | 1. Een spel in `pygame` namaken (eventueel met nieuwe graphics)<br />2. Je favoriete bordspel namaken<br />3. Je favoriete kaartspel namaken<br />4. Een text adventure maken |
| Bot               | Een Discord bot of Telegram bot schrijven die:<br />1. een spelletje met één of meerdere deelnemers kan spelen<br />2. prijsinformatie van het internet afhaalt<br />3. een text adventure speelt<br />4. een pubquiz houdt onder de deelnemers. |
| Web development   | 1. Een dynamische website programmeren in `Flask` of `Django`. Bijvoorbeeld een deel van de ledenadministratie van je sportclub of een messaging-platform met gebruikers of een interactieve klok.<br />2. Een eenvoudige webbrowser met PyWt, waarbij je zelf de Back-knop, bookmarks en nog meer uit moet programmeren<br />3. Bouw een scraper, die data van het internet afhaalt. Bijvoorbeeld een scraper voor prijsinformatie over electrische fietsen.<br />4. Een app, die kan weergeven of een website is 'veranderd' sinds de laatste keer dat je de site bezocht hebt.<br />5. Een app, waarmee willekeurige Wikipedia pagina's kan laten zien, waarbij je de gebruiker ook de optie geeft om categorieën aan te geven, waarbinnen een willekeurige pagina gezocht wordt. Je favoriete rabbit-hole app!<br />7. Een URL-shortener<br />8. Een Instagram-foto of reel downloader. |
| Machine learning  | 1. Train een netwerk op een dataset van Kaggle en bouw zo een prijs-voorspeller voor auto's of grafische kaarten of andere producten. <br />2. Train een netwerk om bepaalde typen beelden te herkennen. Bijvoorbeeld om katten, die in je tuin lopen te kunnen herkennen. |
| Data visualisatie | 1. Gebruik een dataset en de bibliotheek `Matplotlib` of een andere datavisualisatie bibliotheek om een (interactieve) diagram te maken over een onderwerp wat je interesseert. Het is bij dit onderwerp handig om ook na te denken over hoe je aan de data komt. Grote datasets kun je ook via Kaggle vinden. Misschien is het leuk om je diagram interactief te maken met een kaart en selectievakjes. Denk hierbij aan de manier waarop je mobiele telefoon een overzicht kan geven van welke foto's waar zijn gemaakt door ze op een kaart neer te zetten.<br />2. Analyzeer en visualiseer je eigen Netflix-data of jouw data van een ander social media platform. |
| Overige apps      | 1. Een Python-app, waarmee je handig notities kan maken<br />2. Automatiseer delen van je huiswerk (bijvoorbeeld een woordjes-leer-app)<br />3. Een quiz-app.<br />4. Een app die het bestandsformaat in een ander bestandsformaat omzet (bijvoorbeeld iets wat text naar PDF omzet)<br />5. Een app die allerlei eenheden converteert (cm naar inch, celsius naar fahrenheit, $m^2$ m naar $ft^2$, etc)<br />6. Een app die wisselkoersen voor buitenlands geld van het internet afhaalt en ze kan converteren van en naar €.<br />7. Een (grafische) rekenmachine<br />8. Een wachtwoord-generator (met opties)<br />9. Voor de commandline-nerds: een commandline app nabouwen (bijvoorbeeld `ls`/`dir` met een aantal opties)<br />10. Een alarmklok<br />11. Een typesnelheid app |

(moscow)=

## MoSCoW methode

Wanneer je veel energie stopt in het omschrijven van je programma, voordat je gaat programmeren, dan is de kans groot dat het programmeren gemakkelijker gaat. Je weet dan namelijk al beter wat je wel en niet wil. In de software-industrie zijn hier verschillende methodes voor. Een van die methodes is de *MoSCoW*-methode. Het is een manier om prioriteiten te stellen over wat belangrijk en niet belangrijk is voor je project. Het woord MoSCoW is een afkorting, waarbij de letters M, S, C en W de belangrijkste zijn.

| Letter         | Beschrijving                                                 |
| -------------- | ------------------------------------------------------------ |
| M: Must have   | Deze eisen *moeten* in het product komen. Zonder deze eisen is je product niet bruikbaar. |
| S: Should have | Deze eisen zijn zeer gewenst. Zonder deze eisen is je product nog wel bruikbaar. |
| C: Could have  | Wanneer je tijd over hebt, kun je deze eisen nog toevoegen.  |
| W: Won't have  | Deze eisen komen in dit product niet aan bod. Ze zijn mogelijk wel interessant voor een volgend project. |

### Opdracht

1. Maak een lijst van eisen, die je volgens MoSCoW sorteert. M bovenaan, gevolg door S etc.

2. Kies een platform: Web[^1],  Desktop GUI [^2] of Command Line [^3].

   
   Wanneer je kiest voor een Desktop GUI, ook bij datavisualisatie, maak dan een aantal schetsen of tekeningen van hoe je app eruit gaat zien en hoe de gebruiker met je app kan werken.
   
3. Optioneel: voor een goed ontwerp en efficiënter programmeerproces kan het lonen eens te verdiepen in Unified Modelling Language (UML). Dit is een ontwerptool voor het modelleren van je softwarearchitectuur (de opbouw), timingdiagrammen en nog veel meer. Je kunt hiervoor de tool PlantUML gebruiken.

[^1]: Web: Flask, Django (hier komt misschien wat Javascript bij kijken

[^2]: Desktop GUI: een app voor Windows of de Mac met klikbare knoppen. Een game in `pygame` is ook een Desktop GUI app

[^3]: Command Line: een app, die in de console 'leeft' (tekst gebaseerd). Zoals de eindopdracht van Basis van Programmeren met Python.