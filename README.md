# myToken Contract

This is a simple token contract implemented on the Ethereum blockchain. The contract provides functionalities to mint new tokens and burn existing tokens.

## Contract Details
- Token Name: GOROSPE
- Token Abbreviation: GRSP
- Total Supply: 0

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a functions.

Mint Function:
-Increases the total supply of tokens by the specified value and increases the balance of the recipient address accordingly.

Burn Function:
-Decreases the total supply of tokens by the specified value and decreases the balance of the ddress accordingly. This function includes conditionals to ensure that the balance is greater than or equal to the amount to be burned.

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol). Copy and paste the following code into the file:

```javascript
pragma solidity 0.8.18;

contract MyToken {
    // public variables here
    string public tokenName = "GOROSPE";
    string public tokenAbbrv = "GRSP";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances [_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances [_address] -= _value;
        }
    }
}


## Authors

NTC STUDENT   
GOROSPE, BEA D. BSIT 2.1
## License

This project is licensed under the MIT License - see the LICENSE.md file for details
