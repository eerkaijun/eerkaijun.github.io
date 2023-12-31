## Work

### Monad

I'm currently working with the Monad team to build a fully on-chain limit order book. Fundamentally, the main advantage of an order book over an AMM is much lower slippage. However, order book has not really taken off due to the higher gas cost (AMM uses approximation in terms of pricing hence simpler computation). We believe Monad has sufficiently cheap gas to make an order book feasible. More to come soon.


### Arrow Markets

I previously worked with the Arrow Markets team to build a decentralized options protocol. We built both a vault model and also an AMM model. For the vault model, users lock their underlier (e.g. ETH) into a smart contract and are essentially the options writers. Option buyers can then purchase options by paying a premium, which are distributed to the options writers. For the AMM model, users can buy and sell options directly from the AMM. The AMM is bootstrapped with liquidity from the options writers.

My main learnings are decentralized options protocol are fundamentally difficult to scale. The vault model fragments liquidity. Each option has a different combination of strike price and expiration date, and users will need to choose which option to provide liquidity for, where their collaterals cannot be shared. In an AMM model, the AMM is usually undercollaterized for capital efficiency, however that also means that there is a possibility the option buyer might not be made whole during exercise, which is not acceptable in traditional markets. This [article](https://revv.xyz/writing/defi-options-mapping-hype-to-reality) is a great read on the topic.

Many teams have since pivoted to an request-for-quote (RFQ) model, where market makers quote the option price ooff-chain and the trust assumption is that market makers will always be the counterparty for option buyers to exercise their options.