# TowerDefenseTemplate
Dit is een template wat door jullie te gebruiken is voor het juist inleveren van alle producten voor de Towerdefense beroepsopdracht. **Verwijder uiteindelijk de template teksten!**

Je moet ervoor zorgen dat de enemies niet jouw geld pot aanraken, dit doe je door magische "Totems" te kopen. Je krijgt bij elke Bullet een paar coins, dit is per bullet/toren verschillend.


![Schermafbeelding 2024-10-23 004143](https://github.com/user-attachments/assets/62832e39-d562-4fa3-8c15-a8a4e9c536e9)
![Schermafbeelding 2024-10-23 004213](https://github.com/user-attachments/assets/ecc036ae-2f6a-49bb-9a44-2d6c0a0ac417)
![Schermafbeelding 2024-10-23 004226](https://github.com/user-attachments/assets/2b9d5371-3d26-4baf-af3e-ede4ae53a246)





## Product 1: "DRY SRP Scripts op GitHub"

DRY Script ->

https://github.com/JoyceMolenaar0/TowerDefenseTemplate/blob/GameBranch/TowerDefence/Assets/Scripts/Towers/TowerEnabler/BuyTowers.cs
Ik heb het idee dat dit script voldoet aan de DRY eis, omdat ik hier gebruik maak van arrays. Ik kon makkelijk tientallen [SerializeField] neerzetten, maar ik heb arrays gebruikt om dit te voorkomen.

SRP ->

https://github.com/JoyceMolenaar0/TowerDefenseTemplate/blob/GameBranch/TowerDefence/Assets/Scripts/Enemy/Health/DieEnemy.cs
Ik denk dat deze link aan de eis SRP voldoet, omdat dit geen andere scripts nodig heeft om te 'runnen'




## Product 2: "Projectmappen op GitHub"

Je commit de mappenstructuur van je unity project op github en verwijst vanuit je readme naar de root map van je project. Met een netjes en goed gestructureerde mappenstructuur en benamingen van files toon je aan dat je dit leerdoel beheerst. 

Helaas heb ik zelf geen idee hoe ik dit moet doen, dus heb ik hier de link
https://github.com/JoyceMolenaar0/TowerDefenseTemplate/tree/GameBranch/TowerDefence/Assets

Zorg dat deze verwijst naar je Develop branch.

## Product 3: Build op Github

Mijn (nieuwste) build is helaas te groot voor github, maar ik heb nog wel een oude build die ik hier laat zien
https://github.com/JoyceMolenaar0/TowerDefenseTemplate/releases


## Product 4: Game met Sprites(animations) en Textures 

De build van je game bevat textures, sprites en sprite animations(bijv particles) die op de juiste manier zijn gebruikt en zorgen voor een goede afwerking van je game.  

Plaats in je readme een animated gif van je gameplay (+- 10 sec.) waarin de implementatie van je textures en sprites goed te zien is.

![Textures Sprites](readmeVisuals/texturesSprites.gif)

## Product 5: Issues met debug screenshots op GitHub 

Zodra je bugs tegenkomt maak je een issue aan op github. In de issue omschrijf je het probleem en je gaat proberen via breakpoints te achterhalen wat het probleem is. Je maakt screenshot(s) van het debuggen op het moment dat je via de debugger console ziet wat er mis is. Deze screenshots met daarbij uitleg over het probleem en de bijhorende oplossing post je in het bijhorende github issue. 
[Hier de link naar mijn issues](https://github.com/erwinhenraat/TowerDefenseTemplate/issues/)

## Product 6: Game design met onderbouwing 

Je gebruikt een game design tool om je game design vast te leggen en te communiceren. Daarnaast onderbouw je de design keuzes ten aanzien van “playability” en “replayability” voor je game schriftelijk. 

Voorbeeld van een one page design:
![](https://external-preview.redd.it/48mnMpA0TbiihGo4HsJiWrJhK72xeTRwV2o70_AKilw.jpg?auto=webp&s=3a1ae18f0e4fba7a465643987cbe9cf409466e53)

Omschrijf per mechanic welke game design keuzes je hebt gemaakt en waarom je dit hebt gedaan.

*  **Je game bevat torens die kunnen mikken en schieten op een bewegend doel.** 

*Mijn torens hebben ook nog een f.o.v waardoor je pas gaan mikken als enemies in de buurt zijn. ook hebben mijn torens geen 360 graden view maar 90 graden waardoor het een extra uitdaging is voor de speler om de torens ook op de meest tactische manier te roteren.*

*  **Je game bevat vernietigbare vijanden die 1 of meerderen paden kunnen volgen.**  

*Mijn enemies bevatten 3 types: 
1 snelle die ook snel dood gaat. echter als er veel snelle enemies zijn is de kans steeds groter dat ze bij hun doel komen omdat de torens maar 1 enemy tegelijk kan targetten. Het forceert de speler dus om veel goedkope torens te plaatsen.
Ook is er een langzame gepantserde enemy. Deze kan eigenlijk alleen maar worden vernietigd door magische torens die zijn geupgrade. goedkope torens doen bijna geen schade. De speler moet dus een balans gaan zoeken tussen veel goedkope torens en upgraden van torens.
Tot slot is er een vijand die andere enemies healt dit zorgt ervoor dat de speler een extra nadeel heeft en de torens handmatig de deze healer moet laten targetten hierdoor wordt de speler gedwongen om actiever de game te spelen omdat anders geen enkele enemy meer dood gaat.*

*  **Je game bevat een “wave” systeem waarmee er onder bepaalde voorwaarden (tijd/vijanden op) nieuwe waves met vijanden het veld in komen.**

*Onderbouwing hier...*

*  **Een “health” systeem waarmee je levens kunt verliezen als vijanden hun doel bereiken en zodoende het spel kunt verliezen.** 

*Onderbouwing hier...*

*  **Een “resource” systeem waarmee je resources kunt verdienen waarmee je torens kunt kopen en .evt upgraden.**

*Onderbouwing hier...*

*  **Een “upgrade” systeem om je torens te verbeteren.**

*Onderbouwing hier...*

*  **Een “movement prediction” systeem waarmee je kan berekenen waar een toren heen moeten schieten om een bewegend object te kunnen raken. (Moeilijk)**

*Onderbouwing hier...*

## Product 7: Class Diagram voor volledige codebase 

Je brengt je volledige codebase in kaart met behulp van een class diagram. Binnen de classes hoeven geen private members te worden weergegeven. Wel alle public members (fields en methods). Ook geef je indien relevant de relaties tussen je classes weer. Je class diagram plaats je in je readme op github. Evt mag je dit doen m.b.v de [“Mermaid”](https://mermaid.js.org/syntax/classDiagram.html) tool.


```mermaid
---
title: Animal example
---
classDiagram
    note "From Duck till Zebra"
    Animal <|-- Duck
    note for Duck "can fly\ncan swim\ncan dive\ncan help in debugging"
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
        +String beakColor
        +swim()
        +quack()
    }
    class Fish{
        -int sizeInFeet
        -canEat()
    }
    class Zebra{
        +bool is_wild
        +run()
    }

```

## Product 8: Prototype test video
Je hebt een werkend prototype gemaakt om een idee te testen. Omschrijf if je readme wat het idee van de mechanics is geweest wat je wilde testen en laat een korte video van de gameplay test zien. 

[![example test video](https://ucarecdn.com/dbdc3ad0-f375-40ad-8987-9e6451b28b50/)](https://www.youtube.com/watch?v=CzzRML1swF0)

## Product 9: SCRUM planning inschatting 

Je maakt een SCRUM planning en geeft daarbij een inschatting aan elke userstory d.m.v storypoints / zelf te bepalen eenheden. (bijv. Storypoints, Sizes of tijd) aan het begin van een nieuwe sprint update je deze inschatting per userstory. 

Plaats in de readme een link naar je trello en **zorg ervoor dat je deze openbaar maakt**

[Link naar de openbare trello](https://trello.com/b/w60wkKSU/examen-paraphrenia)

## Product 10: Gitflow conventions

Je hebt voor je eigen project in je readme gitflow conventies opgesteld en je hier ook aantoonbaar aan gehouden. 

De gitflow conventions gaan uit van een extra branch Develop naast de "Master"/"Main". Op de main worden alleen stabiele releases gezet.

Verder worden features op een daarvoor bedoelde feature banch ontwikkeld. Ook kun je gebruik maken van een hotfix brancg vanaf develop.

Leg hier uit welke branches jij gaat gebruiken en wat voor namen je hier aan gaat meegeven. Hoe vaak ga je comitten en wat voor commit messages wil je geven?

Meer info over het gebruiken van gitflow [hier](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)

