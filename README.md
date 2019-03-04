# Interview

## Skills I can Bring to the table

## Customer Segmentation (RFM)

### RFM (Recency, Frequency, Monetary Value)

* For data involving purchases (e.g. Service Visits) and time data, you can segment your customers to find the most valuable customers in your current book of business

#### Orders Table:

![orders](/images/orders.png)

#### Aggregate Customers by RFM:
* Recency: Days since last service
* Frequency: # of service visits
* Monetary Value: Total income from services visits

![aggregate](/images/aggregate.png)

#### Create RFM Scores:
* Calculate quartiles for each metric (111 = low recency (visited recently), high frequency (lots of visits), high monetary value)

![rfmscores](/images/rfmscores.png)

### How to monetize:

#### Identify customers and business strategies:
* 111: Visit frequently, recently, and high spend. (_loyalty rewards?_)

* 311 & 411: High spend and frequency but hasn't visted in a while. (_retention efforts?_)

* 114: Frequent small visits (_upsell opportunities?_)

* 441: One large repair (_lower maintenance visits to avoid large repairs again_)

* 444: Low value customer (_avoid spending time on low value clients or study into why they're low value_)


![rfmscores](/images/rfmscores.png)

================================================

================================================

## Predictive Analysis & Interpretation

##### These methods can be used to predict probabilities of any sort of data (i.e. What is the probability an individual or a customer segment will churn?)

### Example (Churn Prediction):

![churndata](/images/churndata.png)

### Feature Importance
#### What are the factors that contribute most to our metric of interest:
![featureimportance](/images/featureimportance.png)

### Partial Dependence
#### If a factor is important, what is it's relationship to our metric of interest:

![overtime](/images/overtime.png)
_Workers doing overtime more likely to churn_

![maritalstatus](/images/maritalstatus.png)
_Single workers more likely to churn_

![monthlyincome](/images/monthlyincome.png)
_Single workers more likely to churn_

![age](/images/age.png)
_Younger workers more likely to churn_

![totalworkingyears](/images/totalworkingyears.png)
_Newer workers more likely to churn_

### Tree Interpretation:

### Global:

![rangeinterpret](/images/rangeinterpret.png)
_Red grouping is individuals most likely to churn, what are the factors contributing to this group?_

### Individual:

![indinterpret](/images/indinterpret.png)
_Works overtime, monthly income < $2,500, single, works in sales_
## What levers can we pull?

### Can't: Marital Status, Age, Total Working Years
### Can: Pay & Overtime

# Experiment:

## How does Overtime affect churn?

![overall_ot_churn](/images/overall_ot_churn.png)

_Comparing Churn between Non-Overtime & Overtime Workers_

* Churn Rate for Non-Overtime: 10.44%
* Churn Rate for Overtime: 30.52%


### Young, single workers are the demographic with the highest risk of churn, What if we focus on overtime for them and see how it affects attrition?

![young_single_churn](/images/young_single_churn.png)

* Churn Rate for Non-Overtime: 29.67%
* Churn Rate for Overtime: 67.50%

### What about those that are also underpaid?

![young_single_lowpay_churn](/images/young_single_lowpay_churn.png)


* Churn Rate for Non-Overtime: 38.46%
* Churn Rate for Overtime: 77.27%

### How does OT affect those outside of this high risk group?

![older_notsingle](/images/older_notsingle.png)

* Churn Rate for Non-Overtime: 7.14%
* Churn Rate for Overtime: 16.88%

### How to monetize:

#### What are the levers we can pull to move our metrics?
* Prevent OT from occuring with high-churn-risk groups
* Model can also predict who is a high risk and we can focus our efforts on retention with high probability individuals
