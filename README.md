# Skriftlig Examination - Introduktion till C#

**Kursnamn**: Introduktion till C#  
**Examination av**: Läranderesultat 1, 2 och 3 (Kunskaper)  
**Betyg**: Icke Godkänt (IG) eller Godkänt (G)  
**Tidsåtgång**: Ca 3-4 timmar  
**Inlämning**: Senast söndag den 9 november (23:59)  
**Format**: Kopiera den här filen och skriv svaren här inne.

---

**Elevens namn**: Theodore Perlman

---

## Instruktioner

- Svara på alla frågor med egna ord
- Det är inte tillåtet att använda AI i sina svar.
- Alla inlämningar kontrolleras i ett antiplagiat-verktyg. Fusk kan leda till disciplinära åtgärder och risk för avstängning.
- Förklara tydligt och koncist - inga långa utläggningar krävs
- Ge korta kodexempel endast där det efterfrågas (oftast räcker 1-3 rader)
- Försök att använda korrekt terminologi.
- Det är okej att använda kursmaterial och anteckningar

---

## Del 1: Objektorienterad programmering i C# (Läranderesultat 1)

### Fråga 1 - Grundläggande OOP

**Vad är objektorienterad programmering?** Förklara med egna ord vad OOP innebär och ge minst två fördelar med att använda OOP.

**Svar 1**: OOP, eller Object-Oriented Programming, innebär att man programmerar i klasser för att skapa objekt för att bygga i sin programmering. En fördel med OOP är att man kan lätt kan återanvända kod, t.ex: Man programmerar en klass för en Person och sedan kan man använda klassen Person för att skapa hur många olika objekt för Person som man behöver istället för att hårdkoda varje Person objekt. En annan fördel med OOP att är koden blir mer lättläst, du vet precis vart du kan hitta metoder, properties och annat för t.ex Person objekt, du kollar bara i class Person.

---

### Fråga 2 - Klasser och Objekt

**.**
a) Förklara skillnaden mellan en klass och ett objekt, använd gärna en analogi från verkligheten för att illustrera din förklaring.

**Svar 2A**: Klass är en mall för hur objektet ska byggas. T.ex: En klass för en Motorcykel är en mall för hur en motorcykel ska se ut och fungera. Motorcykeln måste exempelvis ha två hjul, den måste ha ett styre, en motor, en färg, osv.. Ett objekt i detta fall är den färdiga, verkliga motorcykeln som uppfyller alla krav från mallen. 

b) Vad innebär det om en klass benämns static? Ex: `public static class File`

**Svar 2B**: Om en klass benämns static innebär det att klassen inte behöver instansieras, inga objekt behöver skapas för att kunna nyttja en static klass och dess medlemmar. "Ex: `public static class File`", i denna klass finns det kanske en metod för "Save" för att kunna spara en fil, då kan man bara köra t.ex `File.Save("text.txt");` utan att behöva skapa en instans innan.
Om en klass benämns static innebär det också att klassen bara får innehålla static-benämnda medlemmar.

---

### Fråga 3 - Konstruktorer

**Vad är en konstruktor och vad används den till?** Förklara vad som händer när man skapar ett nytt objekt med `new` keyword.

**Svar 3**: En konstruktor är en metod som existerar i alla klasser. Konstruktorns syfte är att initiera ett objekt och om konstruktorn har parametrar så kommer den kräva att alla parametrar den blivit tilldelad uppfylls när ett objekt av klassen skapas. T.ex: om jag har följande klass, property och parameter;

```public class Person 
{
  public string Name { get; }

  //Konstruktor
  public Person(string name) //Parameter
  {
    Name = name;
  }
}
```

Då är det ett krav att jag fyller i en string när jag skapar ett objekt från klassen. 
Exempelvis: `var person1 = new Person("Alfred");`

En konstruktor kan även vara parameterlös, vilket den är by default, om den är parameterlös innebär det att det inte finns några krav.
När man skapar ett nytt objekt med `new` keyword så innebär det just det, man skapar ett helt nytt, eget, objekt.

---

### Fråga 4 - Properties och Fields

**Förklara skillnaden mellan ett field och en property i C#.** Ge exempel på när man bör använda respektive.

**Svar 4**: Field är endast en variabel i en klass medan en property är en variabel + logik för att hämta (get;) och sätta (set;) värdet för variabeln.

---

### Fråga 5 - Inkapsling

**Vad är inkapsling (encapsulation) och varför är det viktigt?** Förklara skillnaden mellan `private` och `public`, och när man bör använda vad.

