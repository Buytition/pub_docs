[TOC]

# Use Bookmarklet to Quickly Save Timeline Item

SaveNowClub uses bookmarklets for bookmarking web content. Bookmarklets are little javascript links that live in the bookmarks toolbar of your browser.

Here's the bookmarklet we offer: <a href="javascript:q=location.href;if(document.getSelection){d=document.getSelection();}else{d='';};p=document.title;void(open('https://savenowclub.com/timeline/show-form/create-item?url=%27+encodeURIComponent(q)+%27&description=%27+encodeURIComponent(d)+%27&title=%27+encodeURIComponent(p),%27Pinboard%27,%27toolbar=no,width=550,height=400%27));">popup</a> opens a little form window when you want to save a page. It's the fastest way to add a web content.

How to Install and Use Bookmarklet: if you need help to install and/or use our bookmarklet, please refer [this guide](https://www.howtogeek.com/189358/beginner-geek-how-to-use-bookmarklets-on-any-device/).

## Issue with Bookmarklet on Android Chrome

This bookmarklet has been tested working on Chrome browser on PC, Mac and iPhone.  On Chrome browser on an Android phone, clicking this bookmarklet may not open up popup form, if that happens, use the method in [this tutorial](https://paul.kinlan.me/use-bookmarklets-on-chrome-on-android/) can solve that problem. 

# Use Parent Chooser to Quickly Organize Saved Timeline Item

By default, saved timeline item is at top level. Picking a proper uncertainty for it is a great way to organize the timeline item under proper theme for later reference.  You may use `Parent Chooser` tool located on each timeline item page to quickly create or pick existing uncertainty for the item.

# Criteria of Predictions

For content that satisfy the following criteria, it can be classified as `Prediction` type of content:

1. predictions with clear target time frame: clear future target time point of predicted event
2. predictions that are checkable: clear prediction that can be checked by facts
3. predictions that matter: predicted event must matter to audience

Here is [an example](https://finance.creaders.net/2022/06/22/2497071.html) of prediction that does not meet our criteria: 

> 威尔森（Michael Wilson）在内的摩根士丹利策略师21日表示，标普500指数要跌到2,900点至3,100点，才会更加完全反映在经济衰退期间典型的企业获利萎缩。大摩策略师群表示：“目前看来，根据联准会陷入的通膨处境，经济衰退不再只是个尾部风险。”

The reason for not meeting our criteria is because it is a conditional statement of future scenario, cannot be proved as true or false by facts; also it is missing a clear target time frame.

# Our Approach Evaluating a Prediction

From perspectives of statistics and data, predictions of future events are in the forms of probability, this fact makes it hard to evaluate quality of a prediction since a historical event happens only once, you have no chance to calculate actual probability of an event and compare that with the predicted probability.

Instead, we use a simplified and a more straight-forward approach to evaluate prediction accuracy.  We view prediction as one non-random direction pointed out by predictors, after target time of predicted events has been reached, we compare actual fact against original prediction, if they match, then we rate the prediction as `hit`, otherwise, it's rated as `miss`. 
