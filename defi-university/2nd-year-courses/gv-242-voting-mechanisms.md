# GV 242 - Voting Mechanisms

Decentralized autonomous organizations have had the chance to experiment with various different types of voting mechanisms in their path to creating effective governance structures. This course will look at the following aspects of these voting mechanisms:

* Exploring Types of Voting Mechanisms
* Pros and Cons of Each Voting Mechanism

#### Suggested Prior Reading:

{% content-ref url="../1st-year-courses/gv-141-daos.md" %}
[gv-141-daos.md](../1st-year-courses/gv-141-daos.md)
{% endcontent-ref %}

## Introduction

Any society or organization, when migrating from dictatorship-like governance structures to more democratic or community-based approaches has to decide on a voting system that works for them. This revolves around the fact that by querying for the community's needs and wants, you can more effectively govern it.

In DAOs this factor is even more prevalent, since communities can essentially self-govern instead of only using these mechanisms to elect leaders. This means, however, that the effectiveness of its governance structures are even more important. An ineffective, inaccurate and/or easily exploitable voting system will lead to a failure in enacting policies that benefit the DAO.

Traditional voting mechanisms have much room for improvement, and on the bleeding edge of these decentralized ecosystems are DAOs experimenting with each and every new type of voting system people can think of. Let's look at some voting mechanisms that have been used or theorized and point out what they bring to the table:

## Token-Based Voting

The premise behind token-based voting is simple:

$$
\text{1 Token = 1 Vote}
$$

This governance token is usually a liquid asset that represents voting power for a particular DAO. This mechanism works due to directly aligning the success of an organization to financial incentives for its voters. A user wanting to intentionally vote on nefarious proposals or vote against good proposals would risk negatively affecting the organization, which would have negative repercussions on the value of the tokens they are holding.

In this type of voting mechanism, proposals are usually considered 'passed' or 'accepted' if the majority of votes are in its favor. Most DAOs also implement a certain amount of votes necessary for the proposal to pass - usually referred to as a 'quorum' - in order to prevent malicious proposals from passing unnoticed.

As simple and effective as this can be - especially at small scale - there are many downsides to this methodology. Depending on how the quorum is selected, it could be difficult to achieve, requiring an extremely active community in order to pass any proposal. Not only that, but the issues that come with uninformed voters become quite prevalent. If not a lot of effort is put in to ensure all members of the organization know exactly what they are voting for, many voters will vote blindly in order to simply achieve the required number of votes.

While these aspects can be managed, perhaps the biggest criticism of token-based voting is how the mechanism allows for voting power to be concentrated for the wealthy among the organization. It is a simple fact that the more funds you have invested, the more voting power you will have. Not only that, but a malicious actor may buy voting power, use them and immediately sell their voting power in order to not be hit by any financial repercussions of whatever they voted for.

There are ways, albeit imperfect ones, to deal with these issues. Snowball requires users to lock their SNOB (our governance token) for a specific amount of time in order to acquire voting power. This prevents the sudden buying and selling of voting power by outsiders wishing to manipulate votes. Other ways of dealing with this could involve vesting contracts, or other time-based approaches to distribution.

The amount of voting power acquired in this mechanism is also relative to how long the user locked their tokens for. This doesn't completely eliminate the issue regarding concentration of voting power, but it means that someone with less funds could potentially acquire similar or more voting power than someone with more funds if they are more committed to the organization in the long-term (locked their tokens for longer).

## Liquid Democracy

The concept of a liquid democracy involves, as the name suggests, a more liquid distribution of voting power. In practice, this means that members of an organization can delegate their voting power to someone else (a delegate), and have that person represent their interests within the organization.

In order for such a mechanism to work adequately and scale to a sufficient level a few structural components must be in place:

* There must be little to no barriers in place for someone to become a delegate.
* The actions of those delegating their votes should be as anonymous as possible.
* The actions of delegates should be as public as possible.
* There should be no fee or penalty to re-delegating voting power.

If all these components are implemented well enough, it allows voting power to be distributed efficiently to well-informed members of the community who are able to represent a portion of its interests. Delegates could also be able to delegate their combined voting power to another specialist if any proposal involves an area they are not familiar enough with, for example.

While this approach focuses on enabling well-informed decisions and votes to take place, it runs the risk of becoming too centralized if the number of delegates fails to scale appropriately. This is an intrinsic problem within blockchain and other decentralized technologies, however, and puts much emphasis on community-building. For example, as Avalanche grows in usage and utility, it would require more validators in order to scale in a decentralized manner. The same concept applies here.

