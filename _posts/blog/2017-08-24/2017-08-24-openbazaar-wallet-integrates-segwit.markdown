---
title: "OpenBazaar Wallet Integrates Segwit" 
layout: post
date: '2017-08-24 00:30:00 -0300'
---
        
\[et\_pb\_section bb\_built="1" transparent\_background\_fb="default" \_builder\_version="3.0.47"\]\[et\_pb\_row \_builder\_version="3.0.47" background\_size="initial" background\_position="top\_left" background\_repeat="repeat"\]\[et\_pb\_column type="4\_4"\]\[et\_pb\_text admin\_label="Segwit Activated - What It Means for OpenBazaar" \_builder_version="3.0.66"\]

![](https://www.openbazaar.org/wp-content/uploads/2017/08/OpenBazaar-Wallet-Integrates-Segwit-1024x512.png)

Segregated Witness has thankfully activated on the Bitcoin network before the release of OpenBazaar 2.0. This has given us an opportunity to upgrade OpenBazaar to make use of segwit before putting it in the hands of users.

Had segwit activated later, it would have made upgrading to segwit much more difficult as all parties to an escrow transaction (the buyer, vendor, and moderator) would need upgrade before segwit could be used. This would also necessitate the need to build in more complex script negotiations to get all parties to agree on what type of script to use. By implementing segwit now we can, hopefully, reduce the fees users will pay to transact on OpenBazaar.

**Specifics**  
For multisig transactions OpenBazaar will use Bech32 encoded pay-to-witness-script-hash (P2WSH) addresses.

![](https://www.openbazaar.org/wp-content/uploads/2017/08/Segwit-Activated-What-It-Means-for-OpenBazaar.png)

The downside to using this address type is that many external wallets are not yet upgraded to send to these addresses. However, the OpenBazaar internal wallet is, so the worse case scenario if you don’t currently use a segwit compatible wallet is that you can send the coins into the OpenBazaar internal wallet and fund your transaction from there.

For the time being the internal wallet will continue to vend old-style pay-to-pubkey-hash (P2PKH) addresses. We would like to switch to pay-to-witness-pubkey-hash (P2WPKH) addresses but, again, few external wallets support sending to this address type and it would make it difficult for people to send money into the wallet. We could switch to using nested P2SH addresses, but this would be a very disruptive change to our codebase and the benefits aren’t really worth the cost at this point.

Once enough other wallets have enabled sending to P2WPKH we will switch the internal wallet over to P2WPKH. We’ve already done some prep work that will make the transition to the new address type seamless as the wallet will know how to detect payments to and spend from both P2PKH and P2WPKH addresses.

**Escrow with a timeout**  
One related change that we have made but never formally announced is that OpenBazaar2.0 will utilize bip-112 CHECKSEQUENCEVERIFY to add a 45 day (in blocks) timeout to escrow transactions.

One of the big pain points in OpenBazaar v1 was vendors having stuck funds when both a buyer and moderator went unresponsive. By adding a 45 day timeout to the escrow, the vendor will be able to unilaterally move the funds out of escrow and into his wallet after 45 days regardless of whether the buyer and moderator are active or not.

This leaves buyers with 45 days to file a dispute if they have issues with their order (less if they allot time for the dispute resolution process).

**The new scripts look like:**

`OP_IF  
2 <buyer_pubkey><vendor_pubkey><moderator_pubkey> 3 OP_CHECKMULTISIG  
OP_ELSE  
<6480 blocks> OP_CHECKSEQUENCEVERIFY  
OP_DROP  
<vendor_pubkey>  
OP_CHECKSIG  
OP_ENDIF`

If you have any questions or feedback feel free to drop by the [OpenBazaar Slack](http://slack.openbazaar.org/).

\[/et\_pb\_text\]\[et\_pb\_code admin\_label="Social (ALL)" max\_width="800px" disabled\_on="off|off|" \_builder\_version="3.0.53" custom\_css\_main\_element="margin: auto;" saved\_tabs="all"\]<div width="100%" style="margin: 0 auto !important;"><!-- \[et\_pb\_line\_break\_holder\] --><!-- \[et\_pb\_line\_break\_holder\] --><div class="a2a\_kit a2a\_kit\_size\_32 a2a\_default\_style"><!-- \[et\_pb\_line\_break\_holder\] --> <a class="a2a\_button\_tumblr"></a><!-- \[et\_pb\_line\_break\_holder\] --> <a class="a2a\_button\_facebook"></a><!-- \[et\_pb\_line\_break\_holder\] --> <a class="a2a\_button\_twitter"></a><!-- \[et\_pb\_line\_break\_holder\] --> <a class="a2a\_dd" href="https://www.addtoany.com/share"></a><!-- \[et\_pb\_line\_break\_holder\] --></div><!-- \[et\_pb\_line\_break\_holder\] --><!-- \[et\_pb\_line\_break\_holder\] --><script async src="https://static.addtoany.com/menu/page.js"></script><!-- \[et\_pb\_line\_break\_holder\] --><!-- \[et\_pb\_line\_break\_holder\] --></div>\[/et\_pb\_code\]\[/et\_pb\_column\]\[/et\_pb\_row\]\[et\_pb\_row use\_custom\_width="on" width\_unit="off" custom\_width\_percent="100%" custom\_padding="|10%||10%" padding\_mobile="off" background\_color="#f2f2f2" column\_padding\_mobile="on" background\_color\_1="#f2f2f2" parallax\_method\_1="off" parallax\_method\_2="off" parallax\_method\_3="off" parallax\_method\_4="off" background\_position\_1="top\_left" background\_repeat\_1="no-repeat" disabled\_on="off|off|" \_builder\_version="3.0.53" background\_size="initial" background\_position="top\_left" background\_repeat="repeat" custom\_css\_main\_element="border-top: solid 1px #ccc;||border-bottom: solid 1px #ccc;"\]\[et\_pb\_column type="4\_4"\]\[et\_pb\_text admin\_label="Medium Links (Desktop)" max\_width="1000px" disabled\_on="on|on|" \_builder\_version="3.0.53" background\_size="initial" background\_position="top\_left" background\_repeat="repeat" custom\_css\_main\_element="margin: auto;"\]

### Recent Updates

\[/et\_pb\_text\]\[et\_pb\_text admin\_label="Medium Links (Tablet)" max\_width="1000px" disabled\_on="on|off|on" \_builder\_version="3.0.53" background\_size="initial" background\_position="top\_left" background\_repeat="repeat" custom\_css\_main\_element="margin: auto;||padding-left: 10px;||padding-right: 10px;"\]

### Recent Updates

\[/et\_pb\_text\]\[et\_pb\_text admin\_label="Medium Links (Mobile)" max\_width="1000px" disabled\_on="off|on|on" \_builder\_version="3.0.53" background\_size="initial" background\_position="top\_left" background\_repeat="repeat" custom\_css\_main\_element="margin: auto;||padding-left: 10px;||padding-right: 10px;"\]

### Recent Updates

\[/et\_pb\_text\]\[/et\_pb\_column\]\[/et\_pb\_row\]\[/et\_pb\_section\]