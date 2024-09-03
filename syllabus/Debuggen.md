# Het Debuggen van je Programma

Programmeren omvat het schrijven van computer code. En daarbij maak je wel eens fouten. Het is nog een heel karwei om die fouten te vinden. Het vinden van fouten in je programma heet *debuggen* en is een essentieel onderdeel van programmeren. Iedereen maakt dus fouten en bugs zijn onvermijdelijk, zelfs voor de beste programmeurs. In dit hoofdstuk gaan we het hebben over wat debuggen is, waar het woord vandaan komt, en hoe je verschillende technieken kunt gebruiken om je Python-programma's foutvrij te maken. We richten ons op drie belangrijke technieken: debuggen met print-statements, het gebruik van breakpoints en stepping in PyCharm, en het analyseren van je programma met een Python Profiler.

## De Herkomst van het Woord Debuggen

Het woord "debuggen" komt oorspronkelijk uit de vroege dagen van de informatica. In de jaren '40, toen computers nog enorm groot en complex waren, vond een beroemd incident plaats. Een team van ingenieurs ontdekte een echte mot (bug in het Engels) die vastzat in een van de relais van de Mark II-computer. Deze mot veroorzaakte een storing in de machine, en toen ze de mot verwijderden, noemden ze dit "debuggen". Sindsdien is de term blijven hangen en verwijst het naar het opsporen en verhelpen van fouten in computerprogramma's. De juistheid van het verhaal staat nog ter discussie, maar het verhaal geeft wel mooi weer dat een bug op een rare of onverwachte plaats kan zitten.

## Debuggen door Print-Statements

Een van de eenvoudigste manieren om je programma te debuggen is door gebruik te maken van `print`-statements. Je voegt aan je code `print`-statements toe, die informatie over de status van je programma naar de console printen. Je kunt zo zien in wat voor toestand het programma zich bevindt. Laten we een voorbeeld bekijken:

```python
def voeg_getallen_toe(a, b):
    print(f"voeg_getallen_toe: a = {a}, b = {b}")
    resultaat = a + b
    print(f"voeg_getallen_toe: resultaat = {resultaat}")
    return resultaat

som = voeg_getallen_toe(5, 10)
print(f"Hoofdprogramma: som = {som}")
```

In dit voorbeeld gebruiken we `print`-statements om te zien wat de waarden van `a` en `b` zijn, en wat het resultaat is na de optelling. Deze methode is vooral handig als je snel wilt controleren of variabelen de juiste waarden hebben of om te begrijpen hoe je code zich gedraagt op bepaalde punten.

Hoewel `print`-statements nuttig zijn, kunnen ze je programma ook rommelig maken en zijn ze niet altijd de beste manier om complexe problemen op te lossen. Wanneer je de bug gevonden hebt, kan het veel werk zijn om de `print`-statements weer te verwijderen. Om het nog ingewikkelder te maken, is de waarschijnlijkheid dat je met het verwijderen van deze statements weer nieuwe bugs introduceert hoger dan je lief is. Gelukkig is er een meer geavanceerdere vorm van debuggen. Het gebruik van Breakpoints en Stepping.

## Het Gebruik van Breakpoints en Stepping in PyCharm

PyCharm is dus niet alleen handig om al je Python-files bij elkaar te houden, maar ook erg geschikt om te debuggen. Sterker nog, een van de belangrijkste functies van PyCharm is de ingebouwde debugger. Hiermee kun je breakpoints instellen en door je code stappen om te zien wat er gebeurt. Wat breakpoints zijn en hoe je hiermee om gaat, lees je hieronder.

### Breakpoints Instellen

Een breakpoint is een marker die je op een regel code plaatst waar je wilt dat je programma stopt met uitvoeren. Zeg maar een rood stoplicht. Dit geeft je de mogelijkheid om de status van je programma op dat punt te inspecteren. Om een breakpoint in PyCharm in te stellen, klik je eenvoudigweg in de linkermarge naast de regel waar je wilt stoppen.

```python
def vermenigvuldig_getallen(a, b):
    resultaat = a * b
    return resultaat

product = vermenigvuldig_getallen(6, 7)
print(f"Hoofdprogramma: product = {product}")
```

Stel dat we een breakpoint willen instellen op de regel `resultaat = a * b`. Klik in de linkermarge naast deze regel. Wanneer je nu je programma uitvoert in de debug-modus, zal het stoppen bij dit breakpoint.

### Stepping

Wanneer je programma stopt bij een breakpoint, kun je gebruik maken van stepping om je code regel voor regel uit te voeren. Dit helpt je te begrijpen hoe je programma werkt en waar het eventueel misgaat.