**Svar 5**: Inkapsling menas att man skapar lager över det man vill inkapsla och därmed döljer interna detaljer. 
T.ex om jag har en vill lagra pengar och har en `private decimal _balance;` då vill jag helst inkapsla denna field så att man inte ändrar värdet på `_balance` direkt, 
då kan jag istället skapa en property `public decimal Balance ..` så att `_balance` är inkapslat och så kan jag sätta mina kontroller på hur det ska få hämtas och sättas genom get och set metoderna. Skillnaden på private och public är att private endast kan hittas och användas i klassen den är inskriven i. public kan hittas och användas vart som helst.

---

### Fråga 6 - Metoder

**Förklara följande:**

a) Vad är skillnaden mellan en metod som returnerar något (t.ex. `int`) och en `void` metod?  

En metod som returnerar något, t.ex `int` måste alltid ha en return som returnerar ett värde för rätt typ för att metoden ska fungera. T.ex:
```public int Addition()
{
  return x + y;
}
```
Medan en `void` metod inte får returnera ett värde. T.ex:
```public void HelloWorld()
{
  Console.WriteLine("Hello world!");
}
```
b) Vad innebär det att en metod är `static`?

**Svar 6b**: Om en metod är static innebär att metoden tillhör klassen och inte ett objekt, vilket betyder att jag inte behöver skapa ett objekt av klassen för att kunna använda metoden. T.ex
```public class Calculator
{
  public static double Addition(double x, double y)
  {
    return x + y;
  }
}
```
i detta exempel så kan jag kalla på metoden i Main utan att behöva skapa ett nytt objekt, såhär: `Calculator.Addition(x, y)` 
Ett exempel i verkligheten kan se ut såhär: `double result = Calculator.Addition(2.5, 8);`.

---

## Del 2: Applikationstyper (Läranderesultat 2)

### Fråga 7 - Applikationstyper i .NET

**C# och .NET kan användas för att bygga olika typer av applikationer.**

a) Nämn minst tre olika typer av applikationer man kan bygga med C# och .NET (t.ex. console) 

**Svar 7a**: Skrivbordsapplikationer, mobilapplikationer och konsolapplikationer. 

b) Beskriv kort vad dessa applikationstyper har för syfte. 

**Svar 7b**: Skrivbordsapplikationer är program med UI som har som syfte att köras på datorer. Mobilapplikationer är program med UI som är designat att köras på t.ex smartphones och surfplattor. Konsolapplikationer är textbaserade program som körs i konsolen, det kan användas i t.ex utbildningssyfte och testkod bland annat.

---

### Fråga 8 - Konsolapplikationer

**Vi har fokuserat på konsolapplikationer (Console Application) i kursen.**

a) Vad är en konsolapplikation? 

**Svar 8a**: En konsolapplikation är ett textbaserat program som körs i konsolen. 

b) Ge ett exempel på när en konsolapplikation kan vara lämplig att använda. 

**Svar 8b**: I utbildning för att snabbare kunna hoppa in i syntax inlärning och annat teoretiskt utan att behöva bygga ett UI.

---

## Del 3: Datatyper i C# (Läranderesultat 3)

### Fråga 9 - Primitiva Datatyper

**Beskriv följande datatyper och när man använder dem:**

a) `int` 

**Svar 8a**: Datatypen `int` håller ett värde av ett nummertal där decimaler inte är tillåtna. T.ex `int num = 114;`

b) `double` 

**Svar 8b**: Datatypen `double` håller ett värde av ett nummertal där upp till 16 decimaler stödjs. T.ex `double num = 114.38174`

c) `string` 

**Svar 8c**: Datatypen `string` håller ett värde av en sträng av datatypen `char`. 
T.ex `string introduce = "Jag heter Theodore";` detta är en sträng av `char` `"J"` `"a"` `"g"` osv. 

d) `bool`

**Svar 8d**: Datatypen `bool` håller ett värde av antingen true eller false. T.ex `bool verified = false;` eller `bool verified = true;` 

e) Förklara också skillnaden mellan `int` och `double`. 

**Svar 8e**: Skillnaden mellan en `int` och `double` är att `int` inte får innehålla ett värde av decimaler medan `double` får innehålla ett värde av decimaler.

---

### Fråga 10 - Stark typning

**C# är ett starkt typat språk, medan JavaScript är löst typat.**

a) Vad innebär det att ett språk är starkt typat?  

**Svar 10a**: Att ett språk är starkt typat innebär att datatyper är viktiga och strikt kontrollerade. Man måste ange rätt datatyp och förhålla sig till den datatypen om man inte explicit konverterar datatypen till en annan. T.ex C#: `string name = "Theodore";` I ett löst typat språk som JavaScript kan man skriva: `let name = "Theodore";` och sedan skriva `name = 58;` helt lagligt utan explicit konvertering, det löst typade språket konverterar datatypen automatiskt.

