# Cambridge English Vocabulary

This repository contains opinionated vocabulary datasets based on Cambridge English test word lists. The repository currently contains datasets for Young Learners English (YLE) and A2 Key (formerly KET). PET and FCE datasets are not yet available.

The Cambridge lists are guides to expected vocabulary, not exhaustive lists of every word that may appear in an exam.

## Datasets

- [YLE vocabulary](yle-vocabulary-dataset.csv) uses the 2018 Pre A1 Starters, A1 Movers and A2 Flyers lists. Its level flags indicate first appearance.
- [A2 Key vocabulary](ket-vocabulary-dataset.csv) uses the August 2025 A2 Key and A2 Key for Schools list. It contains 1,741 case-sensitive entries and applies to both versions of the exam.

### YLE scope

The YLE dataset covers the 2018 Pre A1 Starters, A1 Movers and A2 Flyers word lists. Each row represents a vocabulary entry, and its level flags identify the earliest list in which it appears.

### YLE columns

All classification flags use `TRUE` or `FALSE`.

- `british` is the leading form; `american` gives the corresponding American form where one is provided. `irregular_plural` records an irregular plural where applicable.
- Exactly one of `starters`, `movers` and `flyers` is `TRUE` for each row, indicating the first list in which the entry appears.
- The grammatical flags identify parts of speech, and the topic flags identify relevant YLE topics.

### A2 Key scope

The A2 Key dataset covers the explicit alphabetical entries on pages 4–23 and the 25 Appendix 2 topic lists on pages 25–32. The source contains 1,728 alphabetical entries and 1,142 topic items, including repeated entries.

The open-ended word sets in Appendix 1 are not expanded. The topic-list shorthands `January - December` and `Monday - Sunday` are represented by the existing entries for the 19 days and months, which are tagged with the Time topic; no new headwords are generated from the ranges.

Entries preserve case and meaningful sense qualifiers. Explicit alternatives and some optional spellings are expanded; for example, `a/an` maps to separate `a` and `an` rows. Equivalent regional forms can instead share a row, such as `grey` and `gray`. Some topic plurals are represented by an existing singular form, such as `holidays` to `holiday`.

### A2 Key columns

All classification and membership flags use `TRUE` or `FALSE`.

- `british` is the case-sensitive leading form and row key; `american` gives the corresponding American form. Multiple alternatives use ` / `, and a symbol is paired with its written name, such as `pound / £`. Where no regional alternative is specified or editorially added, both columns repeat the source form; this does not establish that it is equally common in both varieties.
- `irregular_plural` contains editorially added plural forms, including unchanged plurals and useful alternatives such as `pence / pennies`. Selected spelling exceptions such as `potatoes` are also included; ordinary regular plurals are not listed systematically. Plurals are chosen for the meanings relevant to the list: `staff`, for example, refers to employees, not to a stick. These inflections are not limited to those in the Cambridge list. [Cambridge's noun-form guide](https://dictionary.cambridge.org/grammar/british-grammar/nouns-form) and WordNet were used when reviewing them.
- The grammatical flags share YLE's column names where applicable, with additional flags for abbreviations, auxiliary and modal verbs, phrasal verbs, prepositional phrases, countability and number. A modal, auxiliary or phrasal verb also sets `verb`; a prepositional phrase does not automatically set `preposition`.
- Grammatical flags combine source annotations for an entry, including annotations on regional alternatives and topic cells. They do not distinguish every sense.
- The 25 topic flags reflect Appendix 2, rather than the different YLE topic scheme.

The source's example sentences are not reproduced.

### A2 Key editorial choices

`supermarket / grocery store` is an editorial American alternative, and the topic-only `tourist information` is represented by `tourist information centre` / `tourist information center`. The source's `washing-up` noun is represented by the verb phrase `do the washing up` / `do the dishes`, also tagged with the Food and Drink topic; the separate `wash up` row remains a phrasal verb. `v / vs / versus` is also marked as an abbreviation.

The phone phrases share one entry: `give somebody a call` is used in both varieties, while [Cambridge describes `give somebody a ring` as mainly UK](https://dictionary.cambridge.org/dictionary/english/give-a-call). Other regional equivalents include forms already represented in the YLE dataset and source alternatives such as `aeroplane` / `airplane`. Distinct meanings are kept apart where needed: household `gas` is separate from `petrol` / `gas`, and `chemist (person)` is separate from `chemist (shop)` / `drugstore`. The topic-only household gas and chemist-person rows have an editorial noun flag, but no source POS annotation.

The source labels `action` as an adjective, as in `action movie`. The source also highlights additions, but this dataset does not assign an addition-year flag.

### A2 Key source fixes

- `chips`: American equivalent `biscuit` corrected to `French fries` (p. 7).
- `driver’s licence`: labelled British; corrected to American `driver’s license` (p. 9).
- `practice` (noun): American equivalent `practise` corrected to `practice` (p. 17).
- `training` (noun): the `transitive and intransitive` label is omitted because it applies to verbs (p. 21).
- Measurements topic: `kilometre/kilometre/km` corrected to `kilometre / kilometer / km` (p. 29).

## Sources

1. Cambridge Assessment English. (2018). *Pre A1 Starters, A1 Movers and A2 Flyers word lists: For exams from 2018*. <https://www.cambridgeenglish.org/images/149681-yle-flyers-word-list.pdf>
2. Cambridge Assessment English. (2025). *A2 Key and A2 Key for Schools Vocabulary List*. <https://www.cambridgeenglish.org/images/506886-a2-key-2020-vocabulary-list.pdf>

## License

The datasets and project documentation are available under [CC BY-SA 4.0](LICENSE.txt). The original Cambridge source PDFs carry UCLES copyright notices and are not relicensed by this repository.
