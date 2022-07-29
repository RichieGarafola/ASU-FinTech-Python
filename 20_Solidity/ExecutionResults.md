
# Creating Joint Account with Solidity

📌 Challenge 20

> "Create a smart contract with Solidity, that accepts two user addresses linked to a joint savings account. Implementing a financial institution’s requirements to provide the ability to deposit and withdraw funds from the account.
"


## Table of content
- [Overview of the project](https://github.com/RichieGarafola/ASU-FinTech-Python/edit/main/20_Solidity/jointAccount_README.md#overview-of-the-project) 
- [Project goals](https://github.com/RichieGarafola/ASU-FinTech-Python/edit/main/20_Solidity/jointAccount_README.md#project-goals)
- [Project steps](https://github.com/RichieGarafola/ASU-FinTech-Python/edit/main/20_Solidity/jointAccount_README.md#project-steps)
- [Software version control](https://github.com/RichieGarafola/ASU-FinTech-Python/edit/main/20_Solidity/jointAccount_README.md#software-version-control)



## Overview of the project 

To automate the creation of joint savings accounts, I am creating Solidity smart contract that accepts two user addresses. These addresses will be able to control a joint savings account. Smart contract uses ether management functions to implement a financial institution’s requirements for providing the features of the joint savings account. These features consist of the ability to deposit and withdraw funds from the account.

## Project goals




## Project steps 

    ###Step 1: Create a Joint Savings Account Contract in Solidity
   

* From the provided starter code, open the Solidity file named joint_savings.sol in the Remix IDE.

* Define a new contract named JointSavings:



![alt="joint_savings_solidity"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/joint_savings_solidity.png)

* Define the following variables in the new contract:



![alt="new contract"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/new_contract.png)

* Define a function named withdraw that accepts two arguments: amount of type uint and recipient of type payable address. In this function, code the following:



![alt="withdraw function"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/withdraw_function.png)

* Define require statements



![alt="withdraw function"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/require_statement.png)


* Add an if statement to check if lastToWithdraw is not equal (!=) to recipient. If it’s not equal, set it to the current value of recipient.



![alt="if statement"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/if_statement.png)

* Call the transfer function of the recipient, and pass it the amount to transfer as an argument. Set lastWithdrawAmount equal to amount. Set the contractBalance variable 



![alt="transfer function"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/transfer_function.png)

* Define a public payable function named deposit. In this function, code the following: Set the contractBalance variable, Define a public function, set the values of accountOne and accountTwo 



![alt="public payable function"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/public_payable_function.png)

* Add a fallback function so that your contract can store ether that’s sent from outside the deposit function.



![alt="fall back function"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/fallback_function.png)

    Step 2: Compile and Deploy Your Contract in the Remix VM Berlin



![alt="Berlin Enviornment"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/berlin_enviornment.png)
    
    Step 3: Interact with Your Deployed Smart Contract

To interact with your deployed smart contract, complete the following steps:

* Use the setAccounts function to define the authorized Ethereum address that will be able to withdraw funds from your contract.



![alt="set accounts"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/set_accounts.png)

* Test the deposit functionality of your smart contract by sending the following amounts of ether. After each transaction, use the contractBalance function to verify that the funds were added to your contract:



![alt="test set accounts"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/test_setaccounts.png)

##### Transaction 1: Send 1 ether as wei.



![alt="1 ether as wei"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/1eth_as_wei.png)

##### Transaction 2: Send 10 ether as wei.



![alt="10 ether as wei"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/10eth_as_wei.png)


##### Transaction 3: Send 5 ether.



![alt="send 5 ether"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/send_5eth.png)

##### Once you’ve successfully deposited funds into your contract, test the contract’s withdrawal functionality by withdrawing 5 ether into accountOne and 10 ether into accountTwo. After each transaction, use the contractBalance function to verify that the funds were withdrawn from your contract. 



![alt="withdraw 5 ether"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/withdraw_5eth.png)



![alt="withdraw 10 ether"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/withdraw_10eth.png)

##### Use the lastToWithdraw and lastWithdrawAmount functions to verify that the address and amount were correct.



![alt="last to withdraw"](https://github.com/RichieGarafola/ASU-FinTech-Python/blob/main/20_Solidity/Execution_Results/lastToWithdraw.png)


## Software version control

[Remix IDE](https://remix.ethereum.org) used to interact with Etherium blockchain.

Remix - Ethereum IDE is an open source web and desktop application. It fosters a fast development cycle and has a rich set of plugins with intuitive GUIs. Remix is used for the entire journey of contract development as well as being a playground for learning and teaching Ethereum.
