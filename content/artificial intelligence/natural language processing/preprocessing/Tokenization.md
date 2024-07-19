**Find words - knowing when to split** → results in tokens.

> lemma is the base form of the token
### Challenges
- Punctuation marks and special symbols
	- where does punctuation go?
- Morphosyntactic words
	- contractions
		- *e.g. doesn't*
		- simple expanding may not work
			- *doesn't -> does not*
			- *Carla's home -> home of Carla OR Carla is home*
	- compound words
		- *e.g. rock-and-roll* 
- numbers
	- measurements *e.g. 5 miles*
- utf-8 characters
	- emojis
- errors
	- if source is from OCR, errors from OCR might propagate
- other languages
	- transliterations - (*e.g. Hindi written in English alphabets*)
	- non whitespace delimited (*e.g. Chinese/Japanese*)
	- right to left (*e.g. Arabic*)
- Formats/conventions of stuff may be different
	- telephone numbers, dates, decimals, monetary values, coordinates, etc.
- domain dependence
- named Entities?
	- [[Named Entity Recognition]] combines tokens
	- *e.g. San Francisco*

### Implementations
[[spaCy]]'s tokenization