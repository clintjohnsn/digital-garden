Benchmark algorithm for [[Word-Sense Disambiguation]]

Choose the sense whose dictionary gloss or definition shares the most words with the target word’s neighborhood

- Target word: **w** 
- Context words of w: wj 
- Lexicon definition of senses: **D**() 
- Set of senses of a word: **S**()

![[Pasted image 20240523190846.png]]


##### Pros: 
- No training data needed

##### Cons: 
- not all words have definitions in WordNet
- need to deal with ambiguous context words
- poor performance.
