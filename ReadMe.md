# FastAI course by Jeremy Howard V.5

## Process I found useful for learning this course
1. Listen to lecture completely and take notes (just to help understanding - I don't go back much to them)
2. Retry everything he did on my own, tinker with notebooks until I get stuck, then check the video for what he did
3. Try to change his models to my own ideas (pretty hard to do sometimes)
4. Experiment and play (This is important. When I move to a new lecture immediately, the content does not stick). I try to document the code as well to explain it to myself.

## Lesson 1 (Getting Started)
* Built an Image Classifier
	- Initially was a bird classifier
	- Altered it to an apple classifier

## Lesson 2 (Deployment)
* Got acquainted with Huggingface spaces
	- Used it to deploy minimal model with user interface
	- Used it to run cat/dog classifier by uploading images of either
 
## Lesson 3 (Neural Net Foundation)
* Learned how gradient descent works practically
	- Built an excel-based regression model using tedious methods, then matrix multiplication
* Learned about the various (500+) neural net architectures
* Learned to prioritise quick iteration over data accumulation
* Learned importance of hyper parameters in choosing parameters for model
* Used Paperspace notebooks
	- An upgrade to Kaggle and Google Colab since it uses an actual (not virtual) machine.

## Lesson 4 (NLP)
* Learned to use the state-of-the art Huggingface transformers to build a model
* Learned about NLP classification
	- Built a model for the Kaggle competition: U.S. Patent Phase to Phase Matching
	- Used tokenisation and numericalization to convert data into a usable format for the model to do training
	- Huggingface has pre-trained models that can be used as base models
* Learned about under-fitting and over-fitting models, as well as creating a good validation set
* Learned about the problem of measuring models with a single metric (can result in serious damage to humans reliant on it's performance/predictions)
	- Goodhart's Law states that "When a measurement becomes a target, it ceases to be a good measure." 
* Learned how to understand the Pearson Correlation
	- I've learned this in a statistics course in University, but the practical application is simple: negative means the higher the X value, the lower the Y value, while positive means the higher the X value the higher the Y value
* Used Paperspace to run notebooks
	- Again, much faster than Kaggle

## Lesson 5 (From scratch model)
* Built a model to predict survival for the Kaggle Titanic challenge
* Learned about replacing missing values, normalising skew data, broadcasting, and fitting a linear model
* Constructed Deep Learning Neural Network from scratch
* Used Fastai framework to skip over all manual steps that speed up model production and iteration
	- Does preprocessing with minimal guidance from programmer
	- Recommends good learning rates without tedious experiments
* Learned about Ensembling
	- Build multiple models and combine predictions
* Got an introduction to Random Forests
	- Jeremy describes it as "An ensemble of trees, that are in turn ensembles of binary splits."
	- Binary split splits rows into 2 groups (hence binary)
	- Continuous variables and categorical variables are treated slightly differently (thank goodness for Mathematical Statistics!)
	- We find the best binary split
	- Next lesson we'll do this recursively
* implemented a variant of the OneR classifier

## Lesson 6 (Random forests)
* Random Forests make almost no assumptions about the data and require almost no preprocessing
* Implemented a TwoR model
	- Basically 2 binary splits
	- creates a decision tree
* Jeremy advises to use decision trees on tabular data, so we could get a feel for how this data works and how to best build our model
* Learned about bagging: create many independent decision trees and take the average of all their predictions. If the average of the errors are zero, then they are independent and unbiased (also learned this in a mathematical statistics course in university; a common way to do model validation is to check if the residuals, or errors, are normally distributed)
* To measure the efficiency of a split we use Gini. Gini is a function that determines how well a decision tree was split, ranging from 0 to 0.5, where the lower it is the better the split
	- To look at the Gini of all splits we could use a "feature importance plot"
	- Helps find the best variables to look at
	- More trees always increase accuracy
* Learned about the out-of-bag-error. It is basically measuring the prediction error on the training set using error trees that were not included in the training. This removes the need of a validation set as it helps us to spot overfitting
	- Basically it uses bagging on unused data.
	- Bagging could apparently be done on models other than Random Forests as well.



After I finish the video version of the course, my plan is to read the entire book; then I'll append the extra notes and work to the current repo.
