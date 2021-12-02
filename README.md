# Quenya-SMT
A Quenya-English statistical machine translator trained on the parallel corpora : both the new testament and the old testament.(link: https://folk.uib.no/hnohf/nqnt.htm)

# Method
same as working with other languages with Moses, a more specific demonstration is included in the Code.ipynb file.

# Result
Evaluation result using bleu
BLEU = 5.31, 33.6/9.5/3.1/0.8 (BP=1.000, ratio=1.339, hyp_len=1667, ref_len=1245)

The result of the translator is not ideal, it could still be improved.(implementing the same method on 2 high-resource languages easily yield BLUE result around 20)
The most important reason should be the lack of a large corpus: the current data I worked on has only 914 sentences (although almost all of them are quite long.), more importantly, because all of the datas are Quenya translation of the bible, the vocabulary of the langaueg model is very limited. Not only that it doesn't contain vocabularies associated with mordernity, but there is also a lack of common everyday use vocabulary.

# Example translated sentence
input: "There is no such a thing as god."

output: "Lá ea taite nat ve eru."

# Phrase Table
Below is part of the English-Quenya phrase-table
! 12 but when ||| ! 12 mal íre ||| 1 0.472195 1 0.782111 ||| 0-0 1-1 2-2 3-3 ||| 1 1 1 ||| |||
! 12 but ||| ! 12 mal ||| 1 0.472195 1 0.782111 ||| 0-0 1-1 2-2 ||| 1 1 1 ||| |||
! 12 do not let anyone despise ||| ! 12 áva lave aiquenen nattire ||| 1 0.472195 1 0.782111 ||| 0-0 1-1 2-2 3-2 4-3 5-4 6-5 ||| 1 1 1 ||| |||
! 12 do not let anyone ||| ! 12 áva lave aiquenen ||| 1 0.472195 1 0.782111 ||| 0-0 1-1 2-2 3-2 4-3 5-4 ||| 1 1 1 ||| |||
! 12 do not let ||| ! 12 áva lave ||| 1 0.472195 1 0.782111 ||| 0-0 1-1 2-2 3-2 4-3 ||| 1 1 1 ||| |||
! 12 do not ||| ! 12 áva ||| 1 0.472195 1 0.782111 ||| 0-0 1-1 2-2 3-2 ||| 1 1 1 ||| |||
! 12 for the eyes of the ||| ! 12 an i héruo hendu ||| 0.333333 1.56462e-10 1 0.782111 ||| 0-0 1-1 2-2 3-3 4-5 ||| 3 1 1 ||| |||
! 12 for the eyes of ||| ! 12 an i héruo hendu ||| 0.333333 6.65795e-06 1 0.782111 ||| 0-0 1-1 2-2 3-3 4-5 ||| 3 1 1 ||| |||
! 12 for the eyes ||| ! 12 an i héruo hendu ||| 0.333333 0.472195 1 0.782111 ||| 0-0 1-1 2-2 3-3 4-5 ||| 3 1 1 ||| |||
! 12 for the ||| ! 12 an i héruo ||| 1 0.472195 0.5 0.782111 ||| 0-0 1-1 2-2 3-3 ||| 1 2 1 ||| |||
! 12 for the ||| ! 12 an i ||| 1 0.472195 0.5 0.782111 ||| 0-0 1-1 2-2 3-3 ||| 1 2 1 ||| |||
! 12 for ||| ! 12 an ||| 1 0.472195 1 0.782111 ||| 0-0 1-1 2-2 ||| 1 1 1 ||| |||
! 12 furthermore , may the lord ||| ! 12 ente , nai i heru ||| 1 0.381859 1 0.644785 ||| 0-0 1-1 2-2 3-3 4-4 5-5 6-6 ||| 1 1 1 ||| |||
! 12 furthermore , may the ||| ! 12 ente , nai i ||| 1 0.381859 1 0.644785 ||| 0-0 1-1 2-2 3-3 4-4 5-5 ||| 1 1 1 ||| |||
! 12 furthermore , may ||| ! 12 ente , nai ||| 1 0.381859 1 0.644785 ||| 0-0 1-1 2-2 3-3 4-4 ||| 1 1 1 ||| |||
! 12 furthermore , ||| ! 12 ente , ||| 1 0.381859 1 0.644785 ||| 0-0 1-1 2-2 3-3 ||| 1 1 1 ||| |||
! 12 furthermore ||| ! 12 ente ||| 1 0.472195 1 0.782111 ||| 0-0 1-1 2-2 ||| 1 1 1 ||| |||
! 12 you are not in a ||| ! 12 elde uar mi ||| 0.5 0.0221673 1 0.782111 ||| 0-0 1-1 2-2 3-3 4-3 5-4 ||| 2 1 1 ||| |||
! 12 you are not in ||| ! 12 elde uar mi ||| 0.5 0.472195 1 0.782111 ||| 0-0 1-1 2-2 3-3 4-3 5-4 ||| 2 1 1 ||| |||
! 12 you are not ||| ! 12 elde uar ||| 1 0.472195 1 0.782111 ||| 0-0 1-1 2-2 3-3 4-3 ||| 1 1 1 ||| |||
! 12 you ||| ! 12 elde ||| 1 0.472195 1 0.782111 ||| 0-0 1-1 2-2 ||| 1 1 1 ||| |||
