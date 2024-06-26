# Reentrancy Attack Demonstration

This repository demonstrates the Reentrancy attack on a smart contracts and presents solutions to mitigate it.

A reentrancy attack occurs when a malicious contract calls a function in a vulnerable contract, and then recursively calls back into the vulnerable contract before the first function call finishes. This can lead to unexpected behavior and potentially the draining of funds from the vulnerable contract.

## Smart Contract Details

- [**Attacker.sol**](https://github.com/naganandana-n/Reentrancy-Attack/blob/main/Attacker.sol) \
  This contract is used to perform the reentrancy attack on the bank contract(s).
- [**Bank - Vulnerable.sol**](https://github.com/naganandana-n/Reentrancy-Attack/blob/main/Bank%20-%20Vulnerable.sol) \
  This bank contract is vulnerable to reentrancy attacks.
- [**Bank - Logical Solution.sol**](https://github.com/naganandana-n/Reentrancy-Attack/blob/main/Bank%20-%20Logical%20Solution.sol) \
  This bank contract uses a logical solution to prevent reentrancy attacks by updating the balance before sending funds.
- [**Bank - Reentrancy Guard Solution.sol**](https://github.com/naganandana-n/Reentrancy-Attack/blob/main/Bank%20-%20Reentrancy%20Guard%20Solution.sol) \
  This bank contract uses OpenZeppelin's ReentrancyGuard to prevent reentrancy attacks.

## Images

<img src="https://github.com/naganandana-n/Reentrancy-Attack/blob/main/images/Bank%20Balance.png">
This image shows the initial balance of the bank contract.
<img src="https://github.com/naganandana-n/Reentrancy-Attack/blob/main/images/Output%20-%20Vulnerable%20Bank.png">
This image shows the console output when the attacker contract successfully performs a reentrancy attack on the vulnerable bank contract.
<img src="https://github.com/naganandana-n/Reentrancy-Attack/blob/main/images/Output%20-%20Logical%20Solution.png">
This image shows the console output when the attacker contract attempts to attack the bank contract with a logical solution in place.
<img src="https://github.com/naganandana-n/Reentrancy-Attack/blob/main/images/Output%20-%20Reentrancy%20Guard.png">
This image shows the console output when the attacker contract attempts to attack the bank contract that implements the ReentrancyGuard.

## How to Run

1. Clone the repository.
2. Open [Remix IDE](http://remix.ethereum.org/).
3. Upload the smart contract files to Remix IDE.
4. Deploy the bank contracts and the attacker contract as needed and observe the outputs in the Remix IDE console.

## References

[Reentrancy Attack | Smart Contract Security Tutorial Part 2](https://www.youtube.com/watch?v=3sIwIYfeOD8) \
Note: The code linked to the video may have had issues, which have been addressed and fixed here.
