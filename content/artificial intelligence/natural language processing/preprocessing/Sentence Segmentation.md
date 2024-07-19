Find **EOS** (End of sentence) -boundaries between sentences

### Challenges
- Variation in delimiters
	- . ? ! ; , - :
- Domain dependence
- abbreviations
## Approaches
- **Symbolic**
	- Regular Expressions
		- patterns
	- Dictionaries
		- e.g. abbreviation lists and rules for each kind of abbreviations
	- manual rule coding
		- if then else
		- e.g. first character after potential EOS char should be uppercase 
		- e.g. titles not likely to occur at EOS (e.g., Dr. Jones)
		- 
- **Statistical & ML approaches**
	- [[OpenNLP]]’s Sentence detection
	- [[spaCy]]'s **Statistical Sentence Segmenter** and a Rule-based component (**Sentencizer**)