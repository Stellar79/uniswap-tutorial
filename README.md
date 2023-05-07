# uniswap-tutorial

## white paper summary of any versions
### V1
- Introduction to Uniswap
Uniswap is a decentralized exchange (DEX) built on the Ethereum blockchain. Instead of using an order book like centralized exchanges, Uniswap employs an Automated Market Maker (AMM) smart contract to facilitate the swapping of two assets, such as ETH and ERC20 tokens.
- Swap Mechanics
Token prices in Uniswap are determined algorithmically using a constant product formula (x * y = k). For example, if there are x ETH and y ERC20 tokens (token0) in a liquidity pool, the price will depend on the reserves of the two tokens. When swapping Δy token0 for Δx ETH, the following formulas apply:

x_after = x_before + Δx - (0.3% * Δx)
y_after = k / x_after
Δy = y_before - y_after

The price will be higher when demand increases (reserve decreases). When swapping two ERC20 tokens (token1 and token2), ETH acts as an intermediary.
- Liquidity Providers
Liquidity providers deposit an equivalent value of ETH and ERC20 tokens into a token's associated exchange contract. They earn fees from trades that occur in their pool as a reward for providing liquidity.
- Liquidity Tokens
When liquidity providers add liquidity to a pool, they receive liquidity tokens representing their share of the pool. The amount of liquidity tokens minted is calculated as follows:

amountMinted = ethDeposited / ethPool * totalSupply

- Removing Liquidity
Liquidity providers can withdraw their share of the pool by burning their liquidity tokens. The amounts of ETH and tokens withdrawn are determined by the following formulas:

ethWithdrawn = amountBurned / totalSupply * ethPool
tokenWithdrawn = amountBurned / totalSupply * tokenPool
