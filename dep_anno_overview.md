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


| Universal Dependencies | Description | Example | Notes | Notes |
|---------------------------------------------------------------------------|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [acl](https://universaldependencies.org/u/dep/acl.html) | clausal modifier of noun | First of all , I was really furious of watching a show_**head** starring_**acl** by a different actor , instead of Danny Brook . | The main verb in the modifying clause will take the "acl" annotation | The main verb in the modifying clause will take the "acl" annotation |
| [acl:relcl](https://universaldependencies.org/u/dep/acl-relcl.html) | relative clause modifier | There is something_**head** I like_**acl:relcl** to know from you . | The main verb in the relative clause will take the "acl:relcl" annotation | The main verb in the relative clause will take the "acl:relcl" annotation |
| [advcl](https://universaldependencies.org/u/dep/advcl.html) | adverbial clause modifier | I ask_**head** you for returning_**advcl** my money back . | The main verb in the adverbial clause will take the "acl:relcl" annotation | The main verb in the adverbial clause will take the "acl:relcl" annotation |
| [advmod](https://universaldependencies.org/u/dep/advmod.html) | adverbial modifier | For instance a lot of children nowadays_**advmod** replace_**head** their real life with the virtual world , which computers create . | | |
| [amod](https://universaldependencies.org/u/dep/amod.html) | adjectival modifier | It was about fourty five minutes later than original_**amod** starting_**amod** time_**head** | There are 2 dependencies in this example | There are 2 dependencies in this example |
| [appos](https://universaldependencies.org/u/dep/appos.html) | appositional modifier | It was Katha_**head** , a girl_**appos** who had the same problems like Pat . | | |
| [aux](https://universaldependencies.org/u/dep/aux_.html) | auxiliary | You have_**aux** also written_**head** in your advertisement that it would_**aux** started_**head** at half past seven but it started at 20:15 ! | There are 2 dependencies in this example | There are 2 dependencies in this example |
| [aux:pass](https://universaldependencies.org/u/dep/aux-pass.html) | passive auxiliary | If he had told everybody, J would have been_**aux:pass** blamed_**head** by whole school . | | |
| [case](https://universaldependencies.org/u/dep/case.html) | case marking | If she was not followed by_**case** journalists_**head** , she would n't die . | | |
| [cc](https://universaldependencies.org/u/dep/cc.html) | coordinating conjunction | And_**cc** the reason I choose painting is_**head** it 's being very exciting to me , | | |
| [cc:preconj](https://universaldependencies.org/u/dep/cc-preconj.html) | preconjunct | In conclusion , there are both_**cc:preconj** advantages_**head** and disadvantages of covering celebrities . | | |
| [ccomp](https://universaldependencies.org/u/dep/ccomp.html) | clausal complement | You ca n't imagine_**head** how funny_**ccomp** it was ! | | |
| [compound](https://universaldependencies.org/u/dep/compound.html) | compound | would you check the weather_**compound** forecast_**head** for me , please ? | | |
| [compound:prt](https://universaldependencies.org/u/dep/compound-prt.html) | phrasal verb particle | They make their life style much easy more fast because they need to catch_**head** up_**compound:prt** with the other people . | | |
| [conj](https://universaldependencies.org/u/dep/conj.html) | conjunct | I have knowladge about navigation_**head** , engine_**conj** , ropes_**conj** and knots_**conj** and sails_**conj** as well . | There are 4 dependencies in this example | There are 4 dependencies in this example |
| [cop](https://universaldependencies.org/u/dep/cop.html) | copula | Unfortunatly , Pat was_**cop** n't very good_**head** at keeping secrets . | | |
| [csubj](https://universaldependencies.org/u/dep/csubj.html) | clausal subject | I really think that living_**csubj** will be_**head** like living in the moon , very exciting . | | |
| [csubj:pass](https://universaldependencies.org/u/dep/csubj-pass.html) | clausal passive subject | In the advertisement , it was told_**head** that Danny Brook was starring_**csubj:pass** , but in place of him there was a different actor and he was really dissapointing . | | |
| [dep](https://universaldependencies.org/u/dep/dep.html) | unspecified dependency | MOON LANDING HOAX_**head** : CHURCH = TECHNOLOGY_**dep** & GOVERNMENT - Shuttle Carried on Aircraft model | Example from EWT corpus, limited examples | Example from EWT corpus, limited examples |
| [det](https://universaldependencies.org/u/dep/det.html) | determiner | I would rather be accommodated in a tent because I already have the_**det** necessary material_**head** for camping . | | |
| [det:predet](https://universaldependencies.org/en/dep/det-predet.html) | predeterminer | But sometimes I have to forget my opinion and spent all_**predet** the day_**head** looking for my mother in a huge department-store. | | |
| [discourse](https://universaldependencies.org/u/dep/discourse.html) | discourse element | I would like_**head** to travel on July , please_**discourse** , because that when I am in vacation . | | |
| [dislocated](https://universaldependencies.org/u/dep/dislocated.html) | dislocated elements | steel_**dislocated** or iron , which use for our building , it_**head** can make it stronger and easy to destroy . | Limited examples in corpra | Limited examples in corpra |
| [expl](https://universaldependencies.org/u/dep/expl.html) | expletive | In these gallaries there_**expl** are_**head** Historical paintings , antique furnitures which Chiang used . | | |
| [fixed](https://universaldependencies.org/u/dep/fixed.html) | fixed multiword expression | Then , we should film the English class so_**head** as_**fixed** to_**fixed** show who makes the film . | There are 2 dependencies in this example | There are 2 dependencies in this example |
| [flat](https://universaldependencies.org/u/dep/flat.html) | flat multiword expression | After concert I left with Ricky_**head** Martin_**flat** . | | |
| [flat:foreign](https://universaldependencies.org/u/dep/flat-foreign.html) | foreign words | Lopez 's 1561 book "Libro_**head** de_**flat:foreign** la_**flat:foreign** invencion_**flat:foreign** liberal_**flat:foreign** y_**flat:foreign** arte_**flat:foreign** del_**flat:foreign** Juego_**flat:foreign** del_**flat:foreign** Acedraz_**flat:foreign** " became THE classic on Chess openings , including the one that bears his name . | Example from EWT corpus, only example in corpus, there are 10 dependencies in this example | Example from EWT corpus, only example in corpus, there are 10 dependencies in this example |
| [goeswith](https://universaldependencies.org/u/dep/goeswith.html) | goes with | All my class_**head** mates_**goeswith** are looking forward to go to London . | | |
| [iobj](https://universaldependencies.org/u/dep/iobj.html) | indirect object | I would like to explain_**head** you_**iobj** my experience because I want you to give my money back . | | |
| [list](https://universaldependencies.org/u/dep/list.html) | list | How many jeans_**head** , Pants_**list** , sweater_**list** ect._**list** do I have to take ? | There are 3 dependencies in this example | There are 3 dependencies in this example |
| [mark](https://universaldependencies.org/u/dep/mark.html) | marker | This is the fact that_**mark** shopping is not enjoyable_**head** . | | |
| [nmod](https://universaldependencies.org/u/dep/nmod.html) | nominal modifier | How is the home_**head** of the future_**nmod** will be ? | | |
| [nmod:poss](https://universaldependencies.org/u/dep/nmod-poss.html) | possessive nominal modifier | I will go to your_**nmod:poss** office_**head** this week . | | |
| [nmod:tmod](https://universaldependencies.org/u/dep/nmod-tmod.html) | temporal modifier | Her husband became a citizen_**head** of the US just the week_**nmod:tmod** before last . | Example from EWT corpus | Example from EWT corpus |
| [nsubj](https://universaldependencies.org/u/dep/nsubj.html) | nominal subject | I_**nsubj** will go_**head** to your office this week . | | |
| [nsubj:pass](https://universaldependencies.org/u/dep/nsubj-pass.html) | passive nominal subject | We will not use black clothes as we_**nsubj:pass** are used_**head** to do . | | |
| [nummod](https://universaldependencies.org/u/dep/nummod.html) | numeric modifier | I usually spend my time on playing computer about three_**nummod** hours_**head** a day . | | |
| [obj](https://universaldependencies.org/u/dep/obj.html) | object | Even we could make_**head** a trip_**obj** to Paris in the school holiday ! | | |
| [obl](https://universaldependencies.org/u/dep/obl.html) | oblique nominal | Thank_**head** you very much for you time_**obl** . | | |
| [obl:tmod](https://universaldependencies.org/u/dep/obl-tmod.html) | temporal modifier | I 'm so happy with the experience I lived_**head** last month_**obl:tmod** . | Only example in ESL corpus | Only example in ESL corpus |
| [orphan](https://universaldependencies.org/u/dep/orphan.html) | orphan | So in the last century our daily life changed dramandesly and we became lazy and our life_**head** unpersonal_**orphan** , fast and unromantic . | | |
| [parataxis](https://universaldependencies.org/u/dep/parataxis.html) | parataxis | They would be sinthetic clothes_**head** , I think_**parataxis** made of plastic or something similar . " | There are 2 dependencies in this example | There are 2 dependencies in this example |
| [punct](https://universaldependencies.org/u/dep/punct.html) | punctuation | The scene of Toyko is not beautiful_**head** ,_**punct** but you think that this city is a developing place ._**punct** | Limited examples in corpra | Limited examples in corpra |
| [reparandum](https://universaldependencies.org/u/dep/reparandum.html) | overridden disfluency | It was just unbelievably dissapointing because the reason_**head** I mean_**reparandum** main reason which made me to go was to see Danny Brook . | The root is the head of itself; tag in webanno by first holding shift, and then dragging an arrow from the root tag to itself. | The root is the head of itself; tag in webanno by first holding shift, and then dragging an arrow from the root tag to itself. |
| [root](https://universaldependencies.org/u/dep/root.html) | root | I could n't believe_**root** it but he gave me the contract ot fill it out . | Limited examples in corpra | Limited examples in corpra |
| [vocative](https://universaldependencies.org/u/dep/vocative.html) | vocative | Now Kim_**vocative** , I will finish_**head** my letter but I promise you to write again as soon as possible , maybe if I 've developed the photos of the concert and the stars and the …. | | |
| [xcomp](https://universaldependencies.org/u/dep/xcomp.html) | open clausal complement | Further because I like_**head** to live_**xcomp** in contact with the nature . | | |


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

### `discourse` or `parataxis`
Utterances such as `you know` and `I mean` can be a bit confusing to tag. Although they might seem like like discourse markers, the guidelines for the `discourse` tag [explicitly indicate](https://universaldependencies.org/u/dep/discourse.html) that instances such as `you know` are not counted as discourse markers. Even in cases where these (and related utterances) appear to be functioning as discourse markers, they should be tagged as instances of `parataxis`.
- `I mean_parataxis , at the time I was 28_head` (EWT search:  `[word = "mean" & (edge = "parataxis" | edge = "discourse")] > [word = "I"]`)
- `you know_parataxis, nature hates_head a void` (EWT search: `[word = "know" & (edge = "parataxis" | edge = "discourse")] > [word = "you"]`)

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

### `nmod` or `obl`
Making the distinction between whether a token takes an oblique (obl) or nominal modifier (nmod) dependency comes down to constituency. This distinction often is required when examining prepositional phrases. To make this distinction, one needs to determine the head of the prepositional phrase by asking the question: what is the prepositional phrase modifying?
If the PP is modifying a noun phrase, or argument that is functioning as a noun phrase (see ‘another_DET’ below), the head of *the PP is likely an* **nmod**. Note that these cases of nmod often immediately follow the noun phrase they’re modifying.

- `another_DET_head of your questions_NNS_nmod`

If the PP in question modifies a verb, adjective, or adverb it will likely be tagged as **obl**. Oblique phrases can also immediately follow a noun phrase, so the position/location of the phrase in the sentence isn’t a foolproof heuristic. That is, you can’t determine the dependency of the phrase just by its relative position.

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
