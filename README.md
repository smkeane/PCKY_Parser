# PCKY_Parser

Building a probabilistic CKY (Cocke-Kasami-Younger) parser in Python! Almost finished, just need to...

- tweak some parts of the CNF development
- create function to backtrack through the CKY grid to obtain the most likely parse. 

The parser trains off parsed sentences in the NLTK Treebank corpus, and uses this to develop a lexicon and a context free grammar of rules with probabilities. It then uses the CKY algorithm to move through the subtrees of an input sentence and determine which grammar rules apply to each one.

Since the speed of the parser grows (a lot!) with the size of the grammar, my next goal is to optimize the parser so it can train on more data and develop a large grammar, while also having a reasonable runtime.
