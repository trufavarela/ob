---
title: "First Look: Super Fast Checkout Process In OpenBazaar 2.0" 
layout: post
date: '2017-06-30 00:30:00 -0300'
---
        
\[et\_pb\_section bb\_built="1"\]\[et\_pb\_row\]\[et\_pb\_column type="4\_4"\]\[et\_pb\_text\] Yesterday our designer, Mike Wolf, shared this great tweet about the speed of the purchasing time within OpenBazaar 2.0:

> Purchasing on [@OpenBazaar](https://twitter.com/openbazaar) 2.0 takes as little as 10s with the new internal wallet [$crypto](https://twitter.com/search?q=%24crypto&src=ctag) [$BTC](https://twitter.com/search?q=%24BTC&src=ctag) 😮😮 [pic.twitter.com/nLgKNUh5wg](https://t.co/nLgKNUh5wg)
> 
> — Mike Wolf (@thee_wolf) [June 29, 2017](https://twitter.com/thee_wolf/status/880470093804654593)

We want to be clear that this is an example of how fast it can be to get through the _checkout process_ within the application, not the time it takes the _transaction to clear on Bitcoin_. That will still be dependent on the bitcoin network itself. **Why is the checkout process this fast, now?**

> Because of the internal wallet!

In the current version of OpenBazaar there is no built-in wallet so users need to use a wallet external to the app in order to make purchases. This gif shows the new process for OpenBazaar 2.0, launching soon, which has a wallet built into the application. Instead of being forced to use an external wallet, you will be able to pay bitcoin into the OpenBazaar wallet--where you still control your own keys locally--and then make payments as shown in the gif. This new wallet is an SPV wallet where each user owns their own keys. Users will have this wallet by default though they can swap it out for bitcoind if they prefer. The wallet talks directly to the Bitcoin network, meaning all transactions are on-chain and there are no servers. **Okay...but what's an SPV wallet? ** The most secure way to use Bitcoin is to run a "full node" which means you have the entire copy of the blockchain and you verify all new transactions in new blocks yourself. However, running a full node is inconvenient, requiring a significant amount of disk space and other resources. The average user isn't going to download the entire blockchain.

> That's where **Simplified Payment Verification (SPV)** wallets come in.

The basic idea is that an SPV wallet doesn't verify everything in blocks as accurate, so it doesn't need to download the entire chain. It relies on a trusted node for verification. We're very excited about this new internal wallet because it offers a greater level of convenience and access to users that is reflected in this checkout time.  The whole purchasing flow is smooth and we cannot wait to get OpenBazaar 2.0 into users hands this summer.

* * *

**Are you ready to check it out?** _Sign up for our newsletter [here](https://www.openbazaar.org/newsletter) for opportunities to be one of the first users of version 2.0 [](https://openbazaar.org/) Join us on [Slack](http://slack.openbazaar.org/), [Twitter](https://twitter.com/openbazaar) or [Facebook](https://facebook.com/openbazaarproject)_ _And of course, you can still download [OpenBazaar v.1](https://openbazaar.org/) to shop right now!_ \[/et\_pb\_text\]\[et\_pb\_code admin\_label="Social (ALL)" \_builder\_version="3.0.53" custom\_css\_main\_element="margin: auto;" max\_width="800px" disabled="off" disabled\_on="off|off|" saved\_tabs="all"\]<div width="100%" style="margin: 0 auto !important;"><!-- \[et\_pb\_line\_break\_holder\] --><!-- \[et\_pb\_line\_break\_holder\] --><div class="a2a\_kit a2a\_kit\_size\_32 a2a\_default\_style"><!-- \[et\_pb\_line\_break\_holder\] --> <a class="a2a\_button\_tumblr"></a><!-- \[et\_pb\_line\_break\_holder\] --> <a class="a2a\_button\_facebook"></a><!-- \[et\_pb\_line\_break\_holder\] --> <a class="a2a\_button\_twitter"></a><!-- \[et\_pb\_line\_break\_holder\] --> <a class="a2a\_dd" href="https://www.addtoany.com/share"></a><!-- \[et\_pb\_line\_break\_holder\] --></div><!-- \[et\_pb\_line\_break\_holder\] --><!-- \[et\_pb\_line\_break\_holder\] --><script async src="https://static.addtoany.com/menu/page.js"></script><!-- \[et\_pb\_line\_break\_holder\] --><!-- \[et\_pb\_line\_break\_holder\] --></div>\[/et\_pb\_code\]\[/et\_pb\_column\]\[/et\_pb\_row\]\[et\_pb\_row use\_custom\_width="on" width\_unit="off" custom\_width\_percent="100%" custom\_padding="|10%||10%" padding\_mobile="off" background\_color="#f2f2f2" column\_padding\_mobile="on" background\_color\_1="#f2f2f2" parallax\_method\_1="off" parallax\_method\_2="off" parallax\_method\_3="off" parallax\_method\_4="off" disabled\_on="off|off|" custom\_css\_main\_element="border-top: solid 1px #ccc;||border-bottom: solid 1px #ccc;" background\_position="top\_left" background\_repeat="repeat" background\_size="initial" \_builder\_version="3.0.53" background\_position\_1="top\_left" background\_repeat\_1="no-repeat" disabled="off"\]\[et\_pb\_column type="4\_4"\]\[et\_pb\_text admin\_label="Medium Links (Desktop)" max\_width="1000px" disabled\_on="on|on|" custom\_css\_main\_element="margin: auto;" background\_position="top\_left" background\_repeat="repeat" background\_size="initial" \_builder\_version="3.0.53" background\_layout="light" text\_orientation="left" border_style="solid" disabled="off"\]

### Recent Updates

\[/et\_pb\_text\]\[et\_pb\_text admin\_label="Medium Links (Tablet)" max\_width="1000px" disabled\_on="on|off|on" custom\_css\_main\_element="margin: auto;||padding-left: 10px;||padding-right: 10px;" background\_position="top\_left" background\_repeat="repeat" background\_size="initial" \_builder\_version="3.0.53" background\_layout="light" text\_orientation="left" border_style="solid" disabled="off"\]

### Recent Updates

\[/et\_pb\_text\]\[et\_pb\_text admin\_label="Medium Links (Mobile)" max\_width="1000px" disabled\_on="off|on|on" custom\_css\_main\_element="margin: auto;||padding-left: 10px;||padding-right: 10px;" background\_position="top\_left" background\_repeat="repeat" background\_size="initial" \_builder\_version="3.0.53" background\_layout="light" text\_orientation="left" border_style="solid" disabled="off"\]

### Recent Updates

\[/et\_pb\_text\]\[/et\_pb\_column\]\[/et\_pb\_row\]\[/et\_pb\_section\]