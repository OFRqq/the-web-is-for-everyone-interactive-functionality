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
De user story bestaat uit het toevoegen en bekijken van een playlist. Als ontwerpkeuze heb ik bij het aanmaken van een playlist een verandering in de route gemaakt <br>
`https://the-web-is-for-everyone-interactive-9753.onrender.com/playlist/?succes=De%20playlist%20is%20toegevoegd`.
deze geeft overzichtelijke feedback dat de interactie gelukt is, ook refreshed de pagina en komt de playlist direct erbij. Deze geven duidelijk aan dat de interactie werkelijk wat deed.

https://github.com/user-attachments/assets/84bb08c1-8de9-4510-b4ab-d132e4f68382

## Kenmerken

### control flow
In mijn project heb ik veel gebruik gemaakt van de [control flow liquid template](https://shopify.github.io/liquid/tags/control-flow/). Hiermee kan ik een actie uitvoeren wanneer de data actief is, maar wanneer deze niet gevonden word kan ik een andere actie uitvoeren wat handig is als er bijvoorbeeld iets ontbreekt. 

https://github.com/OFRqq/the-web-is-for-everyone-interactive-functionality/blob/dea2ef25705dc9c19865b92e668542bc8e7dbdbe/views/playlist.liquid#L17-L21
_Als er een image gevonden word laad hij deze in, als deze niet gevonden word geeft hij aan dat er geen image is._

https://github.com/OFRqq/the-web-is-for-everyone-interactive-functionality/blob/dea2ef25705dc9c19865b92e668542bc8e7dbdbe/views/storydetail.liquid#L3-L16

_in dit template worden de detail pagina's van stories ingeladen, als deze niet correct zijn gespeld of niet bestaan word de pagina ingeladen met Story not found_


### partials
Ik heb gebruik gemaakt met partials in de view folder, zo heb ik een head.liquid en een story.liquid. deze kan ik direct inladen op een pagina waardoor ik code niet hoef te herhalen en efficient kan gebruiken.

https://github.com/OFRqq/the-web-is-for-everyone-interactive-functionality/blob/8a318fea725c1587b02e0051edad9b760dd6b440/views/partials/head.liquid#L1-L13

deze render je in een andere liquid file met html via {% render 'partials/story.liquid', story: story %}
     
https://github.com/OFRqq/the-web-is-for-everyone-interactive-functionality/blob/8a318fea725c1587b02e0051edad9b760dd6b440/views/partials/story.liquid#L1-L10

deze render je in een andere liquid file met html via {% render 'partials/head.liquid', title: 'Tumi Mundo' %}

## Installatie
Voor dit project moet je eerst node.JS installeren, dit kan op nodejs.org.

fork daarna dit project en cloon je het zodat dit lokaal gebruikt kan worden.

daarna voer je in de terminal `npm install` in, om gebruik te maken van de package manager.

vervolgens type je `npm start` om de server te starten.

Maak gebruik van 'control' + 'C' om de server te beëindigen.


## Bronnen

## Licentie

This project is licensed under the terms of the [MIT license](./LICENSE).
