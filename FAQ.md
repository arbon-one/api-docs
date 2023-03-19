# FAQs about Arbon, carbon offsets, tokenisation

Do you have a question that you don't see answered here? [Send us an email](mailto:contact@arbon.one) or a DM on [Twitter](https://twitter.com/arbon_one)

## What is this receipt?
- Your Arbon receipt is verifiable proof that a carbon offset was permanently retired on your behalf. It shows the amount of tCO2e that was removed from the atmosphere as a result of the activity that you funded.
- You can verify that it’s yours because of the “Reason” text which contains the unique descriptor that you or the business you bought it from entered when requesting the offset. Depending on how you bought it, this might be a transaction ID, your customer ID with the business, or some message you wanted to put in there, like “Nik’s annual offset”.
- You can verify that this receipt represents a retirement that actually happened because each receipt links to the blockchain transaction where a CO2 token (see below) was “retired” to create the offset. You can find out more about this blockchain transaction and how to interpret it [here](https://github.com/arbon-one/api-docs/blob/main/how-to-read-coorest-transaction.md).

## What happened when I made the offset?
You make a request for a particular amount of tCO2e to be offset. We buy a corresponding amount of CO2 tokens (see below) and instruct the blockchain to destroy these tokens. The record of this instruction, and the record that it happened, is called a ["transaction"](https://github.com/arbon-one/api-docs/blob/main/how-to-read-coorest-transaction.md). This transaction will also contain a description for why the offset happened, and is visible to anyone who wants to look at it.

## What is tCO2e?
Greenhouse gases come in many forms. Carbon dioxide (CO2) is the most well-known, but other gases (including methane, nitrous oxide etc) also cause the atmosphere to trap more heat and thus lead to global warming. Each gas has a different effect size per ton - a ton of methane traps 25 times as much heat as a ton of CO2, for example. In order to make it easier to compare the effectiveness of various greenhouse gas-reducing activities, we convert everything into “tons of CO2 equivalents (tCO2e)”. To continue the example, the removal of one ton of methane would lead to the removal of 25 tCO2e.

## What is a carbon offset?
- A carbon offset is produced when a project reduces the amount of carbon in the air. More specifically, when a project’s claim to have done so is verified by an independent body who can then authorise the creation of the offset.
- These claims are based on the project’s particular characteristics - perhaps they have planted an area of forest, perhaps they have captured carbon from the air and turned it into rocks. Each approach has its own method for estimating the carbon captured, that can then be claimed as an offset.
- Offset claims are independently verified, and increasingly they are measured in real-time by remote sensing technologies such as satellites, drones and internet-of-things devices. Only after this verification is an offset claim available for purchase.

## What is a carbon offset token, or CO2 token?
A token is a representation on a blockchain of a carbon offset claim (see above). These tokens have either been created on the blockchain specifically to represent the claim from the outset, or they represent off-chain offsets which have been brought onto the blockchain via a bridge.

## What is a blockchain?
- A blockchain is a virtual computer made up of dozens of different computers run independently of each other (each of these is known as a “validator”). They coordinate each operation that the computer executes by ensuring that only instructions signed by the correct cryptographic keys are allowed. Because there are so many independent validators, if any of them tries to do an unauthorised operation, the others will catch it. Every operation is recorded as a “transaction” and these are publicly visible via block explorers such as Polygonscan or Etherscan.
- Blockchains can be used to mint, exchange, and destroy virtual “tokens”, which are held by “accounts”. Each account has a cryptographic key, and only someone who knows that key can authorise transactions using the tokens held by that account. These tokens are also governed by certain rules which specify things like who can mint tokens, how many are allowed to exist at a given time and so on. All of these rules, as well as which accounts hold which tokens, and any token transactions, are all publicly visible via a block explorer.
- The upshot of the above properties of a blockchain is that once you code a system to work in a particular way, there are many people (validators) incentivised to ensure that it continues to follow the code, and anyone can inspect the record to verify that it did work as expected. This means there is no need to trust any single person or company’s word on the matter.

## What is a block explorer?
Each public blockchain (like Bitcoin, Ethereum, Polygon, Avalanche etc) has its own “block explorer”. These are sites where you can search for any transaction, account, block or token and inspect all of its properties. As this data is open to anyone running a blockchain node, there are usually multiple block explorers for each blockchain that you can use to surface the same data.

## Doesn’t using a blockchain generate more emissions?
- Not any more! Early blockchains, including Bitcoin, the first blockchain, relied on a procedure known as proof-of-work to ensure consensus among the nodes who make up the blockchain. This requires huge amounts of computing power to operate, and therefore electricity to power those computers.
- More recent blockchains such as Polygon, Celo and since September 2022, Ethereum, use a procedure called proof-of-stake, which uses 99.5% less energy than proof-of-work. Using these blockchains is no less energy-intensive than using the internet, and Polygon (where Coorest tokens are stored) is in fact carbon-neutral.
