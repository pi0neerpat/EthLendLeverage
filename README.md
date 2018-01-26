# EthLendLeverage
A tool for creating loan "Stacks" to create leverage

This is essentially a tool for creating your own P2P futures contracts (is there another term for this?).  This works by creating multiple recursive loans. Doing this by hand is tedious, so we should automate it!  The first version will support creation of loans using the EthLend contract, and buying/withdrawing tokens from a single exchange (e.g., IDEX, EtherDelta, Binance).

# Purpose

Create open-source and free financial tools.
Promote education, inclusivity, and access to crypto tools.

# ELI5:

First familiarize yourself with the EthLend platform (must have Metamask installed) and check out the wiki 
https://app.ethlend.io/main/
https://github.com/ETHLend/Documentation/wiki

Lets say you want to buy houses in Cryptotown. 

1) You are confident that the value of houses in Cryptotown are going to increase at a rate greater than inflation.
2) You enter town with only $100 dollars in your pocket, and buy 1 house outright for $100.
3) You then Take a line of credit on the house for roughly 66% of the value of the home in cash.
4) You use those funds to buy another house for $66 (you now own 2 homes).
5) You take a line of credit on the second house for roughly $43.
6) You use the funds to buy a third house for roughly $43 (you now own 3 homes).
7) Take a line of credit on the second house for roughly $28.
8) Use the funds to buy a fourth house for $28 (now you own 4 homes).
9) Repeat until you get tired (maybe seven times?).
10) Stop and add up the value of houses in your "control" (i.e., $100 + $66 + $43 + $28 + ...). You get a number that approaches $300.  Therefore you now have almost 3x your initial $100 investment, which means that when the market goes up by 10%, your ROI is actually 30%. 

The Good: If the market goes up you realize profits on $300 worth of houses, instead of only $100. 
The Better: When you first stepped foot into Cryptotown, you only had $100. Even if the market goes down, you can lose no more than $100.  Your risk exposure is limited to the first investment used to create the "Loan Stack."
The Bad: Its possible to lose your initial investment. No one will be breaking down your door saying "where is my money"

# Inputs:

Token (e.g., LEND, ANT, DNT, etc.)
Amount (e.g., 100)
Recursions (e.g., 7) 
Installments (e.g., 3)
Installment Days (e.g., 30 Days)

# Outputs:

All loan data
Amount of Token staked
Loan contract addresses

# Difficulties:

The process of waiting for lenders, and deposting/withdrawing from exchanges may take a long time (3 hhours?). The script should be able to be started/stopped mid-process....alternative suggestions?

![Stack Widget](https://github.com/blockchainbuddha/EthLendLeverage/blob/master/StackExplained.png)