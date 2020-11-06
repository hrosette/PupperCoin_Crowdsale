![image](https://user-images.githubusercontent.com/65314799/98406876-57e5d380-2034-11eb-8a8c-cf7e9aaa28aa.png)

# PupperCoin_Crowdsale

## Project Background

A company has decided to crowdsale their PupperCoin token in order to help fund the network development.
This network will be used to track the dog breeding activity across the globe in a decentralized way, and allow humans to track the genetic trail of their pets. The company has already worked with the necessary legal bodies and has the green light on creating a crowdsale open to the public. However, they are required to enable refunds if the crowdsale is successful and the goal is met, and you are only allowed to raise a maximum of 300 Ether. The crowdsale will run for 24 weeks.

Some crowdsale contract features:
* An ERC20 token will be created and be minted through a Crowdsale contract that can be leveraged from the OpenZeppelin Solidity library.
* This crowdsale contract manages the entire process, allowing users to send ETH and get back PUP (PupperCoin).
* This contract will mint the tokens automatically and distribute them to buyers in one transaction.
* The crowdsale contract inherits from `Crowdsale`, `CappedCrowdsale`, `TimedCrowdsale`, `RefundableCrowdsale`, and `MintedCrowdsale`.
* The crowdsale will be conducted on the Kovan testnet in order to get a real-world pre-production test in. 
