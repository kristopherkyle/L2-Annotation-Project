# Guidelines for Dependency Annotation

We will be annotating our corpus for [Universal Dependency Relations (version 2)](https://universaldependencies.org/u/dep/index.html)

If you have questions during annotation, please follow this procedure:
- Check this page
- Check the [Dependency Guidelines](https://universaldependencies.org/u/dep/index.html)
- Check the [ESL Guidelines](http://people.csail.mit.edu/berzak/tle_guidelines/guidelines.pdf)
- Search dependency-annotated corpora with TüNDRA (note that searches are case-sensitive):
	-	Learn how to search [here](https://weblicht.sfs.uni-tuebingen.de/Tundra/help)
	- 	Search the [written ESL corpus](https://weblicht.sfs.uni-tuebingen.de/Tundra/FileBank_b03fc421-4ea6-4eba-96b5-e543dfe72c52/22)
	- 	Search the [English Web Treebank (EWT)](https://weblicht.sfs.uni-tuebingen.de/Tundra/UD_English-EWT_v2.4/)

## Introduction to Dependency Relations
Dependency relations capture functional grammatical relationships between words in an utterance. Each linguistic item in an utterance has one (and only one) syntactic head, but may have multiple (or no) dependents. For example, in the sentence `The hungry person ate the pizza`, the word `person` has one syntactic head `ate`. `person` is connected to `head` via a nominal subject `nsubj` relationship. `person` also has two syntactic dependents: `hungry` (via an adjective modifier relationship `amod`) and `The` (via a determiner relationship `det`).

## UD Annotation Scheme
Here, each dependency relation is described and examples of each are also given.


| Universal Dependencies                                                    | Descrption                                | Example                                                                                                                                                                                                                                                                                                                                                      | Notes                                                                                                                            |
|---------------------------------------------------------------------------|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [acl](https://universaldependencies.org/u/dep/acl.html)                   | clausal   modifier of noun                | First   of all , I was really furious of watching a show_**head** starring_**acl** by   a different actor , instead of Danny Brook .                                                                                                                                                                                                                         | The main   verb in the modifying clause will take the "acl" annotation                                                           |
| [acl:relcl](https://universaldependencies.org/u/dep/acl-relcl.html)       | relative clause modifier                  | There is something_**head** I   like_**acl:relcl** to know from you .                                                                                                                                                                                                                                                                                        | The main verb in the relative   clause will take the "acl:relcl" annotation                                                      |
| [advcl](https://universaldependencies.org/u/dep/advcl.html)               | adverbial clause modifier                 | I ask_**head** you for   returning_**advcl** my money back .                                                                                                                                                                                                                                                                                                 | The main verb in the adverbial   clause will take the "acl:relcl" annotation                                                     |
| [advmod](https://universaldependencies.org/u/dep/advmod.html)             | adverbial modifier                        | For instance a lot of children nowadays_**advmod**   replace_**head** their real life with the virtual world , which computers   create .                                                                                                                                                                                                                    |                                                                                                                                  |
| [amod](https://universaldependencies.org/u/dep/amod.html)                 | adjectival modifier                       | It was about fourty five minutes later than original_**amod**   starting_**amod** time_**head**                                                                                                                                                                                                                                                              | There are 2 dependencies in this example                                                                                         |
| [appos](https://universaldependencies.org/u/dep/appos.html)               | appositional modifier                     | It was Katha_**head** , a girl_**appos** who had the same   problems like Pat .                                                                                                                                                                                                                                                                              |                                                                                                                                  |
| [aux](https://universaldependencies.org/u/dep/aux_.html)                  | auxiliary                                 | You have_**aux** also written_**head** in your advertisement   that it would_**aux** started_**head** at half past seven but it started at   20:15 !                                                                                                                                                                                                         | There are 2 dependencies in this example                                                                                         |
| [aux:pass](https://universaldependencies.org/u/dep/aux-pass.html)         | passive auxiliary                         | If he had told everybody, J would have been_**aux:pass**   blamed_**head** by whole school .                                                                                                                                                                                                                                                                 |                                                                                                                                  |
| [case](https://universaldependencies.org/u/dep/case.html)                 | case marking                              | If she was not followed by_**case** journalists_**head** , she   would n't die .                                                                                                                                                                                                                                                                             |                                                                                                                                  |
| [cc](https://universaldependencies.org/u/dep/cc.html)                     | coordinating conjunction                  | And_**cc** the reason I choose painting is_**head** it 's   being very exciting to me ,                                                                                                                                                                                                                                                                      |                                                                                                                                  |
| [cc:preconj](https://universaldependencies.org/u/dep/cc-preconj.html)     | preconjunct                               | In conclusion , there are both_**cc:preconj**   advantages_**head** and disadvantages of covering celebrities .                                                                                                                                                                                                                                              |                                                                                                                                  |
| [ccomp](https://universaldependencies.org/u/dep/ccomp.html)               | clausal complement                        | You ca n't imagine_**head** how funny_**ccomp** it was !                                                                                                                                                                                                                                                                                                     |                                                                                                                                  |
| [compound](https://universaldependencies.org/u/dep/compound.html)         | compound                                  | would you check the weather_**compound** forecast_**head** for   me , please ?                                                                                                                                                                                                                                                                               |                                                                                                                                  |
| [compound:prt](https://universaldependencies.org/u/dep/compound-prt.html) | phrasal verb particle                     | They make their life style much easy more fast because they   need to catch_**head** up_**compound:prt** with the other people .                                                                                                                                                                                                                             |                                                                                                                                  |
| [conj](https://universaldependencies.org/u/dep/conj.html)                 | conjunct                                  | I have knowladge about navigation_**head** , engine_**conj** ,   ropes_**conj** and knots_**conj** and sails_**conj** as well .                                                                                                                                                                                                                              | There are 4 dependencies in this example                                                                                         |
| [cop](https://universaldependencies.org/u/dep/cop.html)                   | copula                                    | Unfortunatly , Pat was_**cop** n't very good_**head** at   keeping secrets .                                                                                                                                                                                                                                                                                 |                                                                                                                                  |
| [csubj](https://universaldependencies.org/u/dep/csubj.html)               | clausal subject                           | I really think that living_**csubj** will be_**head** like   living in the moon , very exciting .                                                                                                                                                                                                                                                            |                                                                                                                                  |
| [csubj:pass](https://universaldependencies.org/u/dep/csubj-pass.html)     | clausal passive subject                   | In the advertisement , it was told_**head** that Danny Brook   was starring_**csubj:pass** , but in place of him there was a different actor   and he was really dissapointing .                                                                                                                                                                             |                                                                                                                                  |
| [dep](https://universaldependencies.org/u/dep/dep.html)                   | unspecified dependency                    | MOON LANDING HOAX_**head** : CHURCH = TECHNOLOGY_**dep** &   GOVERNMENT - Shuttle Carried on Aircraft model                                                                                                                                                                                                                                                  | Example from EWT corpus, limited examples                                                                                        |
| [det](https://universaldependencies.org/u/dep/det.html)                   | determiner                                | I would rather be accommodated in a tent because I already   have the_**det** necessary material_**head** for camping .                                                                                                                                                                                                                                      |                                                                                                                                  |
| [det:predet](https://universaldependencies.org/en/dep/det-predet.html)    | predeterminer                             | But sometimes I have to forget my opinion and spent   all_**predet** the day_**head** looking for my mother in a huge   department-store.                                                                                                                                                                                                                    |                                                                                                                                  |
| [discourse](https://universaldependencies.org/u/dep/discourse.html)       | discourse element                         | I would like_**head** to travel on July , please_**discourse**   , because that when I am in vacation .                                                                                                                                                                                                                                                      |                                                                                                                                  |
| [dislocated](https://universaldependencies.org/u/dep/dislocated.html)     | dislocated elements                       | steel_**dislocated** or iron , which use for our building ,   it_**head** can make it stronger and easy to destroy .                                                                                                                                                                                                                                         | Limited examples in corpra                                                                                                       |
| [expl](https://universaldependencies.org/u/dep/expl.html)                 | expletive                                 | In these gallaries there_**expl** are_**head** Historical   paintings , antique furnitures which Chiang used .                                                                                                                                                                                                                                               |                                                                                                                                  |
| [fixed](https://universaldependencies.org/u/dep/fixed.html)               | fixed multiword expression                | Then , we should film the English class so_**head**   as_**fixed** to_**fixed** show who makes the film .                                                                                                                                                                                                                                                    | There are 2 dependencies in this example                                                                                         |
| [flat](https://universaldependencies.org/u/dep/flat.html)                 | flat multiword expression                 | After concert I left with Ricky_**head** Martin_**flat** .                                                                                                                                                                                                                                                                                                   |                                                                                                                                  |
| [flat:foreign](https://universaldependencies.org/u/dep/flat-foreign.html) | foreign words                             | Lopez 's 1561 book "Libro_**head** de_**flat:foreign**   la_**flat:foreign** invencion_**flat:foreign** liberal_**flat:foreign**   y_**flat:foreign** arte_**flat:foreign** del_**flat:foreign**   Juego_**flat:foreign** del_**flat:foreign** Acedraz_**flat:foreign** "   became THE classic on Chess openings , including the one that bears his name   . | Example from EWT corpus, only example in corpus, there are 10   dependencies in this example                                     |
| [goeswith](https://universaldependencies.org/u/dep/goeswith.html)         | goes with                                 | All my class_**head** mates_**goeswith** are looking forward   to go to London .                                                                                                                                                                                                                                                                             |                                                                                                                                  |
| [iobj](https://universaldependencies.org/u/dep/iobj.html)                 | indirect object                           | I would like to explain_**head** you_**iobj** my experience   because I want you to give my money back .                                                                                                                                                                                                                                                     |                                                                                                                                  |
| [list](https://universaldependencies.org/u/dep/list.html)                 | list                                      | How many jeans_**head** , Pants_**list** , sweater_**list**   ect._**list** do I have to take ?                                                                                                                                                                                                                                                              | There are 3 dependencies in this example                                                                                         |
| [mark](https://universaldependencies.org/u/dep/mark.html)                 | marker                                    | This is the fact that_**mark** shopping is not   enjoyable_**head** .                                                                                                                                                                                                                                                                                        |                                                                                                                                  |
| [nmod](https://universaldependencies.org/u/dep/nmod.html)                 | nominal modifier                          | How is the home_**head** of the future_**nmod** will be ?                                                                                                                                                                                                                                                                                                    |                                                                                                                                  |
| [nmod:npmod](https://universaldependencies.org/en/dep/nmod-npmod.html)    | noun phrase as adverbial modifier of noun | Yes she is having physical therapy 3 times_**head** a week_**nmod:npmod** .                                                                                                                                                                                                                                                                                  | Example from EWT corpus                                                                                                          |
| [nmod:poss](https://universaldependencies.org/u/dep/nmod-poss.html)       | possessive nominal modifier               | I will go to your_**nmod:poss** office_**head** this week .                                                                                                                                                                                                                                                                                                  |                                                                                                                                  |
| [nmod:tmod](https://universaldependencies.org/u/dep/nmod-tmod.html)       | temporal modifier                         | Her husband became a citizen_**head** of the US just the   week_**nmod:tmod** before last .                                                                                                                                                                                                                                                                  | Example from EWT corpus                                                                                                          |
| [nsubj](https://universaldependencies.org/u/dep/nsubj.html)               | nominal subject                           | I_**nsubj** will go_**head** to your office this week .                                                                                                                                                                                                                                                                                                      |                                                                                                                                  |
| [nsubj:pass](https://universaldependencies.org/u/dep/nsubj-pass.html)     | passive nominal subject                   | We will not use black clothes as we_**nsubj:pass** are   used_**head** to do .                                                                                                                                                                                                                                                                               |                                                                                                                                  |
| [nummod](https://universaldependencies.org/u/dep/nummod.html)             | numeric modifier                          | I usually spend my time on playing computer about   three_**nummod** hours_**head** a day .                                                                                                                                                                                                                                                                  |                                                                                                                                  |
| [obj](https://universaldependencies.org/u/dep/obj.html)                   | object                                    | Even we could make_**head** a trip_**obj** to Paris in the   school holiday !                                                                                                                                                                                                                                                                                |                                                                                                                                  |
| [obl](https://universaldependencies.org/u/dep/obl.html)                   | oblique nominal                           | Thank_**head** you very much for you time_**obl** .                                                                                                                                                                                                                                                                                                          |                                                                                                                                  |
| [obl:npmod](https://universaldependencies.org/cop/dep/obl-npmod.html)     | noun phrase as adverbial modifier         | They are a bit_**obl:npmod** far_**head** from town but they   have huge car park .                                                                                                                                                                                                                                                                          |                                                                                                                                  |
| [obl:tmod](https://universaldependencies.org/u/dep/obl-tmod.html)         | temporal modifier                         | I 'm so happy with the experience I lived_**head** last   month_**obl:tmod** .                                                                                                                                                                                                                                                                               |                                                                                                                                  |
| [orphan](https://universaldependencies.org/u/dep/orphan.html)             | orphan                                    | So in the last century our daily life changed dramandesly and   we became lazy and our life_**head** unpersonal_**orphan** , fast and   unromantic .                                                                                                                                                                                                         | Only example in ESL corpus                                                                                                       |
| [parataxis](https://universaldependencies.org/u/dep/parataxis.html)       | parataxis                                 | They would be sinthetic clothes_**head** , I   think_**parataxis** made of plastic or something similar . "                                                                                                                                                                                                                                                  |                                                                                                                                  |
| [punct](https://universaldependencies.org/u/dep/punct.html)               | punctuation                               | The scene of Toyko is not beautiful_**head** ,_**punct** but   you think that this city is a developing place ._**punct**                                                                                                                                                                                                                                    | There are 2 dependencies in this example                                                                                         |
| [reparandum](https://universaldependencies.org/u/dep/reparandum.html)     | overridden disfluency                     | It was just unbelievably dissapointing because the   reason_**head** I mean_**reparandum** main reason which made me to go was to   see Danny Brook .                                                                                                                                                                                                        | Limited examples in corpra                                                                                                       |
| [root](https://universaldependencies.org/u/dep/root.html)                 | root                                      | I could n't believe_**root** it but he gave me the contract ot   fill it out .                                                                                                                                                                                                                                                                               | The root is the head of itself; tag in webanno by first   holding shift, and then dragging an arrow from the root tag to itself. |
| [vocative](https://universaldependencies.org/u/dep/vocative.html)         | vocative                                  | Now Kim_**vocative** , I will finish_**head** my letter but I   promise you to write again as soon as possible , maybe if I 've developed the   photos of the concert and the stars and the ….                                                                                                                                                               | Limited examples in corpra                                                                                                       |
| [xcomp](https://universaldependencies.org/u/dep/xcomp.html)               | open clausal complement                   | Further because I like_**head**   to live_**xcomp** in contact with the nature .                                                                                                                                                                                                                                                                             |                                                                                                                                  |



## Clarifications and special cases (tags)

### `acl`
The UD guidelines define `acl` as finite or non-finite clauses that modify a nominal. The noun that the clause modifies is the head of the `acl` relation.

The dependent as a VBG:

- `There are many online sites_NNS_head offering_VBG_acl booking facilities`

- `The right to know everything_NN_head happening_VBG_acl in the world`

The dependent as a VBN:

- `I went to your show_NN_head called_VBN_acl “ Over the Rainbow”`

The dependent as a VB in an infinitival clause:

- `I had the chance_NN_head to spend_VB_acl time in London`

Relative clauses are also instances of `acl`, though they are tagged with `acl:relcl`.

- `I saw the man_NN_head you love_VBP_acl:relcl`

### `acl` or `xcomp`
The distinction between `acl` and `xcomp` is sometimes difficult to make. Both dependency relationships can contain infinitive clauses. To distinguish between the two, determine whether the head of the clause is a verb, adjective or a nominal.

If the clause is modifying a verb or adjective then it is typically `xcomp`

- `I started_VBD_head to work_VB_xcomp there yesterday`

- `We should try_VB_head to understand_VB_xcomp technology`

- `Everyone is welcome_JJ_head to join_VB_xcomp our study group`

- `We are very happy_JJ_head to help_VB_xcomp you in any way`

If the clause is modifying a nominal (that is, if the head of the clause is a noun phrase) then it is `acl`.

### Adjectives at the beginning of utterances

There are quite a few sentences in the data that begin with an adjective or an adjectival phrase. We will approach tagging these occurrences differently, depending on the type of utterance and construction it is.

When the adjective is part of an unambiguously implied copular construction, it can be tagged as the root of the sentence…

<fine , thank you > should be tagged as:

- `fine_JJ_root , thank_VBP_parataxis you`

This can also be the case in situations where there is explicit subordination attached to the initial adjective phrase:

< very busy because I attend big project now >

- `Very busy_JJ_root because I attend_advcl big project now`

When there is no explicit subordination, nor an unambiguously implied copular construction, the initial adjective is likely a `discourse` marker. This will often be the case when the adjective can be substituted for other discourse markers like ‘OK’ or ‘yeah’ and gives no clear implication of a copular construction.

<fine , I will do it > will be tagged as:
- `fine_JJ_discourse , I will do_VB_root it`
If there are ambiguous or confusing examples of initial adjectival utterances, be sure to bring them up in the discord/meetings so we can continue to update this heuristic.

### `ccomp`
Clausal complements `ccomp` are given when a clause has an overt subject OR the implied subject can be interpreted as something other than the subject of the head clause (see `ccomp` or `xcomp`).

In most sentences, a `ccomp` dependent has an overt subject and is a `VB` or `JJ` which has a head that is a type of `VB` or `JJ`.
- `I hope_VBP_head you consider_VBP_ccomp these pieces of suggestions .`

`ccomp` can sometimes be a `NN` when it is the head of a `cop` dependent.
- `We thought it would be_VB_cop a joke_NN_head , but it was n’t .`
- `We thought_VBD_head it would be a joke_NN_ccomp , but it was n’t .`


### `ccomp` or `xcomp`
External complements (`xcomp`) are given when a clause has no overt subject AND the implied subject is the same as the head clause. This is most common with infinitive clauses.
- `We try_head to play_xcomp` (ESL search: [edge = "xcomp"], implied subject can only be `We`)
- `We started_head digging_xcomp` ([from guidelines](https://universaldependencies.org/u/dep/ccomp.html); implied subject of `digging` can only be `We`)

Clausal complements (`ccomp`) are given when a clause has an overt subject OR the implied subject can be interpreted as something other than the subject of the head clause.
- `I hope_head you consider_ccomp these pieces of suggestions` (ESL search: [edge = "ccomp"])
- `The boss said_head to start_ccomp digging` ([from guidelines](https://universaldependencies.org/u/dep/ccomp.html); implied subject is possibly/likely `you` not `boss`, so it can't be `xcomp`)
- `I say_head to him do n't bring_ccomp heavy things` (from Spoken corpus, implied subject is `you`, which is different from the subject of the head clause, `I`)

### `csubj`
`csubj` is used when the subject of a clause is itself a clause. The root of the subject clause (not the root of the sentence) is the `csubj` dependent.

`csubj` is often the main verb of the subject clause.
- `To teach_csubj pupils is not easy_head , of course .`

`csubj` is often not a verb when there is a copular verb in the subject clause.
- `It takes_head some time and practice to be able_csubj to focus on the one thought .`

### `discourse` or `parataxis`
Utterances such as `you know` and `I mean` can be a bit confusing to tag. Although they might seem like like discourse markers, the guidelines for the `discourse` tag [explicitly indicate](https://universaldependencies.org/u/dep/discourse.html) that instances such as `you know` are not counted as discourse markers. Even in cases where these (and related utterances) appear to be functioning as discourse markers, they should be tagged as instances of `parataxis`.
- `I mean_parataxis , at the time I was 28_head` (EWT search:  `[word = "mean" & (edge = "parataxis" | edge = "discourse")] > [word = "I"]`)
- `you know_parataxis, nature hates_head a void` (EWT search: `[word = "know" & (edge = "parataxis" | edge = "discourse")] > [word = "you"]`)

### `expl`
`expl` is used for the existential “there”.
- `There_expl¹ are_head¹ a lot of folk stories in the world and there_expl² are_head² a lot of folk stories in Estonia ,`

“it” is marked as `expl` when it is used in extraposition constructions.
- `It_expl was not perfect evening_head for me and my child at all !`
- `As far as I ‘m concerned, I firmly believe that , it_expl ‘s worth_head to pointing out the following :``

### `flat:foreign`
`flat:foreign` is only used when there is a sequence of foreign words. The first foreign word is the head of the flat:foreign dependents.
- `I should have asked then but i did n’t the only line i remember is de_head lunde_flat:foreign bar_flat:foreign .. or something like that .. does anybody know which song i am talking about ?`

### `fixed` vs `flat` vs `compound` vs `compound:prt`

`fixed` is used for multiword expressions which behave like function words or short adverbials.
- `Of_head course_fixed , I became aware of her feelings since a friend of mine overheard a conversation between Pat and other girl .`

`flat` is used for multiword expressions such as names and titles which do not use regular syntactic relations (otherwise see `compound`). The first word in the multiword expression is the head of the flat dependencies.
- `The telephone was invented by Alexander_head Graham_flat Bell_flat in the end of the 19th century .`
`Flat` dependencies are used when a multiword expression is grammaticalized to the extent that there is no clear internal structure or evidence that one of the words is the syntactic head. The first word in the multiword expression is the head of the flat dependencies.
- `New_head York_flat`

`compound` is generally used for multiword expressions of nouns. This does not include mistakenly separated words (see `goeswith`).
- `But the most important innovation of technology_compound development_head is the computer .`
If a multiword expression is headed, it must be a compound dependency to preserve the syntactic hierarchy of the head.
- `Apple_compound pie_head`
However, if a headed mutliword expression is grammaticalized to the extent that there is no clear internal structure or evidence that one of the words is the syntactic head, the flat dependency is used (see `compound`)

Proper nouns which use regular syntactic relations are tagged as `compound` (otherwise see `flat`).
- `This building is situated on the magnificent embankment of Niva_compound¹ River_head¹ with an excellent view on the Hermitage_compound² Museum_head² .`

Multiword expressions of numbers also take the `compound` dependency.
- `The performance started fourty_compound five_head minutes later .`

`compound` can sometimes be a `JJ`.
- `Their selection is top_compound notch_head and the staff is very knowledgeable .`
- `my experience with them was great - low_compound stress_head , very helpful and very personal .`

The particle of an idiomatic phrasal verb is marked as a `compound:prt` dependent. The head of the `compound:prt` dependent is the verb element of the phrasal verb.
- `I could n’t believe it but he gave me the contract to fill_head it out_compound:prt .`


### `goeswith`

`goeswith` is used to mark when two parts of a word are mistakenly separated,
- `Were the people happier in a past than to_head day_goeswith ?`

### `nmod`
“An nmod relation is used for nominal dependents of another noun or noun phrase”. `nmod` relationships are typically realized via prepositional phrases, wherein a prepositional phrase is modifying a noun phrase.

- `our way_NN_head  of  life_NN_nmod`
- `the boys_NNS_head in blue_JJ_nmod`

Note that an `nmod` token can be a nominal itself (as is typical) as well as an attributive adjective (see ‘blue’ in the example above).

`PRP` is sometimes `nmod` because it can function as the nominal dependent of another noun or noun phrase.
- `He has a bestfriend , that was more like a brother_NN_head for him_PRP_nmod.`

### `obl`
In most sentences, an `obl` dependent is an `NNP`, `NN`, or `PRP` which has a head that is a `VB*`, `JJ`, or `RB`.
- `Modern technology plays_VBZ_head an important role in our life_NN_obl .`

An `obl` dependent can also be `IN`. Common `IN` words which can be `obl` dependents include: “with”, “for”, “like”, “from”, “about”, “into”, and “of”.
- `After having visited shops during 10 hours and tried at least 2,000 shoes , I finally found what I was looking_VBG_head for_IN_obl .`
- `The hotel your group has been booked_VBN_head into_IN_obl is called Palace Hotel .`

“Which” and “that” can be `obl` dependents even though they are `WDT`.
- `Here are the information which_WDT_obl you asked_VBN_head me for .`
- `In addition to this , it was not the famous actors that_WDT_obl you have mentionned_VBN_head in the advertisement , so we were disappointed .`

An `obl` dependent can also be `JJ`. This occurs in a variety of contexts.

- A dependent `JJ` is preceded by a `IN`.
	- `'Adobe Acrobat Reader 4.0 may be downloaded_VBN_head for_IN FREE_JJ_obl from www.adobe.com``


- The word “own” when it is preceded by a `PRP$`.
	- `The longer and further they live_VBP_head on their_PRP$ own_JJ_obl , the more they may feel that they need a family .`


- The word “other” when preceded by the word “each”.
	- `Students are talking_VBG_head to each_DT other_JJ_obl when they are having break .`

An `obl` dependent can also be `DET` when it is preceded by a `IN` or `TO`. This occurs with the words “this”, “that”, “all”, and “another”.
- `First_RB_head of_IN all_DET_obl , the advertisement of the show said that Danny Brook was going to be on stage .`
- `Further I would prefer to live in a tent at the Camp , because I am already used_JJ_head to_TO that_DET_obl , because I often spent my holidays in tents .`


### `obl` or `nmod`
Making the distinction between whether a token takes an oblique (obl) or nominal modifier (nmod) dependency comes down to constituency. This distinction often is required when examining prepositional phrases. To make this distinction, one needs to determine the head of the prepositional phrase by asking the question: what is the prepositional phrase modifying?
If the PP is modifying a noun phrase, or argument that is functioning as a noun phrase (see ‘another_DET’ below), the head of *the PP is likely an* **nmod**. Note that these cases of nmod often immediately follow the noun phrase they’re modifying.

- `another_DET_head of your questions_NNS_nmod`

If the PP in question modifies a verb, adjective, or adverb it will likely be tagged as **obl**. Oblique phrases can also immediately follow a noun phrase, so the position/location of the phrase in the sentence isn’t a foolproof heuristic. That is, you can’t determine the dependency of the phrase just by its relative position.

### `obl:npmod`
This relation is used when a noun phrase is used as an adverbial modifier. This relation is often realized in:
(i) measure phrases:
- `The board is six feet_NN_obl:npmod long_JJ_head`
(ii) noun phrases acting adverbially, modifying noun phrases or adjectives:

- `it was a little bit_NN_obl:npmod hard_JJ_head to understand`

- `I can only sing_VB_head a little bit_NN_obl:npmod

- `The actual vote was a little_obl:npmod confusing_head`

(iii) In the constructions “years old” and “years ago”:
- `I am 17 years_obl:npmod old_JJ_head .`
- `That was 4 years_obl:npmod ago_RB_head .`

(iv) to mark time by describing the frequency of a recurring event or state:
- `It ‘s twice my size and eats a rabbit once_head a month_obl:npmod .`
- `I am hiring them to come twice_head a week_obl:npmod`
- `Or will the nearly year_obl:npmod - round_head snow be too much for those who have never experienced snow in their lives ?`

See `obl:npmod` vs. `obl:tmod` vs `nmod:tmod`

### `obl:npmod` vs. `obl:tmod` vs `nmod:tmod`

`obl:tmod` and `nmod:tmod` dependencies are nominal `obl` and `nmod` dependencies which specify time.

The `obl:tmod` dependency marks nominal indicators of time of which are headed by a `VB*`, `JJ`, or `RB`.
- `what are you doing_VBG_head tonight_NN_obl:tmod .`

The `nmod:tmod` dependency is used when a nominal indicator of time is headed by another nominal construction.
- `Are you free for lunch some day_NN_head this week_NN_nmod:tmod ?`

See `nmod` or `obl` for more.

When a temporal word is not headed by a nominal construction (and is therefore a type of obl rather than an nmod:tmod) it is most often an `obl:tmod` dependent, with 2 exceptions where it is instead an `obl:npmod` dependent. (Note that the corpora are inconsistent in this distinction).


Use `obl:npmod` instead of `obl:tmod`:

1) In the constructions “years old” and “years ago”.
- `I am 17 years_obl:npmod old_JJ_head .`
- `That was 4 years_obl:npmod ago_RB_head .`

2) To describe the frequency of a recurring event or state.
- `It ‘s twice my size and eats a rabbit once_head a month_obl:npmod .`
- `I am hiring them to come twice_head a week_obl:npmod`
- `Or will the nearly year_obl:npmod - round_head snow be too much for those who have never experienced snow in their lives ?`


### `nsubj`
`nsubj` is used to mark the subject or agent of a clause. This most frequently occurs before a conjugated verb.
- `On the other hand , it_nsubj looks_head pretty cool .`

When the subject or agent refers to a copular verb (`cop`), the head of the `nsubj` dependent is the same as the head of the `cop`.
- `Google_nsubj is_cop a nice search engine_head .`
- `Is_cop that_nsubj a money maker_head ?`

When “is” or “are” are the head of a preceding `expl` dependent, “is” or “are” are also the head of a following nominal `nsubj` dependent.
- `there_expl¹ are_head¹⁺² only ten computers_nsubj² in the school ,`


### `obl:npmod`
This relation is used when a noun phrase is used as an adverbial modifier. This relation is often realized in:
(i) measure phrases:
- `that document is ten years_NNS_obl:npmod old_JJ_head
- `My sailing days ended many years_obl:npmod ago_RB_head
- `The board is six feet_NN_obl:npmod long_JJ_head`
- Years ago?
(ii) noun phrases acting adverbially, modifying noun phrases or adjectives:

- `it was a little bit_NN_obl:npmod hard_JJ_head to understand`

- `I can only sing_VB_head a little bit_NN_obl:npmod

- `The actual vote was a little_obl:npmod confusing_head`

(iii) Noun phrases as frequency descriptors:

- `Growing up, we went to the beach once_RB_head a year_obl:npmod`

- `I am hiring them to come twice_head a week_obl:npmod`

### `obl:npmod` or `obl:tmod`

Determining whether a phrase is `obl:npmod` or `obl:tmod` can be difficult, as both oblique sub-types can be phrases modifying something with respect to time. The key to distinguishing between the two is determining the purpose behind the phrase. `obl:tmod` phrases are generally used to establish a frame of reference for a verb phrase:

- `I flew_head here last night_obl:tmod`

- `last weekend_obl:tmod , I went_head out on the town`

- `I talked_head this morning_obl:tmod with Tom and he agreed to pay up front`

`obl:npmod` relations, when relaying some sort of temporal sense, often is used as a frequency adverbial:

- `I typically cook dinner twice_RB_head a week_NN_obl:npmod`

Phrases that contain ‘ago’ are tagged as `obl:npmod` as the noun phrase is considered to modify the adverb ‘ago’:

- `I graduated from college a few years_NNS_obl:npmod ago_RB_head`
^note that in the above example, there is a `advmod` relation from ‘graduated’ (head) to ‘ago’ (dependent), as is typical in these types of constructions

### `obl:npmod` vs. `nmod:npmod`
In the uncommon situation where `obl:npmod` is used to describe the
frequency of a recurring event or state, and both the head and the
dependent of the `obl:npmod` relationship are nouns, then the
`nmod:npmod` tag is used instead.
- `Yes she is having physical therapy 3 times_NN_head a
week_NN_nmod:npmod .`

### `punct`

Punctuation is, unfortunately, a slightly tedious element of dependency annotation. Different projects have adhered to different guidelines and processes for annotating punctuation. This means that the corpuses are tagged rather inconsistently when it comes to punctuation, meaning that they likely shouldn’t be used as a guide. Therefore, this section, which is based on the UD version 2, will act as our guide for tagging punctuation.

1) Sentence level punctuation (periods, question marks, exclamation marks etc.)

Sentence level punctuation is attached to the root of the sentence.

- `Go_root home !_punct`

- `The clown was exhausted_root(head¹), because he was juggling three pins ._punct¹ `

2) Clause & phrase level punctuation (commas, quotations, parentheses, occasionally hyphens etc. )

Below are four rules, extrapolated from the UD guidelines page, that are intended to be clear and directional.

(i) Punctuation preceding or following a dependent clause or phrase is attached to the head of that clause (subordinate clauses like relative clauses, adverbial clauses, parataxis, obl, npmods etc.).

- `The woman ,_punct who finished_head the race first ,_punct began to drink water . `

- `Because some kid threw_head a rock at it ,_punct the window shattered . `

- `The other day_head ,_punct I completed the residency application .`

When there are sequential dependent clauses/phrases  (at the same syntactic level), then the following clause takes precedence over the comma separating the two clauses:

- `but ,_punct¹ you know_head¹ ,_punct² you know_head² ,_punct² I went to school .`
- `The other day ,_punct¹ in the DMV_head¹ ,_punct¹ I completed the residency application.`

(ii) Punctuation separating coordinated units attaches to the following conjunct, in accordance with rule (i).

- `I know you must be going nuts with all the events ,_punct so I have not called_head .`
- `I love eating out ,_punct but ,_punct I hate_head spending money .
- `Food like the stuff they eat in Spanish countries like tacos ,_punct¹ beans_head¹ ,_punct² rice_head² ,_punct³ pork_head³ ,_punct⁴ steak_head⁴ ,_punct⁵ ect_head⁵ .`

(iii) Within the relevant clause or phrase, punctuation is attached to the highest syntactic unit (the head) of that clause or phrase.


(iv) Paired punctuation (quotation, parentheses) is attached to the same unit.

- `My favorite film is “_punct The Shining_head ”_punct
- She told me “_punct You did_head a wonderful job yesterday! ”_punct



3) Word level punctuation (word connecting hyphens )

Hyphens, or dashes, connecting two or more words are attached to the higher level (dominant) unit. The dominant unit in these cases is the word following the hyphen.

- ` What do you think of Google’s search -_punct engine_head`

- `Soon it will contain a full -_punct fledged_head operating system`

- `When you have a chance, can you send me an e -_punct mail_head ?`

### `punct` special cases

`,` commas around cc, discourse, and advmods

Discourse, ccs, and advmods only govern punctuation at last resort. Rather, the punctuation that often appears either preceding or proceeding these tags is a dependent of the same unit that governs the cc, discourse, or advmod tag.

- `I love eating out ,_punct but ,_punct I hate_head spending money .
- `fine_discourse ,_punct I’ll do_head it . `
- `I will ,_punct of course ,_punct drive_head you to the airport tomorrow!`

` : `

Colons are treated slightly differently than other clause-level punctuation. Colons are governed by the higher level clause, NOT the dependent clause.

- `AKA may refer_head to :_punct “Also known as” .`

- There is only one thing_head¹ to wear on your feet in summer :_punct¹ comfy sandals . `

### `reparandum`
A `reparandum` dependent is a disfluency which is overridden by a repair. The repair is the head of the `reparandum` dependent.

Overridden disfluencies occur when correcting an utterance:
- `He was the person , he and his wife Jan , introduced_reparandum -- reintroduced_head me and Laura in his backyard in July of 1977 .`

or repeating an utterance:
- `put the heater on the snake he will love it and the_reparandum the_head next day you will have dinner`

### `xcomp`
External complements `xcomp` are given when a clause has no overt subject AND the implied subject is the same as the head clause (see `ccomp` or `xcomp`).

In most sentences, an `xcomp` dependent has an implied subject and is a `VB` or `JJ` which has a head that is a type of `VB` or `JJ`.

`VB` is often `xcomp` when firstly preceded by an infinite `TO`, which is preceded by a type of head `VB`.
- `I really enjoyed_VBD_head to_TO serve_VB_xcomp the drinks to the pop-stars .`

`VBG` is often an `xcomp` when the subject is implied from the head (which is a type of `VB`).
- `Also, I prefer_VBP_head sleeping_VBG_xcomp in a tent than in a long cabin because it is easier to clean .`

`JJ` can be an `xcomp` when it modifies the action of the head. This only happens when the head is a type of `VB`. This can happen in imperative contexts.
- `I am writing you because I felt_VBD_head dissapointed_JJ_xcomp after seeing the musical show “ Over the Rainbow “ .`

Notice that `xcomp` can happen in imperative contexts as both a `JJ` and/or a type of `VB`.
- `Let_VB_head me make_VB_xcomp it clear , you blew my time and money .`
- `Let me make_VB_head it clear_JJ_xcomp , you blew my time and money .`

## Clarifications and special cases (particular words)

### Copular `be`
In most sentences, the main verb of the first independent clause in a sentence is the "Root" of the sentence. In the example `The hungry person ate the pizza`, the syntactic head of `ate` is the "root" of the sentence (which isn't represented aside from the `root` tag.)

In constructions with copular be (e.g., `She is a professor.`), however, the `root` is the predicate (in this case, the nominal complement `professor`). The word `professor` has three dependents `She` via an `nsubj` relationship, `is` via a `cop` relationship, and `a` via a `det` relationship.

In copular constructions with clausal predicates, however, as in `The important thing is to keep calm`, the "normal" conventions are used (`is` is the `root`)

### `so`
The word `so` will most often be in an `advmod` relationship:
- when its head is an adjective as in `so_RB <--advmod-- glad_JJ`
- when it could be substituted for `therefore` as in `I am keen on photography, so_RB I would love_VB to...`
- when it occurs at the beginning of a sentence as in `So, my son_RB loves_VBZ yakiniku because he is young` (sidenote: we may need to re-tag the POS for so in these cases)
