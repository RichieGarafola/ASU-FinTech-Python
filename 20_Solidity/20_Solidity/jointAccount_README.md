
# Creating Joint Account with Solidity

📌 Challenge 20

> "Create a smart contract with Solidity, that accepts two user addresses linked to a joint savings account. Implementing a financial institution’s requirements to provide the ability to deposit and withdraw funds from the account.
"


## Table of content
- [Overview of the project](https://github.com/RichieGarafola/Joint_Savings_Account#overview-of-the-project) 
- [Project goals](https://github.com/RichieGarafola/Joint_Savings_Account#project-goals)
- [Project steps](https://github.com/RichieGarafola/Joint_Savings_Account#project-steps)
- [Software version control](https://github.com/RichieGarafola/Joint_Savings_Account#software-version-control)
    - [Work with GitHub](https://github.com/RichieGarafola/Joint_Savings_Account#work-with-github)
    - [How to install](https://github.com/RichieGarafola/Joint_Savings_Account#how-to-install)
- [Helps recruiters](https://github.com/RichieGarafola/Joint_Savings_Account#helps-recruiters)
- [License](https://github.com/RichieGarafola/Joint_Savings_Account#license)



## Overview of the project 

To automate the creation of joint savings accounts, I am creating Solidity smart contract that accepts two user addresses. These addresses will be able to control a joint savings account. Smart contract uses ether management functions to implement a financial institution’s requirements for providing the features of the joint savings account. These features consist of the ability to deposit and withdraw funds from the account.

## Project goals




## Project steps 

    ###Step 1: Create a Joint Savings Account Contract in Solidity
   

* From the provided starter code, open the Solidity file named joint_savings.sol in the Remix IDE.

* Define a new contract named JointSavings.

 <img width="321" alt="joint savings solidity" src="./images/joint_savings_solidity">

* Define the following variables in the new contract:


<img width="697" alt="new contract" src="./images/new_contract">


* Define a function named withdraw that accepts two arguments: amount of type uint and recipient of type payable address. In this function, code the following:

<img width="563" alt="withdraw function" src="./images/withdraw_function">


* Define require statements

<img width="856" alt="require statement" src="./images/require_statement">


* Add an if statement to check if lastToWithdraw is not equal (!=) to recipient. If it’s not equal, set it to the current value of recipient.

<img width="955" alt="if statement" src="./images/if_statement">


* Call the transfer function of the recipient, and pass it the amount to transfer as an argument. Set lastWithdrawAmount equal to amount. Set the contractBalance variable 

<img width="869" alt="transfer function" src="./images/transfer_function">


* Define a public payable function named deposit. In this function, code the following: Set the contractBalance variable, Define a public function, set the values of accountOne and accountTwo 

<img width="953" alt="public payable function" src="./images/public_payable_function">


* Add a fallback function so that your contract can store ether that’s sent from outside the deposit function.

<img width="612" alt="fall back function" src="./images/fallback_function">


    Step 2: Compile and Deploy Your Contract in the Remix VM Berlin
    
<img width="597" alt="Berlin Enviornment" src="./images/berlin_enviornment">


    Step 3: Interact with Your Deployed Smart Contract

To interact with your deployed smart contract, complete the following steps:

* Use the setAccounts function to define the authorized Ethereum address that will be able to withdraw funds from your contract.

<img width="286" alt="set accounts" src="./images/set_accounts">


* Test the deposit functionality of your smart contract by sending the following amounts of ether. After each transaction, use the contractBalance function to verify that the funds were added to your contract:

<img width="301" alt="test set accounts" src="./images/test_setaccounts">


##### Transaction 1: Send 1 ether as wei.
<img width="282" alt="1 ether as wei" src="./images/1eth_as_wei">


##### Transaction 2: Send 10 ether as wei.

<img width="282" alt="10 ether as wei" src="./images/10eth_as_wei">


##### Transaction 3: Send 5 ether.

<img width="304" alt="send 5 ether" src="./images/send_5eth">



##### Once you’ve successfully deposited funds into your contract, test the contract’s withdrawal functionality by withdrawing 5 ether into accountOne and 10 ether into accountTwo. After each transaction, use the contractBalance function to verify that the funds were withdrawn from your contract. 

<img width="304" alt="withdraw 5 ethereum" src="./images/withdraw_5eth">

<img width="304" alt="withdraw 10 ethereum" src="./images/withdraw_10eth">


##### Use the lastToWithdraw and lastWithdrawAmount functions to verify that the address and amount were correct.


<img width="528" alt="last to withdraw" src="./images/lastToWithdraw">




## Software version control

[Remix IDE](https://remix.ethereum.org) used to interact with Etherium blockchain.

Remix - Ethereum IDE is an open source web and desktop application. It fosters a fast development cycle and has a rich set of plugins with intuitive GUIs. Remix is used for the entire journey of contract development as well as being a playground for learning and teaching Ethereum.