# Oefening 01 - Hello World

Het belangrijkste doel van deze oefening is om je door het proces van het uitvoeren van de tests te leiden en ervoor te zorgen dat alles correct is ingesteld en werkt.

In deze map vind je 2 andere bestanden:
  1. `helloWorld.js`
  2. `helloWorld.spec.js`

Deze opzet zal vergelijkbaar zijn voor alle oefeningen. Het gewone javascript-bestand is waar je je code schrijft, en het `spec`-bestand bevat de tests die controleren of je code werkt.

Laten we eerst naar het spec-bestand kijken:
```javascript
const helloWorld = require('./helloWorld');

describe('Hello World', function() {
  test('zegt "Hello, World!"', function() {
    expect(helloWorld()).toEqual('Hello, World!');
  });
});
```
Helemaal bovenaan het bestand gebruiken we `require()` om de code uit het javascript-bestand (`helloWorld.js`) te importeren zodat we het kunnen testen.

Het volgende blok (`describe()`) is het hoofdgedeelte van de test. In feite voert het je code uit en controleert het of de uitvoer correct is. De functie `test()` beschrijft in gewone taal wat er zou moeten gebeuren en bevat vervolgens de functie `expect()`. Voor dit eenvoudige voorbeeld zou het vrij makkelijk te begrijpen moeten zijn.

Voor nu hoef je je geen zorgen te maken over hoe je tests schrijft, maar je moet wel proberen vertrouwd te raken met de syntax zodat je kunt achterhalen wat de tests van je vragen. Voer de tests uit door `npm test helloWorld.spec.js` in de terminal in te voeren en kijk hoe de test faalt. De uitvoer van dat commando vertelt je precies wat er mis is met je code. In dit geval zou het uitvoeren van de functie `helloWorld()` de zin 'Hello, World!' moeten teruggeven, maar in plaats daarvan geeft het een lege string terug...

laten we dus naar het javascript-bestand kijken:
```javascript
const helloWorld = function() {
  return ''
}

module.exports = helloWorld
```
In dit bestand hebben we een eenvoudige functie genaamd helloWorld die een lege string teruggeeft... wat precies is waar onze test over klaagde. De `module.exports` op de laatste regel is hoe we de functie exporteren zodat deze geïmporteerd kan worden met `require()` in het spec-bestand.

Probeer nu de test te laten slagen door de returnwaarde van de functie aan te passen en voer het testbestand opnieuw uit.

Voor de zekerheid, mocht je nu in de war zijn: de test vertelt je dat het uitvoeren van de functie `helloWorld` de zin `Hello, World!` moet teruggeven. Interpunctie en hoofdletters zijn hier belangrijk, dus controleer dat goed als de test nog steeds niet slaagt.

Zo zou de uiteindelijke functie eruit moeten zien:
```javascript
const helloWorld = function() {
  return 'Hello, World!'
}

module.exports = helloWorld
```

Voor het grootste deel hebben we deze tests zo opgezet dat je alleen de code hoeft te schrijven of aan te passen die getest wordt. Je hoeft je op dit moment geen zorgen te maken over het importeren of exporteren van iets... werk gewoon rond dat stukje code en schrijf wat nodig is om de tests te laten slagen!

## Evaluatie:
# ✅ Evaluatie – Oefening 01: Hello World

| Criteria                                    | Beneden verwachting | Benadert verwachting | Volgens verwachting | Overstijgt verwachting |
|---------------------------------------------|---------------------|----------------------|---------------------|------------------------|
| **Begrip van testopzet** <br> (herkennen van `require`, `describe`, `test`, `expect`) | Herkent de teststructuur niet en begrijpt niet wat gecontroleerd wordt. | Ziet globaal dat de test iets controleert, maar kan de rol van onderdelen niet goed uitleggen. | Legt correct uit dat de test de uitvoer van de functie controleert. | Kan zelfstandig uitleggen hoe de test werkt en waarom testen nuttig zijn in programmeren. |
| **Interpreteren van foutmelding** | Begrijpt de foutmelding niet of negeert deze. | Ziet dat de test faalt, maar kan de reden niet benoemen. | Herkent correct dat de returnwaarde van de functie moet worden aangepast. | Gebruikt de foutmelding actief om snel en zelfstandig tot de juiste oplossing te komen. |
| **Aanpassen van de functie** | Past de code niet of foutief aan, test blijft falen. | Past de code aan maar maakt kleine fouten (bv. interpunctie/hoofdletter). | Past de code correct aan zodat de test slaagt. | Past de code correct aan en kan ook toelichten waarom interpunctie en hoofdletters belangrijk zijn. |
| **Gebruik van testomgeving** <br> (npm test uitvoeren, feedback lezen) | Kan de test niet uitvoeren. | Voert de test uit maar begrijpt de output nauwelijks. | Voert de test correct uit en gebruikt de feedback. | Voert de test zelfstandig uit, lost problemen efficiënt op en helpt eventueel anderen. |

