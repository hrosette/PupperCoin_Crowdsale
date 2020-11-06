# PupperCoin_Crowdsale

An ERC20 token is created that will be minted through a Crowdsale contract that can be leveraged from the OpenZeppelin Solidity library.
This crowdsale contract manages the entire process, allowing users to send ETH and get back PUP (PupperCoin).
This contract will mint the tokens automatically and distribute them to buyers in one transaction.
The crowdsale contract inherits from `Crowdsale`, `CappedCrowdsale`, `TimedCrowdsale`, `RefundableCrowdsale`, and `MintedCrowdsale`.
The crowdsale will be conducted on the Kovan testnet in order to get a real-world pre-production test in. 
