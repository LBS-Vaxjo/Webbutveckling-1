# CSS Help Doc
This Docs contains: <br/>
[Linking](#Linking) <br/>
[Selectors](#Selectors) <br/>
[Properties](#Properties)

---
## <a name="Linking"></a> Linking
### Länka CSS
För att länka ett externt CSS doskument till din HTML fil så använder vi taggen `link` som vi lägger i vår `head`. I taggen så sätter vi attributet `rel` till `stylesheet` och attributet `href` till länken till vårt CSS dokument. Det betyder att vår HTML kod kan se ut såhär:
```html
<head>
    <link rel="stylesheet" href="path/to/my_file.css">
</head>
```
Det går bra att använda lokala / relativa länkar när vi länkar till en CSS fil. Så för att gå en nivå djupare så skriver vi namnet på mappen följt av ett snedsträck  (`first_folder/contiue.css`). För att gå up en nivå använder vi två punkter följt av ett snedsträck (`../upper.css`).
### Länka JavaScript
Länka ett JavaScript-dokument gör vi genom att använda taggen `<script></script>`. Script taggen går att använda både för att skriva JavaScript-kod direkt i taggen och för att länka till ett externt JavaScript-dokument.  

När vi länkar JavaScript går det att göra på två (generellt, men kan vara fler) ställen i koden. Första stället är att skriva `<script src=""></script>` i `<head></head>` taggen. Att länka JavaScript i head-taggen är ofta inte rekommenderat eftersom då kommer koden i JavaScript att köras innan hela HTML dokumentet har laddats in.  
Plats nummer två (och alla andra) är att skriva Script-taggen i `<body></body` istället. Detta är rekommenderat att skripten läggs längst ner på sidan för att låta webbläsaren ladda in hela HTML sidan före den börjar arbeta med JavaScript-koden.  

Exempel:
```html
<body>
	<script src="./link/to/script.js"></script>
</body>
```
## <a name="Selectors"></a> Selectors
En Selector används för att välja ut vilket eller vilka HTML element vi will påverka. Det finns tre olika huvudsakliga selectorer och de är:
* Element selektor
* Klass selektor
* Id selektor

### Element selektor
Element selektor betyder att vi väljer ut HTML element via deras man och ändrar deras utseende. Vi väljer våra HTML element genom att skriva namnet på elementet följt av klammerparenterser. Är du osäker på vad namnet är så är det namnet som står inom vinkelparenterserna. I fallet vi vill ändra på hela vår sidan kan vi använda HTML-taggen  `<body>` och då är elementets namn `body`. Då kan ett exempel se ut såhär:
```CSS
body{
    background-color: grey;
    color: white;
}
```

### Klass selektor
När vi använder oss av Klass selectorer så väljer vi ut de HTML element som har vår tilldelade klass på sig. I HTML så tilldelar vi en klass genom att skriva `class="vårtKlassNamn"` efter vårt elementnamn men före den stängande vinkelparentersern. För att markera att det är en klass som vi väljer i vår CSS så sätter vi en punkt framför namnet på vår klass: `.vårtKlassNamn`.

HTML:
```html
<body class="myClass">

</body>
```

CSS:
```css
.myClass{
    background-color: grey;
    color: white;
}
```

Klasserna som vi skapar kan vi lägga på nästan alla våra HTML element och klasserna kan finnas på flera element samtidigt.

### Id selektor
En id selektor fungerar mycket som en klass selektr men i HTML-taggen byter vi ut `class` mot `id` och i vår CSS byter vi punket mot ett hashtag (`#`).

En stor skillnad i hur id använda är att id ska endast användas på ett element samtidigt. Det betyder att per HTML dokument ska det inte finnas två av samma id. Det betyder inte att det inte går att två av samma, för det gör det, men enligt standader i HTML ska det inte finnas två av samma id.

Såhär kan då HTML och CSS se ut om vi använder id:

HTML:
```html
<body id="myId">

</body>
```

CSS:
```css
#myId{
    background-color: grey;
    color: white;
}
```

## <a name="Properties"></a> Properties
Properties, eller på svenska: egenskaper, är det vi skriver för att ändra utseendet på våra HTML element i vår CSS fil. Altså det som skrivs inuti vårt kodblock i vår CSS.

```css
body{
    /* Här skrivs egenskaper */
    color: black; /* <-- egenskap */
}
```

För en lista på alla egenskaper och vad de gör kolla [här](https://www.w3schools.com/cssref/default.asp).
