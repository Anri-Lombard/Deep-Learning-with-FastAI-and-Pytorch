# FastAI course by Jeremy Howard V.5

## Process I found useful for learning this course
1. Listen to lecture completely and take notes (just to help understanding - I don't go back much to them)
2. Retry everything he did on my own, tinker with notebooks until I get stuck, then check the video for what he did
3. Try to change his models to my own ideas (pretty hard to do sometimes)

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



After I finish the video version of the course, my plan is to read the entire book; then I'll append the extra notes and work to the current repo.
