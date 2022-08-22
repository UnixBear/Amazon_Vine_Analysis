<img src="https://user-images.githubusercontent.com/101137700/181667608-df9f2829-8c87-43fb-a147-774f942b734e.png" width="50"> <img src="https://user-images.githubusercontent.com/101137700/181668163-8e2e28e1-b464-465b-a1a3-29bb096f56ff.png" width="50"> <img src="https://user-images.githubusercontent.com/101137700/181668354-3954e73d-4258-4bb6-922e-7c3aa4bbca7d.png" width="50"> <img src="https://user-images.githubusercontent.com/101137700/181668486-649e7cf7-8af9-4e7e-a9fd-948a43a31e4b.png" width="50">
![](/images/AmazonVineBanner.png)

[Amazon Vine](https://en.wikipedia.org/wiki/Amazon_Vine) is an Amazon program that wrassles up trustworthy reviewers to provide reviews to companies who pay a fee.


## AMAZON VINE REVIEW GOALS
1. to perform an ETL on raw vine review data 
2. to see if there is any interesting correlations with reviews and vine participation and whether or not there is a bias


## Procedure
Using [Google Collab](https://colab.research.google.com/), you can follow along with the steps using first the ETL notebook first follows by the analysis notebook
## Data  
Of the [possible datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt) we're using video games dataset as a test run. Here is a snapshot of the first 20 rows of data:

![](./images/Raw%20DataFrame.png)

## Analysis

### Reviewers
![dataframe screenshot](./images/totalPaidReviewers.png)
As one can see, there are literally no Vine reviewers for this dataset so it would be impossible to determine if there was a bias in 5 star reviews with vine reviewers.  More data would be needed, preferably actual participants who have at least 20 reviews under their belt.

### Further cleaning of data
From consideration, we removed those reviews where they had less than 20 votes and that the ratio of "helpful" votes to the total amount of votes was >= 50%

### 5-✪ reviews
Since there were literally no Vine reviews in this dataset, we could only see the non-participant input and of all the reviews that had 5 stars. Here is a breakdown of the reviews:
![star-reviews](./images/ReviewBreakdown.png)

Since we had 1685 reviews in total, the percentage of 5 star reviews was (631 / 1685 * 100) 37.45%






