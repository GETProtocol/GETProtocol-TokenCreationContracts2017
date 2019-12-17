GET Token
=======

Contract code verified on Etherscan: https://etherscan.io/address/0x8a854288a5976036a725879164ca3e91d30c6a1b#code

GET ICO was finalized in December of 2017:
---------------------
- PreICO:
    - Only whitelisted accounts.
    - limited to a specific amount.
- ICO:
    - different contract from PreICO
    - Only whitelisted acounts
    - 4 different pricing tiers. 

All contracts involved with the ICO have been excluded in this branch as the token is not mintable anymore. 


CONTRACTS
=========

GetToken:
---------
- Tokenmarketnet CrowdsaleToken contract
    - 18 decimals
    - "GET" symbol
    - "Guaranteed Entrance Token" name
- No custom code


Crowdsale.sol
---------
Source: Tokenmarketnet Crowdsale
File:  https://github.com/TokenMarketNet/smart-contracts/tree/master/contracts

ERC20.sol 
---------
Source:  Open Zeppeling
File: openzeppelin-solidity/contracts/token/ERC20/ERC20Basic.sol

MintableToken.sol ERC20
---------
Source: Open Zeppelin
File:  /contracts/token/ERC20/MintableToken.sol

Ownable.sol
---------
Source: Open Zeppelin Ownership 
File: openzeppelin-solidity/contracts/ownership/Ownable.sol

SafeMath.sol
---------
Source: Open Zeppeling Math 
File: openzeppelin-solidity/contracts/math/SafeMath.sol

SafeMathLib.sol
---------
Source: Opn Zeppelin
File:  /AragonOne/zeppelin-solidity/master/contracts/SafeMathLib.sol

StandardToken.sol
---------
Source: Open Zeppeling
File: /aragon/zeppelin-solidity/blob/master/contracts/token/StandardToken.sol

UpgradeableToken.sol
---------
Source: Tokenmarket
File: TokenMarketNet/smart-contracts/tree/master/contracts

UpgradeableAgent.sol
---------
Source: TokenMarketNet
File: TokenMarketNet/smart-contracts/tree/master/contracts


ReleasableToken.sol
---------
Source: Tokenmarketnet
File: /TokenMarketNet/smart-contracts/tree/master/contracts
