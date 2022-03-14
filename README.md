# PCKY_Parser

Building a probabilistic CKY (Cocke-Kasami-Younger) parser in Python! Almost finished, just need to...

- tweak some parts of the CNF development
- create function to backtrack through the CKY grid to obtain the most likely parse. 

The parser trains off parsed sentences in the NLTK Treebank corpus, and uses this to develop a lexicon and a Chomsky Normal Form grammar of rules with probabilities. It then uses the CKY algorithm to move through the subtrees of an input sentence and determine which grammar rules apply to each one.

Since the speed of the parser grows (a lot!) with the size of the grammar, my next goal is to optimize the parser so it can train on more data and develop a large grammar, while also having a reasonable runtime.

Getting Started:
1) The first three code blocks train the parser from a (currently limited) dev dataset, convert the grammar to CNF, and then make the CKY grid. Right now it's set to make a grid for the sample sentence "Pierre will join the board" at the top of the block
2) The fourth code block executes the CKY algorithm, and currently produces the full grid of possible POS tags in each cell
3) The fifth code block is where I'm working out some bugs with the CNF conversion, not much to see here
