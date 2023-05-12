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
**Results**:
![image](https://github.com/keertibajaj/UMKC_NLP_SP2023/assets/45763954/6cd3ff39-112b-4e51-a888-fc7acc27eeca) </br>

## Part 2: Comparison of Own Word2Vec model with pre-trained Word2Vec and GloVe Embedding:
Models used:
1. Own Word2Vec Model - This model is trained on the IMDB movie reviews dataset.
2. Pre-trained Word2Vec Model - This model is the Google News word2vec model.
3. GloVe Embedding - This model is the GloVe 840B word2vec model.
### A. Semantic distance calculation and Visualization:
Semantic distance is a measure of how similar two words are in meaning. There are many different ways to calculate semantic distance, but one common approach is to use the cosine similarity of their word embeddings. Word embeddings are typically learned from a large corpus of text using a neural network. To calculate the cosine similarity of two word embeddings, we first need to compute the dot product of their vectors. The dot product is a measure of how similar two vectors are in direction. The cosine similarity is then calculated as the dot product of the two vectors divided by the product of their lengths. Once we have calculated the semantic distance between two words, we can visualize it using a scatter plot and heatmap. In a scatter plot, each word is represented by a point, and the distance between two points is proportional to the semantic distance between the two words.
</br>
- _Word used to evaluate_: ["cat", "dog", "car", "bus", "happy", "joy", "sad", "depressed", "love", "hate", "book", "paper", "computer", "software", "food", "drink"]
- t-SNE is used to reduce dimensionality of embeddings to get 2 dimensional scatter plot
</br>

**Cosine Similarity Values of Words using Own Word2Vec Model**:</br>
![download](https://github.com/keertibajaj/UMKC_NLP_SP2023/assets/45763954/95ca0f64-3803-445c-8201-3847c7f90090) </br>
**Cosine Similarity Values of Words using Google Pre-trained Word2Vec Model**:</br>
![download](https://github.com/keertibajaj/UMKC_NLP_SP2023/assets/45763954/f5e00ece-b9e8-4d44-888a-61bc3cddc527) </br>
**Cosine Similarity Values of Words using GloVe Embeddings**:</br>
![download](https://github.com/keertibajaj/UMKC_NLP_SP2023/assets/45763954/c57f915b-e1fa-4f89-99dc-a8984a34166d) </br>

**Scatter Plot of Words using Own Word2Vec Model**:</br>
![download](https://github.com/keertibajaj/UMKC_NLP_SP2023/assets/45763954/b1c15bd7-9fe2-40a4-901f-4f53790ab025) </br>
**Scatter Plot of Words using Google Pre-trained Word2Vec Model**:</br>
![download](https://github.com/keertibajaj/UMKC_NLP_SP2023/assets/45763954/45523f0b-c3e5-4e34-9247-fca1bd165cf3)
**Scatter Plot of Words using GloVe Embeddings**:</br>
![download](https://github.com/keertibajaj/UMKC_NLP_SP2023/assets/45763954/b075c06f-853f-4e38-a83a-a6f9eaf14ba9)

### B. A Classification Task using deep Learning Model:
First each of the three word embedding models are trained on the IMDB movie reviews dataset. Then each of the trained word embedding models are used to train a deep learning model for a binary classification task. The deep learning model is a simple long short-term memory networks (LSTM). The performance of each model is evaluated on the IMDB movie reviews dataset. </br>

**Results are as follows** (Accuracy Values):</br>
- Own Word2Vec embedding model - 79.084%
- Google News word2vec model - 79.248%
- GloVe 6B.300d word2vec model - 81.812%

## Part 3: Comparing the Performance of GloVe Embedding and BERT Embedding at the Sentence Level:
In this project, the performance of two popular embedding methods, GloVe and BERT, was compared at the sentence level using a simple neural network and logistic regression. A pre-trained GloVe (6B, 300d) embedding and the BERT embedding provided by the `transformers` library were used. Large Movie Review Dataset is used for this evaluation. For each sentence in the dataset, a fixed-length embedding vector was generated using each method and used as features in the classification models. The data was split into a training set and a test set, with a 80:20 split ratio. </br>

Two classification models were trained for each embedding method, a simple neural network and a logistic regression model. The scikit-learn library was used to implement these models with default hyperparameters. </br>

**Results**: </br>
![image](https://github.com/keertibajaj/UMKC_NLP_SP2023/assets/45763954/8c8ff884-2eb9-466e-8edf-9bcc93a28814) </br>
NN - Neural Network </br>
LR - Logistic Regrssion </br>

The results of the experiments showed that the BERT embedding outperformed the GloVe embedding on all the metrics. The neural network and logistic regression models both achieved higher accuracy, F1-score, and AUC-ROC with the BERT embeddings compared to the GloVe embeddings. The EER (Equal Error Rate) was lower for the BERT embeddings, indicating that this embedding method can better distinguish between positive and negative reviews.

### Conclusions:
1. The Word2Vec model is an effective way to learn vector representations of words that can be used for various natural language processing tasks.
2. Comparing the different word embedding models, the GloVe embedding performed better in terms of semantic similarity calculation, while the own Word2Vec model and the pre-trained Google Word2Vec model performed better in the binary classification task.
3. The semantic similarity calculation and visualization using scatter plots and heatmaps provide an effective way to understand the relationship between words and their similarities.
4. In task 2, the deep learning models trained on the word embeddings achieved high accuracy in the binary classification task, with the best performance achieved using the GloVe Embedding model.
8. In Task 3, the results suggest that the BERT embedding is more effective than the GloVe embedding for sentence-level classification tasks such as sentiment analysis.
9. It is important to note that these results are specific to the movie review dataset and may not generalize to other domains or tasks.
10. Additionally, there are many factors that can influence the performance of these embedding methods, such as the size and quality of the training corpus, the hyperparameters of the model, and the choice of downstream task.
