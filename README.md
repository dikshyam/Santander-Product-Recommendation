# Santander-Product-Recommendation

### Problem Statement
The dataset given for this Kaggle Competition has 1.5 years of customer behaviour data clubbed with 17 binary columns representing products that the bank offers and if that customer has it. Under their current recommendation system that Santander uses for marketing products, a small number of Santander’s customers receive many recommendations while many others rarely see any resulting in an uneven customer experience. In their second competition, Santander is challenging Kagglers to predict which products their existing customers will use in the next month based on their past behavior and that of similar customers. The challenge is to predict what a customer will buy in addition to what they already had at 2016-05-28.

### Data Description
Column #1: Fetch Date ranging from 2015-01-28 to 2016-05-28
Columns #2-#24: Customer Demographics(Age, Sex, Income, Location,etc.)
Columns #25-#48: Products that customers own

### Method 1: Association Rule Mining
#### Wikipedia Definition of ARM:
*Association rule learning is a rule-based machine learning method for discovering interesting relations between variables in large databases. It is intended to identify strong rules discovered in databases using some measures of interestingness.*

Association rules are if-then statements that help to show the probability of relationships between data items within large data sets in various types of databases. Association rule mining has a number of applications and is widely used to help discover sales correlations in transactional data or in medical data sets.
Association rules are created by searching data for frequent if-then patterns and using the criteria support and confidence to identify the most important relationships. Support is an indication of how frequently the items appear in the data. Confidence indicates the number of times the if-then statements are found true. A third metric, called lift, can be used to compare confidence with expected confidence.

### Intuition behind using this approach:
Given the large dataset, and by setting up a high threshold for support and confidence, one could get frequent itemsets for customers i.e. rules. Using these frequent item-sets, we could recommend new products to customers on the basis of what they already own.
