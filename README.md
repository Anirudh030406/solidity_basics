# solidity_basics
This code explain the basics of solidity. In this code we are creating a token in which we will be adding/removing some amount of value from the token
## Description
This contract is written in the ```solidity language```,a language used to write various smart contracts for blockchain. It is executed in the remix IDE, an online platform which compiles and deploys the smart contracts. We have defined three state variables int following code namely ```token_name``` which tells us about the name of our token, ```token_abbreviation``` which abbrevites the name of the token giving it  short form and ```token_supply''' which gives us the value of the token. There are various functions as well, the ```mint()``` function that adds some value to the token and the ```burn()``` function which removes the values of the token.
## Execution 
Open your ```Remix IDE``` Software and install all the dependencies.
1. Create a new file inside the ```contracts``` folder.
2. Write the Licence Identifier and the compiler inside the new created directory.
3. Copy the below code and paste4 it in the new directory-
   ```contract MyToken {

    // public variables here
    string public token_name = "Bitcoin";
    string public token_abbreviation = "Btc";
    uint public token_supply = "enter a number";
    // mapping variable here
     mapping(address => uint) public current;
    // mint function
     function mint(address add, uint num) external {
         token_supply += num;
         current[add] +=num;
     }
    // burn function
     function burn(address add, uint num) external {
         if(current[add] > num){
           token_supply -= num;
           current[add] -=num;
         }
     }
}```

4. Compile and deploy the contract given above.
5. The three state variables created will be displayed on the screen alongwith the function. We will be asked to write the address and the value that were passed as parameters.
6. For the address, we will copy the ```account number``` and paste it in the ```address``` part. 
7. After entering the number we will view the ```token supply```.

## Authors

Anirudh Gautam

## Licence
This contract is written under the License MIT.
