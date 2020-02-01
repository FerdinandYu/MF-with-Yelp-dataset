# MF-with-Yelp-dataset

# Todo breakdown:

## Coding 
- [ ] Choose one data set: Amazon/Yelp
- [ ] Json parser: Json (in HDFS/RDD) -> filter irrelevant entries out -> Spark dataframe
      Entries to keep: ReviewID, UserID, ItemID, Timestamp, Rating
- [ ] Sparse matrix representation: Spark dataframe -> Sparse matrix R
- [ ] Implementation of eALS
- [ ] Pilot experiments - scalability
- [ ] Full scale experiments - performance indicator (scalability, cache hit, time-consumption, RMSE)
- [ ] (opt) online updating


## Document
- [ ] a description of the adopted solution 
- [ ] designed algorithms plus related global comments/description; 
- [ ] comments to main fragments of code 3
- [ ] experimental analysis, concerning in particular scalability
- [ ] comments about the experimental analysis outlining weak and strong points of the algorithms.
- [ ] an appendix including all the code the code.

## Issues
- [x] Ratings range from 1.0 to 5.0
- [x] Can one user give multiple ratings for one business -> Yes
- [ ] How to implement spark cluster
- [ ] load inbalance
- [ ] RAM usage: Yelp: 0.73M reviews, 25K users, 25K items, 128 latent features, .9989 sparsity
                 Amzn: 5M reviews, 117K users, 75K items, 128 latent features, .9994 sparsity
- [x] Parameter values: ```math
                        $$\lambda = 0.01$, $K=128$, $W = 1_{K \times K}$, $c_0=512, \alpha=0.4$$
                        ```
