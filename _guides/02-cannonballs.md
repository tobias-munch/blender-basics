---
layout: default
title: "Afsnit 2: Kanonkugler"
order: 2
---
# Afsnit 2 - Kanonkugler
Nu hvor vi har lært at bevæge både kameraet og nogle objekter, skal vi prøve at lave en simpel figur. I forbindelse med at vi laver en kanon senere, er det oplagt at lave en bunke af kanonkugler.

![Kanonkugler!]({{ site.baseurl }}/z_assets/kanonkugler.png)

Det første sted man starter når man skal lave et objekt, er at se hvilke figurer som objektet består af. Her har vi en simpel fod, og en masse kugler, men lad os fokusere på kanonkuglerne, da det kan være kompliceret hvis man ikke ved hvordan man gør det effektivt.

## Sektion A: Shading og Arrays

Det at lave en kugle er ikke svært - Vi kunne se i forrige afsnit at man bare kan tilføje en UV Sphere, som er tæt nok på en helt rund kugle. En ting vi dog ikke kiggede på før, er hvordan man tilpasser sit nye objekt. Nede i venstre hjørne dukker der en menu op efter man tilføjer et nyt objekt, og folder man den ud kan man tilpasse det nye objekt. 
![Objekt-settings]({{site.baseurl}}/z_assets/objekt-settings.png)

Det eneste der er vigtigt lige nu, er at sætte Radius, som angiver hvor stor kuglen er, til 0,5. Hvis man gerne have den til at se rund ud, kan man venstreklikke på kuglen, derefter højreklikke på den hvilket giver følgende muligheder, og så vælger man *Shade Smooth*.

![shading muligheder]({{ site.baseurl }}/z_assets/shading-muligheder.png)

> **Object Shading:**
> Man kan også vælge *Shade Auto Smooth* og *Shade Flat*, men de gør nogle andre ting end hvad vi skal bruge nu. Den korte forklaring er, at *Shade Smooth* prøver at gøre ALT smooth, hvorimod *Shade Flat* viser objektet præcis som den er. *Shade Auto Smooth* tager højde for hvor på objektet er der rundt/blødere kanter, og hvor der er fladt, og shader efter det. På billedet nedenunder kan du se hvad de gør på en kasse med nogle blødere kanter
> ![shading explainer]({{site.baseurl}}/z_assets/shading-explainer.png)

Nu har vi en rund kugle, men det vil være irriterende og tage lang tid hvis vi skal placere alle kuglerne i hånden. Der kommer til at være 30 styks hvis vi laver fire lag af kugler! Det behøver vi dog ikke at gøre, da vi kan benytte os af *Modifiers*, som er placeret i en tab ude i højre side med et blåt skruenøgle-ikon.
![modifiers-lokation]({{site.baseurl}}/z_assets/modifiers-location.png)
Her skal vi finde den modifier der hedder *Array*, og den ligger inde under *Generate > Array* (Alternativt kan man søge efter Array). Tilføjer man den kan man med det samme at der bliver tilføjet en ny kugle ved siden af den første. Hvis man gerne vil have flere, så ændrer man *Count* til noget andet.

Det er fint med en en række af kanonkugler, men vi ville jo gerne have et helt lag af dem. Hvad kan vi så gøre for at få det? Vi tilføjer da bare en Array-modifier til! Husk at sætte *Count* til det samme som før, og vær opmærksom på, at vi lige nu kopierer rækken i den samme retning som før. For at gøre noget ved det, skal vi ændrer på *Factor X* og *Factor Y* på den anden Array-modifier. De kontrollerer hvilken retning som vi laver vores Array på, og hvor meget den skal bevæges i den retning.
Hvis du har gjort det rigtigt, skulle du gerne have et lag af kanonkugler som på billedet.

![Array with array]({{site.baseurl}}/z_assets/array-with-array.png)

Nu har vi det første lag af bunken, og man kunne sagtens gøre det hele forfra med en ny kanonkugle og tilføje modifiers, men det behøver vi faktisk ikke. Den smarte løsning vil være at kopiere det, som vi allerede har, og ændre lidt på det bagefter!

Prøv at klikke på dit lag af kanonkugler, og så tryk *Shift+D*. Bevæg musen lidt, og så kan du se at du har kopieret laget af kanonkugler, og venstreklikker du nu, placerer du det nye lag (højreklik smider den tilbage til det første lags position). Nu kan man sætte *Count* til én mindre end før, og så har du et nyt lag! Så kan man fortsætte indtil man når den øverste kugle, hvor man kan fjerne de to Array-modifiers, da et Array med *Count=1* ikke gør noget.

<img src="{{site.baseurl}}/z_assets/cannonball-pile.jpg" alt="bunke-af-kanonkugler" style="width:100%">

## Sektion B: En simpel fod

Nu hvor vores bunke af kanonkugler er lavet, kan vi lave en simpel fod som de kan være på.

## Sektion C: Simple materialer