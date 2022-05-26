[TOC]

# Our Approach Evaluating a Prediction

From perspectives of statistics and data, predictions of future events are in the forms of probability, this fact makes it hard to evaluate quality of a prediction since a historical event happens only once, you have no chance to calculate actual probability of an event and compare that with the predicted probability.

Instead, we use a simplified and a more straight-forward approach to evaluate prediction accuracy.  We view prediction as one non-random direction pointed out by predictors, after duration of prediction passes, we compare the factual direction against the original predicted direction, if they match, then we rate the prediction as `Hit`, otherwise, it's rated as `Miss`. 
