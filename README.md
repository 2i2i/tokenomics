# tokenomics of 2i2i - draft version - details could still change

the project is to be a DAO, governed and owned by the tokens of the DAO. this document is about those tokens.

## optimised tokenomics

since we cannot setup perfect tokenomics from the beginning, we should allow changes to tokenomics.
let's treat tokenomics as an optimisation problem. we change parameters of our tokenomics and observe changes to a metric that we want to maximise.
we use some optimisation algorithm to dictitate the next set of tokenomics parameters. and thus we continue until we reach an optimum.

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
