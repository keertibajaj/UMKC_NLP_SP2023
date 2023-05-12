# Report on Process and Observations
## Dataset
**NLTK Movie Reviews Dataset**: The NLTK movie reviews dataset is a collection of 2000 movie reviews, each of which is labeled as either positive
or negative. The dataset contains 1000 positive and 1000 negative reviews. Each review is a short paragraph of text, and the labels are assigned by
human annotators. The reviews are from a variety of sources, including online movie review websites, newspaper articles, and academic journals. </br>
**Large Movie Review Dataset**: The Large Movie Review Dataset (LMDB) is a collection of 50,000 movie reviews from the Internet Movie Database
(IMDb). The reviews are labeled as either positive or negative, and they are highly polarized. This means that the reviews are either very positive
or very negative, and there are very few neutral reviews. The LMDB is a valuable resource in sentiment analysis. It is a large and well-labeled
dataset, and it is easy to use.
## Part 1: Training Own Word2Vec Model
Word2Vec is a neural network model that can be used to learn vector representations of words. These vector representations can be used to find the
similarity between words, to generate word embeddings, and to perform other natural language processing tasks. </br></br>

Once we have trained the Word2Vec model, we can use it to find the similarity between words, to generate word embeddings, and to perform other
natural language processing tasks.
**Results on Current Data** (Accuracy Values):
1. Naive Bayes - 66.96%
2. Logistic regression - 68.12%

## Part 2: Deep Learning Models
### Models Used:
1. RNN
2. LSTM
### Design of Models:
<ol type="a">
  <li>Fewer Parameters (32)</li>
  <li>More Parameters (128)</li>
  <li>Overfitting Strategies Used</li>
</ol>

**Note:**
The above combination of deep learning models result in a total of 6 models. For overfitting strategies, I avoided creating another model as I can compare it with
the More Parameters model. </br>
1. RNN - 1: RNN with fewer parameters
2. RNN - 2: RNN with more parameters
3. RNN - 3: RNN with more parameters and overfitting strategies
4. LSTM - 1: LSTM with fewer parameters
5. LSTM - 2: LSTM with more parameters
6. LSTM - 3: LSTM with more parameters and overfitting strategies

**Results:** </br>
![image](https://user-images.githubusercontent.com/45763954/234467878-a4963d76-711c-4463-9366-c450cbd02b27.png) </br>
### Observations:
1. The performance of the deep learning models is generally better than that of the statistical models but highest accuracy is for Logistic Regression.
2. LSTM models generally perform better than the RNN models, which is expected given the nature of the dataset.
3. Models with overfitting strategies perform better than those without.
4. Interestingly, adding more parameters did not necessarily lead to higher accuracy values

### Conclusions:
1. Variety of reasons can cause Observation-1, such as the quality of the data or the chosen architecture and hyperparameters of the deep learning models.
2. More complex architectures and the use of overfitting strategies help to improve the performance of the models.
3. Model architecture is a more critical factor than the number of parameters.
4. It is crucial to carefully preprocess the data to remove any irrelevant information and to ensure that the data is of high quality.
5. Regularization techniques, such as dropout and early stopping, can also be useful in preventing overfitting.
6. Choosing the right word embeddings can have a significant impact on the performance of the model.
7. Additionally, experimenting with different architectures and hyperparameters can help to improve the performance of the models.
