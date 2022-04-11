# Team Name: BalloonBox

## Project Description
Project name: SCRTSibyl_phase2

SCRTSybil is an oracle for credit score checks developed through an initial Secret Network grant. This is an application to fund a phase #2 expansion of SCRTSibyl through a second grant.

The SCRTSibyl Dapp targets a specific use case: P2P micro-lending, namely facilitating lending and borrowing of microloans ranging between USD 1-25K. As such, the Dapp is already able to compute credit scores to validate users' credibility and to determine how much of a loan (in USD) a user qualifies for.

The oracle runs a credit score check on either the user's preferred bank account (integrating through Plaid API) or the user's Coinbase account (integrating through Coinbase API). The credit check assesses the user's financial health and predicts whether the user can pay back their micro-loan. The Dapp then executes a smart contract to write and store the calculated score into the Secret Network blockchain.

Throughout the process, users are in control of their own data, which is securely stored on-chain through the privacy-preserving Secret Network protocols. Users have even more control over their own data: they can view his score at any time through a read-only secret and costless permission key; they can issue viewing keys by paying a gas fee, to then share the key with third parties issuing them a load; lastly, they can revoke the issued viewing keys by running a state-changing function in the smart contract at the cost of a gas fee.

In phase 2, we want to both expand our use case including loans of USD +25K, but also increase user adoption of the Dapp, by integrating with new data validators, authenticating through different wallets, and allowing the user to self-select the loan currency. We want SCRTSibyl to be able to cater to a wide loan range and for the Dapp to be accessible for an increasingly large pool of crypto investors.

## Problem / Solution

