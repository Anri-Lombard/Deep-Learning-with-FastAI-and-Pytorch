# FastAI course by Jeremy Howard V.5

## Rating of the course
I did not know much about this course, and could not find proper ratings for it, which is why I had low expectations of it. By the third video I realized this is probably the best Machine Learning course I've ever taken, and made the effort to scour high-profile reviews of the course to see if I was missing something. I was not. This is a great course. I would rate it 9/10 if I was a professional with great eperience in the field, and 10/10 if I was a beginner (which I see myself as still). Jeremy is patient and clearly enjoys teaching the course, but his advice reaches far beyond just the course. He recommends strategies for learning Machine Learning by iterating models, to read papers and books in the field, and does so humbly without showing off that he is one of the world's best Machine Learning researchers.

## Process I found useful for learning this course
1. Listen to lecture completely and take notes (just to help understanding - I don't go back much to them)
2. Retry everything he did on my own, tinker with notebooks until I get stuck, then check the video for what he did
3. Try to change his models to my own ideas (pretty hard to do sometimes)
4. Experiment and play (This is important. When I move to a new lecture immediately, the content does not stick). I try to document the code as well to explain it to myself.

## Lesson 1 (Getting Started)
* Built an Image Classifier
	- Initially was a bird classifier
	- Altered it to an apple classifier
* Classifiers are neural networks that take an image and output a probability distribution over the classes, picking the class with the highest probability

## Lesson 2 (Deployment)
* Got acquainted with Huggingface spaces
	- Used it to deploy minimal model with user interface
	- Used it to run cat/dog classifier by uploading images of either
* Huggingface spaces is a great way to deploy models and share them with others
 
## Lesson 3 (Neural Net Foundation)
* Gradient descent is a mathematical optimization technique, which is used to minimize the cost function of a neural network.
* Learned how gradient descent works practically
	- Built an excel-based regression model using tedious methods, then matrix multiplication
* Learned about the various (500+) neural net architectures in the timm library
* Learned to prioritise quick iteration over data accumulation
* Learned importance of hyper parameters in choosing parameters for model
* Used Paperspace notebooks
	- An upgrade to Kaggle and Google Colab since it uses an actual (not virtual) machine.

## Lesson 4 (NLP)
* Learned to use the state-of-the art Huggingface transformers to build a model
* NLP is an acronym for Natural Language Processing
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
* Random Forests are an ensemble of decision trees that make predictions by averaging the predictions of each component tree
* We implemented a TwoR classifier which is a Random Forest with 2 trees. It is a Random Forest because it uses a random subset of the data, and it is a TwoR because it has 2 trees.
	- A TwoR classifier has 2 binary splits, which means 2 trees. Each tree has 2 leaves, which means 4 leaves in total.
* Jeremy advises to use Random Forests on tabular data, so we could get a feel for how this data works and how to best build our model
* Learned about bagging, which is a method of creating a random forest
	- Bagging is an acronym for Bootstrap Aggregation
	- Bootstrap is a method of sampling with replacement
	- Aggregation is a method of combining the results of the samples
* To measure the efficiency of a split we use Gini. Gini is a measure of the probability of a random sample being incorrectly classified if it is randomly labelled according to the distribution of labels in the subset.
	- Higher Ginis are worse
* Learned about the out-of-bag-error
	- This is the error rate of the model on the data that was not used to train the model
	- This is a good way to measure the accuracy of the model without having to create a validation set
* Random Forests are hard to mess up, so we can use them as a baseline model
* Gradient Boosting is a method of creating a Random Forest
	- It is a method of creating a Random Forest by creating a single tree at a time
	- Each tree is created to correct the errors of the previous tree
	- This is a method of creating a Random Forest because it uses a random subset of the data
	- This is a method of creating a Random Forest because it creates a single tree at a time
* The Kaggle leader private leader board is a good way to measure the accuracy of your model, without bias from the programmers
* jeremy recoomends iterating on a model rather than trying to build the best model from the start and realize it is not good enough too late
* Did a Kaggle top submission walktrough
	- fastcore.parallel is a library that allows you to run code in parallel which speeds up any process that would have been done serially
	- ImageDataLoaders is a class that allows you to load images into a model
	- vision_learner is a function that creates a specific type of model
	- lr_find is a function that finds the best learning rate for your model
	- submit as soon as we can
	- For quick iteration everything needs to be fast and easy, even submitting to Kaggle
	- use fastkaggle to share notebooks as well
	- could make different notebooks for each model
	- data augmentation is a method of creating more data by altering the existing data
	- test time augmentation is a method of creating more data by altering the existing data at test time
* Jeremy never uses AutoML or hyper-parameter optimization, he prefers thinking like a scientist and having hypothesis he could test with his models.
* Don't just use a model because it is used by the majority. In this case it is the resnet, Jeremy preferst to use others such as convnext




* In progress... 

After I finish the video version of the course, my plan is to read the entire book; then I'll append the extra notes and work to the current repo.
