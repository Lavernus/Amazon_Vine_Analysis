# Amazon Review Analysis
## Overview
The Amazon Vine program allows companies to pay a small fee and provide products to the Vine members who are then required to  review the products for them. The client wishes to know if there is a noticeable bias toward favorable reviews if the reviewer is a Vine member.
### Purpose
Utilizing PySpark to analyze the review data and AWS to store the data, we will extract a review dataset from Amazon and develop summary statistics from it that will help determine bias in Vine reviews. In this case we will be using their reviews for digital video games.
## Setup
In order to analyze the reviews that had the most impact, I filtered the dataset to only contain reviews that had more than 20 total votes. Of those reviews, I wanted those that were the most helpful, so I further filtered it to contain only the reviews where their number of helpful votes divided by their total votes was equal or greater than 50%.
### Issues
Unfortunately, after filtering the dataset, none of the reviews contained were by Vine members, which will affect the rest of the analysis.
## Results
- Review Totals
   
   ![totals.png](https://github.com/Lavernus/Amazon_Vine_Analysis/blob/main/Images/totals.png)
  -  There were zero Vine reviews in total and 1,685 non-Vine reviews.
- Total 5-Star Reviews
  
  ![stars.png](https://github.com/Lavernus/Amazon_Vine_Analysis/blob/main/Images/stars.png)
  - Since there were no Vine reviews, there were zero 5-star Vine reviews as well. Non-Vine reviews, however, had 631 5-star reviews.
- Percentage of 5-Star Reviews
  
  ![percentage.png](https://github.com/Lavernus/Amazon_Vine_Analysis/blob/main/Images/percentage.png)
  - Since there were no Vine reviews, it would be impossible to calculate the percentage of 5-star reviews for Vine members. For non-Vine members, the percentage of 5-star reviews for video games was 37.4%.
## Summary
Since there were no Vine reviews in the filtered dataset it would be impossible to tell whether there is any positivity bias in Vine reviewers. I would highly reccommend redoing this analysis with a different dataset that has enough Vine reviewers to accurately analyze any bias. 

There are some conclusions that we can draw from this analysis, however. Digital video games are obviously an industry where paid reviews, at least on Amazon, are not the norm. A better analysis would be conducted on categories of products where companies need help convincing people to buy them. This could be industries where smaller companies have to compete with one or two brands that dominate the space, or industries that sell luxury goods that a normal consumer would need to be convinced to splurge on. 

With a new dataset, bias could be determined by comparing the percentage of 5 star reviews between Vine reviewers and non-Vine reviewers. If there was a much larger percentage in Vine reviewers, we could say that Vine members tended to review products more positively, and vice versa. An additional analysis could be performed by analyzing the percentage of 1 star reviews each group gave, as it could inform whether Vine reviewers felt comfortable criticizing products that they recieve for free or if they tended to avoid giving too low of a score to products.
