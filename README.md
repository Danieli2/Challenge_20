# Challenge_20
***

**Background**

A fintech startup company has recently hired me. This company is disrupting the finance industry with its own cross-border, Ethereum-compatible blockchain that connects financial institutions. Currently, the team is building smart contracts to automate many of the institutions’ financial processes and features, such as hosting joint savings accounts.

To automate the creation of joint savings accounts, I created a Solidity smart contract that accepts two user addresses. These addresses will be able to control a joint savings account. My smart contract will use ether management functions to implement a financial institution’s requirements for providing the features of the joint savings account. These features will consist of the ability to deposit and withdraw funds from the account.

***
**Instructions**

The steps for this Challenge are divided into the following sections:
1. Create a Joint Savings Account Contract in Solidity
2. Compile and Deploy my Contract in the JavaScript VM
3. Interact with my Deployed Smart Contract

***

**Step 1: Create a Joint Savings Account Contract in Solidity**

1. I Define a new contract named JointSavings.
2. I Define the following variables in the new contract:
     -Two variables of type address payable named accountOne and accountTwo
     -A variable of type address public named lastToWithdraw
     -Two variables of type uint public named lastWithdrawAmount and contractBalance
3. I Define a function named withdraw that accepts two arguments: amount of type uint and recipient of type payable address. In this function, code the              following:
     -Define a require statement that checks if recipient is equal to either accountOne or accountTwo. If it isn’t, the require statement returns the “You don't       own this account!” text.
      -Define a require statement that checks if balance is sufficient for accomplishing the withdrawal operation. If there are insufficient funds, it returns          the “Insufficient funds!” text.
      -Add an if statement to check if lastToWithdraw is not equal (!=) to recipient. If it’s not equal, set it to the current value of recipient.
      -Call the transfer function of the recipient, and pass it the amount to transfer as an argument.
      -Set lastWithdrawAmount equal to amount.
I Set the contractBalance variable equal to the balance of the contract by using address(this).balance to reflect the new balance of the contract.
then I Defined a public payable function named deposit. In this function, I  coded the following:
1. I Set the contractBalance variable equal to the balance of the contract by using address(this).balance.
2. Define a public function named setAccounts that takes two address payable arguments, named account1 and account2. In the body of the function, I set the          values of accountOne and accountTwo to account1 and account2, respectively.
3. I Added a fallback function so that my contract can store ether that’s sent from outside the deposit function.

***
**Step 2: Compile and Deploy Your Contract in the JavaScript VM**

I Compiled my smart contract. 
In the Remix IDE, I  navigated to the “Deploy & Run Transactions” pane, and then made sure that I selected the “JavaScript VM” as the environment.

***

**Step 3: Interact with Your Deployed Smart Contract**

Now that My contract is deployed, it’s time to test its functionality! After each step, I captured a screenshot of the execution, and Posted it bellow named Execution_Results. 
***

<img width="1438" alt="Screen Shot 2021-11-13 at 12 35 57 PM" src="https://user-images.githubusercontent.com/85910138/141658325-46f54a60-a8e9-4489-a0ce-1908bb9212e5.png">

**Step 4: Execution results**

<img width="1440" alt="Screen Shot 2021-11-13 at 12 19 07 PM" src="https://user-images.githubusercontent.com/85910138/141658126-5dfb2f69-0111-4ea2-b799-f3f1386eb818.png">


<img width="1440" alt="Screen Shot 2021-11-13 at 12 20 40 PM" src="https://user-images.githubusercontent.com/85910138/141658129-1d318654-0669-4212-98ee-374634c87bf6.png">

<img width="1440" alt="Screen Shot 2021-11-13 at 12 21 36 PM" src="https://user-images.githubusercontent.com/85910138/141658132-e9844be7-a424-48bd-abcc-27e155732ef4.png">