## Quadratic Voting

This voting mechanism approaches the problem of the concentration of power to the wealthy from another angle. In short, it increases the price of additional votes on any given proposal. See the following table:

<table><thead><tr><th data-type="number">Vote Number</th><th data-type="number">Token Cost (x^2)</th></tr></thead><tbody><tr><td>1</td><td>1</td></tr><tr><td>2</td><td>4</td></tr><tr><td>3</td><td>9</td></tr><tr><td>4</td><td>16</td></tr><tr><td>5</td><td>25</td></tr></tbody></table>

The cost would continue to climb after the 5th vote, but the same logic applies.

This means that someone with 25 tokens would be able to apply a voting power of 5 votes to any given proposal, while someone with 4 tokens would be able to apply a voting power of 2, for example. Similarly to more standard token-based voting mechanisms, it aligns economic incentives to a user's vote, but limits the impact of extremely wealthy investors from having too much concentration of power.

Where quadratic voting really excels is during proposals where gauging interest for each option proposed is more important, rather than simple yes/no outcome votes. This is because users could assign how many tokens they would like to use to vote for each option based on how much they approve of them, and the quadratic aspect of voting power distribution means that the number of users who approve of any given option is more important than any particular vote weight applied to them.

This also makes quadratic voting the perfect mechanism to vote on items such as public goods funding. On such things - from a utilitarian perspective - one would look for a voting method that would reflect the needs and wants of as large a proportion of members as possible.

A glaring downside to this voting mechanism is its need for an sophisticated method of identifying unique users. A Sybil attack, for example, is where malicious actors create fake identities in order to exert disproportional influence over a network. In the context of a quadratic voting mechanism, this would mean making multiple wallets and voting with them in order to get more votes out of held tokens.

This attack vector can be mitigated with implementations such as staked asset requirements to vote, the use of centralized IDs or even some form of whitelisting that takes place before each proposal, with the user's knowledge or behind-the-scenes. None of these solutions are perfect, however, and could diminish the ability of legitimate members of the organization from participating in governance.

## Conviction Voting

Conviction voting is a very interesting take on voting for very active communities with a lot of proposals up at any given time. This is because it allows users to split their voting power in accordance to how much they support any given proposal, and those with the most interest from the community will pass.

To exemplify this voting mechanism, let's say there are two proposals live, A and B. A user with 100 'voting power' (this could be distributed in a number of ways) can assign 20 votes to proposal A and 80 to proposal B. This would mean that they approve of both proposals and wants them to pass, but thinks proposal B is much more important and should be implemented beforehand. Every X amount of time, the number of votes on proposal A would increase by 20, and the number of votes on proposal B would increase by 80. This leads to the following taking place:

* If the proposal reaches a specific number of votes, it passes.
* If the proposal fails to reach a specific number of votes by a given time, it fails.

The time limit on proposals, as well as the time per tick on votes added should be determined by the organization, and could be dynamically selected. The system should also allow for users to change their votes at any given time. If the user moves their 20 votes from proposal A to proposal B, for example, since their votes have gone from 20 -> 0 on proposal A, the vote amount on the proposal would decrease every tick instead of increasing.

This relatively complicated voting mechanism achieves many interesting outcomes. Primarily, it eliminates sudden shifts in vote outcomes due to large investors jumping in, in exchange for requiring users' voting power to be 'used up' during voting periods. Users could always withdraw their tokens, but that would result in their votes slowly draining out of the proposals they've supported.

This method of voting also makes it much more expensive to purchase voting power or bribe others to support certain proposals. This is because this system values long-term support more than any short-term investment into acquiring voting power.

The downsides with conviction voting mechanisms lies in its implementation. Due to its complexity, it is harder to implement, and even harder to communicate its functionality and utility to an organization's members. It also makes it relatively difficult to pass proposals quickly, even with overwhelming community support. This is because the larger the time limit or number of votes needed, the more secure and effective it is at preventing any potential attack vectors and malicious actors from manipulating its results. Any attempt at passing a proposal quickly by lowering these factors would be risky.

## Closing Thoughts

These are some of the most interesting voting mechanisms being explored by DAOs in the last few years. Perhaps some are happy with what they've created, or maybe the perfect solution is a mixture of many of the mechanisms explored in this course. I guess we'll see when even more experiments take place, and communities perfect their governance systems. Cheers to the future of decentralized governance systems!
