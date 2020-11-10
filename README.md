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

`PupperCoin.sol` file creates a standard `ERC20Mintable` token. It uses an ERC20Detailed contract.

`Crowdsale.sol` file takes in the following parameters:
  * rate - rate in TKNbits
  * wallet - sale beneficiary
  * goal - cap of the crowdsale
  * openingTime - is set equal to `now`
  * closingTime - is set equal to `now + 24 weeks`
  
As mentioned previously, this contract inherits from the following OpenZeppelin contracts:
  * `Crowdsale` - takes in rate, wallet, and token as parameters
  * `CappedCrowdsale` - takes in goal as a parameter
  * `TimedCrowdsale` - takes in openingTime and closingTime as parameters
  * `RefundableCrowdsale` - takes in goal as a parameter
  * `MintedCrowdsale`
  
 It is important to note that the `RefundableCrowdsale` constructor is called instead of the `RefundablePostDeliveryCrowdsale`contract because `RefundablePostDeliveryCrowdsale` inherits the `RefundableCrowdsale` constructor.
 
 ## Testing the Crowdsale
 
 1. Connect to a test network such as Kovan or Ropsten
 2. Fund your account using a test faucet
 3. Compile `Crowdsale.sol` and deploy `PupperCoinSaleDeployer` from the contract dropdown menu.
 4. Under deploy, set name to "puppercoin", symbol as "pup", and goal to 300.
 4. Hit Transact and hit confirm on the Metamask popup.
 4. Under Deployed Contracts, copy the value given for token_address
 
