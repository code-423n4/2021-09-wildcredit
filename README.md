# ✨ So you want to sponsor a contest

This `README.md` contains a set of checklists for our contest collaboration.

Your contest will use two repos: 
- **a _contest_ repo** (this one), which is used for scoping your contest and for providing information to contestants (wardens)
- **a _findings_ repo**, where issues are submitted. (We'll set that one up later.) 

Ultimately, when we launch the contest, this contest repo will be made public and will contain the smart contracts to be reviewed and all the information needed for contest participants. The findings repo will be made public after the contest is over and your team has mitigated the identified issues.

Some of the checklists in this doc are for **C4 (🐺)** and some of them are for **you as the contest sponsor (⭐️)**.

---

# Contest prep

## ⭐️ Sponsor: Provide marketing details

- https://github.com/code-423n4/2021-07-wildcredit/blob/main/wild_credit_logo.png
- https://twitter.com/wildcredit
- https://twitter.com/0xdev0
- https://discord.gg/emcBDpwf6G
- https://wild.credit/

---

# Wild Credit contest details
- $50,000 USDC main award pot
- Join [C4 Discord](https://discord.gg/EY5dvm3evD) to register
- Submit findings [using the C4 form](https://code423n4.com/2021-07-wildcredit-contest/submit)
- [Read our guidelines for more details](https://code423n4.com/compete)
- Starts July 8 2021 00:00 UTC
- Ends July 14 2021 23:59 UTC

This repo will be made public before the start of the contest. (C4 delete this line when made public)

[ ⭐️ SPONSORS ADD INFO HERE ]


Docs: https://wild-credit.gitbook.io/wild-credit/

Wild Credit is a lending protocol. Unlike Compound or Aave which are composed of a "basket" of approved tokens, Wild Credit instead has isolated lending pairs. Similar to Uniswap, each pair does not influence the state of any other pair in any way. This allows much better risk management and allows the protocol to list less liquid tokens.

Both tokens in each lending pair can be used either as collateral or the borrowed token. To borrow one token, the borrower must deposit the other token as collateral. Each account can only borrow one of the tokens at the same time. To borrow the other token, the currently borrowed token must be repaid in full and the collateral must be withdrawn. A lender may deposit both tokens at the same time to earn interest.

Please review all contracts in this repository. Special interest could be given to the `RewardDistribution.sol` contract and how it interacts with the `LendingPair.sol`

A preview of how the protocol will work can be seen on http://kovan.wild.credit/

ERC20 differance: `LPTokenMaster.sol` changes the `_transfer` function

Please disregard anything currently deployed on mainnet. Subject to review is only the code in this repo and nothing else.

External calls are made by the oracles - Chainlink and Uniswap V3 oracles.
