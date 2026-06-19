# bachelor-thesis-LambdaMART-TAS-B
This repository contians code for a comparison between a BM25 + LambdaMART and a BM25 + TAS-B pipeline. The experiments are done on the MSMARCO passage dataset and are evaluated using TREC DL 2019 queries. Effectiveness is measured in NDCG@10, and a CodeCarbon tracker is implemented to measure latency (s), energy usage for CPU, GPU and RAM in W, and carbon emissions in gCO\_2 for indexing/embedding and ranking stages of every phase of the pipeline. 
# Repository structure
This repository consists of a notebook Thesis_LambdaMART.ipynb for the LambdaMART pipeline, BM25 retrieval + LambdaMART reranker and a notebook Thesis_TAS_B.ipynb for the TAS-B pipeline that reuses the BM25 from the Thesis_LambdaMART.ipynb notebook and then applies a TAS-B reranker.
# Running the notebooks
Before running the notebooks make sure you have a google drive directory that matches the project root, or change the project root name
# Running the LambdaMART notebook
Before running the LambdaMART notebook first use the following link to access the old commit: https://github.com/castorini/pyserini/blob/d4a4e390abad1c3185ff5121931454bfc383c2dd/docs/experiments-ltr-msmarco-passage-reranking.md
Clone the pyserini repository, and use git checkout to get back to this version of the pyserini github, before the code was removed.
Upload the entire cloned repository to your google drive, make sure this matches with your root structure

This notebook runs in a Python 3.8 and Java 11 environment with strict requirements in the install packages.
When running installs,  press control C when the cell gets stuck at installing spacy 3.8.2
# Running the TAS-B notebook
The TAS-B notebook runs in a Python 3.12 and Java 21 environment
Implements the same candidate passages from the BM25 retrieval and reranks it using TAS-B sebastian-hofstaetter/distilbert-dot-tas_b-b256-msmarco model.
