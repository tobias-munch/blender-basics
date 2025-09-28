---
layout: default
title: Afsnit 2:Kanonkugler
order: 2
---
# Afsnit 2 - Kanonkugler
Nu hvor vi har lært at bevæge både kameraet og nogle objekter, skal vi prøve at lave en simpel figur. I forbindelse med at vi laver en kanon senere, er det oplagt at lave en bunke af kanonkugler.

![Kanonkugler!]({{ site.baseurl }}/z_assets/kanonkugler.png)

Det første sted man starter når man skal lave et objekt, er at se hvilke figurer som objektet består af. Her har vi en simpel fod, og en masse kugler, men lad os fokusere på kanonkuglerne, da det kan være kompliceret hvis man ikke ved hvordan man gør det effektivt.

### Sektion A: Shading og Arrays

Det at lave en kugle er ikke svært - Vi kunne se i forrige opgave at man bare kan tilføje en UV Sphere, som er tæt nok på en helt rund kugle. Hvis man gerne have den til at se rund ud, kan man venstreklikke på kuglen, derefter højreklikke på den hvilket giver følgende muligheder, og så vælger man *Shade Smooth*.

![shading muligheder]({{ site.baseurl }}/z_assets/shading-muligheder.png)

> **Object Shading:**
> Man kan også vælge *Shade Auto Smooth* og *Shade Flat*, men de gør nogle andre ting end hvad vi skal bruge nu. Den korte forklaring er, at *Shade Smooth* prøver at gøre ==ALT== smooth, hvorimod *Shade Flat* viser objektet præcis som den er. *Shade Auto Smooth* tager højde for hvor på objektet er der rundt/blødere kanter, og hvor der er fladt, og shader efter det. På billedet nedenunder kan du se hvad de gør på en kasse med nogle blødere kanter
> ![shading explainer]({{site.baseurl}}/z_assets/shading-explainer.png)

Nu har vi en rund kugle, men det vil være irriterende og tage lang tid hvis vi skal placere alle kuglerne i hånden. Der kommer til at være 30 styks hvis vi laver fire lag af kugler! Det behøver vi dog ikke at gøre, da vi kan benytte os af *Modifiers*, som er placeret i en tab ude i højre side med et blåt skruenøgle-ikon.
![modifiers-lokation]({{site.baseurl}}/z_assets/modifiers-location.png)