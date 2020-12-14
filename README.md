# Sarcasm detection using BERT

This project uses NLP techniques to classify if tweets are sarcastic or not. BERT is used to train the model and arrive at the predictions.

### How to run the code

1.  The executable code resides in the file *Sentiment_Analysis_with_BERT.ipynb*. This code needs to be directly executed from Google Colab. Click on the button below to open the file in Colab.  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/dilipis/CourseProject/blob/main/Sentiment_Analysis_with_BERT.ipynb)

2.  Once in Colab, the code needs to run on a GPU. From Colab, navigate to **Edit> Notebook Settings**. Select **GPU** from the *Hardware accelerator* dropdown

3.  The notebook can be executed by executing all the code blocks in order by clicking on the black 'Play' button at the top of each block.

4.  In the end, all the predictions are stored in *answer.txt* in the *output* folder in the workspace.

A video tutorial is available [HERE](https://mediaspace.illinois.edu/media/t/1_fvrgixpx)

### How the code works

This project uses BERT (Bidirectional Encoder Representations from Transformers) which is a state-of-the-art machine learning model used for NLP tasks. BERT is a pre-trained NLP model which can be further trained to solve several text classification problems. BERT makes use of Transformer, an attention mechanism that learns contextual relations between words (or sub-words) in a text. 

The HuggingFace Transformers library is used to get the BERT model that works with Tensorflow.


This is how the code works at the high level

 1. Copy the testing and training data from github to the Colab workspace
 2. Read the testing and training data from jsonl file and convert them into a csv file
3. Clean the input data by removing URL and USER tags from the tweets
4. Split the training dataset into training and validation. This will be used to train the model.
5.  Extract only the required columns for further processing. 
6.   Create the BERT model and tokenizer
7.  Convert the training and validation data into the BERT format using the helper functions defined above
8.  Use model.compile to set the optimizer, loss function that BERT will use to train the model
9.  Call model.fit to actually train the model based on the training and validation data
10. Make predictions on the test data based on the trained model. 
11. Write the resuts to *answer.txt* in the *output* folder in the workspace.

### Dependencies

 -   python
-    tensorflow
- transformers
- pandas
-   sklearn
-   os
- urllib
-   jsonlines
- csv



### References
1. [Sentiment Analysis in 10 Minutes with BERT and TensorFlow](https://towardsdatascience.com/sentiment-analysis-in-10-minutes-with-bert-and-hugging-face-294e8a04b671) by **Orhan G. Yalçın**
2. [FigLang2020-Sarcasm-detection Github](https://github.com/BshoterJ/FigLang2020-Sarcasm-detection/blob/master/run_bert.py)
