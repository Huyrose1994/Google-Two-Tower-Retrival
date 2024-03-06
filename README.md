# Dataset
- Classic dataset
- Contains a set of ratings given to movies by a set of users
- Can be treated in 2 ways:
    - Interpreted as expressing which movies the users watched (and rated), which they did not
        - Implicit feedback - Users' watches tell us which things they prefer to see and which they'd rater not see
    - How much the users liked the movies they did watch
        - Explicit feedback - How much they liked by looking at the rating they have given


2 Stages:
    1. Retrieval Stage: Selecting an initial set of hundreds of cancidates from all possible
    candidates
        - Efficiently weed out all candidates that the user is not interested in
        - Has to be computationally efficient
    2. Ranking Stage: Take output from retrieval stage, fine tunes, select the best possible
    handful of recommendations

1. Retrieval Stage
- A query model computing the query representation (normally a fixed-dimensionality embedding vector) using query features
- A candidate model computing the candidate representation (an equally-sized vector) using the candidate features
    - Outputs of the 2 models are then multiplied together
    - Give a query-candidate affinity score

2. Ranking Stage