# Credit-Card-Transactions-using-SQL


## What are the top 100 highest transactions made between 7:00 am and 9:00 am? <br />
SELECT * <br />
FROM transactions_2<br />
WHERE date_part('hour', transactions_2.date) > 7 AND date_part('hour', transactions_2.date) < 9<br />
ORDER BY amount DESC<br />
LIMIT 100;<br />

## Do you see any anomalous transactions that could be fraudulent? <br />
Yes, the largest purchase was $1,617.00, the top four transactions below that were between $748 and $1,131. The other 95 transactions were below $20.00 which shows that majority of merchants aren't making large transactions between 7 and 9 am. Therefore the top five transactions could potentially be fraudulent. 

## Is there a higher number of fraudulent transactions made during this time frame versus the rest of the day?<br />
When looking at another 2 hour block like 11 am to 1 pm, there was only one transaction above $748.
Whereas a popular time for potential fraudulent activity was between 10 pm am and midnight, with 5 transactions above $1,031.

## If you answered yes to the previous question, explain why you think there might be fraudulent transactions during this time frame.<br />
It seems the highest opportunity for fraudulent activity occurs under the times when people are assumed to be asleep so they wouldn't be looking at their banking app or able to stop the transaction as quickly as something happening at 12 pm.

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
