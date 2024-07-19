Weighing scheme for [[Term-Term matrices]]

- Weight contexts according to the distance from the word → further away, lower the weight
- For a window size **±k**, multiply the context word’s frequency at each position by (**k**−distance)/**k**
	- distance of word w<sub>j</sub> from w<sub>t</sub> = t - j -1 
- 
