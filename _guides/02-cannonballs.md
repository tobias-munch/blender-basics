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

<img src="{{site.baseurl}}/z_assets/cannonball-pile.png" alt="bunke-af-kanonkugler" style="width:100%">

Husk i øvrigt at gemme din fil!
## Sektion B: En simpel fod

Nu hvor vores bunke af kanonkugler er lavet, kan vi lave en simpel fod som de kan være på. Da vores bunke af kanonkugler er firkantet i bunden, giver det best mening at bruge en *Cube*. Det første vi skal gøre er, at skalere den så der er plads til kuglerne:

<img src="{{site.baseurl}}/z_assets/fod-fra-top.png" alt="fod-fra-top" style="width:100%">
<img src="{{site.baseurl}}/z_assets/fod-fra-side.png" alt="fod-fra-side" style="width:100%">

Nu skal vi så begynde at redigere i selve objektet, det gør vi ved at ændre fra *Object Mode* til *Edit Mode*, enten ved at skifte det i venstre hjørne eller ved at trykke *Tab* i 3D Viewporten

<img src="{{site.baseurl}}/z_assets/object-mode.png" alt="object-mode" style="width:100%">

Inde i Edit Mode kan vi vælge forskellige dele af objektet, vi gerne vil ændre på. Der er tre måder at vælge dele af objektet: 

* *Vertex Mode*, hvor man arbejder med de enkelte punkter i objektet.
* *Edge Mode*, hvor man arbejder med linjerne mellem hvert vertex.
* *Face Mode*, hvor man arbejder med en hel side af gangen.

Man kan skifte mellem dem ved at trykke på 1, 2 eller 3 i Edit Mode, eller ved at vælge dem som vist på billedet:

<img src="{{site.baseurl}}/z_assets/vertex-edge-face-modes.png" alt="vertex-edge-face-modes" style="width:100%">

Vi skal ind i Face Mode, og have valgt bunden af vores flade kasse. Når man arbejder i *Edit Mode* kan man bevæge, rotere og skalere præcis som vi tidligere har gjort i *Object Mode*, men kun for enkelte dele af vores objekt. Det skal vi bruge til at skalere bunden udad, så siderne på vores fod er skrå.

<img src="{{site.baseurl}}/z_assets/foot-side-askew.png" alt="foot-side-askew" style="width:100%">

Nu skal vi op på den anden side af kassen og have valgt toppen af den. Nu skal vi lave noget der hedder et *Inset*, som er et mindre face inde i et andet face. Det gør vi ved at klikke *I* mens vi har valgt en face, og det begynder at lave den anden face. Træk musen lidt mod midten cirka som på billedet, og klik når du er tilfreds med det:

<img src="{{site.baseurl}}/z_assets/inset-example.png" alt="inset-example" style="width:100%">

Nu består toppen af flere faces end før, men nu har vi en ny og mindre face der har (cirka) samme form som den vi havde før. Vi skal nu have valgt den inderste face, og lave et *Extrude* ved at klikke *E*. Det gør, at man kan trække ny geometri ud af hvad man har valgt, og har skal vi bruge det til at lave et lille hul i vores face. Efter at have trykket på *E* kan du bevæge musen for at vælge, hvor du vil lave de nye faces, og herefter venstreklikke for at bekræfte det:

<img src="{{site.baseurl}}/z_assets/extrude-example.png" alt="extrude-example" style="width:100%">

>**Vigtigt omkring Extrude**
>Hvis du får højreklikket mens du laver en Extrude, kan det godt se ud som om der ikke skete noget, men det gør der! Du vil stadig få lavet den nye extrude, men den kommer til at ligge oven i det gamle. Faces der ligger oven i hinanden er altid en dårlig idé i Blender, men der er et nemt fiks for det. Inde i *Edit Mode*, tryk på *A* for at vælge alt, og derefter *M* for at begynde at *Merge* (slå ting sammen). Her skal vi vælge *By Distance*, hvilket gør at alle de vertices, der er meget tæt sammen, bliver lavet om til én enkel vertex. Hvis du mistænker at noget er galt med dit objekt, så prøv dette!

Det eneste der mangler nu, er at flytte kanonkuglerne tilbage på foden, og så har vi et komplet og færdigt objekt! Hvis man gerne vil have at de flytter sig sammen, kan man vælge alle kanonkuglerne med *Shift+Venstreklik*, og til sidst vælge foden, også med *Shift + Venstreklik*. Med alting valgt, kan vi nu trykke *Ctrl + P*, vælge *Object (Keep Transform)*, og så vil alle kanonkuglerne følge med når man flytter på foden. Det smarte er så, at du kan flytte på kanonkuglerne *uden* at flytte på foden!

Det eneste der er ved vores objekt nu, er at den stadig en kedelig, grå farve. Det kan vi gøre noget ved, ved at give den nogle materialer
## Sektion C: Simple materialer

Inden vi overhovedet går i gang med at lave og sætte materialer, bliver vi nødt til at ændre den måde vi ser objekterne i Blender. Lige nu prøver vi det, der hedder *Solid Shading*, hvor objekterne får den samme farve. Her tager Blender ikke højde for hverken materialer eller lys, så det bliver vi nødt til at ændre. Oppe i højre hjørne af 3D Viewport'en finder du de fire muligheder for shading, og så klikker du på den tredje fra venstre: Material Preview

<img src="{{site.baseurl}}/z_assets/material-preview.png" alt="material-preview" style="width:100%">

Nu skulle alting gerne blive hvid frem for grå, og vi er nu klar til at lave nogle materialer. For at gøre det, skal du først vælge et objekt, og bevæge dig hen på Material-tab'en og klikke på New.

<img src="{{site.baseurl}}/z_assets/material-tab.png" alt="material-tab" style="width:100%">

Der er masser af muligheder herinde, men vi behøver kun tre ting for nu: *Base Colour*, *Metallic*, og *Roughness*. Dem kan du lege rundt med, og sætte nogle farver, som du synes passer til din fod og dine kanonkugler!

Du behøver ikke at klikke *New* hver eneste gang du skal sætte et nyt materiale, tværtimod vil du nogle gang bruge det samme materiale for at kunne lave ændringer flere steder på samme tid. Det kan for eksempel være rigtig smart at bruge det samme materiale på kanonkuglerne. Det kan du gøre ved at klikke på knappen ved siden af *New*, som viser en liste af alle de materiale du har lavet. Så vælger du bare den du vil bruge, og så bruger du det samme materiale flere steder!

<img src="{{site.baseurl}}/z_assets/material-selection.png" alt="material-selection" style="width:50%">

Det var alt for denne uge, næste gang kigger vi på at lave et træhjul. Hvis du har nået det hele i løbet af første gang, kan du gå i gang med at finde et billede af et hjul på internettet, og overveje hvordan man kan lave det.