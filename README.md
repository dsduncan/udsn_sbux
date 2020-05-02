# Udacity data science AB test project #

This exercise attempts to increase the effectiveness of a promotional campaign. 
It is primarily an exercise in AB testing, although there's a neat element of
optimizing for business results as well. This is based on an interview exercise
originally done by Starbucks.

## Requirements ##

The plan is to package all data necessary for training and testing in this repo.

## Objectives ##

Create a model that identifies the people who are most likely to make a purchase
after receiving the promotion (see strong caveat below). There are two metrics
for evaluating this:
1. Incremental response rate (IIR): 
(promotion_buy / promotion_total) - (nonpromotion_buy / nonpromotion_total)
2. Net incremental revenue (NIR): 
(promotion_buy * 10) - (promotion_total * 0.15) - (nonpromotion_buy * 10)

## File Descriptions ##

* `promotion_recommendation.ipynb` - Contains exploration of data and modeling
process, ultimately calls `test_results.py` to see how well I did.
* `training.csv` - Data used for training
* `test_results.py` - Evaluates the predictions of my model against `Test.csv`
* `Test.csv` - Contains test data, consumed by `test_results.py`

## Known Issues ##

For the objective functions given, this isn't actually an uplift model (i.e. the
objective is to find the individuals most likely to purchase after receiving the
promotion, not necessarily those whose likelihood to purchase increases the most
after receiving the promotion). This changes the strategy quite a bit, because
there's no incentive to leave well enough alone. I want to include as many 
people as I can who have a high likelihood to purchase, even if they don't 
receive the promotion.  
This also means I can more or less safely ignore the people who didn't receive 
the promotion in the training set.

## Results ##

 

## Licensing & Acknowledgements ## 
