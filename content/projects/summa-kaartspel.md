+++
author = "Hugo Authors"
title = "Summa College - Fitting Education Cardgame"
date = "2020-03-11"
description = "Showcase of the Summa College Fitting Education Cardgame"
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

For the Summa college I digitized an existing card game. Originally, this project was a study project for my education at Summa College, but the clients were so enthusiastic that I eventually developed a complete realization through my company.

## The Physical Cardgame
The card game was originally developed by employees of Summa College. The aim of the game is to support students with learning troubles. The Card Game makes it easy for students to identify their obstacles and find a suitable solution.

Normally it takes a lot of time to run the deck. There are 3 card categories: Impediments(What is the impediment), Solutions(How do I solve this impediment), Executors(Who is implementing this solution). More than 50 Impediments and solutions are incorporated in the game. So it takes a lot of time to go through all the cards.

{{<mermaid>}}
graph LR
    A(Identify Impediments) --> B(Couple Solutions) --> C(Couple Executors) --> D(Discuss Results)

  
{{</mermaid>}}


## The Digital Cardgame
### Step 1. Authentication
![Kaartspel Inlogpagine](/images/kaartspel-login.png)

The Summa College also sells the rights of the card game to other agencies. It must therefore be possible for other agencies to gain access as well. To realize this I have devised a simple e-mail system. The home page of the application has an input field for a school email. The email domain is a dropdown field. Other schools can add their domain to this and that way only allowed domains can use the application.


### Step 2. Identify Impediments
![Kaartspel Belemmeringen](/images/belemmeringen.png)

The students get to see each impediment once. They can indicate whether or not this impediment applies. If an impediment roughly fits but not quite, the student can explain this on the same page.


### Step 3. Couple Solutions
![Kaartspel Oplossingen](/images/oplossing-1.PNG)

After the impediments have been determined, the students can identify possible solutions. The card game contains many solutions and not all of them apply to every impediment. So a lot of time was lost looking at unnecessary cards.

To solve this, I made the system learning. By analyzing the users, I constantly trained the system, making it faster and more efficient for the students to perform the card game.

As you can see in the photo above, solutions that are often used for a specific obstacle are placed at the top. The further down you go, the less relevant the solutions become.

![Kaartspel Oplissingen 2](/images/oplossing-2.PNG)




### Step 4. Couple Executors
![Kaartspel Uitvoerders](/images/uitvoerders.PNG)

As a final step, the executors are linked to the solutions. This is a similiar method as the solutions. The cards are sorted by relevance and when students often choose certain cards, they will be placed higher and higher.

### Step 5. Results
![Kaartspel Uitvoer](/images/kaartspel-uitvoer.png)

Finally, all cards are placed in a table. The student can then print this table. With the printed page, the student goes to his tutor to discuss the results.