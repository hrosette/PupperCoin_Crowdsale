![image](https://user-images.githubusercontent.com/65314799/98406876-57e5d380-2034-11eb-8a8c-cf7e9aaa28aa.png)

# PupperCoin_Crowdsale

For this project, I created a crowdsale contract using Solidity for the "PupperCoin" token. The goal amount for the crowdsale is 300 Ether and will last 24 weeks.

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
 4. Under deploy, set name to "puppercoin", symbol as "pup", wallet as the address of your Metamask and goal to 300.
 
 ![image](https://user-images.githubusercontent.com/65314799/98741353-1a55b300-2372-11eb-9473-1b346e59d2ed.png)

 4. Hit Transact and hit confirm on the Metamask popup.
 5. Under Deployed Contracts, copy the value given for token_address
 
 ![image](https://user-images.githubusercontent.com/65314799/98741464-512bc900-2372-11eb-8f39-eed4d4e40c31.png)
 
6. Select `PupperCoin` from the contract dropdown menu and paste the token address to At Address field then click the At Address button.
7. Copy the token_sale_address from the `PupperCoinSaleDeployer` deployed contract and switch the contract to `PupperCoinSale` then paste the token_sale_address into the AT Address field and click At Address button.
8. Under Deployed Contracts, expand the PupperCoinSale contract and enter an address from Ganache as the beneficiary under buyTokens.

![image](https://user-images.githubusercontent.com/65314799/98742350-ea0f1400-2373-11eb-87b6-499066e8d046.png)

9. Change to desired value and transact.

 
 
 
