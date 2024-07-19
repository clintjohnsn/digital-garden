Term Frequency - Inverse Document Frequency

Weighing scheme for  [[Term-Document matrices]]

- Term Frequency (TF) => **tf**(t,d) =  log (1 + **count**(t,d))
	- take base 10
	- **count**(t,d) → frequency of term **t** in document **d**
	- the addition of 1 is [[Laplace Smoothing]]
- Inverse Document Frequency (IDF) => **idf**(t) = log(N/**df**(t))
	- N → total number of documents , |**D**|
	- **df**(t) → number of documents in which **t** occurs
- **tf-idf**(t,d) = **tf** (t,d) x **idf**(t)