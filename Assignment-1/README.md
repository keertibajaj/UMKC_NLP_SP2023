# Report on Process and Observations
## Part 1: Probability Distribution Metrics
Calculated information, entropy, cross-entropy and KL Divergence of given distribution.
For cross entropy and divergence, another distribution is considered for calculations
</br>
- Information: I(x) = -log<sub>2</sub>(p(x))
- Cross Entropy: CE(p, q) = $-\sum {p(x)log_2} q(x)$
- KL Divergence: DKL(p, q) = $\sum p(x)log_2  \frac{p(x)}{q(x)}$


## Part 2: Spam Dataset
### Data Preprocessing Pipeline
The data preprocessing consisted of the following steps:
1. **Cleaning:** Removing duplicate data from the .csv file.
2. **Tokenization:** Splitting text data into words.
3. **Part-of-speech Tagging and Filtering:** Identify the POS for each word and filter out words that are not nouns and verbs as required.
4. **Vectorization:** Converting the text data into numerical features using CountVectorizer.
5. **Stop Words:** Removing english stop words such as 'a', 'the', etc,. that usually make low impact on context.

### Modeling
Four Naive Bayes models were built using CountVectorizer, each with a different set of parameters:
1. Model 0: Unigram model with default parameters.
2. Model 1: Only nouns with default parameters.
3. Model 2: Only verbs with default parameters.
4. Model 3: Nouns and verbs with (1,3) n-gram model and default parameters.

Additionally, four logistic regression models were built with comparable parameters to the Naive Bayes models.

### Performance
The performance of each model was evaluated using accuracy score on the test set.</br>
![image](https://user-images.githubusercontent.com/45763954/223944675-bf7bd5ba-e2f7-4f58-9fa2-78cb05d719f4.png) </br>
- Overall, using Naive Bayes classifier, Model 3 performed the best with an accuracy score of 0.9858, followed by Model 0 with an accuracy score of 0.9845. 
Model 1 and Model 2 performed slightly worse comparatively, with accuracy scores of 0.9819 and 0.9284, respectively. 
And using Logistic Regression, Model 0 performed the best with an accuracy score of 0.9755, followed by Model 2 with an accuracy score of 0.9613. 
Model 3 and Model 2 performed slightly worse comparatively, with accuracy scores of 0.9522 and 0.9097, respectively. </br>
- Naive Bayes Model performed better than logistic regression in this case. But this need not be the case always. 
The performance of these two algorithms can depend on the specific dataset and the nature of the problem being solved.
- In general, Naive Bayes tends to perform well on text classification tasks, especially when dealing with high-dimensional data. 
This is because Naive Bayes assumes independence between features, which makes it computationally efficient and reduces the risk of overfitting. 
Naive Bayes also tends to handle noisy data well, and can work with small training datasets.
- Logistic regression, on the other hand, is a more flexible algorithm that can work well with both linear and non-linear relationships between 
the input features and output variable. Logistic regression can also handle large datasets and has a strong theoretical foundation.

### Discussion
- The results show that the (1,3) n-gram model with both nouns and verbs (Model 3) performed the best, 
which suggests that considering the context of the words in the text data can improve model performance. 
Model 0, which used the unigram model, also performed well, which may be due to the fact that it considers all words in the text data without any filtering.
- Models 1 and 2, which only considered nouns or verbs, performed slightly worse. This could be because these models are more restrictive 
in terms of the features they consider, and may miss important information in the text data.
- Comparing the Naive Bayes models to the logistic regression models, we see that the results are comparable. 
This suggests that the choice of algorithm may not have a significant impact on model performance in this case.

### Recommendation
- Based on these results, we recommend using Model 3, which uses both nouns and verbs and (1,3) n-gram model, for classification tasks involving similar text data. 
However, there is potential for further optimization by tuning hyperparameters such as the alpha value for the Naive Bayes models or the regularization 
strength for the logistic regression models.
- Additionally, it may be worthwhile to consider alternative text preprocessing techniques such as lemmatization or stemming, or using more advanced algorithms 
such as Support Vector Machines or neural networks. Further exploration of these options may improve model performance.
