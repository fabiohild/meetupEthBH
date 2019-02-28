slither .
INFO:Slither:truffle compile running...
INFO:Slither:
INFO:Detectors:
Reentrancy in TestToken.withdraw (meetupBH/contracts/Contrato.sol#39-45):
        External calls:
        - msg.sender.call.value(_value)() (meetupBH/contracts/Contrato.sol#41)
        State variables written after the call(s):
        - balances (meetupBH/contracts/Contrato.sol#42)
Reference: https://github.com/trailofbits/slither/wiki/Vulnerabilities-Description#reentrancy-vulnerabilities
INFO:Detectors:
Exploit.fallback (meetupBH/contracts/Contrato.sol#101-105) does not use the value returned by external calls:
        -tokenContract.withdraw(value) (meetupBH/contracts/Contrato.sol#104)
Reference: https://github.com/trailofbits/slither/wiki/Vulnerabilities-Description#unused-return
INFO:Detectors:
Different versions of Solidity is used in :
        - Version used: ['>=0.4.21<0.6.0', '^0.4.0']
        - meetupBH/contracts/Contrato.sol#1 declares pragma solidity^0.4.0
        - meetupBH/contracts/Contrato.sol#1 declares pragma solidity^0.4.0
        - meetupBH/contracts/Contrato.sol#1 declares pragma solidity^0.4.0
        - meetupBH/contracts/Migrations.sol#1 declares pragma solidity>=0.4.21<0.6.0
Reference: https://github.com/trailofbits/slither/wiki/Vulnerabilities-Description#different-pragma-directives-are-used
INFO:Detectors:
Old version (<0.4.23) of Solidity used in :
        - meetupBH/contracts/Migrations.sol#1 declares pragma solidity>=0.4.21<0.6.0
        - meetupBH/contracts/Contrato.sol#1 declares pragma solidity^0.4.0
        - meetupBH/contracts/Contrato.sol#1 declares pragma solidity^0.4.0
        - meetupBH/contracts/Contrato.sol#1 declares pragma solidity^0.4.0
Reference: https://github.com/trailofbits/slither/wiki/Vulnerabilities-Description#old-versions-of-solidity
INFO:Detectors:
TestToken.name (meetupBH/contracts/Contrato.sol#4) is never used in TestToken
TestToken.symbol (meetupBH/contracts/Contrato.sol#5) is never used in TestToken
TestToken.decimals (meetupBH/contracts/Contrato.sol#6) is never used in TestToken
Reference: https://github.com/trailofbits/slither/wiki/Vulnerabilities-Description#unused-state-variables
INFO:Detectors:
Low level call in TestToken.withdraw (meetupBH/contracts/Contrato.sol#39-45):
        -msg.sender.call.value(_value)() meetupBH/contracts/Contrato.sol#41
Reference: https://github.com/trailofbits/slither/wiki/Vulnerabilities-Description#low-level-calls
INFO:Detectors:
Function 'TestToken.TestToken' (meetupBH/contracts/Contrato.sol#19-21) is not in mixedCase
Parameter '_owner' of TestToken.balanceOf (meetupBH/contracts/Contrato.sol#27) is not in mixedCase
Parameter '_value' of TestToken.withdraw (meetupBH/contracts/Contrato.sol#39) is not in mixedCase
Parameter '_to' of TestToken.transfer (meetupBH/contracts/Contrato.sol#47) is not in mixedCase
Parameter '_value' of TestToken.transfer (meetupBH/contracts/Contrato.sol#47) is not in mixedCase
Parameter '_spender' of TestToken.approve (meetupBH/contracts/Contrato.sol#60) is not in mixedCase
Parameter '_value' of TestToken.approve (meetupBH/contracts/Contrato.sol#60) is not in mixedCase
Parameter '_owner' of TestToken.allowance (meetupBH/contracts/Contrato.sol#66) is not in mixedCase
Parameter '_spender' of TestToken.allowance (meetupBH/contracts/Contrato.sol#66) is not in mixedCase
Parameter '_from' of TestToken.transferFrom (meetupBH/contracts/Contrato.sol#70) is not in mixedCase
Parameter '_to' of TestToken.transferFrom (meetupBH/contracts/Contrato.sol#70) is not in mixedCase
Parameter '_value' of TestToken.transferFrom (meetupBH/contracts/Contrato.sol#70) is not in mixedCase
Parameter '_tokenAddress' of Exploit. (meetupBH/contracts/Contrato.sol#90) is not in mixedCase
Function 'Exploit._balance' (meetupBH/contracts/Contrato.sol#107-110) is not in mixedCase
Contract 'balance' (meetupBH/contracts/Contrato.sol#113-117) is not in CapWords
Parameter '_contract' of balance.getBalance (meetupBH/contracts/Contrato.sol#114) is not in mixedCase
Parameter 'new_address' of Migrations.upgrade (meetupBH/contracts/Migrations.sol#19) is not in mixedCase
Variable 'Migrations.last_completed_migration' (meetupBH/contracts/Migrations.sol#5) is not in mixedCase
Reference: https://github.com/trailofbits/slither/wiki/Vulnerabilities-Description#conformance-to-solidity-naming-conventions
INFO:Detectors:
TestToken.totalSupply (meetupBH/contracts/Contrato.sol#23-25) should be declared external
TestToken.balanceOf (meetupBH/contracts/Contrato.sol#27-29) should be declared external
TestToken.deposit (meetupBH/contracts/Contrato.sol#31-37) should be declared external
TestToken.withdraw (meetupBH/contracts/Contrato.sol#39-45) should be declared external
TestToken.transfer (meetupBH/contracts/Contrato.sol#47-57) should be declared external
TestToken.approve (meetupBH/contracts/Contrato.sol#60-64) should be declared external
TestToken.allowance (meetupBH/contracts/Contrato.sol#66-68) should be declared external
TestToken.transferFrom (meetupBH/contracts/Contrato.sol#70-79) should be declared external
Exploit.withdraw (meetupBH/contracts/Contrato.sol#96-99) should be declared external
Exploit.fallback (meetupBH/contracts/Contrato.sol#101-105) should be declared external
Exploit._balance (meetupBH/contracts/Contrato.sol#107-110) should be declared external
balance.getBalance (meetupBH/contracts/Contrato.sol#114-116) should be declared external
Migrations.setCompleted (meetupBH/contracts/Migrations.sol#15-17) should be declared external
Migrations.upgrade (meetupBH/contracts/Migrations.sol#19-22) should be declared external
Reference: https://github.com/trailofbits/slither/wiki/Vulnerabilities-Description#public-function-that-could-be-declared-as-external
INFO:Slither:. analyzed (4 contracts), 38 result(s) found