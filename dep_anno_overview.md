# Guidelines for Dependency Annotation
(this page is in progress)
We will be annotating our corpus for [Universal Dependency Relations (version 2)](https://universaldependencies.org/u/dep/index.html)

If you have questions while annotation, please follow this procedure:
- Check this page
- Check the [Dependency Guidelines](https://universaldependencies.org/u/dep/index.html)
- Check the [ESL Guidelines](http://people.csail.mit.edu/berzak/tle_guidelines/guidelines.pdf)
- Search the ESL corpus
- Search the English Web Treebank (EWT)

## Introduction to Dependency Relations
Dependency relations capture functional grammatical relationships between words in an utterance. Each linguistic item in an utterance has one (and only one) syntactic head, but may have multiple (or no) dependents. For example, in the sentence `The hungry person ate the pizza`, the word `person` has one syntactic head `ate`. `person` is connected to `head` via a nominal subject `nsubj` relationship. `person` also has two syntactic dependents: `hungry` (via an adjective modifier relationship `amod`) and `The` (via a determiner relationship `det`).

## UD Annotation Scheme
Here, each dependency relation is described and examples of each are also given.

**Note that the following `this style` is used for examples.**

| Universal Dependencies | Description                              | Example                                 |Notes|
|:-----------:|------------------------------------------|-----------------------------------------|-----|
| acl                      | clausal modifier of noun | I have a parakeet_**head** named_**acl** cookie                                                         | The dependent will be the main verb in the modifying clause |
| acl:relcl                | relative clause modifier | I saw the man_**head** you love_**acl:relcl**; I ate the cookie_**head** that you made_**acl:relcl**. | The dependent will be the main verb in the relative clause  |
## Clarifications and special cases

### Copular `be`
In most sentences, the main verb of the first independent clause in a sentence is the "Root" of the sentence. In the previous example `The hungry person ate the pizza`, the syntactic head of `ate` is the "root" of the sentence (which isn't represented aside from the `root` tag.)

In constructions with copular be (e.g., `She is a professor.`), however, the head of the nominal subject `She` is `root`. `professor` is a direct dependent of the nominal subject (via an `amod` relationship), and `be` is a dependent of the predicate `professor` via a copular `cop` dependency.

In copular constructions with clausal predicates, however, as in `The important thing is to keep calm`, the "normal" conventions are used (`is` is the `root`)
