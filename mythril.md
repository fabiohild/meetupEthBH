myth -xo markdown json --truffle
# Analysis result for balance

No issues found.
# Analysis results for Contrato.sol

## Integer Overflow
- SWC ID: 101
- Type: Warning
- Contract: TestToken
- Function name: `transferFrom(address,address,uint256)`
- PC address: 1368

### Description

The arithmetic operation can result in integer overflow.
In file: Contrato.sol:73

### Code

```
balances[_to] + _value
```

## Ether send
- SWC ID: 105
- Type: Warning
- Contract: TestToken
- Function name: `withdraw(uint256)`
- PC address: 1812

### Description

It seems that an attacker is able to execute an call instruction, this can mean that the attacker is able to extract funds out of the contract.
In file: Contrato.sol:41

### Code

```
msg.sender.call.value(_value)()
```

## Message call to external contract
- SWC ID: 107
- Type: Warning
- Contract: TestToken
- Function name: `withdraw(uint256)`
- PC address: 1812

### Description

This contract executes a message call to the address of the transaction sender. Generally, it is not recommended to call user-supplied addresses using Solidity's call() construct. Note that attackers might leverage reentrancy attacks to exploit race conditions or manipulate this contract's state.
In file: Contrato.sol:41

### Code

```
msg.sender.call.value(_value)()
```

## State change after external call
- SWC ID: 107
- Type: Warning
- Contract: TestToken
- Function name: `withdraw(uint256)`
- PC address: 1893

### Description

The contract account state is changed after an external call. Consider that the called contract could re-enter the function before this state change takes place. This can lead to business logic vulnerabilities.
In file: Contrato.sol:42

### Code

```
balances[msg.sender] -= _value
```

## Unchecked CALL return value
- SWC ID: 104
- Type: Informational
- Contract: TestToken
- Function name: `withdraw(uint256)`
- PC address: 1893

### Description

The return value of an external call is not checked. Note that execution continue even if the called contract throws.
In file: Contrato.sol:42

### Code

```
balances[msg.sender] -= _value
```

## Integer Underflow
- SWC ID: 101
- Type: Warning
- Contract: TestToken
- Function name: `withdraw(uint256)`
- PC address: 1902

### Description

The substraction can result in an integer underflow.
In file: Contrato.sol:43

### Code

```
total -= _value
```

## State change after external call
- SWC ID: 107
- Type: Warning
- Contract: TestToken
- Function name: `withdraw(uint256)`
- PC address: 1908

### Description

The contract account state is changed after an external call. Consider that the called contract could re-enter the function before this state change takes place. This can lead to business logic vulnerabilities.
In file: Contrato.sol:43

### Code

```
total -= _value
```

## Integer Overflow
- SWC ID: 101
- Type: Warning
- Contract: TestToken
- Function name: `transfer(address,uint256)`
- PC address: 2141

### Description

The arithmetic operation can result in integer overflow.
In file: Contrato.sol:50

### Code

```
balances[_to] + _value
```

## Integer Overflow
- SWC ID: 101
- Type: Warning
- Contract: TestToken
- Function name: `deposit()`
- PC address: 2491

### Description

The arithmetic operation can result in integer overflow.
In file: Contrato.sol:32

### Code

```
balances[msg.sender] + msg.value
```

## Integer Overflow
- SWC ID: 101
- Type: Warning
- Contract: TestToken
- Function name: `deposit()`
- PC address: 2512

### Description

The arithmetic operation can result in integer overflow.
In file: Contrato.sol:33

### Code

```
total + msg.value
```

# Analysis results for Contrato.sol

## Integer Overflow
- SWC ID: 101
- Type: Warning
- Contract: Exploit
- Function name: `fallback`
- PC address: 133

### Description

The arithmetic operation can result in integer overflow.
In file: Contrato.sol:102

### Code

```
withdrawnX++
```

## Message call to external contract
- SWC ID: 107
- Type: Informational
- Contract: Exploit
- Function name: `fallback`
- PC address: 297

### Description

This contract executes a message call to to another contract. Make sure that the called contract is trusted and does not execute user-supplied code.
In file: Contrato.sol:104

### Code

```
tokenContract.withdraw(value)
```

## Message call to external contract
- SWC ID: 107
- Type: Informational
- Contract: Exploit
- Function name: `withdraw()`
- PC address: 826

### Description

This contract executes a message call to to another contract. Make sure that the called contract is trusted and does not execute user-supplied code.
In file: Contrato.sol:98

### Code

```
tokenContract.withdraw(value)
```