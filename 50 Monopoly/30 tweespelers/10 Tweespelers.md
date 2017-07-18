## Opdracht 3: Realisme toevoegen: twee spelers

Monopoly wordt normaal gesproken gespeeld door meer dan één speler, dus laten we een tweede speler introduceren.
Doel van deze opdracht is om eerst te evalueren wat het voordeel is van de speler die begint met gooien en vervolgens te bestuderen hoe
we in het spel dit nadeel voor speler 2 kunnen herstellen.
 
![](Balans.png){:.inline}{: style="width:35%"}

### Tussenstap 1: Het voordeel van speler 1
Maak voor deze opdracht een nieuw bestand aan genaamd monopolyMultiplayer.py binnen dezelfde map als de vorige opdracht.
We willen eerst ontdekken wat het voordeel van de beginnende speler is. Om dat te kunnen doen hebben we eerst twee spelers,
ofwel twee `Piece`s nodig. Ook moeten we nu twee keer het bezit bijhouden. Let hierbij op, als speler 1 iets in zijn
bezit heeft, kan speler 2 dit niet meer kopen! Vergeet niet dat je code uit monopolyTrump.py kan importeren, je hoeft
niet te copy-pasten! 

Dan de vraag zelf, wat is het voordeel van speler 1? Simuleer hiervoor een goed aantal potjes monopoly, en bepaal
het gemiddelde verschil aan vakjes dat speler 1 en speler 2 in bezit hebben als alle vakjes zijn opgekocht.
Print dit verschil op de eerste regel van de output. Bijvoorbeeld als volgt:

	Als beide spelers beginnen met 1500 euro, heeft speler 1 gemiddeld 7 meer vakjes

Let op: bovenstaande antwoord is fout, het goede antwoord mag je zelf ontdekken!


### Tussenstap 2: Het nadeel van speler 2 repareren
Om het nadeel van speler 2 tegen te gaan kunnen we speler 2 meer startgeld toekennen. De vraag is nu,
hoeveel startgeld moet speler 2 krijgen zodat hij gemiddeld net zoveel vakjes in zijn bezit heeft
als alle vakjes zijn opgekocht?

Maak een grafiek met de hoeveelheid aan startgeld voor speler 2 op de x-as, en op de y-as 
het aantal vakjes dat speler 1 meer heeft dan speler 2 als alle vakjes zijn opgekocht. Voor inspiratie
zie de grafiek bovenin. Print vervolgens op de tweede regel van de output (de eerste is voor tussenstap 1)
hoeveel startgeld speler 2 nodig heeft om gemiddeld evenveel vakjes te hebben. Het kan zijn dat je
hiervoor moet interpoleren tussen jouw meetpunten! Bijvoorbeeld als volgt:

	Als speler 2 begint met 1900 euro, hebben beide gemiddeld evenveel vakjes

Let op: bovenstaande antwoord is fout, het goede antwoord mag je zelf ontdekken!


## Testen

	checkpy monopolyMultiplayer

## Samenvatting

De simulatie die we hier gedaan hebben is een versimpelde versie van de vaak zeer complexe 
modellen waarmee grote financiele partijen risico's inschatten en strategieën bepalen. 
Tegelijkertijd worden deze simulaties ook gebruikt door politieke partijen om de effecten 
van hun keuzes door te rekenen in verschillende scenario's.




