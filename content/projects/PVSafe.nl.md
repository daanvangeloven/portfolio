+++
author = "Daan van Geloven"
title = "PVSafe Website"
date = "2022-09-01"
description = "Description of the PVSafe website"
tags = [
    "emoji",
]
+++


Voor PVSafe heb ik 3 samenhangende systemen ontwikkeld. Deze 3 systemen zorgen er samen voor dat de PVSafe afspraken snel en efficiënt kunnen worden ingepland en uitgevoerd. 
Van begin tot eind wordt alles digitaal geregeld. 

Samen met de opdrachtgever hebben we besloten om een open voucher systeem te gebruiken. De klanten kopen via de website een vouchercode en die kan later gebruikt worden om een afspraak in te plannen. De klant koopt op de website een voucher, vervolgens maakt de klant via het 'Mijn PVSafe' systeem een afspraak aan. Een medewerker van PVSafe voert vervolgens via het PVSafe Admin Dashboard de afspraak uit.

{{<mermaid>}}
graph LR
    A(PVSafe Website) --> B(Mijn PVSafe) --> C(PVsafe Admin Dashboard)

  
{{</mermaid>}}

## PVSafe Website 

[De PVSafe website](https://pvsafe.nl) is gemaakt in `wordpress`. Ik had hiervoor gekozen omdat voor de website zelf niet meer nodig was dan wat basispagina's met informatie. Denk hierbij aan een landing pagina, contactformulier, 'over ons' en een winkelpagina voor de vouchers. 

Het gebruikte thema is Astra in combinatie met `woocommerce`. WooCommerce regelt de betalingen van de vouchers en zodra er betaald is wordt er een webhook verstuurt naar de PVSafe API. Deze webhook zorgt ervoor dat de vouchers in de database worden aangemaakt en via een e-mail verstuurd worden naar de klant. 

![PVSafe Homepagina](/images/pvsafe-homepage.PNG)

## Mijn PVSafe
Mijn PVSafe is ontwikkeld in `ASP.NET Core 6 MVC`.  

![Mijn PVSafe](/images/mijn-pvsafe.png)


### Frontend
De front-end voor 'Mijn PVSafe' is compleet geschreven in `tailwind-css`. Tailwind is een front-end css framework dat het sneller maakt om te ontwikkelen. Door het gebruik van tailwind hoef je niet zelf eigen CSS-classes te schrijven. 

De reden dat ik tailwind-css heb gekozen boven concurrerende frameworks, is de aanpasbaarheid. Tailwind heeft geen vooraf ingestelde componenten waardoor een website er meer op maat gemaakt en minder cookie-cutter uit ziet.

### Authenticatie
De Authenticatie van 'Mijn PVSafe' verloopt via `Auth0`. In de toekomst wil ik hier zelf een eigen systeem voor ontwikkelen maar door tijdgebreken hebben we besloten om het voor nu bij een andere partij neer te leggen. Ik heb hierbij gekozen voor een wachtwoordloze authenticatie methode. Er wordt bij het inloggen een code verstuurd via e-mail. Met deze code kan de gebruiker inloggen op zijn account. Deze methode heeft als voordeel dat gebruikers geen wachtwoord kunnen vergeten en het verlaagt de bounce-rate omdat je als gebruiker geen account hoeft aan te maken.

### Data
De Data van PVSafe wordt opgeslagen in een `MySQL Database`. De communicatie met deze database verloopt via `Entity Framework`. Hierbij had ik gekozen voor een model-first implementatie. De database tabellen worden hierbij gegenereerd vanuit de modellen in het PVSafe ASP.NET Project. Dit zorgt voor perfecte integratie tussen de database en Entity Framework.




