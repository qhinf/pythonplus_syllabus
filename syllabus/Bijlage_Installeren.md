# Bijlage: Python en Visual Studio Code installeren

In deze bijlage lees je hoe je Python installeert en hoe je Visual Studio Code gebruikt als ontwikkelomgeving (IDE) voor je Python-projecten. Met Visual Studio Code kun je eenvoudig Python-code schrijven, testen en debuggen, en dankzij de vele extensies kun je je werkomgeving op maat uitbreiden.

---

## Python installeren

Om met Python aan de slag te gaan, heb je eerst een recente versie van Python nodig. De meeste projecten in dit lesmateriaal gaan uit van Python 3.10 of hoger.

### Windows

1. **Download de installer**  
   Ga naar de [officiële Python-website](https://www.python.org/downloads/) en download de nieuwste stabiele release van Python 3 voor Windows.

2. **Voer de installer uit**  
   Dubbelklik op het gedownloade bestand. Zorg dat je bij de eerste stap van de installer het vakje **Add Python to PATH** aanvinkt, zodat je Python straks vanaf de opdrachtprompt (cmd) of PowerShell kunt gebruiken.

3. **Controleer de installatie**  
   Open een opdrachtprompt (cmd) of PowerShell en typ:
   ```bash
   python --version
   ```
   Je zou nu een versienummer moeten zien, bijvoorbeeld Python 3.10.9.

### macOS
1.	**Controleer of Python 3 al aanwezig is**
    
    Open de *Terminal*-app en typ:

    ```bash
    python3 --version
    ```
    Het kan zijn dat je macOS standaard een oudere Python-versie bevat (zoals 2.7). Daarom is het vaak handig om de officiële installatie van Python 3 te gebruiken.

2.	**Download en installeer Python 3**
    
    Ga naar de [officiële Python-website](https://www.python.org/downloads/mac-osx/) en download de macOS 64-bit installer voor de meest recente Python 3-versie. Voer de installer uit en volg de stappen.
3.	**Controleer de installatie**
    
    Open de Terminal opnieuw en typ:

    ```bash
    python3 --version
    ```

    Je zou nu een bericht moeten krijgen met de door jou geïnstalleerde versie, bijvoorbeeld `Python 3.10.9`. Of in ieder geval een versie die hoger ligt dan Python 3.5.

### Linux (optioneel)
Als je op Linux werkt, heb je vaak al een recente Python-versie in je distributie. Je kunt dit controleren met:
```bash
python3 --version
```
Is je versie verouderd? Volg dan de instructies van je specifieke Linux-distributie (bijv. `apt-get`, `dnf`, of `pacman`) om Python 3 te installeren of te upgraden.

## Visual Studio Code installeren
### Downloaden en installeren
1. **Download Visual Studio Code**
    
    Ga naar de [officiële Visual Studio Code-website](https://code.visualstudio.com/) en download de installer voor jouw besturingssysteem (Windows, macOS of Linux).
2. **Volg de installatiestappen**
    
    Volg de instructies van de installer. Op Windows krijg je bijvoorbeeld de optie om “*Add to PATH*” aan te vinken. Dit is handig, maar niet strikt noodzakelijk.

### Visual Studio Code starten
Nadat de installatie is voltooid, kun je Visual Studio Code openen via het icoontje op je bureaublad of in je applicatieoverzicht (Windows Startmenu, macOS Launchpad, of Linux-menu).

## Visual Studio Code configureren voor Python
Voor het schrijven en debuggen van Python-code in Visual Studio Code raden we aan om de **officiële Python-extensie** te installeren.
1. **Open de extensies**.
    
    Klik aan de linkerzijde in Visual Studio Code op het icoon van de **Extensions**-sidebar (de vier blokken).
2. **Zoek naar 'Python'**

    Voer in de zoekbalk `Python` in.
3. **Installeer de Python-extensie**

    Kies de extensie van **Microsoft** en klik op *Install*.

4.	**Eventueel: linting en formatting**

    Installeer ook de extensies voor **Pylint** of **Flake8** (linting) en bijvoorbeeld **Black** of **autopep8** (formattering) als je je code wilt laten controleren en automatisch netjes wilt laten opmaken.

### Python-interpreter selecteren
Visual Studio Code kan met meerdere Python-versies op je systeem omgaan. Om zeker te weten dat je de juiste versie gebruikt, kun je rechtsonder in de statusbalk (of via de Command Palette) de actieve Python-interpreter kiezen.

1.	**Command Palette openen**

    Druk op `Ctrl + Shift + P` (Windows/Linux) of `Cmd + Shift + P` (macOS).

2.	**Kies de interpreter**

    Typ in de Command Palette Python: `Select Interpreter` en kies de gewenste Python-versie.

### PEP8 Style Checking met PyLint

Om je code te laten voldoen aan de PEP8-standaarden (leesbare en consistente Python-code), kun je een linter als **PyLint** installeren:
1.	**Installeer de PyLint-extensie**
	-	Ga naar het **Extensions**-icoon in Visual Studio Code.
	-	Zoek op *PyLint* en installeer de extensie (meestal ook van Microsoft).
2.	**PyLint configureren**
	-	Open een `.py`-bestand in je project.
	-	Visual Studio Code detecteert nu automatisch dat je PyLint hebt. Je krijgt eventuele opmerkingen over je code direct in de editor te zien.
3.	**Lint-fouten bekijken**
	-	Als er PEP8-waarschuwingen of -fouten zijn, verschijnen deze in het **Problems**-paneel (meestal onderin het scherm).
	-	Je kunt dubbelklikken op een waarschuwing om naar de betreffende regel in je code te springen.
4.	**Automatisch formatteren (optioneel)**
	-	Voeg extensies als **Black** of **autopep8** toe om je code automatisch op te schonen.
	-	Na installatie kun je in de Command Palette (`Ctrl+Shift+P` of `Cmd+Shift+P`) zoeken op Format Document.

Door PyLint te gebruiken, blijft je code consistent en overzichtelijk, wat vooral bij grotere projecten van onschatbare waarde is.

## Testen of alles werkt

Om te controleren of alles naar behoren is ingesteld:
1.	Maak in Visual Studio Code een nieuw bestand aan, bijvoorbeeld `hallo.py`.
2.	Voeg de volgende code toe:
    ```python
    print("Hallo, Python!")
    ```
3. Sla het bestand op (bij voorkeur in een nieuwe map, zoals `C:\mijnproject` op Windows of in je Thuismap).
4.	Druk op F5 om te debuggen of gebruik de knop **Run and Debug** (links in Visual Studio Code).
5.	Als alles goed gaat, zie je in het Debug Console-venster `Hallo, Python!` verschijnen.

Is dit gelukt, dan ben je klaar om aan de slag te gaan met de rest van het lesmateriaal!

## Veelvoorkomende problemen en oplossingen
-	**Python niet gevonden**

    Controleer of je Python correct aan je PATH hebt toegevoegd tijdens de installatie of doe dit handmatig in je systeeminstellingen.
-	**Oude Python-versie**

    Verwijder (of update) oude versies, en zorg dat je in VS Code de juiste interpreter selecteert.
-	**Geen uitvoer**

    Check of je het juiste bestand hebt opgeslagen en of je in de juiste directory werkt.
-	**Linting werkt niet**

    Controleer of je de juiste extensie hebt geïnstalleerd en dat in je statusbalk (rechtsonder) de juiste Python-interpreter staat geselecteerd.

**Gefeliciteerd!** Je hebt nu zowel Python als Visual Studio Code geïnstalleerd, geconfigureerd én een PEP8-style checker zoals PyLint toegevoegd. Met deze set-up kun je moeiteloos Python-code schrijven, uitvoeren, debuggen en controleren op stijl en kwaliteit. Ga nu gerust verder met het ontwikkelen van je projecten en veel plezier met programmeren!