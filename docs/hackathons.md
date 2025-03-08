## Hackathons

Hackathons are a great way to experiment with new ideas and toolings. They are usually proxies for me to try out things that I have very little experience in.

### ZK Hack Krakow 2024

UTXO note discovery is a difficult problem to solve for privacy-preserving protocols. For a user to know its balance, the common way is to use its private key to trial decrypt all the UTXO note commitment that exists and compute the balance. The time needed for trial decryption grows linearly as number of UTXO notes increases. We implement a private information retrieval scheme for searchable note indices while maintaining privacy.

ZK Hack once again proves to be a very high quality event for experimenting new things. We won the second overall prize, project details below:
- [Github](https://github.com/eerkaijun/utxo-discovery)
- [Project submission](https://devfolio.co/projects/private-utxo-discovery-6673)

### ETHGlobal London 2024

A solo hack this time where I worked on an MPC protocol on Flashbots SUAVE chain. The idea is that a user will be able to delegate shards of its signing key into different SUAVE nodes, where each node is actually operating a trusted execution environment (TEE). Each time the user would like to submit a transaction, it will simply send the transaction calldata to SUAVE, where the signing key is reconstructed through Shamir secret sharing and used to sign on the calldata. This signed transaction can then be relayed to other chains. As such, the notion of private keys can be abstracted from the users. 

I won two prizes from Flashbots and Nethermind respectively. I've been wanting to try out SUAVE for quite a while and finally getting the chance to do so. More details on the project below:
- [Github](https://github.com/eerkaijun/suave-mpc)
- [Project submission](https://ethglobal.com/showcase/suave-mpc-16pmz)
- [Bite-size Twitter thread](https://x.com/kaijuneer/status/1769473343181254724)

### ZK Hack Istanbul 2023

This is by far one of the best hackathons that I've been to - good quality of hackathon participants and awesome teammates. We wrote low-level cryptographic primitives that reduce a SNARK proving system into a multivariate polynomial problem, which is further reduced through the sumcheck protocol and then eventually transformed into a univariate polynomial. The high level motivation for such transformation is that polynomial commitment scheme such as KZG works better with univariate polynomials than with multivariate polynomials. We also implemented a simplified version of the Spartan SNARK proving system as a proof of concept.

We won the **Chewing Glass** prize which is the top prize for the technical track. I owe it to my two cryptographers teammates who taught me so much - I'm familiar at writing ZK circuits but this is my first time writing such low-level cryptographic circuits (down to even hand-coding the polynomial maths)!

Details of the project is well documented in the Github repository, more information below:
- [Github](https://github.com/gy001/zkhack23)
- [Devfolio submission](https://devfolio.co/projects/hello-hypercube-90c8)


### ETHGlobal Lisbon 2023

When users withdraw funds from a shielded pool or privacy preserving rollup, the best option to ensure privacy is to withdraw the funds to a fresh address, meaning no previous transactions have been done on that address. However, without ETH for gas fee, the fresh address is not able to submit a transaction on-chain to withdraw funds.

We implement an ERC-4337 compatible paymaster that pays for the deployment of a smart account and the gas fee for the funds withdrawal. The user can generate the ZK withdrawal proof as usual, then parse this proof to be the paymaster data in the correct format. Subsequently, the user then submits a UserOp operation for the bundler to execute the transaction.

We won the **Best Account Abstraction Hack** by Ethereum Foundation. I'd been reading about account abstraction for a while but this was my first time being hands-on and playing around with it. More details below:
- [Github](https://github.com/eerkaijun/private-paymaster)
- [Project submission](https://ethglobal.com/showcase/privacy-preserving-paymaster-hap9s)
- [Bite-size Twitter thread](https://x.com/kaijuneer/status/1657863686336200705)


### ZKP Online Hackathon 2023

We built an SDK that allows developers to easily build private DeFi primitives. The SDK contains ZK circuits of a multi-asset shielded pool, client side library to generate the ZK proof, and smart contracts to verify these proofs on-chain. The SDK is designed to be modular and extensible, allowing developers to easily customize features of the shielded pool. Some out-of-the-box capabilities supported by the shielded pool include depositing and withdrawing, tranferring and swapping assets privately.

We won the **first prize** for this hackathon. It's a three weeks long hackathon and by far the one where we built the most extensive and production-ready project. Architecture is well documented in the Github repo, more details below:
- [Github](https://github.com/blockhackersio/zrclib/)
- [Project submission](https://devfolio.co/projects/zrclib-3d7c)

### Others

The above are the ones that I found the projects to be the most interesting. I've also participated and won prizes in a few other hackathons, but to spare you the boredom, feel free to just check out my Github!
