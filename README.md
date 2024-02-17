# NLP

A common task in natural language processing is parsing, the process of determining the structure of a sentence. This is useful for a number of reasons: knowing the structure of a sentence can help a computer to better understand the meaning of the sentence, and it can also help the computer extract information out of a sentence. In particular, it’s often useful to extract noun phrases out of a sentence to get an understanding for what the sentence is about.
In this project, we’ll use the context-free grammar formalism to parse English sentences to determine their structure. In a context-free grammar, we repeatedly apply rewriting rules to transform symbols into other symbols. The objective is to start with a nonterminal symbol S (representing a sentence) and repeatedly apply context-free grammar rules until we generate a complete sentence of terminal symbols (i.e., words). The rule S -> N V, for example, means that the S symbol can be rewritten as N V (a noun followed by a verb).

First, look at the text files in the sentences directory. Each file contains an English sentence. The goal in this problem is to write a parser that is able to parse all of these sentences.

Take a look now at parser.py, and notice the context free grammar rules defined at the top of the file.Notice that Adj is a nonterminal symbol that generates adjectives, Adv generates adverbs, Conj generates conjunctions, Det generates determiners, N generates nouns (spread across multiple lines for readability), P generates prepositions, and V generates verbs.

Next, take a look at the main function. It first accepts a sentence as input, either from a file or via user input. The sentence is preprocessed (via the preprocess function) and then parsed according to the context-free grammar defined by the file. The resulting trees are printed out, and all of the “noun phrase chunks” (defined in the Specification) are printed as well (via the np_chunk function).
