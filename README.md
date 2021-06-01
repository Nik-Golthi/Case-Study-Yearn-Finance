This repository will store a case study report on the Yearn Finance decentralized finance protocol, as well as supporting materials for the report. 

---

# ***Yearn Finance: A Pioneer in Blockchain-based Asset Management***

## *Origin of Yearn Finance*
---

When Andre Cronje first started learning about cryptoassets and blockchain technology in 2017, he was immediately excited by what he heard. “Here was this entire sector that I’ve never really been exposed to where they were claiming they had solved problems that we’ve been struggling with for the last 20 years”, Cronje told Laura Shin during an episode of Shin’s “Unchained” podcast (Cronje, Unchained, 11:15). Cronje’s excitement soon turned to disappointment, however, as he realized that most projects “[didn’t] really have what they are presenting and offering” in their whitepapers (Cronje, Unchained, 11:43).

This would all change in late 2019 with the rise of decentralized finance protocols on the Ethereum blockchain. Cronje, who comes from a traditional fintech background with experience in telecommunications, AI, insurance, and traditional banking, was suddenly excited once again. Developments in the decentralized finance space presented a legitimate use case for blockchain technology, and one that Cronje, a seasoned finance professional, could understand. “A lot of the traditional finance stuff that I used to do [were] possible now, and in a much more autonomous, much more transparent, and a much lower [operational expense] environment”. (Cronje, Unchained, 12:14). 

Around this time, Cronje began experimenting with decentralized finance protocols. He started depositing stablecoins into different DeFi lending protocols such as AAVE, Compound, and dYdX to earn yield. Cronje would monitor which lending protocol was offering the highest yield for depositing stablecoins, and periodically move his funds from protocol to protocol accordingly (Cronje, Unchained, 3:30). 

After doing this for some time, Cronje identified two challenges with his approach. For one, the costs associated with switching between protocols were starting to add up (Cronje, Unchained, 3:50); for every transaction on the Ethereum blockchain, users are required to pay a “gas” fee denominated in Ether to compensate miners for validating transactions. When submitting a transaction, users submit the amount of gas they are willing to pay in order to execute the transaction. In turn, miners prioritize transactions based on the gas fee they stand to earn (Transactions). As a result, during periods of heavy traffic on the Ethereum network, gas fees can be exorbitant as a high volume of users compete to execute transactions.

Aside from the cost of transactions, Cronje also found that a significant amount of time and diligence was required to identify the best yield-earning opportunities, and to move funds around accordingly. Yields offered by each protocol are not static. In fact, these yields can change quite frequently. Therefore, Cronje realized that a considerable amount of time and attention would be required to closely monitor all available yield opportunities and optimize his allocations (Cronje, Unchained, 3:50).

In early 2020, Cronje started working on Solidity smart contracts to codify and automate this process (Cronje, Unchained, 3:50). The project started out as a personal hobby aimed at automation. However, after deploying a successful tool, Cronje began thinking of ways to improve on his pet project. “To get it as granular as possible I needed more people to interact with it, so I opened it so that more people can deposit funds and withdraw funds, and the more people deposit and withdraw, the more accurately it moves between different lending providers, and the higher aggregate yields it creates”, Cronje said (Cronje, Unchained, 4:21). In other words, each time funds were deposited or withdrawn, a smart contract would examine the DeFi landscape and identify the best yield opportunity. Therefore, the more users interacted with the protocol, the more often the protocol would adjust and optimize its strategy. Cronje opened up his personal project to the world, and thus the earliest iteration of Yearn Finance was born.

Cronje would cover the cost of financing Yearn Finance on his own. He spent roughly $40,000 on building the protocol, and double that amount on smart contract audits and web hosting (Stevens). The costs of financing Yearn Finance and the pressure of handling all management decisions started to weigh on Cronje. In response, he decided to open up control of the protocol to the broader community of protocol users through the launch of a YFI governance token in July 2020. YFI tokens were to be earned by those who used the Yearn Finance protocol. In turn, holders of the YFI token would have the ability to propose changes to Yearn Finance, and subsequently vote on such proposals (Cronje, “YFI”). 

