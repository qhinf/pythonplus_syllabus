# Leesbare code

## PEP8 Guidelines

Wanneer je een boek leest, verwacht je ook dat je niet alleen een leesbaar lettertype hebt, maar ook dat er een bepaalde structuur in het boek zit. Hoofdstukken, punten, komma's, lijstjes en al die andere zaken. Deze structuur zorgt ervoor dat je sneller kan begrijpen wat er staat. Het bevordert de leesbaarheid. Bij het lezen van programmeercode is het precies hetzelfde. Je hebt bij Basis van Programmeren met Python een start gemaakt met programmeren en mogelijk niet heel erg gelet op de leesbaarheid. Dat is op zich niet erg. Maar wanneer je met andere mensen gaat samenwerken, dan is de leesbaarheid van je code erg belangrijk. Want je wil natuurlijk dat andere mensen ook kunnen begrijpen wat je bedacht en geschreven hebt. Het schrijven van leesbare code heeft niet alleen nu met samenwerken. Wanneer je je eigen code na een half jaar nog eens terugleest, dan ben je jezelf dankbaar wanneer je leesbare code hebt geschreven.

Voor Python zijn er richtlijnen voor het schrijven van leesbare code. Deze richtlijnen heten de PEP8 Guidelines. Je kunt ze [hier](https://peps.python.org/pep-0008/) vinden.

In de les ga je deze richtlijnen lezen en bespreken.

## Leesbare code

Wanneer je je code helemaal volgens de PEP8 Guidelines opgesteld hebt, dan is er nog een extra toevoeging, die je code leesbaarder maakt. *Commentaar*. In Python is dat een `#` voor je regel code.

Het volgende tekst is een aanpassing van https://kinsta.com/blog/python-comments/

### Inline commentaar

Wil je een kort commentaar leveren om een verheldering van een regel code, dan zet je deze op dezelfde regel als de code. Het commentaar geeft uitleg van de betekenis van die regel.

```python
rand = x + 10 # Maak een rand van 10px
```

### Block commentaar

Wordt een regel code langer dan 79 karakters door een inline commentaar? Dan zet je het op meerdere regels. Dit heet een *block commentaar*. Dit klinkt ook logisch als je meer uitleg nodig hebt. Volgens de PEP8 richtlijnen plaats je een block commentaar vóór het codeblock.

```python
# Sorteer de lijst op de eerste letter, omdat 
# de groupby functie naar sequentiele data zoekt.
persons.sort(key=lambda x:x[0])
data = groupby(persons, key=lambda x:x[0])
```

*Het is niet erg wanneer je de code niet helemaal begrijpt, het gaat om de stijl van commentaar geven.*

### Multi line commentaar

Soms wil je op een stukje code meer toelichting geven, dan er op één regel past. Dan kun je in Python op twee manieren te werk. Of je kunt elke regel een `#` geven. Dat ziet er zo uit:

```Python
# een commentaar
# op meerdere regels
# ziet er zo uit
```

Je kunt ook de methode van multi-line string gebruiken. Dat ziet er zo uit:

```python
print("Multi-line commentaar")
"""
Een commentaar
op meerdere regels
kan er ook zo
uit zien
"""
```

Technisch gezien is dit een string, die op meerdere regels gedefinieerd wordt. Omdat de string niet aan een variabele wordt toegewezen, doet Python er niks mee en is het in feite een commentaar.

### Speciale commentaren

Je kunt je code leesbaarder maken door het toevoegen van commentaren. Dit zorgt ervoor dat de mensen, die je code lezen (inclusief jezelf na verloop van tijd), beter weten wat er gebeurd. Commentaren in Python kunnen ook nog de functie hebben om de workflow rondom een project beter te maken. Dit kan door middel van Docstrings en TODO/FIXME.

#### Docstring commentaar

Het kan voorkomen dat je tijdens het programmeren wil weten wat een bepaalde functie doet. Je wil de documentatie van die functie oproepen. Deze kun je zeer waarschijnlijk wel op het internet vinden. In de Python-interpreter zit ook een `help` -functie. Typ maar eens in de Python-interpreter (*Python Console* in PyCharm): `help(print)`. Dan krijg je allerlei nuttige informatie over de `print`-functie. Deze documentatie kun je voor de functies, die je voor je eigen project schrijft ook maken. Deze standaard wordt **Docstring** genoemd. Sterker nog, de documentatie die je op het internet vindt van bijvoorbeeld de `print`-functie is grotendeels gegenereerd uit DocStrings. Zo ziet een Docstring eruit:

```Python
from collections import namedtuple
Person = namedtuple('Person', ['name', 'age'])

 def get_person(name, age, d=False):
    """
Returns a namedtuple("name", "age") object.
Also returns dict('name', 'age') if arg `d` is True

Arguments:
name  – first name, must be string
age   – age of person, must be int
d     – to return Person as `dict` (default=False)

"""
p = Person(name, age)
if d:
    return p._asdict()
return p
```

In de regels na `def` zet je een multi-line string met een beschrijving van de functie. In deze beschrijving staat:

- Wat de functie oplevert
- Wat de argumenten/parameters van de functie zijn

Wil je meer weten over Docstrings? Het staat allemaal beschreven in de [PEP 257 Guideline](https://peps.python.org/pep-0257/).

#### TODO/FIXME commentaar

Wanneer je code aan het schrijven bent, dan kan het zijn dat je fouten of nieuwe taken voor je project bedenkt, die niet meteen met de flow waar je op dat moment inzit te maken hebben. Je wil eigenlijk je concentratie voor dat ene probleem vast houden en niet meteen dat nieuwe ding induiken. Je kunt natuurlijk een lijstje van dit soort 'zijsporen' op pen en papier bijhouden. Maar je kunt het ook in **TODO/FIXME-commentaren** bijhouden.

- Een TODO-commentaar is om openstaande taken bij te houden
- Een FIXME-commentaar is om gevonden bugs in je code aan te wijzen en bij te houden.

Dat ziet er zo uit:

```python
# TODO W, A, S, D als controls toevoegen
# TODO parallax scrolling background toevoegen

# FIXME collision-detection van sprite class Enemy
```

PyCharm biedt een mogelijk om alle TODO's en FIXME's overzichtelijk weer te geven. Hoe dit voor jouw versie van PyCharm werkt, kijk (hier)[https://www.jetbrains.com/help/pycharm/using-todo.html].

### Wat schrijf je dan in een commentaar?

We hebben het nu gehad over wat voor soort commentaren er zijn en hoe je ze in kan zetten bij je workflow. Maar *wat* schrijf je nu eigenlijk als commentaar.

#### Vermijd het voor de hand liggende

Commentaren waarbij je herhaalt, wat gemakkelijk uit de code is af te leiden zijn overbodig. Bekijk het volgende commentaar:

```python
x = x + 4 # hoog x op met 4
```

Dit commentaar zegt precies hetzelfde als de code al zegt. Het commentaar voegt niets toe. De rol van een commentaar is om het *waarom* van een stuk code uit te leggen. En niet *wat* de code doet te beschrijven. Het commentaar in bovenstaand code fragment kan als volgt herschreven worden:

```python
x = x + 4 # hoog de randbreedte met 4 op
```

#### Houd je commentaren kort en krachtig

Jij vindt het waarschijnlijk ook niet leuk om enorme lange verhalen te lezen en vooral om door te lezen, terwijl je al weet waar het naartoe gaat. Precies zo is het met commentaar bij code. Lees het commentaar van de volgende functie:

```python
# return oppervlakte door berekening: oppervlakte cylinder = (2*Pi*r*h) + (2*Pi*r*r)
def oppervlakte_cylinder(r, h):
  return ((2*3.14*r*h) + 2*3.14*r*r)
```

De commentaar regel is lang en dubbelop. Er staat in het commentaar uitgelegd, wat in de code prima is af te lezen.

Een commentaar dient een samenvatting te geven. Je kunt zo'n samenvatting ook prima in een Docstring zetten. Daarnaast dient een commentaar geen pseudo-code te bevatten. Dit levert vooral verwarring op en de 'code' staat toch al uitgeschreven in de Python-code van de functie. Bovenstaand fragment kan als volgt herschreven worden:

```python
# return de oppervlakte van een cylinder

def oppervlakte_cylinder(r, h):
  return ((2*3.14*r*h) + 2*3.14*r*r)
```

#### Pas op met identifiers

Kijk even mee met het volgende code fragment en bijbehorend commentaar:

```python
# return class() na aanpassing van argument
def func(cls, arg):
    return cls(arg+5)
```

Wat deze code precies doet, is niet belangrijk. Het gaat om het commentaar. Er wordt in het commentaar gesproken over `class()` en `argument`, terwijl deze in de code helemaal niet terug te vinden zijn. Wat er mogelijk gebeurd is, dat na het schrijven van het commentaar, de namen van de variabelen zijn veranderd. En dat deze in het commentaar niet zijn veranderd. En nu is er verwarring. Je kunt natuurlijk wel gaan gissen, maar dat is op zich wel gevaarlijk. Stel dat je de variabelen `x` en `i` omwisselt in je code, maar niet in je commentaar.

Er zijn twee mogelijke oplossingen:

1. Commentaar aanpassen (meer werk)

```python
# return cls() after modifying arg
def func(cls, arg):
    return cls(arg+5)
```

2. Geen variabele-namen gebruiken in je commentaar en een goede samenvatting geven

#### DRY en WET
*DRY* en *WET* staan voor Don't Repeat Yourself en Write Everything Once. Buiten dat dit principes zijn, die je voor het coderen gebruikt, kun je ze ook voor commentaren gebruiken. *DRY* staat voor *Niet in herhaling vallen* en *WET* voor *schrijf het slechts eenmaal*. Het lijkt een beetje op hetzelfde. Kijk even mee met het volgende code-fragment:

```python
# functie doe x klus
def doe_iets(y):
    # x klus kan niet gedaan worden wanneer 7 is groter dan max_limiet
    if y < 400:
      print('Lalala klus x')

```

In dit fragment zijn de commentaren gefragmenteerd (meerdere malen beschreven) en kunnen gemakkelijk naar één enkel commentaar herschreven worden:

```python
# functie om x te doen wanneer arg:y is kleiner dan de max_limiet
def doe_iets(y):
    if y < 400:
      print('Lalala klus x')
```

#### Consistente indentatie

Zorg dat je commentaren op hetzelfde niveau van indentatie staan als de code die beschreven wordt. Is dat niet het geval, dan is het moeilijk te lezen. Kijk naar het volgende voorbeeld:

```python
for i in range(2,20, 2):
# alleen even getallen
    if verifieer(i):
# i zou gecontroleerd zijn door verifieer()
        doe_iets(x)
```

Herschrijf deze commentaren als volgt:

```python
# alleen even getallen
for i in range(2,20, 2):
		# i zou gecontroleerd zijn door verifieer()
    if verifieer(i):
        doe_iets(x)
```

#### Samengevat

- Een commentaar legt het *waarom* van een stuk code uit
- Een commentaar vat samen
- Een commentaar bevat geen pseudo-code
- Vermijdt het gebruik van variabele-namen in de commentaren
- Een commentaar zou de benodigde leestijd van een code fragment moeten doen afnemen! Hou het overzichtelijk
- Zet commentaren op hetzelfde niveau van indentatie als de bijbehorende code

## Zo ziet het er uit

```python
"""
Demonstration of Python basic functionality.
:author: Gert van Lagen
"""

import os
from project import *


def print_variable(name):
    """
    This function receives data via the argument name. Before we print it, we do some checks.
    We check if name is text or a digit. When it is a digit, we square it.
    Name.isdigit() only works for integers, not floats.
    When the name is Python, we make of course make Python Plus of it.
    With the else statement, we make sure we handle unknown data and let the user know about the situation.

    :param name: data you want to print
    :return: None
    """
    if name != "Python" and not name.isdigit():
        print(name)
    elif name == "Python":
        name = "Python Plus"
        print("This is the module", name, ", not Python")
    elif name.isdigit():
        print("Digit = ", int(name))
    else:
        print("I don't know how to handle this input.")


def do_some_calculation():
    """
    This function does some math by getting two user input values and showing a math menu.
    The selected option will perform the math operation on the two values.
    Note that we explicitly have to convert the string input to an integer.
    :return:
    """
    print("Enter value 1:")
    value_1 = input()
    print("Enter value 2:")
    value_2 = input()
    print("Enter math option:\n"
          "1. Addition\n"
          "2. Subtraction\n"
          "3. Multiplication\n"
          "4. Division\n"
          "5. Modulo\n")
    math_option = input()

    match math_option:
        case '1':
            return float(value_1) + float(value_2)
        case '2':
            return int(value_1) - int(value_2)
        case '3':
            return int(value_1) * int(value_2)
        case '4':
            return int(value_1) / int(value_2)
        case '5':
            return int(value_1) % int(value_2)
        case _:
            print("No valid math operation. Make sure you input a number.")


def make_list():
    your_list = []
    print("Enter number of array elements you want to put in the list:")
    items = input()
    # If you didn't provide an integer
    if not items.isdigit():
        print("You should enter a digit")
        return
    # Correct input, create list with desired length
    else:
        for element in range(0, int(items)):
            # print("Enter the data you want to put in the list, element[", element, "]")
            new_element = input(f"Enter the data you want to put in the list, element[{ element }]")
            your_list.append(new_element)
            print("Your list has length ", len(your_list), "and content", your_list)


def file_management():
    """
    This function opens an existing (!) file in read/write mode and writes a string to it in character format
    :return: None
    """
    # Get file handler to test_file.txt. This is a
    fd = os.open("./test.txt", os.O_RDWR)

    # Write line to file and print 10 characters of the file
    os.write(fd, bytes("Hello world!", 'UTF-8'))

    # Close file
    os.close(fd)


def project_management():
    task_list = []
    create_project("Living", task_list)


if __name__ == '__main__':
    # Show menu with Python basics demonstrations
    while True:
        print("\nChoose a Python demonstration from the menu:\n"
              "1. Print text\n"
              "2. Math and types\n"
              "3. Lists\n"
              "4. File management\n"
              "5. Project management\n"
        # Printing some text using print_variable function and do some error handling
        menu_option = input()

        # Handles menu input by calling the functions
        match menu_option:
            case '1':
                print("Enter your input to print:")
                stuff_to_print = input()
                print_variable(stuff_to_print)
            case '2':
                calculation_result = do_some_calculation()
                print(calculation_result)
            case '3':
                make_list()
            case '4':
                file_management()
            case '5':
                project_management()
            case "exit":
                break  # stops the while-loop
            case _:
                print("No menu match\nMake sure you enter a number")

```

