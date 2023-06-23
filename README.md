
# GFX contest details

- Join [Sherlock Discord](https://discord.gg/MABEWyASkp)
- Submit findings using the issue page in your private contest repo (label issues as med or high)
- [Read for more details](https://docs.sherlock.xyz/audits/watsons)

# Q&A

### Q: On what chains are the smart contracts going to be deployed?
mainnet, arbitrum, optimism, polygon


___

### Q: Which ERC20 tokens do you expect will interact with the smart contracts? 
Any ERC20 tokens which trade on univ3
___

### Q: Which ERC721 tokens do you expect will interact with the smart contracts? 
UNI-V3
___

### Q: Which ERC777 tokens do you expect will interact with the smart contracts? 
none
___

### Q: Are there any FEE-ON-TRANSFER tokens interacting with the smart contracts?

Fee-On-Transfer is not guaranteed to work with Univ3 so any incompatiblity is out of scope
___

### Q: Are there any REBASING tokens interacting with the smart contracts?

Rebasing tokens do not work with UniV3 and so any incompatiblity is out of scope
___

### Q: Are the admins of the protocols your contracts integrate with (if any) TRUSTED or RESTRICTED?
restricted. uniswapv3 and chainlink automation should not be able to steal funds
___

### Q: Is the admin/owner of the protocol/contracts TRUSTED or RESTRICTED?
restricted. the owner should not be able to steal funds. 

___

### Q: Are there any additional protocol roles? If yes, please explain in detail:
n/a
___

### Q: Is the code/contract expected to comply with any EIPs? Are there specific assumptions around adhering to those EIPs that Watsons should be aware of?
n/a
___

### Q: Please list any known issues/acceptable risks that should not result in a valid finding.
- If a stable coin pair were to temporarily depeg, and a user places a limit orderwhose tick range encompasses the normal trading tick, there is NO way to cancel the order  because the order is mixed. The user would have to wait for another depeg event to happen so that the order can be fulfilled, or the order can be cancelled.

- amount0Min and amount1Min are set to 0 for _takeFromPosition
___

### Q: Please provide links to previous audits (if any).
https://github.com/crispymangoes/uniswap-v3-limit-orders/blob/main/audit/cyfrin.pdf

https://github.com/crispymangoes/uniswap-v3-limit-orders/blob/main/audit/debaub.pdf
___

### Q: Are there any off-chain mechanisms or off-chain procedures for the protocol (keeper bots, input validation expectations, etc)?
yes, chainlink automation. 
___

### Q: In case of external protocol integrations, are the risks of external contracts pausing or executing an emergency withdrawal acceptable? If not, Watsons will submit issues related to these situations that can harm your protocol's functionality.
yes. 
___



# Audit scope



