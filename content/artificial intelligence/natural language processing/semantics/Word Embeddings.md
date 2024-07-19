
embed semantic meanings of words using vectors - vector representations of words
### Why?
- compute semantic similarity between text
- document retrieval
- apply machine learning on text  - clustering, classification, prediction, etc

> Why can’t we just one-hot encode the vocabulary to create word embeddings?
> Because words are related to each other, and all of the above tasks benefit from modelling the similarity of words.  
## Count-based approaches

1. [[Term-Term matrices]]
2. [[Term-Document matrices]]

#### Weighing Schemes
Not all contextual words are equally important. Commonly, infrequent words are more important than frequent ones, correlated words are more important than uncorrelated words, and so on

1. [[TF-IDF]] for [[Term-Document matrices]]
2. [[Distance Discount]] for [[Term-Term matrices]]

#### Smoothing
Many word pairs should have > 0 counts, but their corresponding matrix entries are 0s because of **data sparsity** (unseen events)

[[Laplace Smoothing]]: Adding 1 to every count (pseudocount)
## Prediction based approaches
- Typically use a [[Neural Network]] model
- compute the probability Pr(**w**|u1 , u2 , ... ) of the event that a target word **w** appears in a context (u1 , u2 , .. ).

- dense vectors (25-1000 dim)
- distributed representations of words
- easily incorporate a new sentence/ document or add a word to the vocabulary.

1.  Language Modelling (Bengio et al., 2003)
	-  predict a next word from m-1 previous words
	-  Each contextual word wj is represented a column of matrix C
	-  1 hidden layer
2.  [[Word2Vec]] 

### Pros
- dense vectors, robust performance

### Cons
- Word embeddings are learned from data → they also capture biases implicitly appearing in the data
	- ethnic and gender biases
- Dealing with unknown words
	- use a special UNK token
	- use characters/ sub-words instead of words
- semantic ambiguity - based on context and knowledge
	- [[Word-Sense Disambiguation]]
	- Deep learning methods like [[ELMO]] and [[BERT]]
- dimensions are not easy to interpret
- **polysemy**: All occurrences of a word (and all its senses) are represented by one vector
	- use different vectors for different senses
- Antonyms appear in similar contexts, hard to distinguish them from synonyms
- get context for long sequences of words
	- average or add vectors → but this is not scalable 


## Evaluation
- **Intrinsic**: 
	- **similarity**: order word pairs according to their semantic similarity 
	- **in-context similarity**: substitute a word in a sentence without changing its meaning.
	- **analogy**: Athens is to Greece what Rome is to ...?
- **Extrinsic**: use them to improve performance in a task, i.e. instead of bag of words → bag of word vectors 