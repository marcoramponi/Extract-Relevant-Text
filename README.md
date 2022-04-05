# Extract Relevant Text
This code can be used to implement a text search algorithm.

Specifically, given an input text, it returns a summary of the most relevant paragraph from a given list of paragraphs.

The logic essentially consists of two components:

### 1. Topic Extractor
I split the data (list of paragraphs) into a predefined number of topics via a non-negative matrix factorization algorithm.
Given an input text, the most 'relevant' topic is then extracted by computing a cosine similarity function.

### 2. Summarization
This is done via a Hugging Face Transformers pipeline object set for summarization task.

### Dataset
In order to test this algorithm I prepared a dataset containing a list of paragraphs from F. Nietzsche.
The preprocessing is aimed at extracting and grouping text by paragraphs.
I also perform some exploratory data analysis along the way.

The original dataset 'nietzsche.txt' is publicly availabe on Kaggle:

https://www.kaggle.com/datasets/christopherlemke/philosophical-texts
