# Bijlage: Nieuw project in Visual Studio Code

In deze bijlage zie je hoe je snel en eenvoudig een nieuw Python-project opzet in Visual Studio Code. 

---

## Een nieuwe map maken

1. **Kies een locatie**  
   Bedenk waar je je project wilt bewaren en maak daar een nieuwe map aan, bijvoorbeeld `C:\MijnProject` (Windows) of in je thuismap op macOS/Linux.

2. **Open de map in Visual Studio Code**  
   - Start Visual Studio Code.  
   - Klik op *File* > *Open Folder…* (Windows/Linux) of *File* > *Open…* (macOS).  
   - Navigeer naar de map die je net hebt gemaakt en open deze.

Je hebt nu de basis van je project klaargezet in Visual Studio Code.

---

## Interpreter instellen (optioneel)

1. **Interpreter selecteren**  
   Rechts onderin de statusbalk van Visual Studio Code kun je de actieve Python-versie zien. Staat er geen Python-versie?  
   - Druk op <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> (Windows/Linux) of <kbd>Cmd</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> (macOS).  
   - Typ `Python: Select Interpreter` en kies de Python 3.x-versie die je wilt gebruiken.

2. **Interpreter ontbreekt?**  
   Als je geen optie ziet voor Python 3.x, controleer dan of je Python correct hebt geïnstalleerd (zie *Bijlage: Python en Visual Studio Code installeren*) en herstart eventueel Visual Studio Code.

---

## Eerste Python-bestand maken

1. **Nieuw bestand**  
   Klik in de *Explorer*-sidebar (het eerste icoontje links in beeld) met de rechtermuisknop op je projectmap. Kies *New File*. 

2. **Bestandsnaam**  
   Noem het bestand bijvoorbeeld `main.py` of `hallo.py`.

3. **Code invoeren**  
   Open het nieuwe bestand en voeg de volgende regel code toe:  
   ```python
   print("hi")
   ```

4. **Bestand opslaan**
   Druk op <kbd>Ctrl</kbd> + <kbd>S</kbd> (Windows/Linux) of <kbd>Cmd</kbd> + <kbd>S</kbd> (macOS) om het bestand op te slaan.

## Code uitvoeren
1.	**Run and Debug**

    Klik in Visual Studio Code links op het *Run and Debug*-icoon (play-icoon met een kever). Als je de Python-extensie hebt geïnstalleerd, kies dan de optie *Python: Current File* (of iets vergelijkbaars).
	
2.	**Run-bestemming kiezen**

    Visual Studio Code kan je vragen om een launch configuration aan te maken. Hiermee wordt je huidige Python-bestand uitgevoerd.
	
3.	**Resultaten bekijken**

    Zodra je het script uitvoert, verschijnt er een *Debug Console* of *Terminal*-paneel onder in beeld. Hier zou `hi` moeten verschijnen.

	
Tip: Je kunt ook met <kbd>F5</kbd> (of <kbd>Fn</kbd> + <kbd>F5</kbd> op macOS) het huidige bestand starten, mits je een Python-debugconfiguratie hebt ingesteld.

## Projectstructuur bijhouden

Je hebt nu je eerste Python-project in Visual Studio Code! Houd je bestanden en mappen netjes geordend. Wil je een extra bestand toevoegen? Klik dan simpelweg in de *Explorer*-sidebar met de rechtermuisknop op je projectmap, kies *New File* of *New Folder* en ga aan de slag.
