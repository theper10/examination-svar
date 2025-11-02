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

**Svar 2B**: Om en klass benämns static innebär det att klassen inte behöver instansieras, inga objekt behöver skapas för att kunna nyttja en static klass och dess medlemmar. "Ex: `public static class File`", i denna klass finns det kanske en metod för "Save" för att kunna spara en fil, då kan man bara köra t.ex File.Save("text.txt"); utan att behöva skapa en instans innan.
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

**Svar 4**: Field är endast en variabel i en klass medan en property är en variabel + metoder för att hämta (get;) och sätta (set;) värdet för variabeln.

---

### Fråga 5 - Inkapsling

**Vad är inkapsling (encapsulation) och varför är det viktigt?** Förklara skillnaden mellan `private` och `public`, och när man bör använda vad.

---

### Fråga 6 - Metoder

**Förklara följande:**

a) Vad är skillnaden mellan en metod som returnerar något (t.ex. `int`) och en `void` metod?  
b) Vad innebär det att en metod är `static`?

---

## Del 2: Applikationstyper (Läranderesultat 2)

### Fråga 7 - Applikationstyper i .NET

**C# och .NET kan användas för att bygga olika typer av applikationer.**

a) Nämn minst tre olika typer av applikationer man kan bygga med C# och .NET (t.ex. console)  
b) Beskriv kort vad dessa applikationstyper har för syfte.

---

### Fråga 8 - Konsolapplikationer

**Vi har fokuserat på konsolapplikationer (Console Application) i kursen.**

a) Vad är en konsolapplikation?  
b) Ge ett exempel på när en konsolapplikation kan vara lämplig att använda.

---

## Del 3: Datatyper i C# (Läranderesultat 3)

### Fråga 9 - Primitiva Datatyper

**Beskriv följande datatyper och när man använder dem:**

a) `int`  
b) `double`  
c) `string`  
d) `bool`

Förklara också skillnaden mellan `int` och `double`.

---

### Fråga 10 - Stark typning

**C# är ett starkt typat språk, medan JavaScript är löst typat.**

a) Vad innebär det att ett språk är starkt typat?  
b) Ge ett exempel på en fördel med stark typning som du märkt av i C#.

---

### Fråga 11 - Arrays och Listor

**Förklara skillnaden mellan en array och en `List<T>` i C#.**

a) När bör man använda en array?  
b) När bör man använda en `List<T>`?  
c) Skriv ett kort kodexempel (1-3 rader) som visar hur man lägger till ett element i en `List<int>`.

---

### Fråga 12 - Dictionary

**Vad är en `Dictionary<TKey, TValue>` och när är den användbar?**

Förklara med egna ord och ge två exempel på scenarion där Dictionary är ett bra val (inget kodexempel krävs).

---

### Fråga 13 - LINQ

**Vad är LINQ och vad används det till?**

Ge exempel på minst två LINQ-metoder du använt (t.ex. `Where`, `Select`, `OrderBy`, `Count`, etc.) och förklara kort vad de gör.

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