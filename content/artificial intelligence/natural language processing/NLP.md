a.k.a **Natural Language Processing**
### Challenges
- natural languages evolve - new words, new meanings, etc
- syntactic rules are flexible
- ambiguity is inherent
- world knowledge is often necessary for  interpretation
- different languages, dialects and styles

### Types of ambiguity in interpretations
- **Phonological**
	- how words sound
	- e.g. I will be *writing/riding* this weekend
- **Lexical**
	- multiple senses of words
	- e.g. I am going to the *bank* (financial entity/river)
- **Syntactic**
	- positions of words
	- words can be noun or verb
		- e.g. I saw her *duck* (animal/crouching)
	- to what the prepositional phrase is attached 
		- e.g. I saw the man on the hill *with the telescope* (Who has the telescope? the man or me? )
- **Semantic**
	- interpretation requires knowledge of the world
	- e.g. The children ate the cookies because they were very hungry (were the cookies hungry or the children?)
## Approaches
- **Symbolic**
	- Rules and dictionary based
	- capture linguistic knowledge written by experts
	- results can be interpreted easily
	- manual effort to make rules
- **Statistical/[[Machine Learning]]** Based
	- data driven, learn or discover patterns
	- supervised/unsupervised ML
	- generalizable, easy domain adaptation (might still need to retrain)
	- manual effort to retrain and label data
	- interpretation - [[Explainable AI]]
- **Hybrid**
	- best (or worst?) of both worlds

## NLP Pipeline
pipeline of components - which tackle some problem - can use any of (symbolic/statistical) approaches.

Sample pipeline- 

![[Pasted image 20240215160143.png]]
## Components

### Preprocessing
- [[Sentence Segmentation]]
- [[Tokenization]] ,  [[Lemmatization]],  [[N-grams]] 
- lowercasing, remove infrequent words, stop words, punctuations or numbers depending on domain & use-case
- [[Named Entity Recognition]]
- [[Annotation Formats]]
- [[POS Tagging]]

### Tasks 
- [[Topic Modelling]]
- [[Sentiment Analysis]]
- [[Relation Extraction]]
- [[Information Extraction]]
- [[Distributional Semantics]]

## Evaluation

> see [[Evaluation of Software Systems]]

- Most NLP tasks are some **classification** problem. We use the [[Gold Standard Data]] to evaluate.
- [[Gold Standard Data]] may be annotated differently by different annotators. We use [[Inter Annotator Agreement (IAA)]] methods to determine the quality of the data.
- We use the same **performance evaluation** techniques used in in supervised classification ML problems

> see [[Evaluation of ML systems#Metrics for Classification]]

#### Testability in  Diagnostic evaluation
For an NLP-based system, design and coverage of diagnostic test suites is hard because the range of phenomena (sentence structures) the system is expected to tackle is hard to anticipate. Test suites using [[Gold Standard Data]] may emphasise idealised linguistic aspect and such tests may be of reduced use in the face of ungrammatical (real) text.
