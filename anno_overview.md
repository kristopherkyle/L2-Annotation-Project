# Part Of Speech (POS) tag annotation manual

This document explains the POS tag set to use.
We are going to use Penn Tags, which is a specified tagset for English.

## POS tagging Scheme
Here, each tag is described and examples of each are also given.
- Penn Tagset is a language specific POS tag set for English You can find the whole manual if you got confused [PennTag POS tagging guideline](https://catalog.ldc.upenn.edu/docs/LDC99T42/tagguid1.pdf).

****Note that the following `this style` is used for examples.**

| Penn Tagset | Description                              | Example                                 |Notes|
|:-----------:|------------------------------------------|-----------------------------------------|-----|
|      CC     | coordinating conjunction                 | `and`         , `but`, `yet`        ||
|      CD     | cardinal number                          | `1`, `third`                                |Numbers should be treated as Adj (JJ) when they have the same distribution as JJ. e.g., a 50-3 victory |
|      DT     | determiner                               | `the`, `a(n)`, `no`, `every`, `another`, `any`, `that`, `these` |`both` and `all` are DT when they occupy the determiner position as in `all roads` or `both times` (see PDT). |
|      EX     | existential there                        | `there` is                                ||
|      FW     | foreign word                             | `d'hoevre`                                ||
|      IN     | preposition                              | `in`, `of`, `like`                            |IN can be categorized as either ADP or SCONJ in UPOS.|
|      IN     | subordinating conjunction                | `although`, `when` |IN can be categorized as either ADP or SCONJ in UPOS.|
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
|     PRP     | personal pronoun (includes reflexive)    | `I`, `he`, `it`, `mine`, `yours`   |Be careful not to confuse PRON (Pronouns) with PROPN (Proper nouns) in UPOS.|
|     PRP$    | possessive pronoun                       | `my`, `his`                                 ||
|      RB     | adverb (typically end with `-ly`, but also includes degree words)  | `however`, `usually`, `naturally`, `here`, `well`, `very`, `too` |A negative particle "not" is an RB in penn tagset, but it should be tagged as PART in Universal POS.|
|     RBR     | adverb, comparative                      | `better`                                  ||
|     RBS     | adverb, superlative                      | `best`  ||
|      RP     | particle                                 | give `up`  |Verbal particles are categorized as ADP in UPOS, not PART.|
|     SYM     | Symbols (Mathematical or scientific)     | `π`, `˚C`                                   ||
|      TO     | to  (all instances of "to")                        | `to` go, `to` him                           |Note that in some cases, "to" is tagged as "IN" in the ONTONOTES corpus. This is incorrect because "to" should always be tagged as "TO"|
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
|     WRB     | wh-abverb                                | `where`, `when`,`why` ||

- Punctuations can be copied as it is.


## Some problematic tags
The following section will outline some frequent problematic cases. This is NOT exhaustive, and if you think your questions is not answered, refer to the following manual [PennTag POS tagging guideline](https://catalog.ldc.upenn.edu/docs/LDC99T42/tagguid1.pdf).

### Adverb (RB) or Particle (RP)
(For more details see the [PennTag POS tagging guideline](https://catalog.ldc.upenn.edu/docs/LDC99T42/tagguid1.pdf) on page 21).
You can insert manner adverbs (e.g., calmly) when they are adverbs.
- to sit calmly `by` (RB)
- \*to give calmly `up` (RP)

### Numbers (I am not sure this is reflected in spaCy)
If they are used to modify nouns, they are JJ, not CD....

## Some problematic words

### "about" (RB, IN, or RP?)
- If "about means "approximately", it should be tagged as RB (e.g., "It will take about one hour")
- If "about" has an object (and does not mean "approximately"), then it should be tagged as IN (e.g., "talking about a species...")
- In some other cases, "about" will be tagged as an RP. (e.g., "bring about change"). See "Adverb (RB) or Particle (RP)" section  for more on this.

### "both", "either", "all", etc. (CC, DT, or PDT?)
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

### "much" (JJ or RB?)
- "much" should be tagged as JJ when explicitly modifying a noun or noun phrase (e.g., "they drank too much **beer**")
- "much" should be tagged as RB if not explicitly modifying a noun or noun phrase (e.g., "they drank too much")

### "one" (CD or NN?)
Sometimes it is unclear whether one is cardinal number or a noun. In general, it should be tagged as a cardinal number (CD) even when it is not clearly that of a numeral

- one (CD) of the reasons
- the only one (NN) of its kind.


