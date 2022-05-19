---
language: J
filename: learnj.ijs
contributors:
  - ["South", "https://github.com/4hg"]
---

```
NB. This is a comment, there are no group comments in J

NB. Some numeric types
1     NB. Integer
_1    NB. Negative integer
0.2   NB. Float, must never start with `.`
1e100 NB. Scientific notation
1j1   NB. Complex number
_     NB. Infinity
__    NB. Negative infinity
_.    NB. Indeterminate 

0 1   NB. Booleans are just integers

NB. Characters
'a'   NB. Characters are denoted with single quotes

NB. Making arrays
1 2 3       NB. Numbers separated by spaces turn into arrays
'abc'       NB. Strings are arrays of characters
'a'         NB. This is a single character
,'a'        NB. This is a string containing one character
1;'a';2     NB. Lists containing different datataypes are made with ;
noun define NB. Multiline string
Hello
world
)

NB. Some J terms:
NB. Verbs - infix functions, evaluate right to left
NB. Adverbs - infix higher order functions, evalate left to right *before* verbs
NB. Basic arithmetic verbs
   1+1
2
   1-2
_1
   3*3
9
   6%2
3

NB. Basic logical verbs

NB. There is no precedence for verbs other than grouping with ()
NB. Sentences are evaluated from right to left.
   10 * 2 + 5
70
   (10 * 2) + 5
25

NB. Operations are vectorized
   1 + 2 3 4
3 4 5
   1 2 3 + 4 5 6
5 7 9
   +: 1 2 3 NB. Monadic +: is double  
2 4 6
NB. A verb that takes up two characters will always end with : or .

NB. Verbs, or functions, come as monads or dyads, which refer to arity
NB. Monadic functions always accept the argument on the right
NB. Dyadic functions are always infix
   <. 10.23 NB. Monadic <. is floor
10
   20 <. 10 NB. Dyadic <. is min
10

NB. defining values
   a =: 1 2 3 NB. Global scope
   a
1 2 3
   a =. 4 5 6 NB. Local scope
   a
4 5 6
NB. Scope only matters in blocks (defined verbs, adverbs, etc)

NB. Making your own verbs and adverbs
NB. x,y: verb arguments
NB. u,v: adverb operands (can be verbs or nouns)
add =: {{ - x + y }} NB. The simplest method
add =: verb define   NB. Another way
 - x + y
)
add =: - +           NB. A tacit function (does not explicitly reference its arguments)


```

## Additional resources

- [Getting Started](https://code.jsoftware.com/wiki/Guides/Getting_Started#Documentation_-_Books) - Several J learning resources.
- [Online J Playground](https://jsoftware.github.io/j-playground/bin/html2/) - An online, interactive J REPL with samples and labs for learning
