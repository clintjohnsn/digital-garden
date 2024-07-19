a.k.a. [[Bag-of-words]]

If word **u** appears in document **d**, **d** is a context of **u**

## Process
1. Acquire large volume of documents
2. count number of times a word **u** appears in a document **d**
3. meaning of a word **u** is the (row-wise) count vector of documents that the word **u** appears in
	- meaning(**u**) = [count(u,d<sub>1</sub>), count(u,d<sub>2</sub>), … ] 
	- vector dimension =  |**D**| → **D** documents
4. meaning of a document **d** is the (column-wise) count vector of words in the document
	- meaning(**d**) = [count(u<sub>1</sub>,d), count(u<sub>2</sub>,d), … ] 
	- vector dimension = |**V**| → **V** is the vocabulary

We get,
A matrix **X**, |**D**| × |**V**| or  |**V**| × |**D**|  
### Pros
- find similar documents
- find documents close to a query (by considering query as a document)
- compare and visualize words
- dimensions are meaningful,[[Explainable AI]]

### Cons
- vectors are sparse, high dimensional → |**V**| and |**D**| are both large
	- use dimensionality reduction techniques like [[Latent Semantic Analysis (LSA)]]
- [[Distributional Semantics]] may not capture entire semantics

### Weighing scheme
[[TF-IDF]]