+++
author = "Hugo Authors"
title = "Summa College - Passend onderwijs kaartspel"
date = "2020-03-11"
description = "Showcase van het summa college passend onderwijs kaartspel"
tags = [
    "markdown",
    "css",
    "html",
]
categories = [
    "themes",
    "syntax",
]

+++

Voor het Summa college heb ik een bestaand kaartspel gedigitaliseerd. Origineel was dit project een studieproject voor mijn opleiding bij het Summa College maar de opdrachtgevers waren zo enthousiast dat ik uiteindelijk via mijn onderneming een complete realisatie heb ontwikkeld. 

## Het Fysieke Kaartspel
Het kaartspel was origineel ontwikkeld door werknemers van het Summa College. Het doel van het spel is om leerlingen met belemmering te ondersteunen. Het Kaartspel maakt het makkelijk voor de leerlingen om hun belemmeringen te identificiëren en een bijpassende oplossing te vinden. 

Normaal gesproken kost het veel tijd om het kaartspel uit te voeren. Er zijn 3 kaart categoriën: Belemmeringen(Wat is de belemmering), Oplossingen(Hoe los ik deze belemmering op), Uitvoerders(Wie voert deze oplossing uit). In het spel zijn meer dan 50 belemmeringen en oplossingen verwerkt. Het kost dus veel tijd om door alle kaarten heen te gaan. 

{{<mermaid>}}
graph LR
    A(Belemmeringen Identificiëren) --> B(Oplossingen Koppelen) --> C(Uitvoerders Koppelen) --> D(Resultaten Bespreken )

  
{{</mermaid>}}


## Het Digitale Kaartspel
### Stap 1. Authenticatie
![Kaartspel Inlogpagine](/images/kaartspel-login.png)

Het Summa College verkoopt de rechten van het kaartspel ook aan andere instanties. Het moet dus mogelijk zijn voor andere instanties om ook toegang te kunnen krijgen. Om dit te realiseren heb ik een simpel e-mail systeem bedacht. De startpagina van de applicatie heeft een invoerveld voor een school-email. Het e-mail domein is een dropdown veld. Andere scholen kunnen hier hun domein aan toevoegen en op die manier kunnen alleen toegestane domeinen gebruik maken van de applicatie.


### Stap 2. Belemmeringen Identificiëren
![Kaartspel Belemmeringen](/images/belemmeringen.png)

De studenten krijgen elke belemmering een keer te zien. Hierbij kunnen ze aangeven of deze belemmering wel of niet van toepassing is. Mocht een belemmering ongeveer passen maar niet helemaal dan kan de student dit toelichten op dezelfde pagina. 


### Stap 3. Oplossingen Koppelen
![Kaartspel Oplossingen](/images/oplossing-1.PNG)

Nadat de belemmeringen bepaald zijn kunnen de studenten mogelijke oplossingen kopllen. Het kaartspel bevat veel oplossingen en ze zijn niet allemaal van toepassing op elke belemmering. Er ging dus veel tijd verloren aan het bekijken van onnodige kaarten. 

Om dit op te lossen heb ik het systeem lerend gemaakt. Door het analyseren van de gebruikers trainde ik het systeem constant waardoor het steeds sneller en efficiënter was voor de leerlingen om het kaartspel uit te voeren.

Zoals je in bovenstaande foto kan zien worden oplossingen die vaak gebruikt zijn bij een specifieke belemmering bovenaan gezet. Hoe verder je naar beneden gaat hoe minder relevant de oplossingen worden. 

![Kaartspel Oplissingen 2](/images/oplossing-2.PNG)




### Stap 4. Uitvoerders Koppelen 
![Kaartspel Uitvoerders](/images/uitvoerders.PNG)

Als laatste stap worden de uitvoerders aan de oplossingen gekoppeld. Dit gaat op ongeveer dezelfde methode als de oplossingen. De kaarten staan gesorteerd op relevantie en wanneer studenten vaak bepaalde kaarten kiezen komen die steeds hoger te staan. 

### Stap 5. Uitvoer
![Kaartspel Uitvoer](/images/kaartspel-uitvoer.png)

Uiteindelijk worden alle kaarten in een tabel geplaatst. Deze tabel kan de student vervolgens uitprinten. Met de uitgeprinte pagina gaat de student naar zijn studiebegeleider om de resultaten te bespreken. 