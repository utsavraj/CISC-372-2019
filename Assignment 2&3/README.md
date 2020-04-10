### Note:
* **A2.ipynb** contains the modified script to to find the best hypertuned model for the Amazon dataset
* **A2_example (Commented).ipynb** contains the commented example code provided by the teacher
* **A3_example (Commented).ipynb** contains the commented example code provided by the teacher

# Final Design
### We choose to improve Assignment 2's code has it already has a very high accuracy at 92.273%
* First, we played around with the parameters of SVC model to see if we can increase the f1-mean score.
  * We went through C, alpha (different values than the comment), penalty (different values than the comment),  gamma and all of them's best performance were their default values.
  * Only changing the kernel to sigmoid increase the f1-mean score by around 1.5%
* It felt due to the metrics that our data was overfitting the training data and in order to decrease not only this issue but also to not rely on only a single classifier, Bagging was used (creates an ensemble of model). Thus, we reached to the accuracy of 94.298% 

# Assignment Q&A

#### For script A2, what is the purpose of `class_weight='balanced'` in cell #3?
`class_weight='balanced'` automatically adjust weights inversely proportional to class frequencies (tfidf) in the input data. The idea behind this is that to increase the penalty for misclassifying minority classes to prevent them from being “overwhelmed” by the majority class.

#### -------------------------------------------------------------

#### In script A2, CountVectorizer is responsible for preprocessing. How can we add stop word removal by using this class? How can we change word-based n-gram to char-based ngram using this class?

For `CountVectorizer`, we can pass the parameter:
* `stopword` to add stop word removal eg. `stop_words='english'` for English
* `analyzer` to change word-based n-gram to char-based ngram eg. `analyzer='char'`

#### -------------------------------------------------------------

#### In Assignment #1, we use GridSearchCV with cross-validation. In A2, are we still using cross-validation? If not, what did we use?

We still using cross-validation as we are divide the training dataset into 80% for training the model and 20% to testing the model to see how it performs with different parameters.

#### -------------------------------------------------------------

#### In script A3, what is the tensor shape of the output from `keras.layers.CuDNNGRU(100)`?

The tensor shape of the output from `keras.layers.CuDNNGRU(100)` is (6 * 100) based on the source code on [GitHub]

#### -------------------------------------------------------------

####  In script A3, what is the purpose of `clipnorm=4`. for the Adam optimizer? Why we need to do it?

The purpose of `clipnorm=4` is that all parameter gradients will be clipped to a maximum norm of 4. This helps in preventing messing up of parameters due to vanishing/exploding gradients and losing the progress made while training the network.

#### -------------------------------------------------------------

[GitHub]: https://github.com/tensorflow/tensorflow/blob/a6d8ffae097d0132989ae4688d224121ec6d8f35/tensorflow/python/keras/layers/cudnn_recurrent.py#L261
