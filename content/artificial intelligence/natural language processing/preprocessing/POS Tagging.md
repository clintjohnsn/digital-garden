identify and assign **part of speech** tags to **tokens** - classify words according to their meaning and role in grammar. e.g. - nouns, pronouns, verbs, adjectives, adverbs, determiners,  conjunctions, prepositions, etc.

[[Tokenization]] is usually performed before or alongside this step. Only one POS tag for a token in each run.

### Tagsets
- [[Penn Treebank tagset]] 
- [[Universal Scheme tagset]]


### Challenges
**Syntactic ambiguity**
- accidental homophones and homonyms 
	- e.g. duck
> homophones & homonyms are words that are pronounced or spelled the same but have different meanings 
- different syntactic roles
	- e.g. To *walk* (verb) vs to go for a *walk*(noun)
	- e.g. *old*(adjective) people vs the *old*(noun)
	- To **disambiguate**:
		- ambiguity usually disappears when token is not in isolation
			- e.g. The garbage *can* (axillary verb) smell vs The garbage *can* (noun) smells
			- might not work - e.g. They *can* fish (can - auxiliary verb/verb) and canning - (verb/noun)
		- come up with rules
			- e.g. A token is very unlikely to be a verb if its preceding word is a determiner
				- I want a *go*
			- e.g. A token is unlikely to be a noun if the immediately preceding word is to
				- I want to *go*
			- A token is more likely to be a possessive pronoun when followed by a common noun
				- He stroked *her* (possessive pronoun) cat 
				- He gave *her* money (personal pronoun) 
					- The rule does not work here
					- look at **sentence structure** in such cases (direct and indirect objects
- to what the **prepositional phrase** is attached or **sentence structure**
	- use [[Syntactic Parsing ]] 
	
### Approaches
- Rule based
- statistical
	- model trained on a POS corpus
		- corpus has each token is labelled with correct POS tag
		- formats
			- each line a token-POS tag pair
			- each sentence has POS tag appended to each token
		- Corpora
			- e.g. [[Penn Treebank corpus]]
			- e.g. [[GENIA corpus]]
