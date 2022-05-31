# Part Of Speech (POS) tag annotation manual

This document provides an initial explanation of the POS tags used. In this project, we will be using the Penn Tagset.

If you have questions when tagging, please follow this procedure:
- check this page
- check the [Original PennTag POS tagging guidelines .pdf](https://catalog.ldc.upenn.edu/docs/LDC99T42/tagguid1.pdf)
- check the [ESL Tagging Guidelines .pdf (section 3)](http://people.csail.mit.edu/berzak/tle_guidelines/guidelines.pdf) and/or section 5 in the shorter [Berzak et al paper](https://www.aclweb.org/anthology/P16-1070.pdf)
- check the corpus using AntConc.
- If the corpus results are ambiguous (they sometimes are!), then bring up the issue in the Discord page or in our weekly meeting and we will address it.
- Please note transcription errors on the [transcription errors sheet](https://docs.google.com/spreadsheets/d/16EfWylNqjdXWA0tud4_oZqFV0zIbq_lOcj5mPLcY8PI/edit?usp=sharing)

## POS tagging Scheme
Here, each tag is described and examples of each are also given.

**Note that the following `this style` is used for examples.**

| Penn Tagset | Description                              | Example                                 |Notes|
|:-----------:|------------------------------------------|-----------------------------------------|-----|
|      CC     | coordinating conjunction                 | `and`         , `but`, `yet`        ||
|      CD     | cardinal number                          | `1`, `two`                                |Cardinal numbers (but not ordinal numbers such as "first") are almost always tagged as CD. The Penn guidelines indicate that numbers can be tagged as JJ when that number is synonymous with an adjective (e.g., a 50-3 [wide/easy/handy] victory)or as an RB when the number is synonymous with an adverb (e.g., they won 50-3 [easily/handily]). These cases, however, are exceedingly rare. When in doubt, tag numbers as CD.|
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
|      $      |dollar sign                               | `$`                   ||
|      "      | quotes                                   | `' "`              | If there is a quote mark at the end of a sentence that is not previously matched (e.g., `This pizza is delicious."`) then do not tag it (it will be cleaned from the data later).|
|(	| Right Facing Bracket |`(`||
|(	| Left Facing Bracket |`(`||
|,| comma | `,`||
|.| end sentence punctuation|`. ! ?`||
|:| colons, semi-colons, ellipses, and hyphens|`: ; - ...` ||

## Dealing with L2 usage
Often, utterances will include "errors". Following the procedures in Berzak et al. (2016), words will be tagged based on their realized form, and not on the intended one (with a few caveats). Guidelines for tagging such instances are provided below:
- Subject-verb (dis)agreement: In the sentence, `A woman open her refrigerator`, `open` should be tagged as `VB` (which represents the surface form), not `VBZ` or `VBD` (either of which could represent the presumptive intended utterance).
- Tense: Erroneous use of verb conjugations/tense are tagged based on the realized form. In the sentence `Yesterday, I eat pizza`, `eat` would be tagged as `VBP`.
- In cases where the form is ambiguous between `VB` another tag (e.g., `VBP`) **AND** the form doesn't agree with the subject in any tense, use the `VB` tag (as in the first example above).
- Plural marking: Words should be tagged according to the realized form. In the sentence `I ate one pizzas yesterday`, `pizza` should be tagged as `NNS`
- Erroneous word form uses whose form cannot be assigned a Penn Tag get the closest reasonable tag. For example, adjectives with a plural marker (e.g., `interestings`) would get the normal `JJ` tag. This is also true for misspellings for which the realized form does not create an alternate word (e.g., `dessk` would be tagged as `NN`)

## Some problematic tags
The following section will outline some frequent problematic cases. This is NOT exhaustive, and if you think your questions is not answered, refer to the following manual [PennTag POS tagging guideline](https://catalog.ldc.upenn.edu/docs/LDC99T42/tagguid1.pdf).

### Adverb (RB) or Particle (RP)?
The [Penn tagging guidelines](https://catalog.ldc.upenn.edu/docs/LDC99T42/tagguid1.pdf) provide a number of test that can be used to distinguish these three tags on pages 9, 10, 11, and 21). A very small set of these are included below:

Prepositions (`IN`) are directly associated with a noun phrase, while particles (`RP`) and adverbs (`RB`) are not.
- look `at_IN` the picture
- blaze `out_IN` into space

You cannot insert manner adverbs (e.g., calmly) between a verb and a particle.
- \*to give calmly `up` (RP)

### Hyphenated words
Hyphenated words with nouns as the root should be tagged as `JJ NN` such as `T_JJ shirt_NN`, according to the tagging guidelines (page 12). This is the case even if the unhyphenated version of the utterance should be tagged as `NN NN`. In the case of a transcribed corpus, this becomes arbitrary, but we will base our tags on how the utterance was transcribed.

### Proper noun `NNP` or `NN`?
As per the Penn tagging guidelines, capitalized words should only be counted as proper nouns when clearly referring to a proper noun (e.g., March, New York Times). When this is unclear, tag nouns as common nouns.

Words such as "state" (as in Washington S/state) and "prefecture" should be counted as common nouns except when used as part of name (e.g., "State Department", "Secretary of State").

## Some problematic words/phrases

### "'s"
`'s` should be tagged as `POS` if used as a possessive and `VBZ` if used as a verb.

If `'s` is incorrectly as a plural, leave the tag blank and add it to the [transcription errors sheet](https://docs.google.com/spreadsheets/d/16EfWylNqjdXWA0tud4_oZqFV0zIbq_lOcj5mPLcY8PI/edit?usp=sharing)

### "about" (RB, IN, or RP?)
- If "about means "approximately", it should be tagged as RB (e.g., "It will take about one hour")
- If "about" has an object (and does not mean "approximately"), then it should be tagged as IN (e.g., "talking about a species...")
- In some other cases, "about" will be tagged as an RP. (e.g., "bring about change"). See "Adverb (RB) or Particle (RP)" section  for more on this.

### between
Between should be tagged as `IN`.
- "I often fly `between_IN` Denver and Eugene"


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

### "cell phone"
The guidelines are a bit unclear on how "cell phone" should be tagged. Based on the corpus, however, `cell phone` should always be tagged as `cell_NN phone_NN`.

### everyday (`JJ`, `NN`, or `RB`?)
Everyday should be tagged as `NN` and not as `RB` following the Penn Guidelines on pages 18-19. If "everyday" directly modifies a noun, then it should be tagged as `JJ`. The utterance "every day" should be tagged as `every_DT day_NN`.
- I go there `everyday_NN`
- Those are my `everday_JJ` jeans.


### "first" (`JJ`, `RB` or `LS`)
`first` (and other ordinal numbers) is most commonly tagged as an adjective JJ as in `the first issue`. When used to introduce a sentence, `first` is  almost always tagged as `RB` as in `First, the president was ...`. It can also be tagged as `LS` when used in a list (but this is rare and confined to short, focused lists).

### "go out" (`IN`, `RB`, or `RP`)
Potential phrasal verbs are generally tagged inconsistently in the corpora between `IN`, `RB`, and `RP`.

In the construction `go out`, some of this inconsistency can be eliminated by
the following guidelines. Note: These guidelines should not be extended to all
phrasal verbs. In these guidelines, the `RB` is excluded for the sake of
consistency. For other phrasal verbs, the `RB` tag should be considered.

If part of the sentence with the word `out` can be replaced with the word `there`, and the sentence retains the same meaning, then `out`
is tagged as `IN`. In this context, `out` modifies a noun phrase.
- `The ball went [out_IN of the park] . → The ball went [there] .`

If replacing part of the sentence containing the word `out` with the word `there` either changes the meaning of the sentence, or makes an ungrammatical sentence,
then `out` is tagged as `RP`. In this context, `out` is a particle of a phrasal verb.
- `I went [out_RP with this girl from my class] . → I went [there] .`
- `I went [out_RP with my friends] . → I went [there] .`
- `The lights went [out_RP] . → The lights went [there] .`

### "have" (`VB*` or `MD`)
"have" has three uses, and all should be tagged with the appropriate `VB*` tag for its use (following the Penn guidelines, page 17 [19 in .pdf]):
- "have" as an auxiliary verb in "She has visited Thailand" gets `VBZ` and in "I have visited Thailand" gets `VBP`
- "have" as a modal auxiliary as in "He has to go to Thailand" gets `VBZ` and "They have to go to Thailand" gets `VBP`
- "have" as a lexical verb in "They had a nice car" gets `VBD`

### Hyphenated word special mentions.
The following guidelines concern niche usage of hyphens. The goal of these
guidelines is to make hyphen usage consistent in these niche situations.

In the word `good - bye`, both `good` and `bye` should be tagged as `UH`.
- `Good_UH - bye_UH . `

ordinal numbers (ex: first, second, third) which are preceded by a `CD` and a hyphen should be tagged as `JJ`.
- `That was twenty_CD -_: sixth_JJ or twenty_CD -_: third_JJ .`

If `so-so` is has a meaning akin to `okay`, then both `so`'s should be tagged as `JJ`.
- `I 'm so_JJ - so_JJ .'`

### "like" (`VB*`, `IN`, or `UH`)
- If "like" is used as a verb, tag it as a verb.
- If "like" is used in a construction that could roughly be replaced with "such as", then it gets a `IN` tag.
- In some cases, "like" will be used as an interjection (sometimes at the end of a sentence). In this case, it gets a `UH` tag. This is less common than the `IN` tag.

### "little" (`JJ` or `RB`?)
- "little" should be tagged as `JJ` when it modifies a noun, as in "I only want a **little** bit".
- This holds true even in the predicate: "That piece of fruit is **little**." (This should be tagged as `JJ`)
- "little" should be tagged as `RB` when it directly modifies a verb, as in the sentence "They slept a **little**." (Here, little is telling us how much they slept)

### "much" (`JJ` or `RB`?)
- "much" should be tagged as JJ when explicitly modifying a noun or noun phrase (e.g., "they drank too much **beer**")
- "much" should be tagged as RB if not explicitly modifying a noun or noun phrase (e.g., "they drank too much")

### "now" (`RB` or `UH`)
- "now" is usually tagged as `RB`, as in "now I know what to do" (now tells us when)
- "now" can also be used as an interjection `UH` as in the sentence "Now, I am not suggesting that..." (where "now" is acting as a filler)

### "of course" (`IN NN` or `RB RB`?)
Following the WSJ texts and the ESL corpus, "of course" should be tagged as `of_RB course_RB` when used as an adverbial phrase as in "Of_RB course_RB, Washington had n't..."

In fairly rare circumstances, "of course" can also be used as in preposition + noun constructions as in the phrase, "As a matter of_IN course_NN, we check the corpus"

### "one" (`CD` or `NN`?)
Sometimes it is unclear whether one is cardinal number or a noun. In general, it should be tagged as a cardinal number (CD) even when it is not clearly that of a numeral

- one (CD) of the reasons
- the only one (NN) of its kind.

### only (`JJ` or `RB`?)
`only` should be tagged as `JJ` if it directly modifies a noun or noun phrase. If it modifies a sentence (or a verb), it should be tagged as `RB`.

 - "It was the `only_JJ` state in the midwest that..."
 - "... trading moves typically last `only_RB` a few hours."

### "police" (`NN` or `NNS`?)

Some nouns like `police` have identical singular and plural forms. See NN vs NNS in the POS Tagging Manual for general rules in testing `NN` vs `NNS`. Below are some examples of tests.

In the construction `call the police`, if the word `police` can be replaced by the word `them`, it is tagged as `NNS`.
- `And after that , you call the police_NNS , and tell whatever you are .`

If `police` is a subject of a `VBZ`, then it is tagged as `NN`.
- `and then police_NN comes_VBZ .`

If `police` is part of a singular compound noun that can be replaced by a singular object pronoun like `him`, `her`, or `it`, then `police` is tagged as `NN`. The word `there` also works as a test for locations.
- `And Taro explained the situation to the police_NN officer .`
- `But we tried to go to the police_NN office .`

### "so" (`RB`, `CC`, or `IN`?)
`So` is quite versatile and can therefore be difficult to tag. Note that `so` is not tagged consistently in the corpus.

`So` will often be used as an adverb (RB) as in "that pizza was `so_RB` good"

`So` can also be used as a coordinating (CC) or subordinating (IN) conjunction.
- If `so` connects two clauses and could be replaced by the word `and` it should be tagged as CC as in "I like pizza, `so_CC` I eat it weekly"
  - Note that the clause including `so_CC` cannot be moved to the beginning of an utterance "\*`So_CC` I eat it weekly, I like pizza"
- If `so` connects two clauses and is followed by `that` or could be replaced with `so that` it is a subordinating conjunction (IN) as in "I eat pizza daily `so_IN` that I can get better at rock climbing"
  - Note that a clause that includes `so_IN` can be moved to the beginning of a sentence (which means that `so_IN` can occur at the beginning of a sentence!) as in "`So_IN` that I can get better at rock climbing, I eat pizza daily"

`so` is tagged as an adverb (RB) when it is the first part of a sentence.
- `So_RB I think it 's good like'`

### "sort of" and "kind of"
`sort of` and `kind of` shoud be tagged as `NN + IN` in cases such as "They had some kind_NN of_IN tool"

However, when used as an adverbial, they should be tagged as `RB + RB` as in "They sort_RB of_RB ran away",

### "that"
`that` is tagged as `DT` in the following circumstances:

1) `that` is a determiner of a noun.

- `I 'd like to finish reading that_DT book by one o'clock .`

2) `that` is a subject, and could be replaced by "it".

- `That_DT was not too bad .`

When `that` introduces a relative clause, it is tagged as `WDT`. A relative clause is a clause which modifies a noun. This means `that` is most commonly tagged as `WDT` when preceded by a noun.

- `The man that_WDT works at the train station .`

If the word `that` can be replaced by the word `which`, `whom`, or `who`, then it should be tagged as `WDT`.

- `The doujou that_WDT we practice at ,` - which
- `The man that_WDT works at the train station .` - who/whom

`that` is sometimes tagged as `RB` when it can be replaced by the word `very`.

- `It 's not that_RB good .`
- `I actually do n't remember that_RB much .`

When `that` doesn't meet the requirements to be tagged as `DT`, `WDT`, or `RB`, then it should be tagged as a subordinating conjunction `IN`.

- `I just remembered that_IN I had a test today .`
- `He got angry at me that_IN his bike broke and his phone got broken .`

### Informal contractions like `wanna`
Ideally, informal contractions like `wanna` will be transcribed as 2 separate tokens. This way, they can be tagged separately.
- `I wan_VBP na_TO catch my flight .`
- `I wann_VBP a_DT economy ticket .`

Informal contractions being transcribed as a singular token is a transcription error. In this case, they should be tagged solely based off of the verb.
- `I wanna_VBP catch my flight .`
- `I wanna_VBP economy ticket .`

Other informal contractions include `gotta` and `gonna`.
- `I 'm gon_VBG na_TO call them .`
- `Yesterday I got_VBD ta_TO go hospital .`

### "Yen" (NN or NNS)
`Yen` should be tagged as NNS as in "one million Yen_NNS", unless it is explicitly used as NN as in "The value of the Yen_NN is increasing"
