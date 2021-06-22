# Text_classification
![1_HgXA9v1EsqlrRDaC_iORhQ](https://user-images.githubusercontent.com/59575205/123011510-30782700-d3c9-11eb-9290-a002bd7c485c.png)

## Using a dataset of researches then build models to classify each research to its appropriate field 
> The main function of this project is text classification, It aims to predict each research with its abstract and title is it belong to computer science field (The field we interest in) or belongs to other fields.

# The trained models are:
- Naive Bayes classifier; as it is proven in different researches that Naive Bayes performs well in many text
classification problems.
- Logistic Regression
- Support Vector Machine

With each classifier I trained the data by using different features to see which one has strong impact on the classification process . 
**There are different ways of transforming text into feature vectors** and new features will be created using the existing dataset. I have applied Count Vectors, followed by Tf-Idf which includes Word Level TF-IDF, N-gram Level TF-IDF, Character Level TF-IDF. I have aimed to train  different models by using these methodologies and compare their performances
- Feature extracted from Count Vectorization: It is used to transform a given text into a vector on the
basis of the frequency (count) of each word that occurs in the entire text.
**HOW dose it work?** By using Count Vectorizer  provided by the scikit-learn library -which creates a
matrix in which each unique word is represented by a column of the matrix, and each text sample from
the dataset is a row in the matrix. The value of each cell is nothing but the count of the word in that
particular text sample. In our data, we have 30950 unique word in abstract! The following figures
shows the most frequent words:
![img1](https://user-images.githubusercontent.com/59575205/123011422-00308880-d3c9-11eb-9454-70b0abc4e4b2.png)

-  Feature extracted from TF-IDF: stands for “Term Frequency – Inverse Document” Frequency
which are the components of the resulting scores assigned to each word.
➢ Term Frequency: This summarizes how often a given word appears within a document.
➢ Inverse Document Frequency: This downscales words that appear a lot across documents.
F-IDF are word frequency scores that try to highlight words that are more interesting, e.g. frequent in
a specific abstract but not across abstracts.


**I did the classifications 3 times , one for abstract only , for title only and then combine the
two columns and classify based on them both to see which column has the most affect on classification
and gave a good results** The table below shows the results:

![Results](https://user-images.githubusercontent.com/59575205/123011309-cd869000-d3c8-11eb-8d8f-60f05b2f5e98.png)

**Finally,** ROC curve is a performance measurement for classification problem. It tells how much model is capable of distinguishing between classes. Higher the AUC, better the model is at predicting.
In this problem I compared the best two models by using ROC curve then I noticed the " Support Vector Classification using Abstract " is better because is Higher.
![ROC](https://user-images.githubusercontent.com/59575205/123011272-be9fdd80-d3c8-11eb-9b16-927015fc2404.png)
