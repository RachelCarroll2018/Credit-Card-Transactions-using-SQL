# Credit-Card-Transactions-using-SQL

## Some fraudsters hack a credit card by making several small transactions, how can we isolate transactions of each cardholder to show small transactions?<br />
SELECT *<br />
FROM transactions_2<br />
WHERE amount < 2;<br />
<br />
## Count the transactions that are less than $2 per cardholder<br />
SELECT COUNT(amount) FROM transactions_2<br />
WHERE amount <2;<br />
Answer: There are 350 transactions that are less than $2<br />
<br />
## Is there any evidence to suggest a credit card has been hacked? Explain your rationale:<br />
Answer: Even though there are a lot of recurring smaller charges made by the same merchant over this data set, there isn't enoguh information to prove fraud from this information alone. We would need to understand the merchant's typical spending habits, have they purchased from the seller before, and more.<br /><br />


## What are the top 100 highest transactions made between 7:00 am and 9:00 am? <br />


## Do you see any anomalous transactions that could be fraudulent? <br />


## Is there a higher number of fraudulent transactions made during this time frame versus the rest of the day?<br />


## If you answered yes to the previous question, explain why you think there might be fraudulent transactions during this time frame.<br />
