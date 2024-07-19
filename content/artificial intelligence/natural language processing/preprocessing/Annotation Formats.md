Documents are typically unstructured or have complicated structures - keeping **human readability** in mind. 

Annotations are mark-ups in the (converted raw text) document that enable **machine readability**. This can be for presentation, metadata and understanding content. 

### Types
- Boundary Notation Annotation
- inline markup language elements
- stand-off annotation
	- delimiter separated values (DSV)
	- JSON
### Boundary Notation Annotation
- done at level of individual tokens
- in the text itself
- for units of interest spanning multiple tokens/ [[Named Entity Recognition]], we can use **BIO**
	- BIO: **B** =begin, **I** = inside, **O** = outside
	- create a table of tokens with their annotations
	- every non entity is tagged **O**
	- every entity tagged with **B** (and optionally the type of entity) and when it spans multiple tokens, use **I**
	- *e.g. The British Prime Minister Tony Blair and ...* -> 
		- *The* -> O
		- *British* -> B-Person
		- *Prime* -> I-Person
		- *Minister* -> I-Person
		- *Tony* -> B-Person
		- *Blair* -> I-Person
		- *and* -> O
	- cannot handle hierarchical or structured annotations
		- nested entities, entity relations, events, etc.

> **event** is a type of entity relation that contain multiple entities participating in an event. *e.g. -> attendees in a **meeting** or attacker and defender in a **war**, etc.*

### Inline markup language elements
- addition of markup tags within text (in-text)
- HTML, XML
- can deal with hierarchical & structured annotations - nested entities, entity relations and events
	- relations can be done using some attributes in the tags and linking via IDs
- impossible to encode overlapping/intersecting annotations
	- *Iraqi city of Basra -> **Iraqi city** and **city of Basra***
- processing/parsing required to and from

### Stand-off annotations
- stored separately from text
- links annotations to text using indexing based on **character offsets**
- can be delimiter separated values (DSV) like CSV or JSON
	- *e.g. Tony Blair -> Person 144 154*
	- *e.g.*
			{ 
				"id" : "199",
				"ne_type": "Person"
				"begin" : "144"
				"end": "154"
				"surface_form" : "Tony Blair"
			} 
- can handle hierarchical, structured and overlapping annotations
- not readily human readable