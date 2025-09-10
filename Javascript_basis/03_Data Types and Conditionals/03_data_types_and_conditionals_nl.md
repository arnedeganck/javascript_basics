<div>
    <font color="#C86B02" markdown="1">
        <h1>JAVASCRIPT</h1>
    </font>
</div>

<div>
    <font color="#D6AD00" markdown="1">
        <h1>Data types and conditionals</h1>
    </font>
</div>

### Inleiding

Er zijn een aantal veelvoorkomende gegevenstypes die je in JavaScript zult tegenkomen, en deze lessen over de basisprincipes geven je een sterke fundering in al deze types. Voordat we dieper ingaan, lees eerst dit [overzicht van de meest voorkomende datatypes in JavaScript](http://javascript.info/types).

---

### Lesoverzicht

Deze sectie bevat een algemeen overzicht van de onderwerpen die je in deze les zult leren.

- Noem de acht gegevenstypes in JavaScript.
- Begrijp het verschil tussen enkele, dubbele en backtick-aanhalingstekens.
- Een variabele/expressie in een string opnemen.
- Begrijp wat een methode is.
- Noem de drie logische operatoren.
- Begrijp wat de vergelijkingsoperatoren zijn.
- Begrijp wat conditionals zijn.
- Begrijp wat nesting is.
- Begrijp wat truthy en falsy waarden zijn.

---

### Strings

Afhankelijk van het soort werk dat je doet, werk je misschien vaker met tekst dan met getallen. Een **string** is een stukje tekst... en is een fundamenteel bouwblok van de taal.

1. Lees en codeer mee met deze [MDN-tutorial over strings in JavaScript](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Strings). Sla de sectie `Concatenation in context` over, want die behandelt concepten die we later bespreken bij DOM-manipulatie.
1. Doorloop [de W3Schools-les over stringmethoden](https://www.w3schools.com/js/js_string_methods.asp) om meer te leren over wat je met strings kunt doen.
1. Woordenschat: een **methode** is een stukje functionaliteit dat is ingebouwd in de taal of in specifieke gegevenstypes. In [de W3Schools-les over stringmethoden](https://www.w3schools.com/js/js_string_methods.asp) heb je enkele methoden geleerd die je op strings kunt gebruiken, zoals `replace` en `slice`. De [MDN-documentatie voor strings](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) biedt een volledig overzicht van nog veel meer ingebouwde stringmethoden. Je hoeft deze niet uit het hoofd te leren, maar de documentatie is een handig naslagwerk, dus sla hem op bij je favorieten!

#### 📑 JavaScript Strings Cheatsheet

| Categorie              | Methode / Concept  | Voorbeeld                                        | Resultaat                          |
|-------------------------|--------------------|--------------------------------------------------|------------------------------------|
| 🔤 Basis               | `.length`          | `"Hallo".length`                                 | `5`                                |
|                         | Indexering         | `"Hallo"[0]`                                     | `"H"`                              |
| 🔍 Zoeken              | `.indexOf()`       | `"Hallo wereld".indexOf("wereld")`               | `6`                                |
|                         | `.includes()`      | `"Hallo wereld".includes("Hallo")`               | `true`                             |
|                         | `.startsWith()`    | `"Hallo wereld".startsWith("Hallo")`             | `true`                             |
|                         | `.endsWith()`      | `"Hallo wereld".endsWith("wereld")`              | `true`                             |
| 🔄 Manipuleren          | `.toUpperCase()`   | `"Hallo wereld".toUpperCase()`                   | `"HALLO WERELD"`                    |
|                         | `.toLowerCase()`   | `"Hallo wereld".toLowerCase()`                   | `"hallo wereld"`                    |
|                         | `.trim()`          | `"  trim  ".trim()`                              | `"trim"`                           |
| ✏️ Delen & vervangen    | `.slice()`         | `"JavaScript".slice(0,4)`                        | `"Java"`                           |
|                         | `.substring()`     | `"JavaScript".substring(4)`                      | `"Script"`                         |
|                         | `.replace()`       | `"Hallo wereld".replace("wereld","Arne")`        | `"Hallo Arne"`                     |
| 🔗 Splitsen & samenvoegen| `.split()`        | `"appel,peer,banaan".split(",")`                 | `["appel","peer","banaan"]`        |
|                         | `.join()`          | `["a","b","c"].join("-")`                        | `"a-b-c"`                          |
| 🧩 Template Literals    | Backticks `` `...` `` | `` `Hoi, ik ben ${naam} en ik ben ${leeftijd} jaar.` `` | `"Hoi, ik ben Arne en ik ben 30 jaar."` |
| 📖 Extra tips           | Escape characters  | `"Arne zei: \"Hallo!\""`                         | `Arne zei: "Hallo!"`               |

---

🔗 **Meer info**  

- [MDN String Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)  
- [W3Schools String Methods](https://www.w3schools.com/js/js_string_methods.asp)  

---

### Conditionals

Nu wordt het leuk... Tot nu toe hebben we nog niet veel gedaan met onze code wat je niet met basiswiskunde zou kunnen. Natuurlijk hebben we de computer verteld hoe hij de berekeningen moet doen, wat het sneller maakt, maar de essentie van programmeren is de computer leren beslissingen te nemen om meer complexe dingen te doen. Conditionals zijn hoe we dat doen.

1. De eerste stap in het leren over conditionals is zorgen dat je [vergelijkingen](http://javascript.info/comparison) goed begrijpt.
1. W3Schools heeft ook een [les over conditionals in JavaScript](https://www.w3schools.com/js/js_if_else.asp).
1. JavaScript.info heeft een [goede tutorial over logische operatoren](http://javascript.info/logical-operators). Een kleine waarschuwing bij de opdrachten: er zullen vragen zijn waarbij je `alert()` ziet met een getal of string tussen de haakjes. Wat hier gebeurt, wordt later in de cursus besproken. Sommige antwoorden zijn nu misschien niet logisch, maar ze kloppen wel en je zult ze begrijpen naarmate je verder komt. Maak je er nu nog niet te druk om!
1. Het [MDN-artikel over conditionals](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals) versterkt het concept en geeft verschillende interessante voorbeelden van hoe je het kunt gebruiken bij het bouwen van websites.
1. JavaScript.info's [les over `if/else`](http://javascript.info/ifelse) behandelt hetzelfde basisconcept (lees het als herhaling!) en - nog belangrijker - biedt de gebruikelijke 'opdrachten' onderaan de pagina!
1. [Lees over de `switch`-instructie](https://javascript.info/switch), die handig is als je meerdere voorwaarden hebt.

#### 📑 JavaScript Conditionals Cheatsheet

| Categorie              | Syntax / Methode         | Voorbeeld                                                                 | Resultaat / Uitleg                                |
|-------------------------|--------------------------|---------------------------------------------------------------------------|--------------------------------------------------|
| 🔍 Vergelijkingen       | `==`                     | `5 == "5"`                                                                | `true` (gelijke waarde, type wordt genegeerd)    |
|                         | `===`                    | `5 === "5"`                                                               | `false` (gelijke waarde én type vereist)         |
|                         | `!=`                     | `5 != "4"`                                                                | `true`                                           |
|                         | `!==`                    | `5 !== "5"`                                                               | `true`                                           |
|                         | `>` `<` `>=` `<=`        | `10 > 3` → `true`, `4 <= 4` → `true`                                      | Vergelijking van grootte                         |
| ⚡ Logische operatoren   | `&&` (AND)               | `(5 > 3 && 2 < 4)`                                                         | `true` als beide voorwaarden waar zijn           |
|                         | `||` (OR)                | `(5 > 10 || 2 < 4)`                                                        | `true` als minstens één voorwaarde waar is       |
|                         | `!` (NOT)                | `!(5 > 3)`                                                                 | `false` (keert de waarde om)                     |
| ✅ If statement          | `if`                     | `if (leeftijd >= 18) { console.log("Volwassen"); }`                        | Code wordt uitgevoerd als de voorwaarde `true` is|
| 🔄 If…else              | `if...else`              | `if (uur < 12) { console.log("Goedemorgen"); } else { console.log("Hallo"); }` | Voert code uit afhankelijk van conditie          |
| 🔁 If…else if…else      | `else if`                | `if (score > 90) { ... } else if (score > 50) { ... } else { ... }`       | Meerdere condities na elkaar testen              |
| 🔀 Ternary operator      | `condition ? expr1 : expr2` | `let resultaat = (leeftijd >= 18) ? "Volwassen" : "Minderjarig";`       | Kortere vorm van `if...else`                     |
| 🔄 Switch statement     | `switch`                 | ```js\nswitch(dag) {\n case "maandag": console.log("Begin vd week"); break;\n case "vrijdag": console.log("Weekend!"); break;\n default: console.log("Gewone dag");\n}\n``` | Handig voor veel mogelijke waarden               |

---

🔗 **Meer info**  

- [MDN Conditionals](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals)  
- [W3Schools JavaScript Conditionals](https://www.w3schools.com/js/js_if_else.asp)  
- [JavaScript.info - If/else](https://javascript.info/ifelse)  
- [JavaScript.info - Logical operators](https://javascript.info/logical-operators)  
- [W3Schools Switch](https://www.w3schools.com/js/js_switch.asp)  

---

### Opdracht

<div class="lesson-content__panel" markdown="1">

Om je goed te laten oefenen, hebben we JavaScript-oefeningen voor je gemaakt. Ze bevatten tests die controleren of je code werkt zoals het hoort. Overal waar je `return` ziet, betekent het dat wanneer de functie klaar is, deze teruggeeft wat er na `return` staat. In toekomstige lessen gaan we dieper in op deze concepten, dus houd nog even vol!

Zorg dat je de volgorde hieronder aanhoudt. Lees alle instructies, let op de terminal en lees alle foutmeldingen.

1. Volg de [instructies in de README van onze `javascript-exercises` repository](/Javascript_basis/Javascript-oefeningen/) om je lokale omgeving op te zetten. Nadat je de repository hebt geforkt, gekloond en Jest hebt geïnstalleerd, bekijk je elke README voordat je de volgende oefeningen in deze volgorde maakt:
    - `01_helloWorld` (Deze oefening is expres heel eenvoudig om te zorgen dat alles goed werkt!)
    - `02_addNumbers`
    - `03_numberChecker`
    - `04_mathEquations`
    - `05_joinStrings`

</div>

### Kenniscontrole

De volgende vragen zijn een kans om na te denken over de belangrijkste onderwerpen in deze les. Als je een vraag niet kunt beantwoorden, klik erop om het materiaal te herzien, maar je hoeft deze kennis niet uit het hoofd te leren of te beheersen.

- [Wat zijn de acht gegevenstypes in JavaScript?](https://javascript.info/types#summary)
- [Welk gegevenstype is NIET primitief?](https://javascript.info/types#objects-and-symbols)
- [Wat is de relatie tussen null en undefined?](https://javascript.info/types#the-null-value)
- [Wat is het verschil tussen enkele, dubbele en backtick-aanhalingstekens voor strings?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Strings#single_quotes_double_quotes_and_backticks)
- [Hoe heet het samenvoegen van strings?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Strings#embedding_javascript)
- [Met welk type aanhalingsteken kun je variabelen/expressies in een string opnemen?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Strings#embedding_javascript)
- [Hoe neem je variabelen/expressies op in een string?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Strings#embedding_javascript)
- [Hoe gebruik je escape-tekens in een string?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Strings#including_quotes_in_strings)
- [Wat is het verschil tussen de slice/substring stringmethoden?](https://www.w3schools.com/js/js_string_methods.asp)
- [Wat zijn de drie logische operatoren en waar staan ze voor?](http://javascript.info/logical-operators)
- [Wat zijn de vergelijkingsoperatoren?](https://javascript.info/comparison)
- [Wat zijn truthy en falsy waarden?](https://javascript.info/ifelse#boolean-conversion)
- [Wat zijn de falsy waarden in JavaScript?](https://javascript.info/ifelse#boolean-conversion)
- [Wat zijn conditionals?](https://www.w3schools.com/js/js_if_else.asp)
- [Wat is de syntax voor een if/else-voorwaarde?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals#basic_if...else_syntax)
- [Wat is de syntax voor een switch-instructie?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals#switch_statements)
- [Wat is de syntax voor een ternary-operator?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals#ternary_operator)
- [Wat is nesting?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals#nesting_if...else)

### Extra bronnen

Deze sectie bevat handige links naar gerelateerde inhoud. Het is niet verplicht, dus beschouw het als aanvullend.

- [Reguliere expressies](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions), vaak regex genoemd, is een hulpmiddel om patronen in strings te vinden of te valideren. Het is echter belangrijk om te weten [wanneer je geen reguliere expressies moet gebruiken](https://softwareengineering.stackexchange.com/questions/113237/when-you-should-not-use-regular-expressions). Er zijn ook andere methoden om strings te verwerken, en regex kan soms trager zijn.
- [Web Dev Simplified's Regular Expressions In 20 Minutes](https://www.youtube.com/watch?v=rhzKDrUiJVk)
