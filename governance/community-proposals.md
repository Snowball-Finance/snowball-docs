# Community Proposals

Snowball is democratically governed by the community through its governance protocol. To vote, you must lock SNOB tokens for xSNOB. One xSNOB is equal to one vote, but fractional votes are allowed.

![](../.gitbook/assets/xSNOB\_4.png)

## Proposals

Anyone with xSNOB tokens can vote on Snowball proposals. For a proposal to pass, there are a few conditions that must be met:

* There must be a minimum of 300,000 votes in favor of the proposal.
* There must be more votes in favor than those against the proposal.

Your vote can be changed after voting in case you've changed your mind.

In order to create a proposal, you must hold a minimum of 50,000 xSNOB. If you do not have the required minimum number of tokens, someone who does can execute the proposal on your behalf. You may only have one active proposal at any given time.

## Submission Process

Anyone with the sufficient xSNOB balance can submit a proposal, but in order to be able to get the votes required to pass it they would need the community's support. This is why, generally speaking, there are some simple stages a proposal goes through prior to being submitted through Snowball's governance smart contract.

### Stage 1: Discussion

At this stage, someone has had an idea regarding something the protocol could do or do better. Many times this is a simple suggestion, and is forwarded to the Snowball team or a community member to implement. If it is a large change in the protocol's functioning, involves treasury expenditure or would affect user funds, it is appropriate to become a proposal for the community to vote on.

We have a section on our [**Discord Server**](https://discord.gg/BPnBYDSqcb) for these discussions to take place, appropriately named 'Governance'. The #town-hall channel can be used to gauge interest and suggest creating a new channel for such discussions. If there is enough interest in the proposal and many community members have voiced their opinions, it can move to the next stage.

### Stage 2: Sentiment Voting

Now that we have observed interest in the proposal in question, we can go through a simple unofficial sentiment vote to see where the community stands. This can be as simple as a post asking people if they are for or against the proposal.

On Discord community members can 'react' with emotes to clarify their position. We can use checkmarks and crosses, numbers for different options, yes/no emotes, anything at all. Other types of off-server polling is acceptable, but might not get the same engagement.

Based on the outcome of the vote, the proposal can be altered and this process can be repeated. If the outcome is positive, there is a large change of the proposal passing if it were to be submitted. Therefore, this is the next logical step.

### Stage 3: Submission

The proposal submission needs to be done by a wallet with at least 50k xSNOB. It could be submitted by someone on behalf of someone else, but on-chain delegation is not available yet. The easiest way to submit a proposal to Snowball's governance contract is through [**here**](https://snowtrace.io/address/0xfdCcf6D49A29f435E509DFFAAFDecB0ADD93f8C0/write-contract#writeContract).

A proposal should include the following items:

* **Title** - A string containing the title of the proposal. Keep this short.
* **Metadata** - This should be a link to a detailed explanation of the proposal. If possible, this should be hosted through IPFS. Here's an [**example**](https://ipfs.snowapi.net/ipfs/QmRQZvu35LriBZZrbhNiZo9yBooBV97uBR3xHTM83SHsaV) of what that would look like.
* **Voting Period** - The duration the proposal should be open for voting. This is a value in seconds, and must be equivalent to at least 3 days.
* **Target** - This is the address of the target contract. Snowball's treasury, for example, would be a common target for proposals to interact with.
* **Value** - If the proposal is a specific transaction to take place, and has an inherent value to it, use this input. Otherwise, simply use 0.
* **Data** - If applicable, these are the encoded bytes for a transaction being proposed. If the proposal cannot be executed entirely on-chain, simply use 0x00.

A successfully submitted proposal will be automatically listed on-site as well as on-chain, and the community will be able to vote on their preferred outcome for the proposal. Announcements on Twitter and Discord, alongside discussion channels can be made in order to bring attention to and discuss active proposals.

## Timelocks

Every proposal must have a voting period of at least 72 hours. Once the voting period comes to an end, there is an execution delay of 24 hours prior to any technical changes to the Snowball protocol.

Every proposal also has an execution window of 14 days (2 weeks), after which the proposal is considered void.

## Community Proposals Resources

{% content-ref url="xsnob/" %}
[xsnob](xsnob/)
{% endcontent-ref %}

{% content-ref url="../faq/xsnob-faq.md" %}
[xsnob-faq.md](../faq/xsnob-faq.md)
{% endcontent-ref %}
