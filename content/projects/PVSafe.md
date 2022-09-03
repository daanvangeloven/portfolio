+++
author = "Daan van Geloven"
title = "PVSafe Website"
date = "2022-09-01"
description = "Description of the PVSafe website"
tags = [
    "emoji",
]
+++


For PVSafe I have developed 3 coherent systems. These 3 systems together ensure that the PVSafe appointments can be planned and executed quickly and efficiently.
Everything is digitally controlled from start to finish. 

Together with the client we decided to use an open voucher system. Customers buy a voucher code via the website, which can be used later to schedule an appointment. The customer buys a voucher on the website, then the customer makes an appointment through the 'My PVSafe' system. A PVSafe employee then carries out the appointment via the PVSafe Admin Dashboard.

{{<mermaid>}}
graph LR
    A(PVSafe Website) --> B(Mijn PVSafe) --> C(PVsafe Admin Dashboard)

  
{{</mermaid>}}

## PVSafe Website 

[De PVSafe website](https://pvsafe.nl) is made with `wordpress`. I had chosen this because the website itself needed no more than some basic pages with information. Think of a landing page, contact form, 'about us' and a checkout page for the vouchers.

The theme used is Astra in combination with `woocommerce`. WooCommerce takes care of the payments of the vouchers and once payment is comeplete, a webhook is sent to the PVSafe API. This webhook ensures that the vouchers are created in the database and sent to the customer via e-mail.


![PVSafe Homepagina](/images/pvsafe-homepage.PNG)

## Mijn PVSafe
Mijn PVSafe is developer in `ASP.NET Core 6 MVC`.  

![Mijn PVSafe](/images/mijn-pvsafe.png)


### Frontend
The front-end for 'My PVSafe' is completely written in `tailwind-css`. Tailwind is a front-end CSS framework that makes it faster to develop. By using tailwind you don't have to write your own CSS classes. 

The Reason I picked tailwind over competing frameworks is the customizability. Tailwind doesn't have preset components which enables you to make your website look more custom and less cookie-cutter. 

### Authenticatie
De Authenticatie van 'Mijn PVSafe' verloopt via `Auth0`. In de toekomst wil ik hier zelf een eigen systeem voor ontwikkelen maar door tijdgebreken hebben we besloten om het voor nu bij een andere partij neer te leggen. Ik heb hierbij gekozen voor een wachtwoordloze authenticatie methode. Er wordt bij het inloggen een code verstuurd via e-mail. Met deze code kan de gebruiker inloggen op zijn account. Deze methode heeft als voordeel dat gebruikers geen wachtwoord kunnen vergeten en het verlaagt de bounce-rate omdat je als gebruiker geen account hoeft aan te maken.

### Data
De Data van PVSafe wordt opgeslagen in een `MySQL Database`. De communicatie met deze database verloopt via `Entity Framework`. Hierbij had ik gekozen voor een model-first implementatie. De database tabellen worden hierbij gegenereerd vanuit de modellen in het PVSafe ASP.NET Project. Dit zorgt voor perfecte integratie tussen de database en Entity Framework.




