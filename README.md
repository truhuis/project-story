## Inspiration
It's hard to buy a house, isn't it? And what if I say it could be much easier? Without waiting [long for the reactions](https://github.com/truhuis/project-story/blob/main/1.png) of the selling party, and finally being told that a [higher offer has been made](https://github.com/truhuis/project-story/blob/main/2.png), or that the house has [already been sold at all](https://github.com/truhuis/project-story/blob/main/3.png). For many people this is very recognizable and we are also very aware of it. That is why Truhuis has come up with an innovative solution that can immediately set the entire real estate market to default and offer a new future full of opportunities for both buyer and seller. The priority for us is mainly on safety and transparency, which we achieve by reducing human involvement in the process as much as possible. Moreover, we also find the time savings very important, because buying a house with current circumstances is just a lot of time-consuming misery.

Research made by several sources has shown that more than 10% of residents in the Netherlands own cryptocurrencies, in fact, only in the past year the percentage has increased from 6.5% to 10%, so to **1.75 million users**. There are more than **100 million crypto wallet holders** worldwide. Undoubtedly, we assume that the percentage will continue to rise in the coming years, as it is becoming more and more common for everyone to use cryptocurrencies, including in everyday life.

We also understand that the state would like to be actively involved in the crypto industry in order to gain more or less control and regulation over it. Truhuis will take a position between the citizen and the state itself, by taking over the role of recognized _land registry (and Cadastre)_, _marketplace_, and _notary_ of the real estate.


## What is Truhuis
**Truhuis** is primarily a word that did not exist until today. This word is formed from the combination of the first three letters of the English word _“true”_ and the Dutch word _“huis”_ - meaning “house” in English and is pronounced almost the same. 

> Truhuis aims to improve Real Estate buying and selling methods using the public Ethereum Blockchain (ERC-721) and smart contracts.


## What Truhuis does
Here are our key points that matter to us:

### Transparency and reliability
		
All purchase and sale transactions are traceable, so verifiable and reliable. All activities are carried out thanks to smart contracts without involving 3rd parties (such as banks or notaries).

### Uniqueness

Uniqueness of each property is achieved thanks to the use of NFT.

### Safety

All transactions are securely processed and stored on the blockchain. Cadastral data is stored in the most secure and decentralized way, thanks to the use of IPFS technology in combination with Filecoin digital storage.
	
### Ease 

Buying the house is much faster and easier thanks to our product! The convenience should be achieved just like visiting a webshop with clothes, only instead of clothes you buy your dream house of which you immediately become the owner with all powers.

### Innovation 

We take advantage of Web3 idea and come to market with a new development that seemed almost unimaginable. Our product makes the work of a notary no longer necessary when buying the house thanks to the smart contracts. 


## How it works
From the very beginning, we understood that the state would play an inseparable role in this process, just like the citizen of the state. Therefore, we decided to turn these roles into smart contracts. We have created `StateGovernment` and assigned it to the USA, whereas the deployer of that smart contract is USA government crypto account.

We imagined such a situation that when, say, a new citizen is beeing registered in the United States (let's call him John), then this `StateGovernment` calls the `registerCitizen` function in which a new `Citizen` smart contract is created, wherein all John's data such as identity information is entered. USA `StateGovernment` then stores the address of this `Citizen` smart contract in its database and links it to John's account. In this way, Truhuis can easily verify that John actually has a permanent residence in the US and therefore can (in theory) freely buy real estate within the USA.

### Truhuis Cadastre

Before a real estate can exist on the blockchain, it must be issued as an NFT in the `TruhuisCadastre` smart contract. Arguments are entered into the `safeMint` function, such as who is gonna be the owner of this NFT, token URI (real estate metadata) and the country where this property is located. Truhuis Cadastre needs to know the location in order to request `StateGovernment` for information about the Transfer Tax amounts when selling this tokenized Real Estate.

### Truhuis Marketplace

Then, the owner who was assigned to this NFT ID has the full right to dispose of this Real Estate as he wants. For example, he can sell it. To do this, John lists his NFT in the `TruhuisMarketplace` smart contract. Before allowing the house to be browsed, this marketplace checks if John is actually the owner of the NFT and requests some autentication data through Truhuis Cadastre and State Government and verifies John. If the verification is successful, then the house is officially listed.

When that house has stood for sale for some time, it is found by a suitable buyer (let's call Emma). Emma also goes through verification, where Truhuis Marketplace makes sure that she has the right to freely buy real estate in the United States. After that, she finds John's house and buys it, paying in an ERC-20 stablecoin.

After the payment, Emma is entitled to a cooling-off period, which in a real case is 3 days (depending on the state). This payment amount is frozen in the Truhuis vault. Then the registration of a new Chainlink Keeper takes place, where the Truhuis Marketplace address and the token ID of this sold NFT are entered. The Chainlink Keeper then talks to the contract's `checkUpkeep` function, which verifies whether the cooling-off period (3 days) have passed since the purchase. After these three days, the Chainlink keeper calls the `performUpkeep` function, which sends the NFT ownership from John to Emma and sends money to John. Thus, Truhuis allows Chainlink Keeper to automate this last and at the same time the most important piece in this whole process.

### Real estate metadata
To store cadastral data in the most secure and decentralized way, we use IPFS technology in combination with Filecoin. We uploaded the Cadastre map via Web3Storage and attached the output hash value to the image key. Before minting an NFT, a full token URI is needed. We receive this token URI from Pinata, which in turn receives a ready-made JSON metadata.

> 2 examples of how the NFT metadata looks like in 2 different countries:

- **the Netherlands**

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

- **the USA**

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


## Challenges we ran into
1. While thinking about the project structure, we encountered the issue of user verification. That's where two contracts StateGovernment.sol and Citizen.sol are taking significant place. We imagined that everyone in the world has their own crypto wallet and this serves as an identification proof for each person. The world wherein there are no traditional paper passports, physical plastic driver's licenses, paper birth certificates and marriage certificates, etc. This method of identification reduces the case of identity spoofing, falsification of documents and it helps to reduce the amount of production and recycling of plastic and paper, and hence the cutting down of trees and air pollution.
But there is a trade off that plays a big role here. If the user loses access to the Private Key, then access to everything is also lost. Therefore, we assumed that the private key could be implanted in the form of a [microchip into the human body](https://www.bbc.com/news/business-61008730).

2. Recognition of the state and introduce the legal force of a similar procedure for registering real estate, buying, selling and owning it.


## Accomplishments that we're proud of
We are glad that we have reached the solution of user verification, albeit in a slightly futuristic way, but quite feasible in the long term. We are proud that we have a clear understanding of how to bring the entire process from user verification to the transfer of NFT Real Estate ownership to the buyer.


## What's next for Truhuis
1. After the hackathon, we will continue to improve the start-up. Improve user and real estate verification process. Implement Truhuis Auction where users can make bids in the most transparent manner ever existed before in the Real Estate industry.
2. Collect feed back from the blockend dev community and organizations involved in the traditional Real Estate market around the globe. And based on this, gradually improve the product in order to enter the mainnet.
3. Further cooperate with Chainlink Keepers and implement Chainlink Data Feeds.
4. Release UI and website working with Moralis.
5. Improve metadata storage methods and work more closely with IPFS technology and Filecoin.
6. Be open to cooperation with already existing companies in the world of real estate.
7. Implement resolutive conditions during the drafting of the purchase agreement.
8. Introduce Metaverse feature so that a potential buyer can perform the viewing without getting up from the coach.
9. Integration of the AAVE protocol or creation of a new protocol that will act as a Mortgagee, which will be able to take Truhuis NFT real estate as collateral. In this case, we will need to create a decentralized Appraiser that can be operated as a Chainlink oracle. Thus, the buyer will be able to buy the property with a mortgage.


## Thanks!
We would like to thank the jury and workshop presenters for the effort you have put in for this hackathon. Thanks to its existence, most great ideas after that take their path to the real world full of possibilities and opportunities.


## Follow us
- [Twitter](https://twitter.com/truhuis)
- [GitHub](https://github.com/truhuis)