- **Step Over (F8)**: Voert de huidige regel uit en gaat naar de volgende regel in dezelfde functie.
- **Step Into (F7)**: Gaat de functie binnen als de huidige regel een functieaanroep is.
- **Step Out (Shift+F8)**: Voert de rest van de huidige functie uit en gaat terug naar de aanroepende functie.

Je ziet in het *Variables*-deel welke variabelen welke waarde hebben op dat moment van uitvoer. Dit zorgt ervoor dat je heel gedetailleerd kan nagaan hoe je code werkt. En dit helpt je weer met het opsporen en oplossen van bugs.

In de volgende video zie je hoe de code van `vermenigvuldig_getallen` zich gedraagt in de debugger van PyCharm. #TODO

## Een Python Profiler om het Gedrag van je Programma te Analyseren

Naast het debuggen met print-statements en breakpoints, is het soms nodig om dieper te graven in de prestaties van je programma. Een profiler helpt je hierbij door te meten hoeveel tijd je code in beslag neemt en hoeveel geheugen het gebruikt.

Een populaire profiler voor Python is cProfile. Deze profiler wordt meegeleverd met de standaard Python-bibliotheek en is eenvoudig te gebruiken.

### Gebruik van cProfile

Om cProfile te gebruiken, kun je het eenvoudigweg importeren en je code erdoorheen laten draaien. Hier is een voorbeeld:

```python
import cProfile

def langzame_functie():
    totaal = 0
    for i in range(1000000):
        totaal += i
    return totaal

def snelle_functie():
    return sum(range(1000000))

def hoofdprogramma():
    langzame_functie()
    snelle_functie()

cProfile.run('hoofdprogramma()')
```

Wanneer je dit programma uitvoert, geeft cProfile je het volgende rapport:
```
        7 function calls in 0.062 seconds

   Ordered by: standard name

   ncalls  tottime  percall  cumtime  percall filename:lineno(function)
        1    0.000    0.000    0.062    0.062 <string>:1(<module>)
        1    0.000    0.000    0.009    0.009 main.py:13(snelle_functie)
        1    0.000    0.000    0.062    0.062 main.py:16(hoofdprogramma)
        1    0.053    0.053    0.053    0.053 main.py:7(langzame_functie)
        1    0.000    0.000    0.062    0.062 {built-in method builtins.exec}
        1    0.009    0.009    0.009    0.009 {built-in method builtins.sum}
        1    0.000    0.000    0.000    0.000 {method 'disable' of '_lsprof.Profiler' objects}
```

Je ziet hier gedetailleerd hoeveel tijd elke functie in beslag neemt en hoe vaak elke functie is aangeroepen. Hiermee kun je bijvoorbeeld stukken code vinden, die onnodig vaak aangeroepen worden, zodat je vervolgens met de debugger weer kan kijken hoe je je code kan optimaliseren.

### Geheugengebruik Analyseren

Naast tijdsprofielen is het soms ook belangrijk om te weten hoeveel geheugen je programma gebruikt. Zeker wanneer je met grote datasets werkt, bijvoorbeeld bij een AI-toepassing, dan kan inzicht in het geheugengebruik van je programma ervoor zorgen of je je programma kan draaien of niet. Een handige tool hiervoor is `memory_profiler`. Deze tool geeft je inzicht in het geheugengebruik van je programma, wat vooral nuttig is bij het werken met grote datasets of geheugenintensieve taken.

Om `memory_profiler` te gebruiken, moet je het eerst installeren:

```bash
pip install memory_profiler
```

Je kunt de `memory_profiler` ook in PyCharm installeren in het tabblad *Python Packages* onderin je PyCharm scherm.

Vervolgens kun je de tool gebruiken door je code te decoreren met `@profile`:

```python
from memory_profiler import profile

@profile
def geheugen_intensieve_functie():
    grote_lijst = [i for i in range(1000000)]
    return sum(grote_lijst)

geheugen_intensieve_functie()
```

Wanneer je dit programma uitvoert, geeft memory_profiler je het volgende rapport:

```
Line #    Mem usage    Increment  Occurrences   Line Contents
=============================================================
     3     19.7 MiB     19.7 MiB           1   @profile
     4                                         def geheugen_intensieve_functie():
     5     58.0 MiB     38.3 MiB     1000003       grote_lijst = [i for i in range(1000000)]
     6     65.2 MiB      7.2 MiB           1       return sum(grote_lijst)

```

Je ziet nu dat de `geheugen_intensieve_functie` ongeveer 65MB aan geheugenruimte inneemt. Dat is op zich voor dit programma niet heel spannend. Maar wanneer je het net even verkeerd aanpakt, kan het net zo goed 65GB worden en dan heb je waarschijnlijk te weinig werkgeheugen en wordt je computer traag.