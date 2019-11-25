# Part Of Speech (POS) tag annotation manual

This document explains the POS tag set to use.
There are two types of POS tags we are going to use: 1) PennTag and 2) Universal Part of Speech (UPOS). The first one, PennTag is a more specified tagset for English while UPOS is general.

In most cases, PennTag can be automatically converted to UPOS, but there are certain cases where we need to tag unique UPOS. In this document, we will cover what we would like you to know before starting POS tag annotation.


## POS tagging Scheme
Here, each tag is described and examples of each are also given.
Note will detail some specific issues on tagging.
- Penn Tagset is a language specific POS tag set for English You can find the whole manual if you got confused [PennTag POS tagging guideline](https://catalog.ldc.upenn.edu/docs/LDC99T42/tagguid1.pdf).
- UPOS stands for Universal POS tag, which lists major lexical categories [Universal POS tags](https://universaldependencies.org/u/pos/).

****Note that the following `this style` is used for examples.**

| Penn Tagset |     UPOS    | Description                              | Example                                 |Notes|
|:-----------:|:-----------:|------------------------------------------|-----------------------------------------|-----|
|      CC     |    CCONJ    | coordinating conjunction                 | `and`         , `but`, `yet`        ||
|      CD     |     NUM     | cardinal number                          | `1`, `third`                                |Numbers should be treated as Adj (JJ) when they have the same distribution as JJ. e.g., a 50-3 victory |
|      DT     |     DET     | determiner                               | `the`, `a(n)`, `no`, `every`, `another`, `any`, `that`, `these` |`both` and `all` are DT when they occupy the determiner position as in `all roads` or `both times` (see PDT). |
|      EX     |     PRON    | existential there                        | `there` is                                ||
|      FW     |      X      | foreign word                             | `d'hoevre`                                ||
|             |      X      | additional word in multi-word expression | ??                                      ||
|      IN     |     ADP     | preposition                              | `in`, `of`, `like`                            |IN can be categorized as either ADP or SCONJ in UPOS.|
|      IN     |    SCONJ    | subordinating conjunction                | `although`, `when` |IN can be categorized as either ADP or SCONJ in UPOS.|
|      JJ     |     ADJ     | adjective                                | `green`                                   ||
|     JJR     |     ADJ     | adjective, comparative                   | `greener`                                 ||
|     JJS     |     ADJ     | adjective, superlative                   | `greenest`                                ||
|      LS     |             | list marker                              | 1)                                      ||
|      MD     |     AUX     | modal                                    | `could`, `will`, `may`, `would`, `shall`, etc.  ||
|      –      |    PUNCT    | superfluous punctuation                  | `.` `,` `(` `)`                                 ||
|      –      |      X      | missing tag                              |                                         ||
|      NN     |     NOUN    | noun, singular or mass                   | `table`                                   ||
|     NNS     |     NOUN    | noun plural                              | `tables`                                  ||
|     NNP     |    PROPN    | proper noun, singular                    | `John`, `CNN`,                              |Includes Acronyms (`CNN`, `BBC`, `NATO`, etc.)|
|     NNPS    |    PROPN    | proper noun, plural                      | `Vikings`                                 |Includes Acronyms (`CNN`, `BBC`, `NATO`, etc.)|
|     PDT     |     DET     | predeterminer  (i.e., determiner-like elements that precede an article or possessive pronouns)                        | `both` the boys , `all` his marbles, `both` the girls, `half` the time, `such` a good time, `quite` a mess, `rather` a nuisance  |**See DT carefully**|
|     POS     |     PART    | possessive ending                        | friend`'s ` , John`'s`, the parents`'`  ||
|     PRP     |     PRON    | personal pronoun (includes reflexive)  | `I`, `he`, `it`, `mine`, `yours`   |Be careful not to confuse PRON (Pronouns) with PROPN (Proper nouns) in UPOS.|
|     PRP$    |     DET     | possessive pronoun                       | `my`, `his`                                 ||
|      RB     |     ADV     | adverb (typically end with `-ly`, but also includes degree words)  | `however`, `usually`, `naturally`, `here`, `well`, `very`, `too` |A negative particle "not" is an RB in penn tagset, but it should be tagged as PART in Universal POS.|
|     RBR     |     ADV     | adverb, comparative                      | `better`                                  ||
|     RBS     |     ADV     | adverb, superlative                      | `best`  ||
|      RP     |     ADP     | particle                                 | give `up`  |Verbal particles are categorized as ADP in UPOS, not PART.|
|      –      |    SPACE    |                                          |                                         ||
|     SYM     |     SYM     | Symbols (Mathematical or scientific)      | `π`, `˚C`                                   ||
|      TO     |     PART    | to  (Infinitival)                        | `to` go, `to` him                           ||
|      UH     |     INTJ    | interjection                             | `uhhuhhuhh`                               ||
|      VB     | VERB or AUX | verb, base form   (subsumes imperatives, nfinitives, subjunctives)  | `take`                                    |Auxiliary needs to be differentiated from lexical verbs in the UPOS.|
|     VBD     | VERB or AUX | verb, past tense                         | `took`                                    |Auxiliary needs to be differentiated from lexical verbs in the UPOS. <br/> "D" represents "-ed"|
|     VBG     | VERB or AUX | verb, gerund/present participle          | `taking`                                  |Auxiliary needs to be differentiated from lexical verbs in the UPOS. <br/>"G" represents "-ing"|
|     VBN     | VERB or AUX | verb, past participle                    | `taken`                                   |Auxiliary needs to be differentiated from lexical verbs in the UPOS. <br/>"N" represents "-en"|
|     VBP     | VERB or AUX | verb, sing. present, non-3d              | `take`                                    |Auxiliary needs to be differentiated from lexical verbs in the UPOS. <br/> "P" represents "Present tense" |
|     VBZ     | VERB or AUX | verb, 3rd person sing. present        | `takes`                                   |Auxiliary needs to be differentiated from lexical verbs in the UPOS. <br/> "Z" represents the morpheme "-z" in 3 person singular "s"|
|     WDT     |     DET     | wh-determiner                            | `which`                                   ||
|      WP     |     PRON    | wh-pronoun                               | `who`, `what`, `whom`                ||
|     WP$     |     DET     | possessive wh-pronoun                    | `whose`                                   ||
|     WRB     |     ADV     | wh-abverb                                | `where`, `when` ||
|      –      |      X      | unknown                                  |                                         ||
|      –      |             | space                                    |                                         ||


## Some problematic cases
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

### Numbers (I am not sure this is reflected in spaCy)
If they are used to modify nouns, they are JJ, not CD....


### "one" (CD or NN?)
>Sometimes it is unclear whether one is cardinal number or a noun. In general, it should be tagged as a cardinal number (CD) even when it is not clearly that of a numeral

- one (CD) of the reasons
- the only one (NN) of its kind.
-

### Adverb (RB)or Particle (RP) (See the [PennTag POS tagging guideline](https://catalog.ldc.upenn.edu/docs/LDC99T42/tagguid1.pdf) on page 21).

You can insert manner adverbs (e.g., calmly) when they are adverbs.
- to sit calmly `by` (RB)
- \*to give calmly `up` (RP)
