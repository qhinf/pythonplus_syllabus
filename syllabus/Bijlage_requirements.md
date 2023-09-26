# Bijlage: Gebruik van `requirements.txt`

Een `requirements.txt` maakt het eenvoudig om op een andere machine je Pythonproject te installeren en te runnen. Het is verplicht om een `requirements.txt` te gebruiken bij deze Python Plus module.

1. Maak een bestand ‘requirements.txt’ en plaats het bij je andere .py bestanden;
2. Open `requirements.txt` en voeg alle geïnstalleerde en gebruikte python packages toe aan requirements.txt door het runnen van de volgende command in de Terminal van PyCharm:

```
pip freeze > .\requirements.txt
```

3. Als je een nieuwe package nodig hebt, kun je ze op de volgende manier toevoegen `<packagename>==version`, bijvoorbeeld:

`Tensorflow==2.11.0`
4. Om de packages vervolgens te installeren open je de terminal en voer je het volgende commando uit:
```
pip install -r .\requirements.txt
```
5. Voor het toevoegen van nieuwe packages, update je dus de `requirements.txt` en installeer je de file. Vergeet de packages niet te importeren in je .py files.
6. Je kunt kijken of alle packages up to date zijn door middel van het commando: 
```
pip list --outdated
```
7. Je kunt alle packages updaten door middel van het commando: 
```
pip upgrade -r requirements.txt
```
Of een specifieke package door middel van het commando:
```
pip install -U packagename
```
8. Meer tips en trucks kun je hier vinden: (https://learnpython.com/blog/python-requirements-file/)