b) Ge ett exempel på en fördel med stark typning som du märkt av i C#.

**Svar 10b**: Jag tycker att koden blir extremt mycket tydligare och risken för oförutsedda buggar är mycket mindre.

---

### Fråga 11 - Arrays och Listor

**Förklara skillnaden mellan en array och en `List<T>` i C#.**

a) När bör man använda en array?  

**Svar 11a**: En array bör användas när man vet i förväg antalet man vill förvara i arrayen. T.ex om jag vet att jag vill förvara 10st int datatyper och aldrig vill förändra antalet så passar en array perfekt. 

b) När bör man använda en `List<T>`? 

**Svar 11b**: en `List<T>` bör användas när jag är osäker på antalet jag kommer förvara i listan eller om jag vill ta bort eller lägga till i listan vid ett senare tillfälle. 

c) Skriv ett kort kodexempel (1-3 rader) som visar hur man lägger till ett element i en List<int>. 

**Svar 11c**: 
`List<int> numbers = new();` 
`numbers.Add(5);`

---

### Fråga 12 - Dictionary

**Vad är en `Dictionary<TKey, TValue>` och när är den användbar?**

Förklara med egna ord och ge två exempel på scenarion där Dictionary är ett bra val (inget kodexempel krävs).

**Svar 12**: Dictionary kan vara ett bra val i ett scenario där man vill slå upp spelarna i olika fotbollslag. T.ex "Barcelona": "Lamine", "Raphinha", "Pedri" osv. Dictionary kan även vara ett bra val i ett scenario där man exempelvis vill konvertera landskoder till landsnamn. T.ex "DK": "Danmark" "SV": "Sverige" osv

---

### Fråga 13 - LINQ

**Vad är LINQ och vad används det till?**

Ge exempel på minst två LINQ-metoder du använt (t.ex. `Where`, `Select`, `OrderBy`, `Count`, etc.) och förklara kort vad de gör.

**Svar 13**: Man kan t.ex använda `Where` för att filtrera smycken som har ett värde under 2000kr och använda en `Count` på det för att få fram hur många smycken som har ett värde under 2000kr. `Where` används alltså för att filtrera fram objekt utifrån ett vilkor, t.ex: smycken under 2000kr eller personer med färre än 10 fingrar osv. `Count` används för att få fram antalet objekt som uppfyller ett villkor.

---

## Inlämning och Bedömning

### Format

- Ladda upp den här md filen med dina svar på It's learning senast den 9 november 2025. För de
  som hellre vill länka till sin Git får ni också göra det.

- Skriv ditt **namn** i dokumentet

### Bedömning

#### Godkänt (G)

För att få **Godkänt** krävs att du:

- Besvarar **alla 13 frågor**
- Visar förståelse för grundläggande koncept
- Ger tydliga förklaringar med egna ord
- Använder korrekt terminologi
- Ger kodexempel där det efterfrågas (behöver inte vara perfekt, men ska visa förståelse)

#### Icke Godkänt (IG)

Du får **Icke Godkänt** om:

- Flera frågor är obesvarade eller mycket ofullständiga
- Svaren visar grundläggande missförstånd av koncept
- Svaren är uppenbart kopierade från AI eller andra källor utan egen förståelse
- Svaren är så kortfattade att de inte visar förståelse

**Vid gränsfall**: Om du är nära G men några svar är otillräckliga kan du få möjlighet att komplettera specifika frågor.

---

## Tips för att lyckas

- Börja med frågorna du känner dig säkrast på
- Svara koncist - kvalitet över kvantitet
- Läs igenom dina svar innan inlämning
- Börja i tid - du har två veckor på dig
- Fråga på lektioner om något är oklart

**Kom ihåg**: Det viktiga är att du visar att du **förstår** koncepten, inte hur mycket du skriver. Tydliga, korta förklaringar är ofta bättre än långa utsvävningar.

---

## Hjälp och resurser

### Tillåtet

- Använda kursmaterial och dina egna anteckningar
- Titta på kod du själv skrivit under kursen
- Använda C# dokumentation (docs.microsoft.com)
- Fråga läraren om du inte förstår vad en fråga betyder
- Man får också använda AI för egen inlärning

### Inte tillåtet

- Kopiera svar från ChatGPT eller andra AI-verktyg
- Kopiera svar från klasskamrater eller internet
- Låta någon annan skriva dina svar

---

**Lycka till! 🚀**