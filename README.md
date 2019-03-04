# Interview

## Skills I can Bring to the table

## Customer Segmentation (RFM & K - Means Clusters)

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

#### Identify top customers:
* 111: Visit frequently, recently, and high spend
* 311 & 411: High spend and frequency but hasn't visted in a while, worth retention efforts?
* 444: Low value customer

![rfmscores](/images/rfmscores.png)
