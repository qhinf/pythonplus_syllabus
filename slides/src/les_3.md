<!-- .slide: data-background-gradient="linear-gradient(to bottom right, #f1881c, #ffffff)" -->

# Python Plus

Q-highschool / Les 3: Debugging

***

## Vandaag

- Wat is debugging?
- Technieken om bugs te vinden
- De debugger in VS Code
- Werken aan je project

***

## Wat is een bug? 🐛

Een fout in je code waardoor het programma niet doet wat jij wilt.

---

## Soorten fouten

| Type | Voorbeeld |
|------|-----------|
| **Syntaxfout** | Vergeten dubbele punt, haakje |
| **Runtimefout** | Delen door nul, variabele niet gevonden |
| **Logische fout** | Programma draait, maar geeft verkeerde uitvoer |

Notes:
Syntaxfouten worden door Python meteen gemeld. Logische fouten zijn het lastigst.

***

## Techniek 1: Print-debugging

```python
def bereken_gemiddelde(cijfers):
    print(f"cijfers: {cijfers}")       # debug
    totaal = sum(cijfers)
    print(f"totaal: {totaal}")         # debug
    return totaal / len(cijfers)
```

Simpel, maar effectief!

---

## Techniek 2: De debugger

VS Code heeft een ingebouwde debugger:

1. Klik op de regel waar je wil stoppen → **breakpoint**
2. Start met **F5**
3. Inspecteer variabelen in het paneel

Notes:
Demo: laat een breakpoint zetten en variabelen inspecteren.

---

## Breakpoints

- Rood bolletje in de kantlijn = breakpoint
- Programma pauzeert op die regel
- Je kunt dan door de code stappen:
  - **F10** – stap over (volgende regel)
  - **F11** – stap in (ga functie in)
  - **F5** – doorgaan tot volgend breakpoint

---

## Variabelen inspecteren

In de debugger zie je:
- Waarde van alle variabelen op dat moment
- De **call stack**: welke functies zijn aangeroepen

***

## Techniek 3: Lees de foutmelding!

```
Traceback (most recent call last):
  File "main.py", line 12, in <module>
    resultaat = bereken(0)
  File "main.py", line 7, in bereken
    return 10 / getal
ZeroDivisionError: division by zero
```

- **Laatste regel** = het probleem
- **Regelnummer** = waar het mis gaat

Notes:
Veel mensen scrollen meteen omhoog. Wijzen op: lees van onder naar boven.

---

## Techniek 4: Rubber duck debugging 🦆

Leg je code uit aan een denkbeeldige eend \
(of aan iemand anders).

Terwijl je het uitlegt, vind je de fout zelf.

***

## Aan de slag!

- Gebruik de debugger als je vastloopt
- Commit regelmatig
- Zorg dat je projectonderwerp doorgegeven is

Notes:
Rondlopen voor individuele gesprekken: voortgang Git-gebruik, projectonderwerp.
