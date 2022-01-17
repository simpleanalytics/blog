---
title: Wordt Google Analytics straks verboden in de EU?
author_slug: iron
author: Iron Brands
excerpt: "Op 13 januari heeft de Autoriteit Persoonsgegevens (AP) openlijk vraagtekens gezet bij het legale gebruik van Google Analytics in Nederland. In haar verklaring impliceerde het AP dat het gebruik van Google Analytics in de toekomst verboden kan worden. In dit artikel gaan we hier dieper op in."
image: https://assets.simpleanalytics.com/images/blog/why-simple-analytics-is-a-great-alternative-to-google-analytics/ga-vs-sa.png
lang: nl
---

Op 13 januari heeft de Autoriteit Persoonsgegevens (AP) [openlijk vraagtekens gezet bij het legale gebruik van Google Analytics](https://autoriteitpersoonsgegevens.nl/nl/onderwerpen/internet-telefoon-tv-en-post/cookies#hoe-kan-ik-bij-google-analytics-de-privacy-van-mijn-websitebezoekers-beschermen-4898) in Nederland. In haar verklaring impliceert het AP dat het gebruik van Google Analytics in de toekomst verboden kan worden.

Dit komt nadat de DSB (de Oostenrijkse equivalent van het AP) na uitvoerig onderzoek inderdaad [bevestigde dat het gebruik van Google Analytics in strijd is met de GDPR regelgeving. ](https://noyb.eu/en/austrian-dsb-eu-us-data-transfers-google-analytics-illegal)

We zijn er wat dieper ingedoken om te zien wat er nu echt aan de hand is.

Let's explore!

{% include gif.html slug="going-on-a-adventure" alt="Going on a adventure" width="400px" %}

1.  [Aanklacht](#1-aanklacht)
2.  [Uitspraak](#2-uitspraak)
3.  [Reactie van Google](#3-reactie-van-google)
4.  [Implicaties](#4-implicaties)

## 1. Aanklacht

Op 14 augustus 2020 heeft een persoon (de 'data subject') een website bezocht over gezondheidsonderwerpen, terwijl de 'data subject' was ingelogd met zijn/haar persoonlijke inloggegevens. De website in kwestie maakte gebruik van [Google Analytics](https://analytics.google.com/analytics/web/) om de bezoekers van hun website te volgen en te controleren.

Een paar dagen later, op 18 augustus 2020, diende [NOYB](https://noyb.eu/en) (een NGO voor digitale rechten) namens de 'data subject' een klacht in bij het DSB. De klacht werd ingediend tegen zowel de website in kwestie als Google, als eigenaar van Google Analytics.

In de klacht werd aangevoerd dat het versturen van gegevens aan Google in strijd is met de GDPR-regelgeving, aangezien Google als een "aanbieder van elektronische communicatiediensten" kan worden aangemerkt. Dit betekent dat Google kan worden opgedragen om persoonsgegevens over EU-burgers aan Amerikaanse inlichtingendiensten te verstrekken. Dit betekent dat persoonsgegevens van EU-burgers onvoldoende beschermd zijn tegen Amerikaanse overheidsinstanties en dus in strijd zijn met de GDPR regels.

Dit is het kritieke punt in de aanklacht. Om het ronduit te zeggen: Het gaat niet hierin niet zozeer om het gebruik van Google Analytics door de website in kwestie, het gaat om de overdracht van uw persoonsgegevens aan Amerikaanse providers.

## 2. Uitspraak

Het is de eerste klacht die resulteert in een beslissing met betrekking tot de zogenaamde ["Schrems II"](https://iapp.org/news/a/the-schrems-ii-decision-eu-us-data-transfers-in-question/), die verwijst naar de uitspraak dat het overdragen van gegevens aan Amerikaanse providers in strijd is met de GDPR regelgeving. Deze uitspraak is sinds juli 2020 van kracht, maar werd tot nu toe door gegevensverwerkers genegeerd.

De klacht die NOYB namens de 'data subject' heeft ingediend, omvatte meerdere stukken die beide partijen in de loop van 1,5 jaar hebben ingediend. Google betoogde dat zelfs als er een verstrekking van gegevens had plaatsgevonden, de gegevens niet als persoonsgegevens konden worden aangemerkt omdat ze op geen enkele manier konden worden toegewezen aan de 'data subject'. Bovendien voerden zij aan dat er rekening gehouden moest worden met een "risk-based approach", aangezien het risico dat de gegevens daadwerkelijk zouden moeten worden doorgegeven aan de Amerikaanse overheid zeer gering was.

Het [DSB](https://www.data-protection-authority.gv.at/) oordeelde anders en zag af van de meeste door Google aangevoerde argumenten.

Google kan worden aangemerkt als een "aanbieder van elektronische communicatiediensten" en kan worden gelast persoonsgegevens bekend te maken. Het niveau van bescherming van persoonsgegevens wordt daarom ontoereikend geacht. Aanvullende maatregelen die Google heeft genomen, werden ook ontoereikend geacht. Zij konden geenszins voorkomen dat persoonsgegevens aan de Amerikaanse inlichtingendiensten werden verstrekt.

## 3. Reactie van Google

Russell Ketchum, head of productmanagement van Google Analytics, [reageerde namens Google](https://blog.google/around-the-globe/google-europe/google-analytics-facts/). Hij verklaarde dat "Google Analytics consumenten helpt met de naleving van de wetgeving door hen een reeks controles en hulpmiddelen te bieden". Hij gaf aan dat IP-adressen kunnen worden geanonimiseerd en dat het verzamelen van gegevens kan worden uitgeschakeld en verwijderd (op verzoek).

Ik denk dat hij hier de plank volledig misslaat. In zijn reactie spreekt hij vooral vanuit het standpunt van de website-eigenaar. Hij stelt dat organisaties controle hebben over de gegevens die zij verzamelen.

Het gaat echter niet om website-eigenaren, het gaat om website bezoekers. Hun gegevens moeten worden beschermd en daar is de GDPR voor bedoeld.

Het punt is de overdracht van gegevens aan Amerikaanse providers, die onder toezicht staan van de Amerikaanse overheid, zoals Google. Hij gaat hier slechts in één zin op in en stelt dat voordat gegevens worden doorgegeven aan servers in de VS, IP-adressen worden geanonimiseerd.

Dit is nog steeds in strijd met de [GDPR-regelgeving](https://lawspeed.com/gdpr-transfers-of-data-to-the-united-states/). Het DSB oordeelde dat zelfs geanonimiseerde IP-adressen persoonsgegevens zijn, omdat ze gecombineerd kunnen worden met andere digitale gegevens, om een bezoeker te identificeren. Dit is ook waar de meeste privacy-vriendelijke alternatieven voor Google Analytics, de mist in gaan. Bij Simple Analytics hebben we de belofte gemaakt om nooit, maar dan ook [nooit IP adressen op te slaan](https://docs.simpleanalytics.com/what-we-collect). Zelfs niet op een geanonimiseerde manier, zoals veel van onze concurrenten wel doen.

## 4. Implicaties

Bottom line: Dit is een goede beslissing, maar geen nieuwe. Het is een bevestiging van wat in juli 2020 is beslist, maar nu lijkt het meer impact te hebben. Persoonlijk heb ik het gevoel dat de wet nu wel zal worden gehandhaafd.

Als we geloven dat dit het geval is, verwacht ik dat meer EU-lidstaten het Oostenrijkse voorbeeld zullen volgen. De NOYB heeft in totaal 101 klachten ingediend in meer EU-lidstaten en spreekt van een "gecoördineerde reactie". Nederland is na Oostenrijk de eerste die openlijk vraagtekens zet bij het legale gebruik van Google Analytics.

Er zijn twee oplossingen, zoals Max Schrems (erelid van NOYB) opmerkte. Ofwel moeten Amerikaanse aanbieders buitenlandse gegevens buiten de VS hosten, ofwel moet de VS gaan voldoen aan de juiste regelgeving inzake gegevensbescherming.

Als we er niet in slagen een van de bovengenoemde oplossingen te implementeren, zullen we in de toekomst andere producten aan de beide kanten van de oceaan gaan gebruiken.

Hoe dan ook, dit biedt anderen de kans om te concurreren met Google en 'Big Tech' als geheel.

Wij bij [Simple Analytics](https://simpleanalytics.com/) hebben een privacy-first alternatief voor Google Analytics gebouwd. Onze missie is om organisaties te laten zien dat web analytics anders kan door accurate inzichten te bieden en tegelijkertijd GDPR compliant te zijn, out-of-the-box. Je hoeft je ook geen zorgen te maken over het verstrekken van data aan Amerikaanse servers, [aangezien onze servers in Nederland staan](https://docs.simpleanalytics.com/locations). Probeer het zelf uit en [geef ons een kans](https://simpleanalytics.com/welcome).

Cheers,

Adriaan & Iron

<img
  loading="lazy"
  class="avatar"
  src="https://assets.simpleanalytics.com/images/people/adriaan.jpg"
  referrerpolicy="no-referrer"
  alt="Adriaan van Rossum"
/><img
  loading="lazy"
  class="avatar"
  src="https://assets.simpleanalytics.com/images/people/iron.jpg"
  referrerpolicy="no-referrer"
  alt="Iron Brands"
/>
