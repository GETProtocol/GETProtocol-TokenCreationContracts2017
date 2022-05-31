**Note: In Q4 of 2017 the GET Protocol held a public token generation event (TGE). The contracts in this repo contain the contracts used to price, issue and eventually finalize the GET TGE. On the 28th of December in 2017 all minting and pricing contracts where finalized. This means that all the functions and their abilities are not accessible anymore.**

## About the GET ERC20 Token
In a practical sense this means that that:
- No more GET tokens can be minted by *anybody*, not even a token holder majority.  
- Since there is no admin function in the finalized contract GET ERC20 contract; no entity can pause, revert or interfere with token ownership.
- In conclusion the GET token is completely trustless and new issuance is impossible.


## GENERAL INFO Repository
============

This repo contains the contracts that are going to be used in the GET ICO. The Ico consists of a public presale phase starting on 25th of October and a sale phase starting on 15th of November. Both phases are whitelist only. The contract addresses will be revealed by GUTS through a customized version of the GUTS Tickets application. Presale and sale are handled by different contracts, so that we can assure that we can reveal the crowdsale address when it starts and be able to lock the token price at a closer date to the crowdsale start.

### Presale phase 25/10
-------------------

Presale uses the contracts GetPreCrowdsale, GetPrePricingStrategy and GetPreFinalizeAgent, following the TokenMarketNet structure for Crowdsales. Pricing is a flat price per coin. Presale has a total maximum cap and a maximum cap per user, which is applied by the GetWhitelist contract. When Presale is finalized, the variables holding the tokens sold and the wei raised are moved to the sale contract, so sale needs to be deployed before presale is finalized.

### Sale phase 15/11
----------------

Sale uses the contracts GetCrowdsale, GetPricingStrategy and GetFinalizeAgent, following the TokenMarketNet structure for Crowdsales. Pricing consists of four flat prices per coin (tiers) chosen depending on the amount of wei invested already in the sale.  Sale has a total maximum cap and a maximum cap per user per tier, which is applied by the GetWhitelist contract. It also has a minimum funding goal, which will cause the contract to move to Refunding mode if it is not reached. When sale is finalized, tokens are minted to User Growth Multisig, Stability Fund Multisig and the Bounty Fund Multisig.

### INSTALLATION - TESTING
======================

1. Install truffle https://github.com/trufflesuite/truffle
2. yarn
3. npm install -g ethereumjs-testrpc
3. truffle compile
4. start testrpc 
`./start_testrpc`

5. migrate
`truffle migrate --network=testrpc`

6. run tests (you need node v8.6.0 for that - or a version that supports async-await)
`truffle test --network=testrpc`
Note: after running tests you need to restart testrpc or migrate again, because we change the time of testrpc, so next runs will fail.

7. structure
 - In token_market_net/ -- only token_market_net contracts.
 - In node_modules/zeppelin-solidity/contracts -- OpenZeppelin contracts.
 - in util/ -- test helpers and some parity helpers (to update address_book.json). 
 - The Get.... contracts are the GET ico contracts

Note that in truffle.js network_id 42 is mandatory for kovan.
