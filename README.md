# GoodStrᵅ: Your Simple Web Store Solution
...with whisper addresses for enhanced privacy!

![GoodStr Logo](https://alpha.goodstr.io/assets/img/GoodStr_logoG.png)

**Empower your online business with whisper addresses for unparalleled privacy for you and for your customers.**

---

### Introduction

Ever thought of setting up an online store but got overwhelmed with the complexities? GoodStr is here to change that narrative. No more dealing with servers, payment gateways, or compromising your privacy. With GoodStr, you get a hassle-free, privacy-focused web store solution.

### What is this?

GoodStr is a solution to the following problem: we often wish we had a store where we could sell stuff, but then we remember how hard it is to set up a store. First you need a server -- which probably costs money, unless you self host one, which is hard -- then you need to set up the store, which means styling it, adding payment methods, connecting a bank account or paypal or stripe or similar (and dealing with their fees), then add shipping options, then add your products, then -- assuming you want to accept bitcoin too -- you've probably got to install some special software or a special plugin or give custody to some third party. And you also lose your privacy because you're probably giving your `xpubs` to those folks too.

---

### Why Choose GoodStr?

- **Simplicity at its Best**: Host on GitHub pages or run it locally. No server hassles.
- **Stylish Out-of-the-Box**: No need for custom styling (though we might add that feature soon!).
- **Bitcoin Payments**: No third-party payment processors. Just pure, decentralized Bitcoin.
- **Whisper Addresses**: Enhanced privacy with our unique [whisper addresses](https://github.com/supertestnet/whisper-addresses/) feature.
- **Self-Custodial Wallet**: Your earnings, your control. Withdraw anytime, anywhere.
- **Nostr Integration**: Say goodbye to traditional servers. With Nostr, you get a decentralized solution.

---

### Getting Started

1. **Visit**: Head over to [GoodStr](https://alpha.GoodStr.io) to begin.
2. **Backup Your Magic String**: This is crucial. It's your access key to manage your store and funds.
3. **Create Your Store**: Name it, add products, and you're good to go!

> **Important**: Always keep your magic string safe. It's the key to your funds and store management.

---

# What if there was a simpler way?
We're always innovating. Here's what to expect soon:

Nostr makes a lot of stuff that used to need a server not need one anymore. Or at least, you can often use a public nostr relay instead of a regular server. So wondered if we could make a simple webstore that removes almost all of the hassles experienced in the past. So behold GoodStr:

- [x] It's hosted on github pages, which is free and easy
- [x] Or you can download the index.html file and run it locally, also free and easy
- [x] You don't need to style it because it already looks great
- [ ] Ok that's a total lie, it looks like trash. Maybe we will add custom styling as a feature someday
- [x] You don't need to add a payment method -- we'll use bitcoin, which is free and easy
- [x] When you visit the store for the first time your browser autogenerates a nostr private key for you, which is free and easy
- [x] A bunch of bitcoin private keys will be derived from that nostr private key, which is free and easy
- [x] It uses my old [whisper addresses](https://github.com/supertestnet/whisper-addresses/) idea to preserve some of your privacy, which is free and easy
- [x] You just add products and shipping info and there is no other special software or plugins to run
- [x] It gives you a shareable link where anyone can visit your store, which is free and easy
- [x] It gives you a private link where you can manage your store, e.g. add more products or remove existing ones -- all free and easy
- [x] The built in bitcoin wallet is self-custodial and lets you withdraw your earnings whenever you want for free, and it's easy
- [x] If you notice an underlying theme here it's that running a store used to be costly and hard but this tool makes it free and easy

# How do we try it?

Just visit this link: https://alpha.GoodStr.io

You'll be guided through a simple three step procedure: first, backup your "magic string" (which is just your nostr private key and a set of default relays, hex encoded), then log in with it, then start creating your store. There is hardly any setup process for the store itself, you just name it and immediately start adding products. When you're done you'll get a shareable link where anyone can view your store.

Important! Save your magic string. It contains your private key which you'll need to access your money and manage your store. If you lose your magic string you lose your money. Keep it secret, keep it safe!

Also make sure you withdraw your money from the store frequently. The site uses whisper keys, which are sent to you in dms and not stored anywhere except on whatever relay you use. We don't trust nostr relays to store my dms forever so we recommend you withdraw your money quickly when you receive it, don't just let it sit there for weeks on end or the nostr relay you are connected to might delete your dms or go offline and leave you stranded without access to your money

# What are some upcoming features?

Not sure. Usually after we get a project to a state like this one is in we abandon it in favor of something else that's more exciting. But if we do keep at it I'd like to add these features:

- [ ] Give merchants a button to let customers set the price on an item (e.g. for "donation" items or "pay what you want" items)
- [ ] Include the product id with each product in a customer's order
- [ ] Create a uuid for each order and put it in the invoice description
- [ ] On a lightning payment's "Inspect transaction" link, instead of opening to lnbits, show a modal with instructions: "open lnbits, go to the searchbar, type this in"
- [ ] Educate merchants about resources like thebitcoincompany.com where they can use their earnings to buy visa gift cards -- e.g. merchants with a fiat webshop can load a visa card via bitcoin and unload it as usd in their regular shop, thus putting their bitcoin earnings into their regular workflow
- [ ] Make a downloadable version with a rest api
- [ ] Custom ordering -- people have complained that the order in which products appear on their frontend does not match the order in which they appear on the backend, and they'd also like to be able to set them in a particular order without needing to copy/paste stuff between different boxes
- [ ] Custom styling -- people like to make things look nice and feel like it's themed after their regular blog or website or whatever. Ok cool but visual flare isn't very important to me so maybe someone else can add code for that. Do a pull request!
- [ ] An aggregator -- what if the shop client aggregated all the products that ship to your region and displayed them all on one page regardless of who the actual merchant is? That could be super cool, like a craigslist but on bitcoin+nostr! Plus you could have categories and e.g. just browse all the offers by people who sell gift cards, or browse all the offers by people who want to trade fiat for bitcoin, etc.
- [ ] Ratings -- these would become very important if there was an aggregator service but they are a frequent request anyway, even without that. We hesitate to add ratings because we don't know a good way to do them on nostr (they are easy to spoof and we don't currently know a decent way to filter out spoofs -- someone tell me how to do it!)
- [ ] Celebrity escrow -- we think it would be cool if merchants could list several bitcoin celebrities who they are ok with using as an escrow agent. People like Matt Odell or Peter McCormack could advertise that they are willing to play the role of an escrow if anyone wants to use them as one. Then users could add them as an escrow by including their nostr pubkey as 1 of 3 keys in a multisig. Most of the time, this escrow option would probably not be used, so the escrow agent may never even even know their services were enlisted. But if the two parties can't agree on what to do, they can DM their escrow agent and say "Hey we used your key in our bitcoin transaction and now we have a dispute, please side with me/them!" It would be so cool, and very useful if people start using this for fiat-to-bitcoin trades
- [ ] Satoshi escrow -- many years ago Satoshi had an idea to do escrow without a third party. His idea was that you could put money in an address that your counterparty can withdraw from only if you give them a secret piece of data. Then you withhold that secret piece of data til they send you your product. If they never send you the product, you're out of luck, but at least they don't get to run off with your money. It would be pretty easy to modify GoodStr to support this -- right now your browser DMs the whisper key to the seller as soon as you pay, but if we just DM'd a proof of knowledge of that key instead, you could wait til the seller delivers your product before actually giving him or her the key that actually lets them access the money
- [ ] The hebrew hodl -- another model of escrow without a third party is where the buyer and the seller both deposit the full value of the trade into a 2 of 2 address. Then they've got each other by the balls, so to speak, because either one can burn the other one's money. (The name "hebrew hodl" comes from a passage in the bible where Abraham and his servant swore an oath to each other which, in part, involved one of them letting the other one grab him by the balls to prove he had complete confidence in him.) So they'd better not have an irreconcilable dispute or both will lose their money. The only way both make it out ahead is through cooperation. We am thinking about adding all of these escrow models as options that merchants can advertise support for so that users can select one if they don't fully trust the seller.
- [ ] Connect your node -- right now GoodStr gives you an lnbits account but that is probably not a very scalable model and it's also custodial, meaning everyone will probably eventually get rugpulled by lnbits. To fix that, we want to make it easy for merchants to connect this app to their own node, that way they can only rug themselves. We hope to do this by writing an LND wrapper that lets you expose the "getInvoice" function and the "checkInvoice" function over nostr. We'll see how that goes
- [ ] Add more items to this upcoming features list -- yes, this is a meta feature, but we don't want to think about more stuff to add to this list so just write an issue so we can think about it ok?

# Things that used to be upcoming features but are now added (or fixed, if they were bugs)

- [x] Better nostr connections -- about a third of the time when we load this page we don't actually get a connection to the nostr relay we use. It just sort of times out and an error message appears in my console. The user has no visiblity into this, the site just doesn't work (and if you're trying to view a store it just won't populate) which is super frustrating. It typically works when we refresh but we can automate that without refreshing the page so we should do that. (I should also add automatic reconnection logic in case the connection drops.)
- [x] Lightning support in a complex way -- we can probably add lightning support through submarine swaps so that the money *actually* goes into one of your regular addresses. But if we do that, it probably won't be very pretty, and it will probably confuse people because their wallet will say their payment is pending for a very long time while we wait for the buyer to come online to finish the submarine swap
- [x] Lightning support in a simple way -- we can ask sellers for a lightning address and then pull invoices from that to display to buyers. This is very easy to do but it comes with several wrinkles. One is, the page won't be able to automatically detect the payment status because we can't check the blockchain when you do a lightning payment, lightning payments are only visible to the buyer and the seller. Since we can't tell whether the payment happened we can't automatically give users a receipt with their proof of payment. Users will have to press a button to generate their receipt and just accept that it does not contain a proof of payment (but they'll probably have one on their phone so that's probably okay). Also, I'm a bit ambivalent about lightning addresses. We like them because they offer an excellent user experience. But they are such a pain to actually set up in a self-sovereign way that almost everyone uses a custodial one. That feels icky. We like that the way whisper addresses work and it seems like lightning addresses are very far removed from that. So we hesitate to add support for them. But maybe. Keep hammering at me for support.
- [x] Ok the above two are a bit wrong now. We added lightning support, but not through the simple way *or* the complex way. Instead we decided to generate an lnbits account for every user and publish their invoice key on their store. That way buyers can use the merchant's invoice key to generate invoices and check if they are paid. The downside is, any buyer can also see your lightning balance and your transaction history. Eventually we plan to add support for connecting this to your own node and if we do that we plan to make it more private.
- [x] Add custom relays -- users are no longer limited to just one hardcoded relay. There are now three hardcoded relays, but they appear as a query parameter in your store url so you can easily change them if you want to use different ones.
- [x] Portable shipping status -- previously when you click Shipped on an order, GoodStr stored the fact that you shipped that product in your browser's local storage. If you did that on your computer and then went to manage your store on your phone, your phone wouldn't know you shipped the product, so it would still show it as needing to be shipped. (Unless the money went into a bitcoin address and then you withdrew it.) Now we made it so that when you click Shipped on an order, GoodStr sends a dm that references the shipped order in a tag, and then if you switch devices GoodStr can load those dms and thus know which orders you shipped.
- [x] Better error handling -- sometimes mempool.space's api starts rate-limiting you, which causes errors, which can stop the page from running. Worst case scenario: you just paid for an order when the page crashes and you lose your money forever.
- [x] Change "sign up" to "get started"
- [x] Revise homepage to look more like an altcoin website such as getmonero.org -- they really know how to make a site look nice

---

## Contribute

GoodStr thrives on community contributions. Whether it's code, design, or feedback, every bit helps. Check out our [contribution guidelines](#) to get started.

---

## Support & Community

Got questions? We've got answers. Dive into our [FAQ](https://alpha.GoodStr.io/onboarding.html#faqs#) or join our vibrant [community](https://bolt.fun/project/goodstr) for support.

---

## Credits

- Design & Coms: https://SuperAtic.com
- Illustrations: https://UnDraw.io
- Fonts: https://fonts.Google.com
- Engine: https://github.com/supertestnet/superstore/
- Matrix: https://archive.ph/iBAr8


## License

This project is licensed under the XYZ License - see the [LICENSE.md](#) file for details.

---

**GoodStrᵅ - Simplifying E-commerce, One Store at a Time.**

---
