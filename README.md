# LangMap: An automatic approach to compute a cartography of various languages based on lexical similarity.

This notebook (LangMap.ipynb) uses pairwise normalized Levenshtein distance [[1]](#1) between vectors of words to estimate a measure of lexical similarity between two languages. Iterating over multiple languages computes a similarity matrix.

In order to chose a representative vector of words, we use 207 Swadesh lists [[2]](#2) for each languages. Due to the lack of a dedicated dataset, we created our own by translating the original English list into various languages via Google Translate (see Total_Google.csv).

From there on, using non-supervised learning clustering algorithm, such as DBSCAN [[3]](#3), we can cluster languages together based on pre-computed similarities.

Finally, we create a 2D projection, using Multi-Dimensional Scaling (MDS) [[4]](#4), to create a plot of our results.

On a side note, we also created a similarity graph from the similarity matrix, and used Louvain clustering [[5]](#5) to compute another partitioning of the languages (see LangMap-GraphApproach).


## References
<a id="1">[1]</a> 
Schulz, Klaus U.; Mihov, Stoyan (2002).
"Fast String Correction with Levenshtein-Automata".
International Journal of Document Analysis and Recognition.
5 (1): 67–85.
CiteSeerX 10.1.1.16.652.
doi:10.1007/s10032-002-0082-8.
S2CID 207046453.

<a id="2">[2]</a> 
David Kamholz, Jonathan Pool, Susan Colowick (2014).
"PanLex: Building a Resource for Panlingual Lexical Translation".

<a id="3">[3]</a> 
Ester, Martin; Kriegel, Hans-Peter; Sander, Jörg; Xu, Xiaowei (1996).
Simoudis, Evangelos; Han, Jiawei; Fayyad, Usama M. (eds.).
"A density-based algorithm for discovering clusters in large spatial databases with noise".
Proceedings of the Second International Conference on Knowledge Discovery and Data Mining (KDD-96)
AAAI Press. pp. 226–231. 

<a id="4">[4]</a> 
Borg, I.; Groenen, P. (2005).
"Modern Multidimensional Scaling: theory and applications (2nd ed.)".
New York: Springer-Verlag.
pp. 207–212.
ISBN 978-0-387-94845-4.

<a id="5">[5]</a> 
Blondel, Vincent D; Guillaume, Jean-Loup; Lambiotte, Renaud; Lefebvre, Etienne (9 October 2008).
"Fast unfolding of communities in large networks".
Journal of Statistical Mechanics: Theory and Experiment.
2008 (10): P10008.
arXiv:0803.0476.
Bibcode:2008JSMTE..10..008B.
doi:10.1088/1742-5468/2008/10/P10008.
