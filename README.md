# CSS to the Rescue @cmda-minor-web 2020 - 2021

## Week 1 - Mijn plan
### Kickoff

### Opdracht
Ik heb gekozen voor de CSS Zen Garden. Bij de CSS Zen Garden is het de bedoeling om _alle_ mogelijkheden van CSS te ontdekken. Hierbij mmoest je kiezen uit een context en twee eisen.
Ik heb 2 contexten gekozen: **print-stylesheet** & **prefers-reduced-motion**.
Voor de eisen heb ik gekozen voor: **SVG toepassen** & **Responsive zonder media queries**.

Mijn grootste uitdagingen zijn:

* [x] Een visueel leuk/mooi uiterlijk verzinnen en creëren
* [x] Responsive maken d.m.v. goed en slim gebruik te maken van relative units
* [x] Classes en ID's vermijden
* [x] CSS Grid toepassen en een stapje verder hiermee te gaan
* [x] Onbekende functies gebruiken zoals clamp()
* [x] Logica in CSS creëren

#### Inspiratie & Schetsen
Ik heb inspiratie op gedaan voor mijn ontwerp:  
In de opdracht-uitleg.pdf had Vasilis veel verschillende posters laten zien om inspiratie op te doen, deze trekken mij aan:  
![Inspiratie1](https://user-images.githubusercontent.com/58043913/109858068-a9f1db00-7c5b-11eb-8125-e5aaadf52d14.png)
![Inspiratie2](https://user-images.githubusercontent.com/58043913/109858146-c1c95f00-7c5b-11eb-8def-b6da05df145d.png)
![Inspiratie3](https://user-images.githubusercontent.com/58043913/109858255-df96c400-7c5b-11eb-9625-1034d00133b8.png)
![Inspiratie4](https://user-images.githubusercontent.com/58043913/109858302-ef160d00-7c5b-11eb-9317-aaa1210f4788.png)
![Inspiratie5](https://user-images.githubusercontent.com/58043913/109858389-09e88180-7c5c-11eb-8da2-95a57fa6083a.png)

Ik heb daarnaast nog gezocht op Google, Dribbble , Behance, etc. naar afbeeldingen van food menu's en inspiratie opgedaan.

**Schetsen**  
Ik ben geïnspireerd gaan schetsen:
![Schets1](https://user-images.githubusercontent.com/58043913/109859224-01447b00-7c5d-11eb-9c73-517d00515947.jpg)
![Schets2](https://user-images.githubusercontent.com/58043913/109859241-03a6d500-7c5d-11eb-842f-aa8b320f830c.jpg)
![Schets3](https://user-images.githubusercontent.com/58043913/109859248-04d80200-7c5d-11eb-8c71-2bc08176f8fd.jpg)
![Schets4](https://user-images.githubusercontent.com/58043913/109859251-05709880-7c5d-11eb-9241-57195d8d6a93.jpg)

## Week 2
Ik begon met wat leuke expirementjes:

**Titel in spiegelbeeld**  
![Titelspiegelbeeld](https://user-images.githubusercontent.com/58043913/109860816-e115bb80-7c5e-11eb-8bbf-eefff8c5fd60.png)  
Deze titel staat nu in spiegelbeeld door middel van:
```css
transform: scale(-1, 1);
```

**Grid**  
De gerechten staan naast elkaar door `display: grid;`:

![grid](https://user-images.githubusercontent.com/58043913/109861681-de679600-7c5f-11eb-9170-5563317b4671.png)

**Clip-paths**  
![Clippath](https://user-images.githubusercontent.com/58043913/109861028-26d28400-7c5f-11eb-89cb-1c1a2550ca00.png)  
Met clip-path kan je een element uitsnijden in je gewenste vorm:
```css
clip-path: polygon(25% 0, 5% 50%, 5% 60%, 50% 100%, 95% 60%, 95% 50%, 75% 0);
```  
Deze clip-paths kan je animeren, met een hover heb ik deze geanimeerd naar:  
![Clippath2](https://user-images.githubusercontent.com/58043913/109861244-61d4b780-7c5f-11eb-8639-e96eb045526e.png)


Door `position: sticky;` op de content van de gerechten te zetten krijg je een leuk scroll effect:  
![Sticky](https://user-images.githubusercontent.com/58043913/109861437-95174680-7c5f-11eb-9e42-dffa46fd38d7.png)
Hier scrollt de text mee tot aan de beneden rand van het gerecht.

### Evaluatie
Grid ging best soepel en zonder moeilijkheden.

`clip-path` was nieuw voor mij, ik heb zeker wat lopen puzzelen met de **clip-path**, omdat de paths best ingewikkeld zijn met alleen maar procenten of andere cijfers is het lastig te begrijpen. Maar met behulp van [Clippy](https://bennettfeely.com/clippy/) is het een stuk makkeljker om gewenste paths te maken. Ik heb daarnaast zelf lopen sleuten aan de cijfers etc en goed geëxperimenteerd.

Volgende week wil ik graag echt wat vormgeving gaan toepassen en een mooi geheel neerzetten.


## Week 3
Ik ben deze week meteen begonnen met experimenteren van de vormgeving, ik vond het spiegelbeeld effect van de titel wel leuk, maar qua vormgeving en uitstraling niet zoveel hebben. Door een gastspreker bij dit vak ben ik geïnspireerd geraakt om het volgende te maken:  
![titelvormgeving](https://user-images.githubusercontent.com/58043913/109869514-41115f80-7c69-11eb-8db7-54afc7649b23.png)  
Ik heb hierbij een `:before` selector gebruikt. Deze ziet er als volgt uit:
```css
    content: "R";
    color: white;
    display: block;
    shape-outside: ellipse(100% 50% at -80% 50%);
    width: 5rem;
    height: 12rem;
    float: left;
    margin-right: -50px;
    background: var(--color-red);
    border-radius: 0% 100% 100% 0% / 50% 50% 50% 50%;
```
Hier heb ik geëxperimenteerd met een combinate van `shape-outside` en `border-radius`. De shape-outside kende ik nog niet voordat de gastspreker dit introduceerde. Border-radius kende ik al wel, maar had hier nog niet echt mee geëxperimenteerd, ik kwam nooit verder dan `border-radius: 20px;`.

Kleine vormgeving toegepast aan de subtitles:  
![subtitle](https://user-images.githubusercontent.com/58043913/109870091-f8a67180-7c69-11eb-8dd3-8d5c36425436.png)  
Hover:  
![subtitlehover](https://user-images.githubusercontent.com/58043913/109870130-01974300-7c6a-11eb-972d-fcd7fbe8a26e.png)  

Vormgeving van gerechten klein beetje aangepast:  
![gerechtenvorm](https://user-images.githubusercontent.com/58043913/109870228-2095d500-7c6a-11eb-83ea-5ef7f90c9661.png)  
Hover:  
![gerechtenvormhover](https://user-images.githubusercontent.com/58043913/109870312-3c00e000-7c6a-11eb-919d-cf060397add9.png)  
Vormgeving van sub-koppen:  
![image](https://user-images.githubusercontent.com/58043913/109870422-5b980880-7c6a-11eb-80cc-85e4bf3250ad.png)  
Hierbij heb ik gebruik gemaakt van `:before` en `:after`. Deze heb ik tevens ook geanimeerd.

Ik ben best trots op de vormgeving van de sub-koppen. Ik vind de kleur leuk en het effect met die zwarte en lichtgroene letters erg pakkend. Hierdoor heb ik de achtergrond kleur veranderd:  
![background](https://user-images.githubusercontent.com/58043913/109870910-eed13e00-7c6a-11eb-9374-355e85803adc.png)  

In een thema-sessie van Vasilis over typografie heb ik geleerd over _variable fonts_. Deze fonts hebben meerdere aanpasbare attributen/eigenschappen dan normale fonts. [v-fonts.com](https://v-fonts.com/) heeft veel leuke fonts en je kan meteen ermee experimenteren.
Ik heb [Ancho](https://v-fonts.com/fonts/ancho) uitgekozen om in mijn eigen website te gebruiken.
Deze heb ik als volgt geanimeerd:  
![Animatie](https://user-images.githubusercontent.com/58043913/109872623-f560b500-7c6c-11eb-9a96-0bfaa2498364.gif)  
Dit heb ik voor elkaar gekregen met deze code:
```css
font-family: ANCHO;
font-variation-settings: "wght" 52;
animation: varFont 1s infinite alternate;

@keyframes varFont {
	to {
		font-variation-settings: "wght" 500;
		letter-spacing: 2px;
		text-shadow: -10px -10px 3px #cc4d4d;
	}
}
```

Ik heb de titel aangepast naar:  
![Title animation](https://user-images.githubusercontent.com/58043913/109873117-9b142400-7c6d-11eb-8ca9-37c66d568f8b.gif)  
Ook hieraan heb ik een animatie on hover toegevoegd. Met `letter-spacing` en `text-shadow`.

**Mes / CSS Logica**  
Ik heb een mes toegevoegd als SVG, deze interactief gemaakt met een checkbox. Deze mes "snijdt" door het woord logo heen en en dan komt er bloed:  
![Knife](https://user-images.githubusercontent.com/58043913/109929058-6b453a80-7cc6-11eb-8542-f6c0dcf41ae6.gif)  
Dit is gelukt met CSS logica, dat gaat als volgt:
```css
input#switch:checked ~ label>.knifeSvg {
	transform: rotate(50deg);
}
```
Logica: **Als** de checkbox gecheckt is, dan moet de mes 50graden draaien.  
Ik heb tijdens de kickoff meer gespeeld met logica. Bekijk dat [hier](https://jelmerovereem.github.io/css-to-the-rescue-2021/).

**Reduced motion**  
Ik ben ook begonnen met reduced motion, ik heb eerst op internet een klein beetje opgezocht wat dit betekent voor het web. Het houdt simpelweg in dat je animaties en bewegende beelden zoveel mogelijk vermijdt als mensen dit liever hebben.
Dit kan als volgt in css:
```css
@media (prefers-reduced-motion) {
	h2:before, h2:after {
		animation: dissolve 2s;
	}

	main>section>article, main>article {
		transition: none;
	}
}
```
Hier verminder ik de beweging in de sub-koppen en zet ik simpelweg een transition uit. 

### Evaluatie
Ik ben blij/trots dat ik een stuk verder ben gekomen met mijn vormgeving, nu heb ik meer motivatie om er leuke dingen mee te doen en meer te experimenteren.
Ik heb mezelf uitgedaagd met de `:before`,`:after` en `text-shadow` properties.
Voor mij waren de variable fonts echt nieuw en vind dat ik daar van heb geleerd en iets leuks mee heb gemaakt.
Ik heb veel gepuzzled met hoe de titel eerst was, met `shape-outside` en `border-radius`, het is niet helemaal zoals ik wilde, maar heb er wel zeker van geleerd.

Ik wil voor volgende week(vakantie/afronding) meer responsiveness erin gooien, het meer als geheel maken, spelen met gradients en print style sheet toevoegen.


## Week 4 (vakantie/afronding)
Ik ben begonnen met het afmaken van het geheel en de vormgeving.

**Gerechten**
Ik heb de titels van de gerechten gestyled en geanimeerd met text-shadows:  
![textshadow](https://user-images.githubusercontent.com/58043913/109930802-59649700-7cc8-11eb-929f-95ee2b15e7a5.gif)  
Ik heb gespeeld met _layered text-shadows_, dit houdt in dat je meerdere text-shadows toevoegt aan een element:
```css
--textshadow-color1: black;
	--textshadow-color2: white;
	text-shadow: 0px 0px 0 var(--textshadow-color1), -2px -2px 0 var(--textshadow-color1), -4px -4px 0 var(--textshadow-color2), -6px -6px 0 var(--textshadow-color1), -8px -8px 0 var(--textshadow-color2),
				0px 0px 0 var(--textshadow-color1), -2px 2px 0 var(--textshadow-color1), -4px 4px 0 var(--textshadow-color2), -6px 6px 0 var(--textshadow-color1), -8px 8px 0 var(--textshadow-color2);
```
En deze op hover geanimeerd, door simpelweg de waarden de tegenovergestelde waarde te geven, 2px wordt -2px:
```css
main>section>div>article>h3:hover {
	text-shadow: 0px 0px 0 var(--textshadow-color1), 2px 2px 0 var(--textshadow-color1), 4px 4px 0 var(--textshadow-color2), 6px 6px 0 var(--textshadow-color1), 8px 8px 0 var(--textshadow-color2),
				0px 0px 0 var(--textshadow-color1), 2px -2px 0 var(--textshadow-color1), 4px -4px 0 var(--textshadow-color2), 6px -6px 0 var(--textshadow-color1), 8px -8px 0 var(--textshadow-color2);
}
```

De prijzen van de gerechten heb ik een pop-art achtig ontwerp gegeven met `-webkit-text` properties:  
![priceanimation](https://user-images.githubusercontent.com/58043913/109931232-e27bce00-7cc8-11eb-9377-55aa57cb92ec.gif)  
Met behulp van [deze codepen](https://codepen.io/creatz/pen/pooBeev) heb ik geëxperimenteerd met deze properties:
```css
main>section>div>article div {
	-webkit-text-fill-color: transparent;
	-webkit-text-stroke-width: 1px;
	-webkit-text-stroke-color: white;
	text-shadow: 2px 2px #ff1f8f, 5px 5px black;
	transition: text-shadow .6s;
}

main>section>div>article div:hover {
	text-shadow: 0px 0px #ff1f8f, 1px 1px black;
}
```

Daarna heb ik elk gerecht gestyled met een `display: grid;`, om hier nog verder mee te experimenteren:  
![recipegrid](https://user-images.githubusercontent.com/58043913/109931510-3dadc080-7cc9-11eb-9ad3-c5c25b6d482e.png)  
Ik heb hier gespeeld met `grid-areas` om de titel boven de beschrijving en prijs te houden:
```css
display: grid;
align-items: center;
grid-template-columns: 90% 10%;
grid-template-areas:
"title title"
"description price";

/* Bij de elementen de grid-area geven */
grid-area: title;
```

Voor de dynamiek/differentiatie heb ik de nth-child(even) een geanimeerde gradient gegeven:  
![backgroundgradientanimate](https://user-images.githubusercontent.com/58043913/109931995-ea883d80-7cc9-11eb-88ce-3ba144b869c6.gif)  
De achtergrond heeft een `repeating-conic-gradient()` en met custom properties kan je de angle animeren:
```css
main>section:nth-child(even) {
	background-image: repeating-conic-gradient(from var(--conicHoek) at 70% 50%, var(--color-red), black, lightgreen, var(--color-red));
	animation: rotateGradient 30s infinite alternate;
}

@property --conicHoek {
  syntax: '<angle>';
  inherits: false;
  initial-value: .4turn;
}

@keyframes rotateGradient {
	from {
		--conicHoek: 0turn;		
	}

	to {
		filter: invert(100%);
		--conicHoek: 1turn;
	}
}
```
Ik heb ook een filter toegepast voor een extra leuk effect:  
![inverteffect](https://user-images.githubusercontent.com/58043913/109932193-28856180-7cca-11eb-9f54-db0a3abd9e23.png)

Ik heb de quotes geanimeerd met ook een gradient en deze laten draaien:  
![quotes animate](https://user-images.githubusercontent.com/58043913/109932906-18ba4d00-7ccb-11eb-802d-5d66753ba288.gif)

**Responsive main grid**  
Ik heb daarna een responsive grid zonder media queries toegepast:  
![responsivegrid](https://user-images.githubusercontent.com/58043913/109932335-58346980-7cca-11eb-8118-a3ba4c87080e.png)  
Hierbij staan de gerechten op breed beeld naast elkaar, maar zodra je het scherm kleiner maakt gaan ze onderelkaar:  
![image](https://user-images.githubusercontent.com/58043913/109932511-93cf3380-7cca-11eb-88f0-6f4eea370ae8.png)  
Dit gaat als volgt:
```css
main {
	--auto-grid-min-size: clamp(50%, 700px, 100%);
	display: grid;
	grid-template-columns: repeat(auto-fill, minmax(var(--auto-grid-min-size), 1fr));
}
```
Ik had eerst `--auto-grid-min-size: 700px;`, maar daar kreeg ik wat problemen mee zodra het scherm kleiner werd. Dus ik ben verder gaan experimenteren en kwam toen met `--auto-grid-min-size: min(100%, 700px);`, dit loste het probleem op, maar ik wilde in week 1 mezelf uitdagen met clamp(), dus ben daar naar gaan zoeken en het is gelukt! :) 

**Print-style-sheet**
Nu ik tevreden was met het geheel ben ik begonnen aan de print style sheet. Deze initieer je zo:
```html
<head>
	<link rel="stylesheet" media="print" href="styles/print.css">
</head>
```
styles/print.css
```css
@media print {
	/* code */
}
```
Hier heb ik gekeken naar dat een restaurant ook moet uitkijken met print kosten, dus heb ik de kleuren verminderd. Gradients printen nooit mooi uit, dus heb die ook uitgezet. De gerechten heb ik precies formaat van a4 gegeven, zodat deze goed worden uitgeprint.

**Tab-index**  
Om de website toegankelijk te maken voor mensen die alleen het toetsenbord gebruiken en met de toets `tab` navigeren heb ik handmatig `tab-index` toegevoegd aan de elementen.

**Reduced motion**  
Ik heb het reduced motion stuk verder uitgewerkt door de animaties uit te schakelen en de text-shadows eraf te halen. De text-shadows bewegen niet, maar ze geven wel een dynamiek effect wat ook storend kan zijn.

### Evaluatie
Ik ben trots op de animaties en hierbij ook de reduced motion. Ik vind de gradients erg goed gelukt.  
Ik ben ook heel blij met dat het is gelukt met de clamp() en responsive zonder media queries. Ik heb echt lang moeten tobben met die grid auto-fill en minmax. Ik heb dit ook nog geprobeerd met flexbox, maar dat mislukte.

Ik wil graag nog een navigatie toevoegen voor meer toegankelijkheid. En eigenlijk nog meer experimenteren met allemaal leuke animaties en coole css properties, maar ik ben zeker trots in hoever ik al ben gekomen!

## Bronnen
* [conic-gradient](https://codepen.io/shooft/pen/YzpVjOw)
* [print-style-sheet](https://www.sitepoint.com/css-printer-friendly-pages/)
* [responsive zonder queries (1)](https://archive.hankchizljaw.com/wrote/create-a-responsive-grid-layout-with-no-media-queries-using-css-grid/)
* [responsive zonder queries (2)](https://blog.logrocket.com/flexible-layouts-without-media-queries/)
* [gradient text](https://css-tricks.com/snippets/css/gradient-text/)
* [pop art text effect](https://codepen.io/creatz/pen/pooBeev)
* [CSS grid](https://css-tricks.com/snippets/css/complete-guide-grid/)