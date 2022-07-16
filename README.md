# tokenomics and governance of 2i2i - draft version - details could still change

2i2i is to be a DAO, governed and owned by the tokens of the DAO. this document is about those tokens.

## governance

governance is the act of making decisions for the system. the process of decision making is voting. each gov token will count equally towards the available options in a vote. proposals should generally be formulated such that there is a 'change' option and a 'no change' option. the 'change' option can have a required threshold (>= 50%). if the threshold is not met, the system remains unchanged. this lends the system stability and changes are only enacted if perceived as valuable enough.

we can have our governance completely on-chain, unlike the current governance of Algorand. to avoid double voting and without the possibility of querying transactions within an on-chain contract, the gov tokens need to be locked in the contract as long as voting is open.

at first glance, the locking of gov tokens seems restrictive towards the voter. this can be alleviated via the 'receipt' token.
when a voter locks their coins in the governance contract, they receive 1:1 receipt tokens in exchange. these tokens can be exchanged back to the gov tokens anytime after the voting period has ended.

should the receipt tokens be tradable? i.e. should the voter be economically bound to the gov token after declaring their vote?
both options are possible

### receipt tokens are frozen

there is an argument that 'freezing' gov tokens is essential so accounts do not acquire the tokens, vote with malintent and immediately sell them; all this to harm the project or for trading gains.
if this is the overriding thinking of the project, they can simply have the receipt tokens frozen in the account.
Algorand has this requirement for it's own gov tokens, but solves the problem without receipt tokens because it counts the votes off-chain.

### receipt tokens are not frozen

there are some arguments as well to allow trading of gov tokens after submitting one's own vote publicly but before the voting period has ended.

since the vote would be public, in theory, the malicious actor has no inside information. the market could react just as quickly as the malactor after their single vote. the malactor would need to acquire gov tokens, at a high cost assuming they buy a vote influencing amount. after voting and receiving receipt tokens, they could sell the receipt tokens, which again requires a high cost. the malactor only benefits if their vote is detrimental to the system and they sell their receipt tokens faster than the market and overcome the loss from buying and selling a large position.

on the other hand, for normal actors, a tradable receipt token represents freedom. they can vote and immediately use the receipt tokens elsewhere in DeFi instead of losing out. this makes voting a low and fixed cost effort.

rather than requiring accounts to freeze their gov tokens during long periods (e.g. months), we only need locking during the voting periods, which is a more precise solution. each vote is independent.

### on-chain voting

other contracts, like e.g. an update contract, can depend on the result of a vote by asking the governance contract about the result.
the governance contract keeps the vote tally in it's own global state.
if the governance contract confirms the vote result for 'change', the update contract can update the system contract. in fact, the vote should be based on the update contract. voters are voting to allow or disallow the running of the update contract. this gives the community true power over the system code.


## optimised tokenomics

since we cannot setup perfect tokenomics from the beginning, we should allow changes to tokenomics.
let's treat tokenomics as an optimisation problem. we change parameters of our tokenomics and observe changes to a metric that we want to maximise.
we use some optimisation algorithm to dictitate the next set of tokenomics parameters. and thus we continue until we reach an optimum.
in my opinion, an algorithm that works very well with multi-dimensional 

the parameters that can be changed would be the percentages of the tokens that are allocated for certain purposes.

changes to the tokenomics are generally controlled by the DAO, i.e. governance, i.e. the DAO token holders themselves, excluding the treasury itself.

the optimisation has to include restrictions, such as not allowed the increase of the team allocation, as the team initially holds the majority voting power and could keep increasing their share.

the currently proposed metric to optimise is **TVL growth**.

summmary
every aspect of tokenomics can change via governance except to increase team shares.

## fixed parameters of tokenomics

none of the tokens can be frozen or clawed back.

20% is given to the team and can never increase. these are vested as follows: blockwise, second granular, linear unlocking via a smart contract with full unlocking after 2 years.

## initial parameters of tokenomics

ecosystem incentives - should be largest share of tokens - distribute over 5-10 years
activity rewards
contributor rewards
liquidity providing rewards
partnerships
borderless split:
15-25% team
10-20% seed sale
5-10% strategic sale
2.5-5% public sale
5-15% treasury
35%-45% ecosystem
