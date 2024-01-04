# Text Summarization 
* Abstractive Methods: generation of new text, generally using some text generation approach. Nowadays sequence to sequence models
* Extractive Methods: identify the most relevant sentences in a document and present them in document order
  - Can be done by training a classifier to predict a label in-summary/not-in-summary
  - Can be done by training a scoring function
* Scoring sentences can be done by computing a series of “relevance” features and use them to produce an score
* Scores are used to select top-scoring sentences for the summary upto a compression rate
* We will use a neural network to “learn” how to score sentence based on a number of features
* The network will be a logistic regression neural network or a variation
* Dr Inventor Dataset
  - Scientific Documents in the Computer Graphics area
  - Annotated at several levels including summarization
* We need to normalize the text: tokenize, remove unnecessary information, normalize, etc.
* We need to define features computed for each sentence
* Word Embedding Features
* Transform each sentence into a vector of word embeddings by averaging the embeddings of each word => this will give you 50 features
* Transform the TITLE of the document into a vector of word embedding
* Transform the ABSTRACT of the document into a vector of word embedding by averaging the vectors of the sentences in the abstract
