# Interactive Functionality

Ontwerp en maak voor een opdrachtgever een interactieve toepassing die voor iedereen toegankelijk is

De instructie vind je in: [INSTRUCTIONS.md](https://github.com/fdnd-task/the-web-is-for-everyone-interactive-functionality/blob/main/docs/INSTRUCTIONS.md)


## Inhoudsopgave

  * [Beschrijving](#beschrijving)
  * [Gebruik](#gebruik)
  * [Kenmerken](#kenmerken)
  * [Installatie](#installatie)
  * [Bronnen](#bronnen)
  * [Licentie](#licentie)

## Beschrijving
Voor Tumi Mundo heb ik een website gemaakt waarbij verhalen kunnen worden bekeken en is de core functie om playlists toe te voegen. Daarnaast kan je ook specifieke verhalen bekijken die zijn geladen uit de Tumi Mundo API en terug gaan naar de hoofd pagina. audio is uitgeschakeld omdat deze niet goed koppelde aan het juiste verhaal.
[Live website](https://the-web-is-for-everyone-interactive-9753.onrender.com/)

## Gebruik
De user story bestaat uit het toevoegen en bekijken van een playlist. Bij het aanmaken van een playlist word de pagina refreshed en verandert de route naar <br>
`https://the-web-is-for-everyone-interactive-9753.onrender.com/playlist/?succes=De%20playlist%20is%20toegevoegd`
deze geeft feedback over dat de interactie gelukt is. _de data van nieuwe playlists laad pas in nadat de website opnieuw gestart is._

https://github.com/user-attachments/assets/84bb08c1-8de9-4510-b4ab-d132e4f68382

## Kenmerken
Ik heb gebruik gemaakt met partials in de view folder, zo heb ik een head.liquid en een story.liquid. deze kan ik direct inladen op een pagina waardoor ik code niet hoef te herhalen en efficient kan hergebruiken.

https://github.com/OFRqq/the-web-is-for-everyone-interactive-functionality/blob/8a318fea725c1587b02e0051edad9b760dd6b440/views/partials/head.liquid#L1-L13

     {% render 'partials/story.liquid', story: story %}
     
https://github.com/OFRqq/the-web-is-for-everyone-interactive-functionality/blob/8a318fea725c1587b02e0051edad9b760dd6b440/views/partials/story.liquid#L1-L10

{% render 'partials/head.liquid', title: 'Tumi Mundo' %}

## Installatie
Voor dit project moet je eerst node.JS installeren, dit kan op nodejs.org.

fork daarna dit project en cloon je het zodat dit lokaal gebruikt kan worden.

daarna voer je in de terminal `npm install` in, om gebruik te maken van de package manager.

vervolgens type je `npm start` om de server te starten.

Maak gebruik van 'control' + 'C' om de server te beëindigen.


## Bronnen

## Licentie

This project is licensed under the terms of the [MIT license](./LICENSE).
