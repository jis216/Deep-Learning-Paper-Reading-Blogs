<a href="https://www.codecogs.com/eqnedit.php?latex=\sum_{<x_1...x_n>&space;\in&space;V^&plus;&space;}p(x_1,&space;x_2,&space;...&space;x_n)&space;=&space;1" target="_blank">

# Notes on Language Modeling
**Related Resources:**
Michael Collins: [Course Notes for COMS w4705: Language Modeling](http://www.cs.columbia.edu/~mcollins/courses/nlp2011/notes/lm.pdf)

**Keywords and Notation:**
- corpus: set of sentences in some language
- 

## What is Language Modeling?
A language model is defined as follows. First, assume that we have a vocabulary V, which is the set of all words in the language. A *sentence* in the language is a sequence of words *x<sub>1</sub>, x<sub>2</sub>, ... x<sub>n</sub>*, where  *x<sub>n</sub> &isin; V*, and we assume that x<sub>n</sub> is a special symbol, STOP.

Given this corpus, we could estimate the parameters of a language model. And we assume that x<sub>n</sub> is a special symbol STOP. We'll define V<sup>+</sup>  to be the set of all sentences with the vocabulary V: this is an infinite set.

**Definition of Language Model**: A language model consists of a finite set V, and a function *p(x<sub>1</sub>, x<sub>2</sub>, ... x<sub>n</sub>)* such that:

1. For any 
<img src="https://latex.codecogs.com/gif.latex?<x_1...x_n>&space;\in&space;V^&plus;,&space;p(x_1,&space;x_2,&space;...&space;x_n)&space;\geq&space;0" title="<x_1...x_n> \in V^+, p(x_1, x_2, ... x_n) \geq 0" /></a>

2. *In addition,*

<img src="https://latex.codecogs.com/gif.latex?\sum_{<x_1...x_n>&space;\in&space;V^&plus;&space;}p(x_1,&space;x_2,&space;...&space;x_n)&space;=&space;1" title="\sum_{<x_1...x_n> \in V^+ }p(x_1, x_2, ... x_n) = 1" /></a>

*Hence p(x_1, x_2, ... x_n) is a probability distribution over the sentences in V<sup>+</sup>*

As one example of a (very bad) method for learning a language model from a training corpus, consider the following. 

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTY5NzQ2OTYyNV19
-->