---
title: "OpenBazaar and Bitcoin Fees" 
layout: post
date: '2017-11-16 00:30:00 -0300'
---
        
\[et\_pb\_section bb\_built="1"\]\[et\_pb\_row\]\[et\_pb\_column type="4\_4"\]\[et\_pb\_text \_builder\_version="3.0.76" background\_layout="light" border\_style="solid"\] ![OpenBazaar & Bitcoin Fees](https://www.openbazaar.org/wp-content/uploads/2017/11/OpenBazaar-Bitcion-Fees-1024x512.png)   OpenBazaar currently uses Bitcoin for all payments, which allows us to enjoy the primary benefit of the leading cryptocurrency: secure payments without needing to trust a third party. No payment processors or banks needed, you control your own trade and your own money. Bitcoin has many advantages over other payment methods, but there are disadvantages as well. One disadvantage is obvious to anyone using OpenBazaar at the moment: Bitcoin fees are extremely high. OpenBazaar started in mid-2014, when fees averaged less than $0.10, and fees still averaged only around $0.20 when we began work on OpenBazaar 2.0 in summer 2016. In the past year we've seen rapid increases in fees, and the past week has seen fees at levels that severely inhibit lower value ecommerce transactions (fees are now well over $5). The reasons for the increase in fees is complicated and not the purpose of this article. It's also important to note that these fees are not guaranteed to stay this high forever - it's possible that fees will drop to more ecommerce-friendly levels soon - but we aren't just crossing our fingers waiting for this to happen.

> ### The question is, what has OpenBazaar done about high Bitcoin fees, and what more can be done?

What we've done
---------------

The new version of OpenBazaar, released Nov 1st, has a built-in Bitcoin wallet. We choose to build a wallet into the software because it gave users a better experience and because it allowed us to do more complicated Bitcoin transactions, such as multisig escrow and timelock. The OpenBazaar development team decided to implement **Segwit** (a change to Bitcoin that can create cheaper transactions) in order to alleviate fee pressure and so that OpenBazaar wallets were compatible with other wallets as Segwit adoption increased. Segwit was implemented at launch, and is used by default when possible in transactions. As fees increased we also saw the need to limit user's actions to prevent transactions from being stuck in the escrow multisig. We use **2-of-3 multisig** for **moderated payments** and a **1-of-2 multisig** for **offline ordering**. Multisig transactions are powerful tools, but they require two Bitcoin fees instead of one. Not normally a problem with $0.10 fees, but when you are purchasing a $5 item and there's a $5 fee, your payment will never be released to the vendor. Also, vendors are naturally upset to pay a $5 fee when receiving payment for a $10 item, which is effectively a 50% fee. For a detailed look at how Bitcoin fees work in OpenBazaar, you can read point #5 in our [vendor guide](https://www.openbazaar.org/blog/openbazaar-vendor-guide-what-to-expect-when-selling-on-the-worlds-largest-decentralized-marketplace/). We have addressed this by preventing users from purchasing items which aren't significantly higher than the current fee price. This prevents stuck transactions and angry vendors, but it also prevents people from using OpenBazaar for buying or selling inexpensive items. We want OpenBazaar to be a free marketplace for anyone to buy and sell anything, regardless of the overall price of the good or service, so this solution wasn't something we were happy to implement.

What we will do
---------------

Though we've adopted Segwit in an effort to help our users reduce Bitcoin fees, second layer solutions like the Lightning Network aren't available for end users yet so that will remain a bit of a waiting game. Next, however, we are working to **integrate other cryptocurrencies** into OpenBazaar. Work on this has already begun and several community members from other coins have been working on integration. Initially we'll likely offer just two or three other cryptocurrencies in addition to Bitcoin, but the long term goal is for OpenBazaar to be coin agnostic and allow payments in any cryptocurrency. Because OpenBazaar is a fully decentralized p2p network, supporting various cryptocurrencies isn't a simple change. This is currently the development team's top priority, but users will need to wait more than Two Weeks™ to be able to use the new coins.

What you can do
---------------

There are a few things you can do that will reduce the impact of high fees.

1.  1.  **Everyone: Be mindful of prices and fees**   If you're a vendor, consider listing higher value items while fees are high and being clear with buyers about why you are or aren't willing to sell certain items and / or have certain prices. Buyers should pay attention to the fees when purchasing as well.
     2.  **Vendors: Keep your stores online**   When buyers place an order while the vendor is offline, the vendor pays an extra Bitcoin fee when they fulfill the order. Vendors who want to avoid paying that extra fee should keep their store running as often as possible.
     3.  **Developers: Help get your favorite coin added to OpenBazaar!**   If you're a developer, particularly if you're knowledgeable with cryptocurrencies, you can help us integrate these new coins.   If you're not a developer, but you want another cryptocurrency integrated into OpenBazaar, try to get some community support to urge the coin's developer community to contribute. Either way, please join us on [Reddit](https://reddit.com/r/openbazaar) or [click here](https://docs.google.com/forms/d/e/1FAIpQLSdEXqnREdncZYEXYSaE_wK41UV6JkBqNxqY5X-6J3oFNlZ72Q/viewform) to be invited to join us on Slack to contribute to the discussion!
    
     
    
    * * *
    
    **Still want to get started as we share some growing pains?**  
    [Download OpenBazaar](https://openbazaar.org/download) now!   \[/et\_pb\_text\]\[et\_pb\_code admin\_label="Social (ALL)" \_builder\_version="3.0.53" custom\_css\_main\_element="margin: auto;" max\_width="800px" disabled="off" disabled\_on="off|off|" saved\_tabs="all"\]<div width="100%" style="margin: 0 auto !important;"><!-- \[et\_pb\_line\_break\_holder\] --><!-- \[et\_pb\_line\_break\_holder\] --><div class="a2a\_kit a2a\_kit\_size\_32 a2a\_default\_style"><!-- \[et\_pb\_line\_break\_holder\] --> <a class="a2a\_button\_tumblr"></a><!-- \[et\_pb\_line\_break\_holder\] --> <a class="a2a\_button\_facebook"></a><!-- \[et\_pb\_line\_break\_holder\] --> <a class="a2a\_button\_twitter"></a><!-- \[et\_pb\_line\_break\_holder\] --> <a class="a2a\_dd" href="https://www.addtoany.com/share"></a><!-- \[et\_pb\_line\_break\_holder\] --></div><!-- \[et\_pb\_line\_break\_holder\] --><!-- \[et\_pb\_line\_break\_holder\] --><script async src="https://static.addtoany.com/menu/page.js"></script><!-- \[et\_pb\_line\_break\_holder\] --><!-- \[et\_pb\_line\_break\_holder\] --></div>\[/et\_pb\_code\]\[/et\_pb\_column\]\[/et\_pb\_row\]\[et\_pb\_row use\_custom\_width="on" width\_unit="off" custom\_width\_percent="100%" custom\_padding="|10%||10%" padding\_mobile="off" background\_color="#f2f2f2" column\_padding\_mobile="on" background\_color\_1="#f2f2f2" parallax\_method\_1="off" parallax\_method\_2="off" parallax\_method\_3="off" parallax\_method\_4="off" disabled\_on="off|off|" custom\_css\_main\_element="border-top: solid 1px #ccc;||border-bottom: solid 1px #ccc;" background\_position="top\_left" background\_repeat="repeat" background\_size="initial" \_builder\_version="3.0.53" background\_position\_1="top\_left" background\_repeat\_1="no-repeat" disabled="off"\]\[et\_pb\_column type="4\_4"\]\[et\_pb\_text admin\_label="Medium Links (Desktop)" max\_width="1000px" disabled\_on="on|on|" custom\_css\_main\_element="margin: auto;" background\_position="top\_left" background\_repeat="repeat" background\_size="initial" \_builder\_version="3.0.53" background\_layout="light" text\_orientation="left" border\_style="solid" disabled="off" module\_alignment="left"\]
    
    ### Recent Updates
    
    \[/et\_pb\_text\]\[et\_pb\_text admin\_label="Medium Links (Tablet)" max\_width="1000px" disabled\_on="on|off|on" custom\_css\_main\_element="margin: auto;||padding-left: 10px;||padding-right: 10px;" background\_position="top\_left" background\_repeat="repeat" background\_size="initial" \_builder\_version="3.0.53" background\_layout="light" text\_orientation="left" border\_style="solid" disabled="off" module\_alignment="left"\]
    
    ### Recent Updates
    
    \[/et\_pb\_text\]\[et\_pb\_text admin\_label="Medium Links (Mobile)" max\_width="1000px" disabled\_on="off|on|on" custom\_css\_main\_element="margin: auto;||padding-left: 10px;||padding-right: 10px;" background\_position="top\_left" background\_repeat="repeat" background\_size="initial" \_builder\_version="3.0.53" background\_layout="light" text\_orientation="left" border\_style="solid" disabled="off" module\_alignment="left"\]
    
    ### Recent Updates
    
    \[/et\_pb\_text\]\[/et\_pb\_column\]\[/et\_pb\_row\]\[/et\_pb\_section\]