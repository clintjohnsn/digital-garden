a.k.a. Word-Word matrices or Co-occurrence vectors
## Process
1. Requires a large volume of data
2. basic preprocessing steps: [[Tokenization]], [[Lemmatization]], etc
3. count number of times word **u** appears with word **v**
4. meaning of a word **u** is the vector of counts (named word vector)
	- **meaning**(u) = [count(u,v<sub>1</sub>),  count(u,v<sub>2</sub>), …]

We get,
- A matrix **X** <sub>n × m</sub> where n = |V| (target words) and m = |V<sub>c</sub> | (context words)
	- usually a square matrix
- context window of **±k** words (to the left & right)
### Pros
- compute similarities between words using cosine
- visualize words
- dimensions are meaningful, [[Explainable AI]]
#### Cons
- cannot capture semantics beyond words
- [[Distributional Semantics]] may not capture entire semantics
- vectors are sparse, high dimensional
	- use dimensionality reduction techniques  like [[Latent Semantic Analysis (LSA)]]

### Weighing scheme
[[Distance Discount]]