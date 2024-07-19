1. Start with a small set of **seed patterns** and **seed tuples**
	- e.g.  seed pattern: /* has a hub at */ 
	- seed tuple:  Ryanair - Charleroi
2. Search for the terms in the seed tuple, within a corpus of documents
3. Use the search results to extract new patterns
	- /[ORGANISATION], which uses [LOCATION] as a hub/
	- consider context before, between and after the 2 entities 
4. Search for additional tuples using the new patterns (to grow set of tuples)
![[Pasted image 20240210191938.png]]
