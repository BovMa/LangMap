# LangMap: An automatic approach to compute a cartography of various languages based on lexical similarity.

This notebook (LangMap.ipynb) uses pairwise normalized Levenshtein between vector of words to estimate a measure of lexical similarity between two languages. Iterating over multiple languages computes a similarity matrix.

In order to chose a representative vector of words, we use 207 Swadesh lists for each languages. Due to the lack of a dedicated dataset, we created our own by translating the original English list into various languages via Google Translate (see Total_Google.csv).

From there on, using non-supervised learning clustering algorithm, such as DBSCAN, we can cluster languages together based on pre-computed similarities.

Finally, we create a 2D projection, using Multi-Dimensional Scaling (MDS), to create a plot of our results.

On a side note, we also created a similarity graph from the similarity matrix, and used Louvain clustering to compute another partitioning of the languages (see LangMap-GraphApproach).


