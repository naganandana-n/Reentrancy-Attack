# Reentrancy Attack Demonstration

This repository demonstrates the Reentrancy attack on a smart contract and presents solutions to mitigate it.

## Files in the Repository

- **Attacker.sol**: Smart contract that performs the reentrancy attack.
- **Bank - Vulnerable.sol**: Vulnerable bank contract that is susceptible to reentrancy attack.
- **Bank - Logical Solution.sol**: Improved bank contract with a logical solution to prevent reentrancy.
- **Bank - Reentrancy Guard Solution.sol**: Bank contract implementing OpenZeppelin's ReentrancyGuard to prevent reentrancy.

## Reentrancy Attack Overview

A reentrancy attack occurs when a malicious contract calls a function in a vulnerable contract, and then recursively calls back into the vulnerable contract before the first invocation finishes. This can lead to unexpected behavior and potentially the draining of funds from the vulnerable contract.

## Smart Contract Details

### Attacker.sol

This contract is used to perform the reentrancy attack on the `EtherBank` contract.

### Bank - Vulnerable.sol

This contract is vulnerable to reentrancy attacks.

### Bank - Logical Solution.sol

This contract uses a logical solution to prevent reentrancy attacks by updating the balance before sending funds.

### Bank - Reentrancy Guard Solution.sol

This contract uses OpenZeppelin's ReentrancyGuard to prevent reentrancy attacks.

## Images

### 1. Bank Balance

This image shows the initial balance of the bank contract.

### 2. Output - Vulnerable Bank

This image shows the console output when the attacker contract successfully performs a reentrancy attack on the vulnerable bank contract.

### 3. Output - Logical Solution

This image shows the console output when the attacker contract attempts to attack the bank contract with a logical solution in place.

### 4. Output - Reentrancy Guard

This image shows the console output when the attacker contract attempts to attack the bank contract that implements the ReentrancyGuard.

## How to Run

1. Clone the repository.
2. Open the Remix IDE.
3. Upload the smart contract files to Remix IDE.
4. Deploy the bank contracts and the attacker contract as needed and observe the outputs in the Remix IDE console.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