Additionally, in an unconventional move, Cronje chose not to distribute any of the initial YFI token supply to himself. Instead, he chose to earn his share of YFI tokens the same way as everybody else: by using the protocol. At the time, Yearn’s launch of the YFI governance token was viewed as “the most favorable supply distribution for a DeFi community” (Lau). 

---
## *Yearn's Core Products*
---

Yearn Finance was initially the product of Andre Cronje’s desire to automate the process of optimizing his stablecoin yields across a breadth of Decentralized Finance lending protocols. As mentioned above, Cronje set out to solve two key problems: 1) costs associated with frequently transacting on the Ethereum network and 2) the tedious work of monitoring yields and allocating funds across protocols.

Cronje addressed both of these challenges with Yearn Finance’s first product: Earn. Earn, or yEarn,  is a “lending aggregator that strives to attain the highest yield for supported coins” (“yEarn”). To get started, users simply deposit their respective token into one of the Earn pools.

[yEarn](https://v1.yearn.finance/earn)

![yEarn](https://i.imgur.com/jLlg0WU.png)

In return, the user receives a yield-bearing yToken. For example, if one were to deposit USDC tokens into the USDC Earn pool, they would receive yUSDC tokens. The yToken, in this case yUSDC, would represent the USDC deposited into the Earn pool, as well as the future potential yield earnings generated by the Earn lending aggregator (Cronje, Unchained, 13:50) . As such, yTokens are “an ever-incrementing object of the underlying assets”, Cronje explains (Cronje, Unchained, 14:37). “They will forever be increasing in value, as long as there is yield opportunity,” Cronje explains. At the same time, users never have to worry about losing their initial deposits. “If there isn’t yield opportunity, they will still be equivalent to their underlying assets. [Initial deposits] can’t diminish in terms of value” (Cronje, Unchained, 15:04). Additionally, transaction fees would be shared across pool participants. 

With Earn, Cronje had devised an automated lending aggregator that would identify the optimal yield strategy for pool depositors, allocate pool funds accordingly, and socialize the cost of transactions. However, as the DeFi landscape matured, new challenges arose. In particular, the advent of yield farming opened up new opportunities for yield. Yield farming, or liquidity mining, “is a process that allows cryptocurrency holders to lock up their holdings, which in turn provides them with rewards” (Dedezade).

Yield farming rewards often come in the form of another token. Protocols offer token rewards as incentives to attract users and lock up liquidity. This influx of novel yield opportunities also added greater complexity to the process of yield optimization. It became clear to Cronje that a simple on-chain automated strategy would not suffice. “Yield farming now all of a sudden was at a point where robo-advisers could no longer do their job because they could not get sufficient data to do their job”, Cronje commented in an appearance on the Bankless podcast (Cronje, Bankless, 51:45). Instead, in a marketplace that was quickly growing in complexity, Yearn would require “external mechanisms for people to provide inputs” and determine the best strategies (Cronje, Unchained, 5:55).

Cronje launched the Yearn Vaults to address the changing yield landscape. Yearn Finance describes Yearn Vaults, or yVaults, as smart “savings accounts for your crypto assets” (“Overview”). Yearn Vaults are not dissimilar from yEarn from a user experience perspective; users deposit tokens into yVaults and receive yv tokens in exchange. For example, if a user deposits USDC into the USDC yVault, they receive yvUSDC tokens in return (“Vault Tokens”). 


[yVaults](https://yearn.finance/vaults/)


![yVaults](https://imgur.com/frXDmkX.png)


Behind the scenes, however, the yVaults offered a key enhancement. Whereas yEarn is built on a simple, relatively static strategy aimed at optimizing yield from depositing to lending platforms, yVaults consist of dynamic strategies. [Strategies](https://docs.yearn.finance/yearn-finance/yvaults/vaults-and-strategies) are submitted by seasoned DeFi participants and Solidity developers, and are voted on by the Yearn governance community (Cronje, Bankless, 53:12) . If a strategy contract is approved by the community and implemented into a vault, the strategy writer is “entitled to a small percentage of returns generated by the vault” (Miguel). Moreover, each yVault can execute multiple strategies, thus allowing the “flexibility to manage capital efficiently during different market scenarios” (“Overview”). In short, yVaults leverage expertise from experienced DeFi participants and Solidity developers to devise effective yield-generating strategies in an ever-changing landscape, while also maintaining a simple set-and-forget interface for depositors.

Both yVaults and yEarn are aimed at passive investors that are looking for an easy way to earn yield on their stablecoins and other cryptoassets. While other yield aggregator protocols have entered the marketplace, Yearn Finance has a few advantages over its competitors. For one, as the first such protocol to launch, Yearn enjoys a first-mover advantage. Secondly, Yearn has built a strong community of users and contributors through the use of incentives. Strategists are incentivized by earning a share of rewards earned by a successful strategy, and depositors are incentivized to provide capital by the yields they earn. Additionally, Yearn Finance has on-boarded salaried developers and other contributors who receive a percentage of yield revenue (see slides 7 and 10 of 1Q 2021 Yearn Quarterly Report referenced in citations). Furthermore, by stepping down as the sole director of Yearn Finance and opening up ownership of the protocol via the fair launch of the YFI governance token, Andre Cronje fostered a passionate governance community. Lastly, Yearn Finance’s openness to collaborate with other DeFi protocols has not only facilitated the merge of developer talent across protocols, but also positions Yearn to build an ecosystem of “symbiotic financial protocols that increase the capital efficiency of DeFi as a whole” (Otto and Watkins).



---
## *On-Chain Asset Management: A New Paradigm*
---

Yearn Finance is a collection of products in Decentralized Finance that “provides lending aggregation, yield generation and insurance on the Ethereum blockchain” (“Introduction”). Decentralized Finance, or DeFi, is “a blockchain-based financial infrastructure” that “refers to an open, permissionless, and highly interoperable protocol stack built on public smart contract platforms” (Schär 153). Although a relatively new field, DeFi is a fast-paced, ever-evolving industry. Major developments in DeFi include the creation of USD-pegged stablecoins, decentralized exchanges, decentralized lending platforms, decentralized derivatives, and on-chain asset management (Schär 154,160). Two prominent DeFi innovations are the aforementioned yield farming and composability, or the combination of “multiple applications and protocols, thereby creating new and exciting services” (Schär 168-169).

Yearn Finance operates in the on-chain asset management sector of DeFi, but interacts with many of the other sectors mentioned above as well. The protocol also participates in both composability and yield farming. Yearn’s actively managed yVaults were introduced in direct response to complexity borne from the rise of yield farming. Furthermore, the protocol exemplifies the DeFi ethos of composability through its many partnerships with other protocols. 

While Yearn Finance was a pioneer in the yield aggregation and asset management sectors of DeFi, a plethora of other asset management protocols have entered the space as well. Other competitors in the space include Alpha Finance, Rari Capital, Harvest Finance, Enzyme Finance, Badger Finance, Set Protocol, Vesper Finance, dHedge, and yAxis. Enzyme Finance and Set Protocol “allow anyone to create new investment funds” (Schär 168). Similarly, dHedge also allows anyone to “set up their own investment fund on the Ethereum blockchain”, and allows users to invest in these funds (Balakrishnan and Kelly). Prospective dHedge fund investors can track and compare the performance of the different funds on the protocol; fund performance is publicly displayed on a leaderboard (“Managers”). 

Alpha Finance, Harvest Finance, Vesper Finance, Badger DAO, and yAxis all offer set-and-forget yield farming strategies, similar to Yearn Finance. Alpha Finance offers a slight variation on this approach, however, as Alpha allows leveraged yield farming. By allowing depositors access to excess capital, Alpha offers depositors a chance at “higher farming APY and trading fees APY” (“1. Alpha”). Badger DAO also differentiates itself from the pack by focusing specifically on Bitcoin-based yield aggregation strategies on the Ethereum blockchain. 

---
## *Performance & Adoption*
---

The two best measures of Yearn Finance’s success are the yields earned by yEarn and the yVaults, and user adoption of its products. Currently, there are several yVaults that are offering estimated net annualized yields after fees in excess of 20 percent. Additionally, even Yearn’s stablecoin yVaults are offering annualized yields after fees ranging between 8 percent (USDT) and 24 percent (sUSD). Remarkably, the Dai and USDC stablecoin vaults, which are managing $640M and $325M respectively (as of May 31, 2021), are currently offering estimated annual yields of 10 and 12 percent, respectively (see link to Yearn Finance Vaults in citations).

[yVaults](https://yearn.finance/vaults/)
![yVaults](https://imgur.com/8DudwbT.png)

Yearn’s simpler, more conservative Earn pools have posted strong performance as well. In fact, the Earn stablecoin pools have earned an estimated APY of 8.32% since their inception in mid-2020 (as of May 31, 2021; see link to Y Pool Statistics in citations).

[Yearn Pool Statistics](https://curve.fi/combinedstats)
![Yearn Pool Statistics](https://imgur.com/4tLsjsG.png)


Depositors to yEarn and yVault are never risking their underlying deposits. At any time, users are welcome to withdraw the initial funds deposited in full. As such, Andre Cronje has likened Yearn products to smart savings accounts. From this perspective, the yields earned by the Yearn Finance protocol are remarkable. According to Bankrate’s weekly national survey for the week of March 31, 2021, the “national average interest rate for savings accounts is 0.07 percent” (Goldberg). Furthermore, Bankrate’s survey found that the highest interest rates offered by online savings accounts are roughly 0.50 percent. This pales in comparison to the potential yields offered by the yEarn pools and yVault.

Another testament to Yearn Finance’s success is the sheer amount of capital Yearn has under management. Yearn Science, a tool that tracks the total value locked in the protocol, estimates that Yearn Finance currently has roughly $3.9B worth of assets under management across its various products. The fact that the protocol has locked billions of dollars worth of assets into its products in less than a year demonstrates that Yearn has achieved a clear product-market fit (see link to Yearn Science in citations).

[Yearn.Science](https://yearn.science/)
![Yearn.Science](https://imgur.com/B1vPoXH.png)

Moreover, Yearn Finance is currently leading the on-chain asset management sector by a wide margin in terms of total value locked. In comparison, competitors like [Alpha](https://defipulse.com/alpha-homora), [Vesper](https://defipulse.com/vesper), [Badger](https://defipulse.com/badger-dao), [Set Protocol](https://defipulse.com/set-protocol), and [Harvest Finance](https://defipulse.com/harvest-finance) have roughly $1.2B, $660M, $620M, $210M, and $180M worth of assets under management (as of May 31, 2021). Other competitors like [yAxis](https://defipulse.com/yaxis), [Rari Capital](https://app.rari.capital/), [Enzyme Finance](https://defipulse.com/enzyme-finance), and [dHedge](https://defipulse.com/dhedge) all manage under $100M worth of assets (see “TVL” links in citations). 

Yearn Finance has not escaped controversy, however. One of the primary risks in DeFi is smart contract risk. Any vulnerabilities in a smart contract could potentially be exploited by enterprising hackers for lucrative sums. Yearn suffered a smart contract hack in February 2021 that resulted in the theft of $11M worth of assets from one of its vaults (Partz). Although Yearn Finance reimbursed the stolen funds, such hacks pose significant reputational risk. Furthermore, Yearn is particularly vulnerable as a result of its many partnerships and integrations with other DeFi protocols. While these partnerships create tremendous value for Yearn, it is also true that “these interactions introduce severe dependencies” (Schär 171). A single smart contract issue along a chain of integrated protocols could “potentially have widereaching consequences for multiple applications” (Schär 171). This risk is something Yearn Finance must account for and consider going forward, especially as it looks to continue expanding its user base.

---
## *Future Considerations*
---
In many ways, Yearn Finance has been quite successful. The protocol was a pioneer in the field of on-chain asset management on the Ethereum blockchain, and has grown to manage several billion dollars worth of assets in less than one year. Yearn’s AUM growth is a testament to both the efficacy of its products and the simplicity of its user experience. While Yearn faces ever-growing competition in the fast-paced DeFi landscape, the protocol is well-positioned to thrive. As a DeFi pioneer, Yearn has established partnerships with a wide range of other DeFi applications, which has facilitated innovation and attracted contributions from some of the best Solidity developer talent in the space.

In my opinion, two keys to Yearn Finance’s continued success are user growth and enhanced security. In terms of growth, Yearn stands to expand its user base from both the cryptonative community and those who are less familiar with blockchain technology. While the Ethereum blockchain remains the chain with the most activity and largest developer community, other competing blockchains such as Binance Smart Chain, Avalanche, Polkadot, and Solana are emerging. These alternative chains are surging in popularity in direct response to heavy traffic and exorbitant fees on the Ethereum network. Several of these chains, such as Avalanche and Binance Smart Chain, are compatible with the Ethereum Virtual Machine “which enables cross-chain operability for Ethereum assets” (Bogdanov). By expanding to alternative chains, Yearn Finance could potentially attract new users, particularly more recent retail participants who have foregone the Ethereum blockchain in favor of more inexpensive alternatives. 

Expanding to additional blockchains could increase Yearn’s base of users who are already cryptonative. That said, DeFi is still a very niche community with a relatively small number of participants. As a result, it could be argued that Yearn Finance currently stands to gain significantly more users from the non-cryptonative community. To that end, I believe Yearn should consider investing in efforts to increase the awareness of cryptocurrency, DeFi, and the Yearn Finance ecosystem to the broader population. These efforts could be in the form of advertising or a free educational series made available to the public. Another effort would be to clean up the yEarn and yVault naming conventions. Terms such as yTokens, yvTokens, and others are confusing, especially for novice non-cryptonative users. In a similar vein, further simplifying the user interface could assist greatly in on-boarding new users. Yearn is still in its infancy, so these considerations might not be relevant at the moment; focusing on refining its products and attracting and compensating developer talent are likely the protocol’s top priorities at the moment. However, in the long-term, encouraging adoption by the non-cryptonative community could prove beneficial to Yearn’s continued success.

Lastly, I believe Yearn Finance needs to continue to invest heavily in smart contract audits and security. As mentioned earlier, the protocol is especially susceptible to smart contract risk as result of its many partnerships with other DeFi applications. Investing heavily in audits and taking the time to thoroughly address all audit findings could certainly slow Yearn’s pace of innovation. While this could be a short-term detriment in an industry that moves at breakneck pace, the potential long-term reputational risk of additional smart contract hacks is significantly more damaging. Additionally, as the current leader in on-chain asset management on the Ethereum blockchain, Yearn Finance stands to lose the most from further hacks. For this reason, it would be wise for Yearn Finance to continually invest time and capital into the review and protection of its smart contracts.

---
---
### **Citations**:

1) “1. Alpha Homora V1 on Ethereum.” Alpha Finance Lab, Alpha Finance, last edited 10 May 2021, https://alphafinancelab.gitbook.io/alpha-finance-lab/alpha-products/alpha-homora.

2) Balakrishnan, Ashwath and Liam Kelly. “DeFi Review: An Investor’s Guide to dHedge.” Crypto Briefing, 21 August 2020, https://cryptobriefing.com/defi-review-investors-guide-dhedge/.

3) Bogdanov, Dimitar. “Ethereum alternatives on the rise: should we expect to see an Ethereum killer soon?” Limechain Tech, 27 April 2021, https://limechain.tech/blog/ethereum-alternatives/.

4) Cronje, Andre. “YFI.” Medium, 17 July 2020, https://medium.com/iearn/yfi-df84573db81 .

5) Cronje, Andre, guest. “YFI: Farming the Farmers.” Bankless, episode 25, 10 August 2020, https://www.youtube.com/watch?v=tMhpWq2X5hY.

6) Cronje, Andre, guest. “Andre Cronje of Yearn Finance on YFI and the Fair Launch: ‘I’m Lazy.’” Unchained, episode 190, 15 September 2020, https://www.youtube.com/watch?v=SZvDoEJ6wdU&t=2433s.

7) Dedezade, Esat, et al. “What is Yield Farming? Beginner’s Guide.” Decrypt, 23 November 2020, https://decrypt.co/resources/what-is-yield-farming-beginners-guide.

8) Fabian Schär, "Decentralized Finance: On Blockchain- and Smart Contract-Based Financial Markets," Federal Reserve Bank of St. Louis Review, Second Quarter 2021, pp. 153-74. https://doi.org/10.20955/r.103.153-74

9) Goldberg, Matthew. “What is the average interest rate for savings accounts?” Bankrate, 1 April 2021, https://www.bankrate.com/banking/savings/average-savings-interest-rates/.

10) “Introduction.” Yearn Finance Docs, Yearn Finance, last edited 26 May 2021, https://docs.yearn.finance/

11) Lau, Daryl. “YFI A Tale of Fair Launch, Governance, and Value.” Deribit Insights, 24 July 2020, https://insights.deribit.com/market-research/yfi-a-tale-of-fair-launch-governance-and-value/. 

12) “Managers.” dHedge Docs, dHedge, last edited March 2021, https://docs.dhedge.org/dhedge-protocol/managers.

