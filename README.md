# Compound-V3-Liquidator-Smart-Contract
A Solidity smart contract designed to efficiently and securely liquidate under-collateralized positions on the Compound V3 decentralized lending protocol. This project demonstrates a deep understanding of DeFi mechanics, on-chain interaction, and smart contract security best practices.

## Description
The liquidator contract monitors the health of borrower accounts on Compound
V3. When an account's health factor drops below a predetermined liquidation threshold, the contract automatically executes the liquidation process. This involves repaying a portion of the
borrower's debt and, in return, acquiring a discounted amount of their collateral, thereby generating a profit. The entire process is handled in a single, atomic transaction to mitigate risk.

## Key Features
* **Health Factor Monitoring:** Programmatic logic to calculate borrower's health factor
and identify
eligible positions for liquidation.
**On-Chain Interaction:** Secure
and
direct calls to the Compound
V3
protocol's liquidate function.
**Profitability Check:** A pre-execution check to ensure the liquidation is profitable, accounting for gas costs and the liquidation bonus•
* **Gas Efficiency:** The contract is
optimized to reduce gas usage, making it more competitive in a congested block environment.
* **Security Focus:** Designed with reentrancy guards and other secure coding patterns to prevent common DeFi exploits.
  * **Solidity:** The primary language for the smart contract.
* **Hardhat / Foundry:** Development environment and testing framework for local blockchain simulation and deployment.
* **Ethers. js / Web3. js:** For scripting, deploying, and interacting with the contract.
* **Compound V3 Protocol:** The targeted DeFi protocol for the liquidation strategy.
* ## How It Works
1. **Funding:** The contract is initialized and funded with the base asset required for liquidation (e.g., USDC,
DAI) •
**Identification:** The contract listens for or is triggered to scan for
borrower accounts with a health factor below 1.
liquidatable position- liquidate
**Execution:** Upon identifying a
the contract
calls the Compound V3 function.
4. **Repayment:** The contract repays a portion of the borrower's debt using its own capital.
5 . **Acquisition:** In return, the
contract
receives a portion of the
borrower's collateral, plus a liquidation bonus.
6. **Profit:** The difference between
the value of the acquired collateral and the repaid debt constitutes the profit, which is retained by the contract.
 ## Contribution
This project is a personal exploration of DeFi protocol security and functionality. Contributions or suggestions for improvement are welcome.
