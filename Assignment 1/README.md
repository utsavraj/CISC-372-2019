### Note:
* **A1.ipynb** contains the running to model to. find the best hypertuned model for the AirBnB dataset
* **A1_example (Commented).ipynb** contains the commented example code

# Assignment One Q&A

#### So here we have a public leaderboard and a private leaderboard. Each of them use a different subset of the testing set test.csv (well we can just treat them as two different testing sets). For the public leaderboard, you can try 3 times per day and observe the performance right away. Why should we limit the number of trials per day?

#### -------------------------------------------------------------

#### For the private leaderboard, it will be used only after the assignment submission deadline for evaluation. Why it is designed like this??
This is done so that people do not create models that overfits/replicates the answers for the testing sets as they will have higher f1-mean score but not an useful model. Using the testing set allows people to judge how their model performs in data it has never seen before and hence, ensures that the model is not overly fitting the training sets.

#### -------------------------------------------------------------

#### Which model did you use (just pick one of them) and how did you control its flexibility? When did you make it more flexible and when did you make it less?

Logistic Regression is one of the models are used 

#### -------------------------------------------------------------
