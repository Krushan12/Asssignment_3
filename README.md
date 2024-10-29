﻿# Asssignment 3

 Q1. Refer to the notebook on generating names using next-character prediction and modify it for generating text using next-word prediction (You have to implement MLP based text generator. However, it is recommended to refer to Andrej Karpathy’s blog post on the Effectiveness of RNNs).
Visualize the embeddings using t-SNE if using more than 2 dimensions or using a scatter plot if using 2 dimensions and write your observations. Write a streamlit application that asks users for an input text, and it then predicts the next k words or lines. In the streamlit app, you should have controls for modifying context length, embedding dimension, activation function, random seed, etc. You can use any one of the datasets mentioned below.

## Hints:

    a. For text-based datasets, you can remove special characters except “full stop (.)” so that it can be used to split sentences. However, you cannot ignore special characters for other datasets like for C++ code. You will have to treat text between newlines as a statement. To remove special characters from a line, you can use the following code snippet:

        import re
        line = re.sub('[^a-zA-Z0-9 \.]', '', line)

        It will remove everything except alphanumeric characters, space and full-stop.

    b. Convert the text to lowercase and use unique words to create the vocabulary.
    c. To create X, and y pairs for training, you can use a similar approach used for next-character prediction.
    d. You may have to use a larger embedding size for words. (For example: 32 or 64)
    e.Use a similar model as used for next-character prediction. Here, you may have to increase the size of hidden layers. (For example, 1024).
    f.