13) Miguel, Alejandro. “Yearn Earn vs. Yearn Vaults - What’s the Difference.” DeFi Rate, 2 March 2021, https://defirate.com/yearn-earn-vs-yearn-vaults/.

14) Otto, Jonathan, and Ryan Watkins. “The Theory of the Yearn.” Messari, Messari, 10 December 2020, https://messari.io/article/the-theory-of-the-yearn.

15) “Overview.” Yearn Finance Docs, Yearn Finance, last edited 26 May 2021, https://docs.yearn.finance/yearn-finance/yvaults/overview.

16) Partz, Helen. “Yearn.Finance puts expanded treasury to use by repaying victims of $11M hack.” Cointelegraph, 9 February 2021, https://cointelegraph.com/news/yearn-finance-puts-expanded-treasury-to-use-by-repaying-victims-of-11m-hack.

17) Stevens, Robert. “Exclusive: YFI’s Andre Cronje is tired, broke and close to quitting DeFi.” Decrypt, 7 August 2020, https://decrypt.co/37995/exclusive-yfi-andre-cronje-broke-quitting-defi.

18) “Transactions.” Ethereum Organization, Ethereum Foundation, last edited 29 March 2021, https://ethereum.org/en/developers/docs/transactions/.

19) “Vault Tokens.” Yearn Finance Docs, Yearn Finance, last edited 26 May 2021, https://docs.yearn.finance/yearn-finance/yvaults/vault-tokens.

