# Virus

![](virus.jpg){:.inline}{: style="width:100%"}

Voor o.a. de farmaceutische industrie is het belangrijk om de succeskans van een geneesmiddel te bepalen.
Dit is lastig analytisch te doen, maar we kunnen het wel modelleren. 

## Opdracht

In deze opdracht ga je virusdeeltjes simuleren, welke kunnen reproduceren en sterven. 
Daarna gaan we een geneesmiddel introduceren, en het effect op de viruspopulatie bestuderen.


### Tussenstap 1: Een virusdeeltje

Als model voor een virusgenoom gaan we gebruik maken van een DNA string welke bestaat uit de vier nucleotiden ATGC. 
A (Adenine) is altijd verbonden met T (Thymine), G (Guanine) is altijd verbonden met C (Cytosine). 
Voor de representatie doen we het volgende, een serie van nucleotides in een string.
Aangezien er maar 4 mogelijkheden zijn voor baseparen (AT, GC, TA, CG), kunnen we dit encoderen met de 4 letters.
Zie bijvoorbeeld de volgende string:

	AGTC

Dit is een DNA string met alle vier base paren, eerst het paar AT, dan GC, dan TA, en als laatste CG.
Effectief laten we telkens het aanhangende nucleotide weg, dat maakt de representatie wat simpeler!

Maak een nieuw bestand aan genaamd `virus.py` (hopelijk vind jouw virusscanner dit okee ;).
Schrijf een functie `generateVirus(length)`. 
Deze functie accepteert één argument, length, dat is een integer die de lengte van het virusgenoom representeerd.
De functie moet een string returnen bestaande uit een willekeurige sequentie van nucleotides.

Tip: kijk eens naar de `random.choice()` functie!


### Tussenstap 2: Muteren

Zodra een virus wordt geboren heeft deze een kans te muteren. 
Muteren is het veranderen van één willekeurig basepaar voor een willekeurige ander.
Bijvoorbeeld van AGTC naar ATTC.

Schrijf een functie `mutate(virus)`.
Deze functie accepteert één argument, virus, dat is een string van nucleotides.
De functie moet een string returnen bestaande uit dezelfde nucleotides, waarvan er één is gemuteerd.


### Tussenstap 3: Reproductie

Een virus heeft een kans zich voort te planten op elke tijdstap in de simulatie.
Schrijf hiervoor een functie `reproduce(viruses, reproductionRate, mutationRate)`



Schrijf een functie `dobbelstenenWorp()` binnen `monopolyTrump.py`. De functie
moet geen argumenten accepteren, en de uitkomst van de dobbelstenen worp als integer
returnen. Let op, binnen Monopoly heb je als speler twee dobbelstenen! Zo heb je de meeste
kans om 7 te gooien, en kun je 1 helemaal niet gooien. Om deze functie te implementeren kun je
gebruik maken van de functie `randint()` van de `random` module. Google maar!


### Tussenstap 2: Rondlopen

Nu we dobbelstenen hebben kunnen we rondlopen op het bord. Om het aan jezelf te bewijzen, loop een rondje, 
en stop zodra je weer voorbij start bent (positie 0). Print na elke zet (dobbelstenen worp) het naam van het vakje
en de waarde van het vakje waar de pion op staat. Zoiets:

	Na worp 0: brink, 60
	Na worp 1: velperplein, 120
	Na worp 2: neude, 180
	...
	Na worp 7: dorpsstraat, 60


### Tussenstap 3: Bezit

Rondlopen is één ding, maar we willen straks ook straten, stations en nutsbedrijven kunnen kopen. We hebben dus iets 
nodig om bezit te onthouden. Simpelweg een lijst zou hiervoor onhandig zijn, want sommige vakjes kun je niet kopen.
Hier kunnen we handig een dictionary gebruiken. Waar we de namen van de vakjes kunnen gebruiken als keys, en daaraan
als value kunnen koppelen of ze al gekocht zijn of niet (een boolean). Als we dan enkel de namen van de vakjes die je
kan kopen in de dictionary stoppen, kunnen we straks heel makkelijk controlleren hoeveel er al is gekocht!

Om te beginnen hebben we een dictionary nodig, en moeten we deze vullen met alle namen van vakjes welke je kan kopen.
Dit zijn de vakjes met een waarde (anders gezegd, alle vakjes met een waarde hoger dan 0). Dit is jouw taak: schrijf een
functie genaamd: `bezit(board)`. Deze functie accepteert als argument een `Board`, en returned een
dictionary, met alle vakjesnamen met een waarde hoger dan 0 als keys, en alle values met waarde `False`.


### Tussenstap 4: Trump
We hebben nu een bord, een pion, dobbelstenen, en een manier om bezit bij te houden. Tijd om voor Trump te gaan spelen.
Onze vraag is, hoe vaak moet je dobbelen voordat je alles in bezit hebt? Je kan enkel een vakje kopen als je erop staat!

Zorg dat je dit niet één keer simuleert, maar een gezond aantal keer, zeg 1000, 10000 keer? Mag best een paar seconden
duren, maar niet te lang (`checkpy` kapt je af na 10 seconden)!

Als output moet je programma het aantal keren dobbelen dat gemiddeld nodig was printen in de eerste regel van de output.

Zet jouw code van tussenstap 4 binnen `if __name__ == "__main__":`, dit zorgt er voor dat jouw code enkel wordt uitgevoerd als `__name__`
gelijkt is aan de string `"__main__"`. Huh? Python heeft een aantal verborgen variabelen en functies, deze beginnen en 
eindigen allemaal met `__`. Eén daarvan is `__name__` dat is een naam die Python aan de module toekent. Run je de module
direct, dan is die naam `"__main__" (denk ook terug aan C!). Ofwel `if __name__ == "__main__":` zegt letterlijk, voer de 
code hieronder enkel uit, als je deze module direct runt, en niet als je deze importeert.

## Testen

	checkpy monopolyTrump
