# Analysis Results
## Message call to external contract
- Type: Warning
- Contract: D
- Function name: `_function_0xeea4c864`
- PC address: 1038

### Description
This contract executes a message call to an address provided as a function argument. Generally, it is not recommended to call user-supplied adresses using Solidity's call() construct. Note that attackers might leverage reentrancy attacks to exploit race conditions or manipulate this contract's state.

In *<TESTDATA>/inputs/kinds_of_calls.sol:6*

```
_e.call(bytes4(sha3("setN(uint256)")), _n)
```
## Unchecked CALL return value
- Type: Informational
- Contract: D
- Function name: `_function_0xeea4c864`
- PC address: 1038

### Description
The return value of an external call is not checked. Note that execution continue even if the called contract throws.

In *<TESTDATA>/inputs/kinds_of_calls.sol:6*

```
_e.call(bytes4(sha3("setN(uint256)")), _n)
```
