### Note:
* **A1.ipynb** contains the running to model to. find the best hypertuned model for the AirBnB dataset
* **A1_example (Commented).ipynb** contains the commented example code

# Final Design
* Used the already preprocessed data given the example to train several classificaton models
* Choose the two highest F1-macro score models - Logistic Regression (0.67877) & Random Forest (0.674981)
* For Both Models:
  * Used Randomsied Search CV (5 Times CV)  to get an idea for range for parameters to tune
  * Used Grid Search CV (5 Times CV) to get the ideal parameters value
* Used the best model (Logistic Regression) to predict the test set provided and submitted the answer on Kaggle 
* If Significant increase in accuracy then, continued with Grid Search with lower range, otherwise decrease the number of parameters to tune
* Repeat the last two steps with the other model (Random Forest).

# Assignment One Q&A

#### So here we have a public leaderboard and a private leaderboard. Each of them use a different subset of the testing set test.csv (well we can just treat them as two different testing sets). For the public leaderboard, you can try 3 times per day and observe the performance right away. Why should we limit the number of trials per day?

This not only forces the people to think on how their model works and how to optimise it more before trials as well as save computation resources but also limits the chance to overfit the training dataset and evens the playing field for all the people by providing only 3 trials per day.

#### -------------------------------------------------------------

#### For the private leaderboard, it will be used only after the assignment submission deadline for evaluation. Why it is designed like this??
This is done so that people do not create models that overfits/replicates the answers for the testing sets as they will have higher f1-mean score but not an useful model. Using the testing set allows people to judge how their model performs in data it has never seen before and hence, ensures that the model is not overly fitting the training sets.

#### -------------------------------------------------------------

#### Which model did you use (just pick one of them) and how did you control its flexibility? When did you make it more flexible and when did you make it less?

Logistic Regression is one of the models used in my code. It's flexibility was controlled by hypertuning the parameters for a certain range - the smaller the range provided, the less flexibility it had. When the model started to perform poorly/little increase than before with F1-score, I relaxed the model and vice versa.

#### -------------------------------------------------------------
