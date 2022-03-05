# Team Name: BalloonBox

## Project Description
Project name: SCRTSybil_phase2


SCRTSybil is an oracle for credit score checks developed through an initial Secret Network grant. This is an application to fund a phase #2 expansion of SCRTSibyl through a second grant. The SCRTSibyl Dapp targets a specific use case: P2P micro-lending, namely facilitating lending and borrowing of microloans ranging between $1-25K USD. As such, the Dapp is already able to compute credit scores to validate users' credibility and to determine how much of a loan (in USD) a user qualifies for. The oracle runs a credit score check on either the user's preferred bank account (integrating through Plaid API) or the user's Coinbase account (integrating through Coinbase API). The credit check assesses the user's financial health and predicts whether the user can pay back their micro-loan. The Dapp then executes a smart contract to write and store the calculated score onto the Secret Network blockchain. Throughout the process, the user is in control of his own data, which is securely stored on-chain through the privacy-preserving Secret Network protocols. The user has even more control over his own data: he can view his score at any time through a read-only secret and costless permission key; he can issue viewing keys by paying a gas fee, to then share the key with third parties issuing him a load; lastly, he can revoke the issued viewing keys by running a state-changing function in the smart contract at the cost of a gas fee. In phase 2, we want to both expand our use case including loans of +$25K USD, but also increase user adoption of the Dapp, by integrating with new data validators, authenticating through different wallets, and allowing the user to self-select the loan currency. We want SCRTSibyl to be able to cater to a wide loan range and for the Dapp to be accessible for an increasingly large pool of crypto investors. 


## Problem / Solution  


Phase 2 of SCRTSibyl features the following extensions:
 - more wallets: we will build an integration through the novel Citadel.One Secret wallet. The user can then choose to authenticate into SCRTSibyl through their preferred wallet (Keplr or Citadel)
 - more validators: we will integrate through the Binance API. Binance is a well-established and growing crypto exchange platform and we want to allow users who don't own a wallet in Coinbase the chance to get their score calculated by connecting their Binance account instead. Thus, users have now the choice to connect either their Coinbase account, their Binance account, or both. 
 - smart currency selector: the user interacts with the SCRTSibyl UI to custom-choose the currency (fiat or crypto) he prefers to receive a loan in. The Dapp will automatically standardize all the metrics in the credit scoring algorithm to the chosen currency. The range of currencies will be initially limited to a predetermined set (USD, EUR, BTC, ETX, USDT, USDC, BNB, XRP). We will integrate with [CoinAPI.io](https://github.com/coinapi/coinapi-sdk) to perform real-time currency conversion.
 - risk indicators: we will increase the output accuracy of the credit scoring model by returning low/medium/high-risk indicators on the scoring bin assigned to the user. For example, imagine a user qualified for a mini-loan ranging from $5-10K USD. This scoring bin is rather broad, and a user may be very well suited to receive a loan of $6K but may struggle to pay back a loan worth $9K. Thus, we'll develop three categories to assess the risk level for given users to receive their associated loans. The same user qualifying for $5-10K USD may be a low-risk user in receiving a $6K loan but is a high-risk user for a $9K loan. 
 - query credit score history: a user's score may change and improve over time and we want to give users with a positive pedigree the possibility to demonstrate the improvement in their credit history. We'll implement a query function to fetch the chronologically ordered list of their credit scores with associated timestamps. The user will be in control of their credit score history and, if he so chooses, will be able to share it with third parties. 


## Team Members
* Michael Brink
* Matteo Mortelliti
* Yuchen Lin
* Mayllon Miranda
* Irene Fabris
* Hongbin Lin
* Yoon Kim

## Team Code Repos
- https://github.com/BalloonBox-Inc BalloonBox official repository
- https://github.com/MichaelBrink Michael Brink
- https://github.com/mmortelliti Matteo Mortelliti
- https://github.com/yul761 Yuchen Lin
- https://github.com/m3mayllon Mayllon Miranda
- https://github.com/irene-bbox Irene Fabris
- https://github.com/BalloonBox-Hongbin Hongbin Lin 
- https://github.com/yoon-bbox Yoon Kim
 


## Additional Information :heavy_plus_sign:

#### Why SCRT

1. **How did you hear about the SCRT Network Grants?** We have been collaborating with the SCRT Labs Team for the last 4 months and we are just about to complete and release the very first Credit Score Oracle we developed for the Secret Network.

2. **Have you ever applied for other grants?** Yes, this is a follow-up grant to expand the work we completed after the first SCRT grant we received in January 2022.
 
