# BLOCK FRAUD CLASSIFICATION

Link to the streamlit app: https://share.streamlit.io/valcilio/deploy-repos/fraud/webapp.py

![houses prices analytics](https://i.ibb.co/VjdbtdJ/Fraud-Detection-1.png)

## **PREMISES:**

For the development of the project, we created a fictitious company called "Blocker Fraud Company", which is a company specialized in detecting fraud in financial transactions made through mobile devices. The company has a service called “Blocker Fraud” in which it guarantees the blocking of fraudulent transactions.

The company's business model is of the Service type with the monetization made by the performance of the service provided, that is, the user pays a fixed fee on the success in detecting fraud in the client's transactions.

However, the Blocker Fraud Company is expanding in Brazil and to acquire customers more quickly, it has adopted a very aggressive strategy. The strategy works as follows:


- **1** - The company receives 25% of each transaction value truly detected as fraud.
- **2** - The company receives 5% of each transaction value detected as fraud, however the transaction is legitimate.
- **3** - The company gives back 100% of the value for the customer in each transaction detected as legitimate, however the transaction is actually a fraud.

## **Attributes List:**

| Attributtes    |                                                              |
| -------------- | ------------------------------------------------------------ |
| step           | maps a unit of time in the real world. In this case 1 step is 1 hour of time. Total steps 744 (30 days simulation). |
| type           | CASH-IN, CASH-OUT, DEBIT, PAYMENT and TRANSFER.              |
| amount         | amount of the transaction in local currency.                 |
| nameOrig       | customer who started the transaction                         |
| oldbalanceOrg  | initial balance before the transaction                       |
| newbalanceOrig | new balance after the transaction                            |
| namedest       | customer who is the recipient of the transaction             |
| oldbalanceDest | initial balance recipient before the transaction. Note that there is not information for customers that start with M (Merchants). |
| newbalanceDest | new balance recipient after the transaction. Note that there is not information for customers that start with M (Merchants). |
| isFraud        | This is the transactions made by the fraudulent agents inside the simulation. In this specific dataset the fraudulent behavior of the agents aims to profit by taking control or customers accounts and try to empty the funds by transferring to another account and then cashing out of the system. |
| isFlaggedFraud | The business model aims to control massive transfers from one account to another and flags illegal attempts. An illegal attempt in this dataset is an attempt to transfer more than 200.000 in a single transaction. |

## **Solution Plan:**

Defined that what they need is a fraud detection for the financial transactions we will:

**1 -** Gain understanding of the data through a statistical and exploratory analysis of the data and also derive new columns of data.

**2 -** Validation of business hypotheses to produce insights and manual selection of columns to be used that will add to the selection via algorithm.

**3 -** Preparation of data for model training and model selection.

**4 -** Selection of the best model parameters through the random search method.

**5 -** Translation and interpretation of the error to transform the model result into business value.

**6 -** Deployment of the model with a way that allow the Block Fraud to check new transactions manually and easily from any where.

With all the solution planned the item to show in the end was designed to be:

- The accuracy of this model.
- One telegram bot to the business people access all the information.
- One video explaining the solution to the business people learn how use the solution.

## **Financial Results**

With the test database used we gettered this result:

1. With transactions detected as fraud and truly as fraud the Block Fraud earned $63,232,835.63

2. With transactions detected as fraud, but in truth detected legitimate the Block Fraud earned $25,604.72

3. With transactions detected as legitimate, but in truth as fraud the Block Fraud returned $825,711.76

The total database test in this situation was with 133093 transactions.

The machine learning model has a precision score of 99%, then the false positive is less than 0,1% making this prediction reliable.

## **Next Steps**

As next steps is expected to:

- Explain the business people how use the streamlit app to make predictions if transactions is fraud or no.
- Get new data to improve the model performance (better the recall metric).
- Train another models to help other areas.

## **Conclusion**

On this way the Block Fraud will be able to predict the frauds and do its services with more facility and the employees will be able to predict on his own if the transaction is fraud or no.

Then, is expected that the Block Fraud earn at least 99% of his predictions like truth.

## Learns

With this project my main learn was about classification models, here I learned about how train and uses classification models and I learned more about financial problems too.