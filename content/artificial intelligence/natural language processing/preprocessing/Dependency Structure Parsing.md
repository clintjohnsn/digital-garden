used for [[Syntactic Parsing]] and [[Relation Extraction]]
## Dependency Parsing
 
  **Dependency** -  an asymmetric binary relation linking two lexical items (tokens): one is the head and the other is the dependent.
- The [[head]] of a sentence (a.k.a. the root) is the main verb of the sentence; subject and object become it’s **dependents**.
- if a token is modifying/specifying/describing another token
	- the modifying token → dependent
	-  the modified token → head
- **Dependency structure/graph**
	- look for dependencies between each pair of tokens
	- identify the modifier and modified token
	- a link from head to token specifying the grammatical function
	- **Grammatical functions/dependency relation types**
		- [[Universal dependency relations]]
	- this forms a directed graph **G** (V = tokens ,E = grammatical functions) with a linear precedence order on V
	- Example (Horizontally arranged) -
	  ![[Pasted image 20240208213019.png]]
	- Example (Tree of tokens)
	  ![[Pasted image 20240208214420.png]]
	- Example (Tree of POS)
	  ![[Pasted image 20240208214509.png]]
	- Example (Machine Readable, using indentation)
	    ![[Pasted image 20240208214754.png]]
	- Example (Machine Readable, [[spaCy]])
	  ![[Pasted image 20240208215150.png]]

### Alternate dependency structure parsing methods

An alternative dependency structure parsing method is via [[Predicate-Argument Structures (PAS)]] e.g.  [[Enju Parser]]

> whether the arguments are required depends on the token (verb). See [[Endocentric and exocentric constructions]] 


