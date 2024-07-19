- predicting the context given a word  **w<sub>t</sub>

- Let wt-1,...,wt-m, wt+1,...,wt+m be the context
- Pr(w<sub>t</sub> | context) * Pr (context) = Pr(context | w<sub>t</sub>) * Pr(w<sub>t</sub>)
- Pr(context) and Pr(w<sub>t</sub>) are uniform distributions and are constants
- Pr(context | w<sub>t</sub>) = Product { Pr(w<sub>j</sub> | w<sub>t</sub>) } for all js

[[Word2Vec]] is a skip-gram model
