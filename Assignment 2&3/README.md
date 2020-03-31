### Note:
* **A2.ipynb** contains the modified script to to find the best hypertuned model for the Amazon dataset
* **A2_example (Commented).ipynb** contains the commented example code provided by the teacher
* **A3.ipynb** contains the modified script to to find the best hypertuned model for the Amazon dataset
* **A3_example (Commented).ipynb** contains the commented example code provided by the teacher

# Final Design
## For A2:
* Sample Text

## For A3:
* Sample Text

# Assignment Q&A

#### For script A2, what is the purpose of `class_weight='balanced'` in cell #3?
`class_weight='balanced'` automatically adjust weights inversely proportional to class frequencies (tfidf) in the input data. The idea behind this is that to increase the penalty for misclassifying minority classes to prevent them from being “overwhelmed” by the majority class.

#### -------------------------------------------------------------

#### In script A2, CountVectorizer is responsible for preprocessing. How can we add stop word removal by using this class? How can we change word-based n-gram to char-based ngram using this class?

For CountVectorizer, we can pass the parameter:
* stopword to add stop word removal eg. stop_words='english' for English
* analyzer to change word-based n-gram to char-based ngram eg. analyzer='char'

#### -------------------------------------------------------------

#### In Assignment #1, we use GridSearchCV with cross-validation. In A2, are we still using cross-validation? If not, what did we use?

Sample Text

#### -------------------------------------------------------------

#### In script A3, what is the tensor shape of the output from `keras.layers.CuDNNGRU(100)`?

Sample Text

#### -------------------------------------------------------------

####  In script A3, what is the purpose of `clipnorm=4`. for the Adam optimizer? Why we need to do it?

Sample Text

#### -------------------------------------------------------------
