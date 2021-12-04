#### Market-basket Analysis on IMDB
## Introduction

This project will deal with one of the most relevant techniques for charactering data: the discovery of frequent itemsets.

I used the IMDB dataset from Kaggle that I studied to find the most frequent actors and actress and the most frequent pairs of actors and actress. I applied a market
basket model where I used, as items, the actors and actress and, as baskets, the movies in which the actors and actress played. 

To find solutions, I applied two different algorithms: Apriori and Fp Growth. 

Due to the massive dataset, it was essential to adopt Apache Spark.


## Conclusions
After a pre processing step and an exploratory analysis, I applied the Apriori and FPGrowth algorithms to achieve the goal. By exploiting Apache Spark environment, I was able to identify the most frequent actors, pairs, triples and quadruples of actors in mostly movies of the dataset used. Both algorithms achieve the same results in different ways by managing to scale up the massive dataset used.

In conclusion, even if the two algorithms are different, they found the same results when we impose a restrictive threshold. When we imposed it, a pair should be considered frequent when played together at least 130 movies; the two algorithms identified as frequent pair:  Matsunosuke Onoe and Kijaku Ôtani, that played together 146 movies. The confidence and their lift better explain the positive relationship between the two actors and their estimates in the two algorithms confirmed the result.

In the project, it is underlined how crucial is the choice of the threshold to consider an item as frequent or not. The two algorithms behave in two different ways and their difference need to be taken into account: Apriori finds the frequent itemsets with candidate generation, while FP Growth algorithm discovers the frequent itemsets without generating candidates. 

In the beginning of the analysis I started with a less restrictive threshold (frequent was an item, pair, triples that played 10 movies) and then I used a threshold of 130 movies. Due to the choice of a more restrictive threshold or less can let us achieve different results: it is possible to achieve more triples, quadruples if the threshold is less restrictive. By a less restrictive threshold the two algorithms can achieve different results.


For the goal of the project, I checked the quality of the frequent pair, retrieved with a restrictive threshold by the two algorithms and I confirmed the goodness of result of this Market Basket Analysis.
