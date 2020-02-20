# DeFi Audit

## Key Points
Code quality: Trusting teams have implemented best practices for developing high quality, tested software should not be taken for taken for granted. Detailed due diligence needs be done at regular intervals.

Ownership structure & upgrade logic: Knowing the ownership structure of the protocol is much more important than just saying "oh look it has an admin key"! Most of the time the admin is a contract which has its own logic. Furthermore analysis around how often the admin key is used should be done including how easy is to audit what the changes actually are.

Liquidity Analysis: On-going monitoring around the attack vector of flash loan liquidity compared to assets used by platform liquidity. This is something that you can kind of gauge at the moment but isn't really easy to continually check. Teams should think about what safe-guards they're taking to ensure bootstrapping liquidity slowly isn't vulnerable to flash loan attacks. Governance tokens beware.

Oracle Analysis: If you're going to use on-chain oracles, don't just assume a large whale won't manipulate them, actually do the math! I think before it's been too easy to dismiss the fact that a large whale wouldn't risk their capital. Now anyone can become a whale without the capital!

Bootstrap Insurance Liquidity: With the advent of new insurance protocols such as Nexus and Opyn, taking the other side of the insurance is a great way to signal confidence to your users that you're willing to pay out losses in the case that they want insurance. It probably won't even cost that much considering a static solidity audit runs $50k - $200k USD and most people won't purchase insurance. Adding to this, just lend out funds in a lending protocol earning interest while you have your ETH/DAI parked inside.

Liquidity Caps: As much as everyone wants to ship fast, rushing the deployment process and not capping your down-side can be a hazard. If you're going to cut corners, ensure that the total amount lost is on a much smaller scale. MakerDAO is a great example of this by having the cap on total amount of DAI being able to be minted. Lending protocols might want to think about adding a cap similar to this as well.

---
sources [DeFi Weekly](https://defiweekly.substack.com/p/announcing-defi-audits-and-the-holistic?utm_campaign=post&utm_medium=email&utm_source=copy)