Phase 2 of SCRTSibyl features the following extensions:

 - **Expand validator options**: we will integrate through the Binance API. Binance is a well-established and growing crypto exchange platform and we want to allow users who don't own a wallet in Coinbase the chance to get their score calculated by connecting their Binance account instead. Thus, users have now the choice to connect either their Coinbase account, their Binance account, or both. 
 
 - **Allow smart currency selection**: the user interacts with the SCRTSibyl UI to custom-choose the currency (fiat or crypto) he prefers to receive a loan in. The Dapp will automatically standardize all the metrics in the credit scoring algorithm to the chosen currency. The range of currencies will be initially limited to a predetermined set (USD, EUR, BTC, ETX, USDT, USDC, BNB, XRP). We will integrate with [CoinAPI.io](https://github.com/coinapi/coinapi-sdk) to perform real-time currency conversion.
 
 - **Improve risk indicators**: we will increase the output accuracy of the credit scoring model by returning low/medium/high-risk indicators on the scoring bin assigned to the user. For example, imagine a user qualified for a mini-loan ranging from USD 5-10K. This scoring bin is rather broad, and a user may be very well suited to receive a loan of USD 6K but may struggle to pay back a loan worth USD 9K. Thus, we'll develop three categories to assess the risk level for given users to receive their associated loans. The same user qualifying for USD 5-10K may be a low-risk user in receiving a USD 6K loan but is a high-risk user for a USD 9K loan. 
 
 - **Add credit score history**: a user's score may change and improve over time and we want to give users with a positive pedigree the possibility to demonstrate the improvement in their credit history. We'll implement a query function to fetch the chronologically ordered list of their credit scores with associated timestamps. Users will be in control of their credit score history and, if they so choose, will be able to share it with third parties.

## Detailed Product Description

### Components

## Go-to-Market Plan

## Value Capture for Secret Network Ecosystem

## Company
Company Website - Official Repository
* [BalloonBox](https://www.balloonbox.io/) - [repository](https://github.com/BalloonBox-Inc)

## Team Members
Personal LinkedIn - Personal Repository
* [Michael Brink](https://www.linkedin.com/in/michael-brink-680b3767/) - [repository](https://github.com/MichaelBrink)
* [Matteo Mortelliti](https://www.linkedin.com/in/matteo-mortelliti/) - [repository](https://github.com/mmortelliti)
* [Mayllon Miranda](https://www.linkedin.com/in/mayllon-miranda-8aa9b0163/) - [repository](https://github.com/m3mayllon)
* [Irene Fabris](https://www.linkedin.com/in/irenefabris/) - [repository](https://github.com/irene-bbox)
* [Hongbin Lin](https://www.linkedin.com/in/hongbinlin/) - [repository](https://github.com/BalloonBox-Hongbin)
* [Yoon Kim](https://www.linkedin.com/in/imyoonkim/) - [repository](https://github.com/yoon-bbox)

## Team’s Experience

All team members of SCRTSybil are from Balloon Box Technology Inc., a FinTech company based in Vancouver, BC specialized in software engineering & data science solutions from design through launch. Besides a string of projects for clients all around the world, our team is experienced in developing web apps for crypto asset management, custom Ledger-integrated apps, integrating with PSPs, crpyto exchanges and KYC providers, visualizing big data on L1 & L2s and building wallet solutions. Our team members are proficient in Python, C++, Java, Javascript, and other object-oriented and development languages. 
 
Our team consists of the following roles:
- Product Architect (Full product architecture) 
- Full Stack Engineer (Core framework)
- Designer (UI/UX on the web application)
- Backend Engineer (APIs, database structure, DevOps)
- Data Scientist (x2) (Credit Score algorithm + build)
- Product Manager (Community, articles, GitHub house-keeping, managing public PRs)

## Development Roadmap

### Overview

- **Total Estimated Duration:** 14 weeks
- **Full-Time Equivalent (FTE):** 3.5
- **Total Costs:** USD 120,000

Our team will require 3.5 months to complete this project (subject to a mutually agreed upon solution design that both Bbox and SCRT feel excited about). We intend to have 2 developers full-time, 2 data scientists full-time, and 1 UX/UI designer part-time, a product architect, and a project manager. We can receive payments in 4 disbursements, one at the beginning of the grant, three after completion of each milestone.
We would be willing to consider part payment (up to 50%) in SCRT, BTC or ETH. The grant can be paid to either of the following addresses:

- BTC address: bc1qz36smg7zg9d2de7qurj9a49fetemavta39a9zp
- ETH address: 0x3ffA0e66091742a867430D140E36826c06ba19Be
- SCRT address: secret18qeg7lx63wkqvy9e295slufvch5rfel2v23tsu

**Initial amount at grant issuance:** USD 20,000
 
### Milestone 1 - APIs, Integration, Credit Score Algorithm
- **Estimated duration:** Week 1-8
- **Costs:** USD 50,000

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | Provide inline documentation of the code. |
| 1a. | API module | Build Binance validator. |
| 1b. | API module | Build currency selector. |
| 1c. | API module | Refine risk model. |
| 2. | Data Cleaning | Setup VM with sufficient resources for score computation. |
| 3. | Data Integration | Overlay web2 with web3 validation data for the new API. |
| 4. | ML Module - Build | Build an light ML model to calculate user credit score. |
 
### Milestone 2 - Test and Validation
- **Estimated duration:** Week 8-10
- **Costs:** USD 20,000

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | We will provide inline documentation of the code. |
| 0c. | Test Guide | Run unit tests to ensure functionality and robustness of core functions (~70%). |
| 1. | ML Module - Deploy | Train, test, deploy the new ML model and compute credit scores. |
| 2. | Contract | Execute the smart contract, written in Rust, to encrypt the calculated credit score to SCRT Network blockchain. |

### Milestone 3 - WebApp: Framework + UI 
- **Estimated duration:** Week 11-14
- **Costs:** USD 30,000

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | We will provide inline documentation of the code for the WebApp framework. |
| 1. | Framework | Implement SCRT wallet Login, personal info input, hover+select+OAuth2 in chosen validator |

| 3. | UI Module | Design the UI flow for retrieving the score history. | 
| 4. | UI Module | WebApp aesthetics and functionalitiy refinements. |
| 5. | Tutorial | We will publish a video tutorial that walks a user through the SCRTSybil WebApp instructing them on the new features. | 

## Additional Information

### Why SCRT?

1. **How did you hear about the SCRT Network Grants?** We have been collaborating with the SCRT Labs Team for the last 4 months and we are just about to complete and release the very first Credit Score Oracle we developed for the Secret Network.

2. **Have you ever applied for other grants?** Yes, this is a follow-up grant to expand the work we completed after the first SCRT grant we received in January 2022.
 
### Scope and Limitations


### Future Plans
