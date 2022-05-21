# Looking for Suspicious Transactions using SQL

## Background

Fraud is prevalent these days, whether you are a small taco shop or a large international business. While there are emerging technologies that employ machine learning and artificial intelligence to detect fraud, many instances of fraud detection still require strong data analytics to find abnormal charges.

In this project I analyzed historical credit card transactions and consumption patterns in order to identify possible fraudulent transactions.

The three main tasks at hand: 

1) Define a database model to store the credit card transactions data and create a new PostgreSQL database using your model.

2) Data-Engineering: Create a database schema on PostgreSQL and populate your  database from the CSV files provided.

3. Data-Analysis: Analyze the data to identify possible fraudulent transactions trends data, and develop a report of your observations.

---

### Data Analysis
#### Part 1:

  * What are the top 100 highest transactions made between 7:00 am and 9:00 am and are there any anomalous transactions that could be fraudulent?
 From 7 am to 9 am, 95% of the data set's transactions were $20.44 or below. The other 5% of transactions had a large jump in amount, with the top transaction being $1,617 and the respective 4 below being $1131, $1060, $1017, and $748. Given that the overwhelming majority of transactions are $20 or less, these amounts could be considered fraudulent.


  * Is there a higher number of fraudulent transactions made during this time frame versus the rest of the day?

  * If you answered yes to the previous question, explain why you think there might be fraudulent transactions during this time frame.

#### Part 2:

Your CFO has also requested detailed trends data on specific card holders. Use the [starter notebook](Starter_Files/challenge.ipynb) to query your database and generate visualizations that supply the requested information as follows, then add your visualizations and observations to your markdown report:      

* The two most important customers of the firm may have been hacked. Verify if there are any fraudulent transactions in their history. For privacy reasons, you only know that their cardholder IDs are 2 and 18.

  * Using hvPlot, create a line plot representing the time series of transactions over the course of the year for each cardholder separately. 
  
  * Next, to better compare their patterns, create a single line plot that contains both card holders' trend data.  

  * What difference do you observe between the consumption patterns? Does the difference suggest a fraudulent transaction? Explain your rationale.

* The CEO of the biggest customer of the firm suspects that someone has used her corporate credit card without authorization in the first quarter of 2018 to pay quite expensive restaurant bills. Again, for privacy reasons, you know only that the cardholder ID in question is 25.

  * Using Plotly Express, create a box plot, representing the expenditure data from January 2018 to June 2018 for cardholder ID 25.
  
  * Are there any outliers for cardholder ID 25? How many outliers are there per month?

  * Do you notice any anomalies? Describe your observations and conclusions.
