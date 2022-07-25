# Joint-Saving Smart Contract

A fintech startup company has recently hired you. This company is disrupting the finance industry with its own cross-border, Ethereum-compatible blockchain that connects financial institutions. Currently, the team is building smart contracts to automate many of the institutions’ financial processes and features, such as hosting joint savings accounts.

To automate the creation of joint savings accounts, I'll create a Solidity smart contract that accepts two user addresses. These addresses will be able to control a joint savings account. My smart contract will use ether management functions to implement a financial institution’s requirements for providing the features of the joint savings account. These features will consist of the ability to deposit and withdraw funds from the account.

## What will i create?

- The completed Solidity JointSavings smart contract.
- Eight images these images should confirm that the deposit and withdrawal transactions, which are designed to test the JointSavings functionality in the JavaScript VM, worked as expected.


# Step 1 Create Contract

Create the inital _Smart Contract_ here we define our _variables of our Contract_. Two **address that are made payable**, (keep in mind the syntax from solidity [here is a link to the _documentaion_](https://docs.soliditylang.org/en/v0.5.11/introduction-to-smart-contracts.html?highlight=storage#storage-memory-and-the-stack)) an **address made public** that shows the _last to withdrawn_, an **unassigned integer made public** to show the _last amount withdrawn_, and finally an **unassigned made public** integer for the _contract balance_.

within the contract after I created the Variables for the contract, Below I create the function withdraw with in _parenthesis_ I pass through 2 arguments.
these areguments are to be used when the user wants to withdraw to take in and **uint amount, address that is payable recipient**. Also, making this function public (which we will do throughout the whole contract will let others see and use the function) that has a
- **Require statement** that checks the recipients are _authorized_
- **Require statement** that check if funds are available to make the withdraw
- An **if statement** that will check the last to withdraw
- call the transfer function that passes the amount
- set the balance equal to amount
- set the contract balance of the contracts account

Now that I have created a **Smart Contract** and the first **Function Withdraw** within the Contract to let authorized users withdraw. Now we are to create a **deposit function** that  _payble_ and _public_ that is set using _(this)_ attribute that refrences the _Contract Balance_.

This Function is to **Set Accounts** that is takes the following **address payable of account1, address payable of account2** that is made public so anyone can use it or see it. This sets the accounts a authorized accounts that takes in the arguments to set the values of accountOne and accountTwo.

Fincally the last function to take in any ether that is sent outside the deposit function. **function () external payable**

# Step 2 Compile, Launch, Interact

Using the [Remix Ethereum IDE](https://remix-project.org/) we are able to compile our code to check for syntax errors. This is a _Good Practice_ for cleaner code to make sure all isssues are solved before the next step of launching the smart contract. After making sure that you have set the compiler to the right **pragma**, compiled the code to take care of any syntax errors or any errors that might have been there its time to _Deploy_.

