## Motivatie voor project

Lastig is dat om een huis te kopen, toch? En wat als ik zeg dat het veel makkelijker kan?
[Zonder lang te wachten op reacties](https://github.com/truhuis/project-story/blob/main/1.png), en uiteindelijk te horen krijgen dat er weer een [hoger bod](https://github.com/truhuis/project-story/blob/main/2.png) is gedaan, of dat het huis überhaupt [al verkocht](https://github.com/truhuis/project-story/blob/main/3.png) is. Voor veel mensen is dit heel herkenbaar en wij zijn er ons ook heel bewust van.

Daarom komt Truhuis met een innovatieve oplossing die meteen de hele onroerende markt kan op default zetten en nieuwe toekomst vol kansen voor zowel de koper als verkoper kan bieden. De prioriteit ligt voor ons vooral op de veiligheid en transparantie, die wij bereiken door menselijke betrokkenheid zoveel mogelijk te verminderen bij het proces. 
Bovendien vinden wij de tijdbesparing ook heel belangrijk, want het kopen van huis met huidige omstandigheden is gewoon een veel tijd nemende ellende.

Uit door meerdere bronnen gemaakte onderzoek is gebleken dat in Nederland ruim 10% van inwoners de bezitters zijn van cryptovaluta, sterker nog, alleen in het afgelopen jaar is percentage van 6,5% naar 10% gestegen, dus naar 1,75 miljoen gebruikers. Wereldwijd zijn er meer dan 100 miljoen cryptoportemonnee-houders. Ongetwijfeld gaan wij ervanuit dat het percentage met komende jaren verder blijft stijgen, want het wordt steeds gewoonlijker voor iedereen om cryptovaluta te gebruiken, ook in het dagelijkse leven.

Ook snappen wij dat de staat graag actief betrokken wil zijn bij crypto-wereld om min of meer controle en regulering daarover te krijgen.
Truhuis zal positie nemen tussen de burger en de staat zelf, door de rol van erkende kadaster, marketplace en notaris van het onroerende goed over te nemen. 

## Wat is Truhuis

Truhuis is ten eerste het woord dat niet bestond tot vandaag. Dit woord is gevormd door combinatie van eerste drie letters van een Engels woord “true” en een Nederlands woord “huis”.

Truhuis streeft ernaar om de aankoop-, verkoop- en eigendomsmethoden van onroerend goed te verbeteren met behulp van de openbare Ethereum Blockchain (ERC-721) en slimme contracten.

## Wat Truhuis doet

Hier zijn onze kernpunten die voor ons van belang zijn.

### Transparantie en betrouwbaarheid
Alle aankoop-en-verkoop-transacties zijn traceerbaar, dus verifiërend en betrouwbaar. Alle activiteiten worden uitgevoerd dankzij smart-contracten zonder 3de partijen (denk aan banken of notaris) erbij te betrekken.

### Uniekheid 
Uniekheid wordt bereikt dankzij gebruik van NFT. 

### Veiligheid 
Alle transacties worden veilig verwerkt en bewaard op de blockchain. Kadaster-gegevens worden bewaard op de meest beveiligde en gedecentraliseerde manier, dankzij gebruik van IPFS-technologie in combinatie met Filecoin digital storage.

### Gemakkelijkheid
Het kopen van het huis gaat dankzij ons product veel malen sneller en gemakkelijker!
Het is net een webshop met kleren, alleen in plaats van kleren koop jij je droomhuis waarvan jij per direct de eigenaar wordt met alle bevoegdheden.
 
### Innovatief
Wij maken gebruik van Web3-structuur en komen op de markt met een nieuwe ontwikkeling die vrijwel onvoorstelbaar leek te zijn. Ons product maakt het werk van notaris niet meer noodzakelijk bij het kopen van het huis dankzij de smart-contracten.



### Hoe het werkt

Vanaf het begin begrepen wij dat de staat een grote rol zal spelen in dit proces, net zoals burger van de staat. Daarom hebben wij besloten om deze rollen uit te werken in smartcontract. We hebben StateGovernment gecreëerd en toegewezen aan Nederland, terwijl de uitvoerder van smart-contract een crypto-account van de Nederlandse overheid is.

We stelden ons een dergelijke situatie voor dat wanneer, laten we zeggen, een nieuwe burger wordt geregistreerd in het Koninkrjk der Nederlanden (laten we hem Jan noemen), deze staatsoverheid de registerCitizen-functie aanroept waarin een nieuw Citizen smart contract wordt gemaakt, waarin alle Jan's gegevens zoals identiteitsgegevens worden ingevoerd. NLD `StateGovernment` slaat vervolgens het adres van dit `Citizen` slimme contract op in zijn database en koppelt het aan Jan's account. Op deze manier kan Truhuis eenvoudig verifiëren dat Jan daadwerkelijk een vaste verblijfplaats heeft in Nederland en dus (in theorie) vrij onroerend goed kan kopen binnen de staat.
 
### Truhuis Kadaster 

Voordat een onroerend goed op de blockchain kan bestaan, moet het worden uitgegeven als een NFT in het smart-contract van `TruhuisCadastre`. Argumenten worden ingevoerd in de `safeMint`-functie, zoals wie de eigenaar wordt van deze NFT, token URI (real estate metadata) en het land waar dit eigendom zich bevindt. Truhuis Cadastre heeft de locatie nodig om informatie bij `StateGoverment` aan te kunnen vragen over overdrachtsbelasting voor verkoop van het tokenized Real Estate.

### Truhuis Marketplace

Vervolgens heeft de eigenaar die aan deze NFT-ID is toegewezen, het volledige recht om over dit onroerend goed te beschikken zoals hij wil. Hij kan het bijvoorbeeld verkopen. Hiervoor noteert Jan zijn NFT in het slimme contract van `TruhuisMarketplace`. Alvorens het huis te doorzoeken, controleert deze marktplaats of Jan daadwerkelijk de eigenaar is van de NFT en vraagt om enkele authenticatiegegevens via `TruhuisCadastre` en de `StateGovernment` en verifieert Jan. Als de verificatie succesvol is, staat de woning officieel op de lijst.

Als dat huis al een tijdje te koop staat, wordt het gevonden door een geschikte koper (laten we haar Emma noemen). Emma gaat ook door de verificatie, waarbij Truhuis Marketplace ervoor zorgt dat ze het recht heeft om gemakkelijk onroerend goed in Nederland te kopen. Daarna vindt ze het huis van Jan en koopt het, betalend in een ERC-20 stablecoin.

Na de betaling heeft Emma recht op een bedenktijd, die in werkelijkheid 3 dagen is (afhankelijk van de staat). Dit betalingsbedrag wordt bevroren in de Truhuis-kluis. Vervolgens vindt de registratie van een nieuwe Chainlink Keeper plaats, waarbij het Truhuis Marketplace-adres en de token-ID van deze verkochte NFT worden ingevuld. De Chainlink Keeper communiceert vervolgens met de `checkUpkeep`-functie van het contract, die controleert of de bedenktijd (3 dagen) verstreken is sinds de aankoop. Na deze drie dagen roept de Chainlink-keeper de functie `performUpkeep` aan, die het NFT-eigendom van Jan naar Emma stuurt en geld naar Jan stuurt. Zo stelt Truhuis Chainlink Keeper in staat om dit laatste en tegelijkertijd het belangrijkste onderdeel van dit hele proces te automatiseren.

### Real estate metadata

Om de data te bewaren op de meest veilige en gedecentraliseerde manier, gebruiken wij IPFS-technologie in combinatie met Filecoin. We hebben de kadaster-kaart geüpload via Web3Storage en de output van hashwaarde aan de afbeeldingssleutel gekoppeld.
Voordat een NFT wordt aangeslagen, is een URI vereist. Wij krijgen de URI van Pinata, die op zijn beurt de klaargemaakte JSON metadata ontvangt. 

> 2 examples of how the NFT metadata looks like in 2 different countries:

- **Nederland**

```json
{
    "name": "Truhuis Real Estate # 2",
    "description": "Truhuis aims to improve the property buying and selling methods with the help of the public Ethereum Blockchain (ERC-721) and smart contracts.",
    "image": "ipfs://bafybeibjcvb7hxdtcn3yb7vae4p3n54jppahmfe5sndokx4jq6jfyhshs4",
    "attributes": [
        {
            "location": {
                "street_name": "De Monchyplein",
                "street_number": "97",
                "addition": "",
                "postcode": "3072 MM",
                "city": "Rotterdam",
                "state": "South Holland",
                "country": "NLD",
                "coordinates": {
                    "latitude": "51,90589\u00b0 N",
                    "longitude": "4,48945\u00b0 E"
                }
            }
        },
        {
            "house_type": "Apartment"
        }
    ]
}
```
![Cadastre Map Token ID 2](https://github.com/truhuis/project-story/blob/main/cadastre-map-token-id-2.png)

- **VS**

```json
{
    "name": "Truhuis Real Estate # 4",
    "description": "Truhuis aims to improve the property buying and selling methods with the help of the public Ethereum Blockchain (ERC-721) and smart contracts.",
    "image": "ipfs://bafybeicp74n7atomu7gy36h2uhrp5y6p5nxre6lh62qxiw6zbgvsfgka74",
    "attributes": [
        {
            "location": {
                "street_name": "Park Avenue",
                "street_number": "432",
                "addition": "96",
                "postcode": "10022",
                "city": "New York",
                "state": "New York",
                "country": "USA",
                "coordinates": {
                    "latitude": "40,76167\u00b0 N",
                    "longitude": "73,97186\u00b0 W"
                }
            }
        },
        {
            "house_type": "Condo"
        }
    ]
}
```
![Cadastre Map Token ID 4](https://github.com/truhuis/project-story/blob/main/cadastre-map-token-id-4.png)

## Uitdagingen die wij zijn doorlopen 

1.	Terwijl we nadachten over de projectstructuur, kwamen we het probleem van gebruikersverificatie tegen. Dat is waar twee contracten StateGovernment.sol en Citizen.sol significant plaatsvinden. We stelden ons voor dat iedereen in de wereld zijn eigen crypto-portemonnee heeft en dit dient als identificatiebewijs voor elke persoon. De wereld waarin er geen traditionele papieren paspoorten, fysieke plastic rijbewijzen, papieren geboorte- en huwelijksakten, enz. zijn. Deze identificatiemethode vermindert het geval van identiteitsvervalsing, vervalsing van documenten en helpt de hoeveelheid productie en recycling van plastic en papier, en daarmee het kappen van bomen en luchtvervuiling. Maar er is een afweging die hier een grote rol speelt. Als de gebruiker de toegang tot de privésleutel verliest, gaat ook de toegang tot alles weg. Daarom gingen we ervan uit dat de privésleutel in de vorm van [een microchip in het menselijk lichaam](https://www.bbc.com/news/business-61008730) kon worden geïmplanteerd.

2.	Erkenning van de staat en invoering van de rechtskracht van een soortgelijke procedure voor het registreren van onroerend goed, het kopen, verkopen en bezitten ervan.


## Prestaties waar we trots op zijn

We zijn blij dat we de oplossing van gebruikersverificatie hebben bedacht, die op een enigszins futuristische is, maar ook op de lange termijn best haalbaar is. We zijn er trots op dat we een duidelijk begrip hebben van hoe we het hele proces van gebruikersverificatie tot de overdracht van eigendom van NFT Real Estate aan de koper kunnen brengen.

## What’s next for Truhuis

1.	Na de hackathon gaan we verder met het verbeteren van de start-up. Verbeteren van het verificatieproces voor gebruikers en onroerend goed. Implementeer Truhuis Veiling waar gebruikers biedingen kunnen uitbrengen op de meest transparante manier die ooit heeft bestaan in de vastgoedsector.
2.	Feedback verzamelen van de blockend ontwikkelaarsgemeenschap en organisaties die betrokken zijn bij de traditionele vastgoedmarkt over de hele wereld. En op basis daarvan het product geleidelijk verbeteren om het mainnet te bereiken.
3.	Verder samenwerken met Chainlink Keepers en Chainlink Data Feeds implementeren.
4.	User Interface aanmaken en hem koppelen met Moralis.
5.	Verbeter de opslagmethoden voor metadata en nauwer werken samen met IPFS-technologie en Filecoin.
6.	Open staan voor de samenwerking met al bestaande bedrijven in de vastgoedwereld.
7.	Implementeer ontbindende voorwaarden bij het opstellen van de koopovereenkomst.
8.	Introduceer de functie Metaverse zodat een potentiële koper de bezichtiging kan uitvoeren zonder op te staan van de bank.
9.	Integratie van het AAVE-protocol of totstandkoming van een nieuw protocol dat als Hypotheeknemer gaat fungeren en Truhuis NFT-vastgoed als onderpand kan nemen. In dit geval moeten we een gedecentraliseerde taxateur maken die kan worden gebruikt als een Chainlink-orakel. Zo kan de koper het onroerend goed kopen met een hypotheek.

Bedankt!

We willen de jury en workshoppresentatoren bedanken voor de moeite die jullie hebben gedaan voor deze hackathon. Dankzij het bestaan ervan nemen de meeste geweldige ideeën daarna hun weg naar de echte wereld vol mogelijkheden en kansen.

## Follow us
- [Twitter](https://twitter.com/truhuis)
- [GitHub](https://github.com/truhuis)
