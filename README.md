# Part Of Speech (POS) tag annotation manual

This document explains the POS tag set to use.
We are going to use PennTag, which is a specified tagset for English.

## POS tagging Scheme
Here, each tag is described and examples of each are also given.
- Penn Tagset is a language specific POS tag set for English You can find the whole manual if you got confused [PennTag POS tagging guideline](https://catalog.ldc.upenn.edu/docs/LDC99T42/tagguid1.pdf).

****Note that the following `this style` is used for examples.**
<br><span style="color:red">** Update [12/3/2019]: The function word 'to' have two tags, TO and IN. When it is used as infinitival to as in "want `to`," "decided `to`," and "going `to`,"" they are tagged as TO. When it is used in contexts such as "go `to` the park", we consider it as IN (because it functions to specify the direction in which the event happens).</span>


| Penn Tagset | Description                              | Example                                 |Notes|
|:-----------:|------------------------------------------|-----------------------------------------|-----|
|      CC     | coordinating conjunction                 | `and`         , `but`, `yet`        ||
|      CD     | cardinal number                          | `1`, `third`                                ||
|      DT     | determiner                               | `the`, `a(n)`, `no`, `every`, `another`, `any`, `that`, `these` |`both` and `all` are DT when they occupy the determiner position as in `all roads` or `both times` (see PDT). |
|      EX     | existential there                        | `there` is                                ||
|      FW     | foreign word                             | `d'hoevre`                                ||
|      IN     | preposition                              | `in`, `of`, `like`                        |Include `to` when they are in go `to` or come `to`|
|      IN     | subordinating conjunction                | `although`, `when` ||
|      JJ     | adjective                                | `green`                                   ||
|     JJR     | adjective, comparative                   | `greener`                                 ||
|     JJS     | adjective, superlative                   | `greenest`                                ||
|      LS     | list marker                              | `1)`  `a)` `B)`                           ||
|      MD     | modal                                    | `could`, `will`, `may`, `would`, `shall`, etc.  ||
|      NN     | noun, singular or mass                   | `table`                                   ||
|     NNS     | noun plural                              | `tables`                                  ||
|     NNP     | proper noun, singular                    | `John`, `CNN`,                              |Includes Acronyms (`CNN`, `BBC`, `NATO`, etc.)|
|     NNPS    | proper noun, plural                      | `Vikings`                                 |Includes Acronyms (`CNN`, `BBC`, `NATO`, etc.)|
|     PDT     | predeterminer  (i.e., determiner-like elements that precede an article or possessive pronouns)                        | `both` the boys , `all` his marbles, `both` the girls, `half` the time, `such` a good time, `quite` a mess, `rather` a nuisance  |**See DT carefully**|
|     POS     | possessive ending                        | friend`'s ` , John`'s`, the parents`'`  ||
|     PRP     | personal pronoun (includes reflexive)    | `I`, `he`, `it`, `mine`, `yours`   ||
|     PRP$    | possessive pronoun                       | `my`, `his`                                 ||
|      RB     | adverb (typically end with `-ly`, but also includes degree words)  | `however`, `usually`, `naturally`, `here`, `well`, `very`, `too` ||
|     RBR     | adverb, comparative                      | `better`                                  ||
|     RBS     | adverb, superlative                      | `best`  ||
|      RP     | particle                                 | give `up`  ||
|     SYM     | Symbols (Mathematical or scientific)     | `π`, `˚C`                                   ||
|      TO     | to  (Infinitival)                        | `to` go, `to` him, going `to` see   |`to` as in go `to` is IN, not TO |
|      UH     | interjection                             | `uhhuhhuhh`                               ||
|      VB     | verb, base form   (subsumes imperatives, nfinitives, subjunctives)  | `take`                                    ||
|     VBD     | verb, past tense                         | `took`                                    |"D" represents "-ed"|
|     VBG     | verb, gerund/present participle          | `taking`                                  |"G" represents "-ing"|
|     VBN     | verb, past participle                    | `taken`                                   |"N" represents "-en"|
|     VBP     | verb, present, non-3rd person sing.      | You `take`, They `take`, I `take`etc.     |"P" represents "Present tense" |
|     VBZ     | verb, present, 3rd person sing.          | `takes`                                   |"Z" represents the morpheme "-z" in 3 person singular "s"|
|     WDT     | wh-determiner                            | `which`                                   ||
|      WP     | wh-pronoun                               | `who`, `what`, `whom`                ||
|     WP$     | possessive wh-pronoun                    | `whose`                                   ||
|     WRB     | wh-abverb                                | `where`, `when`, `how` |`when` in a temporal sense is tagged as *WRB*, When it is used to mean "if", they are *IN*|

- Punctuations can be copied as it is.


## Some problematic cases (We are trying updating this to reflect your questions).
The following section will outline some frequent problematic cases. This is NOT exhaustive, and if you think your questions is not answered, refer to the following manual [PennTag POS tagging guideline](https://catalog.ldc.upenn.edu/docs/LDC99T42/tagguid1.pdf).


### Both, either, all, etc. (CC, DT, or PDT?)
If both, either is directly modifying a noun, they are determiner (DT).
- Both (DT) boys
- All (DT) girls
- The boys all (DT) left for school.

If they precede an article or possessive pronouns, they are predeterminer (PDT).
- Both (PDT) the boys
- All (PDT) the girls

If both or either are used with coordinating conjunctions, they are CC.
- Both (CC) X and Y.
- Either (CC) A or B
?? Both of the two.

### Numbers
It is CD in most cases.



### "one" (CD or NN?)
>Sometimes it is unclear whether one is cardinal number or a noun. In general, it should be tagged as a cardinal number (CD) even when it is not clearly that of a numeral


- one (CD) of the reasons
- the only one (NN) of its kind.

### Adverb (RB)or Particle (RP)
(For more details see the [PennTag POS tagging guideline](https://catalog.ldc.upenn.edu/docs/LDC99T42/tagguid1.pdf) on page 21).
You can insert manner adverbs (e.g., calmly) when they are adverbs.
- to sit calmly `by` (RB)
- \*to give calmly `up` (RP)

### "to" (TO or IN?)
The function word 'to' have two tags, TO and IN.
It is TO when it is used as infinitival to as in "want `to`," "decided `to`," and "going `to`".
It is IN when it is used in contexts such as "go `to` the park" (because it functions to specify the direction in which the event happens).

### What is "nandaro"?
There are some Japanese words inserted in the sentences. We have deleted as many of these instances as possible, but the automatic detection failed in some cases... If you think you don't know the word, it may be the case that it is a Japanese word (Hence FW tag). If you are unsure about your decision, you can email Masaki (L1 speaker of Japanese) to see if they are FW.
