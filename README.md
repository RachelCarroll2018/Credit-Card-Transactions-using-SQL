# Credit-Card-Transactions-using-SQL

### Some fraudsters hack a credit card by making several small transactions

How can we isolate transactions of each cardholder to show small transactions?<pre>
SELECT *<pre>
FROM transactions_2<pre>
WHERE amount < 2;<pre>

Count the transactions that are less than $2 per cardholder
SELECT COUNT(amount) FROM transactions_2
WHERE amount <2;
Answer: There are 350 transactions that are less than $2

Is there any evidence to suggest a credit card has been hacked? Explain your rationale:
Answer: Even though there are a lot of recurring smaller charges made by the same merchant over this data set, there isn't enoguh information to prove fraud from this information alone. We would need to understand the merchant's typical spending habits, have they purchased from the seller before, and more.


