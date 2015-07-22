---
layout: page
title: CMS - Instellingen
---

Deze pagina verduidelijkt de verschillende opties in het CMS onder het kopje _Instellingen_.

# Website Instellingen

Klik op instellingen in de navigatie. Het eerste kopje op deze pagina zijn de _website instellingen_. Hieronder bevinden zich de volgende instellingen:

- site_name
- site_url
- site_email
- site_shipping
- meta_robots
- default_product_image
- maximum_page_product
- order_number_prefix
- mail_server
- smtp_server
- smtp port
- smtp secure
- smtp_auth
- smtp_username
- smtp_password


## site_name

Dit word gebruikt om de naam van de website op te geven. Deze naam wordt ook boven aan uw hoofdpagina weergegeven.

## site_url

Dit wordt gebruikt om links te genereren en te gebruiken. Bijvoorbeeld bij de details van een product staat een knop “Bekijk op uw website”. Deze knop gebruikt site_url om de URL naar het product te maken.

## site_email

De site_email is de standaard email waar automatische emails vandaan worden verzonden. bijvoorbeeld no-reply@<uwwebsite> of info@<uwwebsite>.

## site_shipping

site_shipping is de waarde die standaard gebruikt word voor de verzendkosten. Bijvoorbeeld de verzendkosten zijn 5.95 dan moet hier 5.95 ingevuld worden. 
Dit bedrag word standaard bij elke bestelling toegevoegd.

## meta_robots

meta_robots zorgen voor de indexering in een zoekmachine. Bijvoorbeeld dat uw website zichtbaar is in google.

## default_product_image

default_product_image is de placeholder voor afbeelding waar nog een afbeelding voor geupload moet worden. 


## maximum_page_product

Hier word het maximum aantal producten weergeven op 1 pagina. Elke rij bestaat uit 5 producten. Bijvoorbeeld 20 producten op een pagina als maximum geeft 4 rijen van 5 producten.

## order_number_prefix

In de database is er een veld “OrderID”, als er standaard een waarde voor de OrderID staat dan moet deze hier in worden gevuld. Om bijvoorbeeld `DC_00001` te krijgen zal er in dit veld `DC_0000` in moeten gevuld worden.

## mail_server 

Hier zijn twee opties beschikbaar:

- Mail van server gebruiken 						
- Eigen smtp server opgeven 

## smtp_server

De SMTP_server verbind met de mail server. Het zou bijvoorbeeld `mail.example.com` kunnen zijn.

- Geef de SMTP server op

## smtp_port
		
Geef de poort van de SMTP server op

## smtp_secure	
			
Hier word aangegeven als de verbinding beveiligd is of onbeveiligd. Er zijn hier 3 opties voor.

- Onbeveiligd, hiermee word aangegeven dat de verbinding naar de server onbeveiligd is.
- SSL, Secure sockets layer. Dit zorgt voor een encryptie op je verbinding en dit is de voorganger van TLS.
- TLS, Transport layer security. Dit zorgt voor een encryptie op je verbinding.
 						
## smtp_auth 

smtp_auth geeft aan dat de mail server wel of geen login gegevens nodig heeft. Hier zijn twee mogelijkheden:

- Ja
	- Als de server vereist om in te loggen, geef dan de username en het wachtwoord op bij smtp_username en smtp_password.

- Nee
	- Als de server niet vereist om in te loggen laat dan de smtp_username en smtp_password leeg.

## smtp_username

Dit is de gebruikersnaam die gebruikt word voor het inloggen op de mail server.

Geef de gebruikersnaam van de SMTP server op.

## smtp_password

Dit is het wachtwoord die gebruikt word voor het inloggen op de mail server

Geef het wachtwoord van de SMTP server op.

# Prijs Instellingen

## price_base

Hier wordt bepaalt hoe de product geprijsd moeten worden. De API geeft 3 verschillende prijzen door:

