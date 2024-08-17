
# CREATE A TOKEN 

This Solidity contract defines a simple token called MyToken. The contract includes functionality to mint new tokens, burn existing tokens, and track balances of different addresses.



## FEATURES

- Public variables to store token details:

   Token Name ('tokenName')
   
  Token Abbreviation ('tokenAbbrv')
 
  Total Supply ('totalSupply')
- Mapping to store balances of addresses ('balances').
- 'mint' function to create new tokens.
- 'burn' function to destroy tokens with checks to ensure sufficient balance.


## CONTRACT DETAILS

PUBLIC VARIABLES

- 'string public tokenName;'
 
  Stores the name of the token.
- 'string public tokenAbbrv;'
  
  Stores the abbreviation of the token.
- 'uint256 public totalSupply;'

  Stores the total supply of the token.

MAPPING 

- 'mapping(address => uint256) public balances;'

  Maps addresses to their respective token balances.
## FUNCTIONS

Constructor

constructor(string memory _name, string memory _abbrv)

- Initializes the token name and abbreviation.
- Parameters:
- '_name': The name of the token.
- '_abbrv': The abbreviation of the token.

Mint Function

function mint(address _to, uint256 _value) public

- Increases the total supply by the specified '_value'.
- Increases the balance of the specified address '_to' by '_value'.
- Parameters:
- '_to': The address to receive the minted tokens.
- '_value': The number of tokens to mint.

Burn Function

function burn(address _from, uint256 _value) public

- Decreases the total supply by the specified '_value'.
- Decreases the balance of the specified address '_from' by '_value'.
- Ensures that the address '_from' has enough balance to burn the specified '_value'.
- Parameters:
- '_from': The address from which tokens will be burned.
- '_value': The number of tokens to burn.

## USAGE

Deployment

1.Open Remix.

2.Create a new file and paste the contract code.

3.Compile the contract.

4.Deploy the contract, specifying the token name and abbreviation in the constructor.
## INTERACTING WITH THE CONTRACT

- Mint Tokens:

- Use the mint function to create new tokens and assign them to an address.
- Example: mint("0xYourAddress", 1000) will mint 1000 tokens to 0xYourAddress.

- Burn Tokens:

- Use the burn function to destroy tokens from an address.
- Ensure that the address has enough tokens to burn.
- Example: burn("0xYourAddress", 500) will burn 500 tokens from 0xYourAddress.
## License

[MIT](https://choosealicense.com/licenses/mit/)

