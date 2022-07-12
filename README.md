# capstone-project

Blossom Bank also known as BB PLC is a multinational financial services group, that offers retail and investment banking, pension management, asset management and payments services, headquartered in London, UK.

New technology comes with demerits and loop holes , the bank has been experiencing some fraud. The problem here is to create a system that identifies patterns that correlates with fraud and nip fraud  in the bud before it occurs. The data provides us with attributes of a transaction . The attributes will be evaluated to observe whether there are attributes that engages in similar patterns before fraud  occurs


Exploratory Data Analysis


Cash out and payment has the highest rate of transaction , cash in is lower than cash out for the bank in terms of count 
Some accounts received as much as 98 credit  transactions count while some accounts just had 1 credit transaction

In terms of amount value , transfer had the largest volume of transaction while cash out and cash in where relatively the same 

Most positive fraud occurred with just two payment types, cash out and transfer

Most of the transaction used between 15 and 20 hours, while some outliers where recognized

There is a strong correlation between old balance   and new balance of the destination account  which is normal

No strong correlation was seen between fraud and any feature in the data set , this might be due to the large unbalance in the data between fraud and non fraudulent transaction in the bank


Machine Learning Insights

There are several ways to approach this classification problem taking into consideration this unbalance.

Collect more data? Nice strategy but not applicable in this case
Changing the performance metric:
Use the confusion matrix to calculate Precision, Recall
F1score (weighted average of precision recall)
Use Kappa - which is a classification accuracy normalized by the imbalance of the classes in the data
ROC curves - calculates sensitivity/specificity ratio.
Resampling the dataset

Essentially this is a method that will process the data to have an approximate 50-50 ratio.
One way to achieve this is by OVER-sampling, which is adding copies of the under-represented class (better when you have little data)
Another is UNDER-sampling, which deletes instances from the over-represented class (better when he have lot's of data)


Because of the unbalance ratio of fraudulent transactions to non fraudulent transactions in the bank, the data has to be balanced so that our machine learning model can work in situations where  fraud is much higher and also lower 

Another challenge is to make sure that out model detect as many as possible true positives and minimize false negatives in the machine learning model.

Accuracy score examines how well the trained dataset is able to predict true positives and true negatives, it is important for our model to be able to spot fraud 100 percent of the time
cross validation across the 4 models is 100% , which proves that our model is not over fitted or under fitted across the data set
The ROC AUC score helps us to compare ground truth to predicted probabilities , some the models examined gave us 100 percent when examined, personally since we have a model that have done a 100 percent across the three validation techniques , i will go for any of the four models
Based on the nature of the institution , i will suggest that the model should be more concerned with limiting false negatives that is fraud that go undetected rather than false positives


Benefit to Blossom Bank

The Benefit of the project to blossom bank is that patterns that precedes fraud can be detected and measured  , thus enabling the bank to detect fraud early before it occurs

This will improve safety in the bank , thus customers will feel secured.

Growth in the bank customer base and ranking.

Pattern in fraud can be detected and blocked as continuous growth occurs. 


