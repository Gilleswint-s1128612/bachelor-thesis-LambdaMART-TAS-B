# bachelor-thesis-LambdaMART-TAS-B
This repository contians code for a comparison between a BM25 + LambdaMART and a BM25 + TAS-B pipeline. The experiments are done on the MSMARCO passage dataset and are evaluated using TREC DL 2019 queries. Effectiveness is measured in NDCG@10, and a CodeCarbon tracker is implemented to measure latency (s), energy usage for CPU, GPU and RAM in W, and carbon emissions in gCO\_2. 

# Running the notebooks
Before running the notebooks make sure you have a google drive directory that matches the project root, or change the project root name
# Running the LambdaMART notebook
Before running the LambdaMART notebook first use the following link to access the old commit https://github.com/castorini/pyserini/blob/d4a4e390abad1c3185ff5121931454bfc383c2dd/docs/experiments-ltr-msmarco-passage-reranking.md
Clone the pyserini repository, and use git checkout to get back to this version of the pyserini github, before the code was removed.

Run all cells,  press control C when the cell gets stuck at installing spacy 3.8.2