20) “yEarn.” Yearn Finance Docs, Yearn Finance, last edited February 2021, https://docs.yearn.finance/yearn-finance/earn. 

---
---
### **Additional Sources**:


- [Yearn Earn](https://v1.yearn.finance/earn)

- [Yearn Vaults](https://yearn.finance/vaults/)

- [Yearn Vaults & Strategies](https://docs.yearn.finance/yearn-finance/yvaults/vaults-and-strategies)

- [yEarn Stablecoin Pool Statistics](https://curve.fi/combinedstats) - See y Pool stats

- [Yearn 1Q 2021 Quarterly Results](https://github.com/yearn/yearn-pm/blob/master/financials/reports/2021Q1-yearn-quarterly-report.pdf)

- [Yearn.Science](https://yearn.science/)

- [Alpha Finance TVL](https://defipulse.com/alpha-homora)

- [Vesper Finance TVL](https://defipulse.com/vesper)

- [Badger DAO TVL](https://defipulse.com/badger-dao)

- [Set Protocol TVL](https://defipulse.com/set-protocol)

- [Harvest Finance TVL](https://defipulse.com/harvest-finance)

- [yAxis TVL](https://defipulse.com/yaxis)

- [Rari Capital TVL](https://app.rari.capital/)

- [Enzyme Finance TVL](https://defipulse.com/enzyme-finance)

- [dHedge TVL](https://defipulse.com/dhedge)