- `price` de verkoopprijs van dit product op [Inktweb.nl](https://www.inktweb.nl/) inclusief BTW
- `purchase` de inkoopprijs voor dit product, exclusief BTW
- `msrp` de adviesverkoopprijs (_manufacturer's suggested retail price_) exclusief BTW

## Prijs formule

Om de formule te wijzigen klik op de knop “Wijzigen?”. 
Er verschijnen twee velden: Het eerste veld is de _operator_ en het tweede veld is de _waarde_. 

De beschikbare operators zijn `+` `x` `-` deze beïnvloeden de waarde vóór de operator met de waarde na de operator. Het waarde veld beinvloed de waarde na de operator.


### Voorbeeld: Prijs + BTW + € 5
Om de formule `((prijs * 1.21) + 5)` te krijgen:

- Klik op “Wijzigen?”.
- Selecteer “x” als operator .
- Vul bij waarde 1.21 in. (De waarde 1.21 staat gelijk aan 121% dus de prijs incl. BTW)
- Klik op het groene plusje om een extra veld toe te voegen.
- Selecteer “+” als operator.
- Vul bij de waarde 5 in.
- Klik op “Bewerken”.
 
Een product van € 1,- wordt nu € 6,21. Een product van € 10,- wordt nu € 17,10.

# Technische Instellingen

Klik op instellingen in de navigatie. Binnen de instellingen is een kopje “Prijs instellingen” te vinden. 

- api_key
- api_test
- api_debug
- api_restrict
- mollie_api_key
- zipcode_api_key
- zipcode_api_secret

## api_key

De `api_key` word geleverd door Inktweb.nl, hiermee authenticeert Dropcart zich bij de database van Inktweb.nl.

## api_test

Hier word aangegeven als er verbinding gemaakt moet worden met de test server of niet.

De `api_test_ heeft twee opties:

- true
	- Dropcart zal verbinden met de test server van Inktweb.nl. Hier zullen bestellings processen getest kunnen worden en zullen deze niet als bestelling verschijnen bij Inktweb.nl. 

- false
	- Er zal verbinding gemaakt worden met de hoofdserver van Inktweb.nl

## api_debug

Debugging word gebruikt om fouten in de code makkelijk te vinden. Deze functie bevat twee opties. 

- true
	- Boven aan de pagina zal de informatie worden weergegeven met betrekking tot fouten in de code.

- false
	- Standaard instelling
	- De pagina zal worden geladen zoals normaal en de debugger staat uit.

## api_restrict

Geeft bij de API call aan of het assortiment beperkt moet worden. 

- true
	- Standaard instelling
	- De API wordt beperkt tot informatie wat reseller is voor deze `api_key`. Als er bijvoorbeeld extern is ingesteld om een bepaald product niet te tonen wordt deze dankzij deze instelling ook weggelaten uit de API.

- false
	- Alle informatie uit de API zal doorgestuurd worden.

## mollie_api_key

Mollie wordt gebruikt om betalingen af te handelen. De Mollie API key is te verkrijgen via de [website van Mollie](https://www.mollie.com/nl/).

## postcode_api_key

## postcode_api_secret

API credentials verkrijgbaar via [Postcode.nl](https://www.postcode.nl/). Vult automatisch de `straatnaam` en `stad` aan bij het afrekenen aan de hand van `postcode` en `huisnummer`.

# Database backup

Klik op instellingen in de navigatie. Binnen de instellingen is een kopje “Database backup” te vinden.

Hier word een backup gemaakt van de database. Er zal een bestand gedownload worden, dit bestand kan gebruikt worden om uw database te herstellen met de gegevens die op het moment van downloaden er in staan.

# Download bestellingsoverzicht
Hier is een overzicht van de bestellingen te downloaden. Vul een "van" datum in in de format `dd-mm-jjjj`. Bijvoorbeeld `01-01-2015` en een eind datum `01-30-2015`. 
