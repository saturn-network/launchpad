# Saturn Launchpad

Here you will find all the configuration files for running an IDEO (initial decentralized exchange offering) on Saturn Launchpad. And the steps you need to take to set up your own IDEO. If you need any help, please come and ask on our forum: https://forum.saturn.network.

# Before you proceed

Your IDEO will be powered by Saturn Protocol, which supports any ERC20 or ERC223 token deployed on Ethereum or Ethereum Classic. Saturn Protocol is truly decentralized and features an order book which is completely on chain. This means that unlike a centralized launchpad service, you will never give up control of your investment session's token allocation & will receive raised funds directly to your wallet. All investors who wish to participate in your IDEO will need to use a dApp browser to interact with Saturn Protocol. You can find [a list of compatible dApp browsers here](https://forum.saturn.network/t/what-do-you-need-to-start-trading-on-saturn-network/2206).

## How to set up and launch your IDEO on Saturn Launchpad

* Step 1: First you will need to list your token on Saturn Protocol. This is automated and free, [please follow the guide we have published here](https://forum.saturn.network/t/saturn-protocol-token-self-listing-guide/2005).
* Step 2: Navigate to your token's order book on our asset lists, and using the **Create Order** button on the right set up your IDEO's investment sessions. You do this by creating **Sell Orders**, where the **Amount** field will be the session's token supply and the **Price** is the session's token price. For example, if your IDEO has multiple sessions at different token prices then you will need to create several sell orders to match this or if your whole IDEO is at one token price then you would just create one sell order. The important part is on the **Receipt** page, for each sell order you create, you need save the transaction hash.
* Step 2: Fork the project's repository, if you have never used Github before, [we recommend watching this tutorial first](https://www.youtube.com/watch?v=YTbRzhQju4c).
* Step 3: Upload your token's logo and banners to the image directory, please provide all images on a transparent background in PNG format. We require the following sizes for your token logo: 200x200 and 250x250. For your banner, please provide 728x90 and also 300x50.
* Step 4: Add your project's IDEO information to the config.json file. All this information will be displayed on your Saturn Launchpad listing, so please ensure it is as complete as possible. You can use [a JSON validator to make sure you have set up the format correctly](https://jsonlint.com/).

Here is an example IDEO which has four sessions at different token prices & supply. The **order_tx** line is where you need to enter the transaction hash for the sell order(s) you created.  

```
[
  {
    "name": "Mastercoin Invest",
    "symbol": "MS",
    "total_supply": "400000000",
    "decimals": 18,
    "blockchain": "ETH",
    "address": "0x411079f1b50ac2583a458a7cce1d1afdf4f8842e",
    "images": {
      "logo250x250": "https://github.saturn.network/launchpad/images/MS_250x250.png",
      "logo200x200": "https://github.saturn.network/launchpad/images/MS_200x200.png",
      "banner728x90": "https://github.saturn.network/launchpad/images/MS_banner_728x90.png",
      "banner300x50": "https://github.saturn.network/launchpad/images/MS_banner_300x50.png"
    },
    "sessions": [
      {
        "start_date": "2019/06/01",
        "end_date": "2019/06/08",
        "session_supply": "2200000",
        "order_tx": "0xTBD1"
      },
      {
        "start_date": "2019/06/09",
        "end_date": "2019/06/15",
        "session_supply": "1800000",
        "order_tx": "0xTBD2"
      },
      {
        "start_date": "2019/06/16",
        "end_date": "2019/06/22",
        "session_supply": "1400000",
        "order_tx": "0xTBD3"
      },
      {
        "start_date": "2019/06/23",
        "end_date": "2019/06/29",
        "session_supply": "1100000",
        "order_tx": "0xTBD4"
      }
    ],
    "social_media": {
      "saturnforum": "https://forum.saturn.network/t/masternode-invest-token-15-03-2019-listing-date-get-a-montly-revenue-from-cryptocurrency-masternode/3247",
      "twitter": "https://twitter.com/Masternodeinves",
      "facebook": "https://www.facebook.com/Masternodeinvest",
      "instagram": "",
      "reddit": "https://www.reddit.com/user/masternode_invest",
      "telegram": "https://t.me/joinchat/BAZrwkhLqCvhDUKubdCH1Q",
      "linkedin": "https://www.linkedin.com/company/masternode-invest/",
      "bitcointalk": "https://bitcointalk.org/index.php?topic=4516590.msg40664067#msg40664067",
      "website": "https://masternodeinvest.io/",
      "whitepaper": "https://masternodeinvest.io/wp-content/uploads/2018/10/English_WP-41.pdf",
      "youtube": "https://www.youtube.com/channel/UCd7-hS2zA4c0bi6gXPps1fw",
      "medium": "https://medium.com/@Masternodeinves",
      "github": "https://github.com/Masternodeinvest/",
    },
    "youtube_summary": "https://youtu.be/0M2KcjnIhm8",
    "project_summary": "Masternode Invest is a company, operating in Fintech environment, allowing people to invest on cryptocurrency masternode. The seed of our mission is to increase the possibility to invest on coin with POS-Masternode consensus algorithm. We are the first and unique project in this environment that gives you a proof of transparency , once invested on us, you will have our MS token associated to a smart contract, that will share automatically dividends every 30 days.",
    "roadmap": [
      {"when": "October 2018", "milestone": "Start Private Sale (Completed)"},
      {"when": "November 2018", "milestone": "Start KYC Process (Completed)"},
      {"when": "December 2018", "milestone": "Start Masternodes (Completed)"},
      {"when": "January 2019", "milestone": "First rewards into your wallet (Completed)"},
      {"when": "February 2019", "milestone": "Start application POOL masternodes; Get revenue from POOL fee for any MS token holder"},
      {"when": "March 2019", "milestone": "Launch of token on exchanges"},
      {"when": "May 2019", "milestone": "App for your phone to monitor investment"}
    ]
  }
]
```
* Step 5: Create a Pull Request.

**Please note we have to manually approve pull requests and we may refuse requests containing abusive content or misleading information that will alienate our website visitors.**

**Our exchange is [censorship-free](https://forum.saturn.network/t/our-philosophy/1550), so there are no restrictions on which projects or who can use Saturn Launchpad. However, if we feel there is not adequate information provided for potential investors to do their own research on your project then we may ask you to provide this information before your IDEO goes live.
