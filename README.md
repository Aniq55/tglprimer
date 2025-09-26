# tglprimer
A Primer on Temporal Graph Learning: benchmarks &amp; datasets


# Temporal Graph Learning (2020–2025): Benchmarks, Code & Datasets

## 1) Regression (forecasting on temporal graphs)

| Model (Venue, Year)                                                                              | Code                                             | 3 common datasets they report on                                                  |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------ | --------------------------------------------------------------------------------- |
| **STG-NCDE: Graph Neural Controlled Differential Equations for Traffic Forecasting** (AAAI 2022) | GitHub: jeongwhanchoi/**STG-NCDE** ([AAAI][1])   | **PEMS04**, **METR-LA**, **PEMS-BAY** (plus others in paper) ([AAAI][1])          |
| **D2STGNN: Decoupled Dynamic Spatio-Temporal GNN** (VLDB 2022)                                   | GitHub: GestaltCogTeam/**D2STGNN** ([GitHub][2]) | **METR-LA**, **PEMS-BAY**, **PEMS04/PEMS08** ([arXiv][3])                         |
| **MTGNN: Connecting the Dots – Multivariate TS with GNNs** (KDD 2020)                            | GitHub: nnzhan/**MTGNN** ([GitHub][4])           | **Electricity**, **Traffic**, **Solar-Energy** (also Exchange-Rate) ([GitHub][5]) |

---

## 2) Classification (temporal node property prediction)

| Model (Venue, Year)                            | Code                                                   | 3 widely used datasets                                                                                                                              |
| ---------------------------------------------- | ------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| **TGN: Temporal Graph Networks** (ICML 2020)   | GitHub: twitter-research/**tgn** ([GitHub][6])         | **Wikipedia (tgbl-wiki)**, **Reddit (tgbl-comment)**, **MOOC/LastFM-style interaction data** (also used across TGB) ([Temporal Graph Benchmark][7]) |
| **TGAT: Temporal Graph Attention** (ICLR 2020) | TGAT reference implementations on GitHub ([GitHub][8]) | **Wikipedia**, **Reddit**, **MOOC** (temporal node/edge tasks) ([Temporal Graph Benchmark][7])                                                      |
| **GraphMixer** (ICLR 2023)                     | GitHub: **GraphMixer** (official) ([GitHub][9])        | **tgbl-wiki**, **tgbl-comment**, **tgbn-reddit / tgbn-trade** (TGB node & link property suites) ([Temporal Graph Benchmark][7])                     |

> Note: The **Temporal Graph Benchmark (TGB)** provides unified splits + evaluators for node/link property prediction; many recent papers report on **tgbl-wiki**, **tgbl-review**, **tgbl-comment**, **tgbl-coin**, and **tgbn-reddit / tgbn-trade**. ([Temporal Graph Benchmark][7])

---

## 3) Temporal Link Prediction

| Model (Venue, Year)                          | Code                                   | 3 classic/modern datasets                                                                                          |
| -------------------------------------------- | -------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **TGN: Temporal Graph Networks** (ICML 2020) | twitter-research/**tgn** ([GitHub][6]) | **Wikipedia**, **Reddit**, **tgbl-review**/ **tgbl-coin** (temporal link property) ([Temporal Graph Benchmark][7]) |
| **TGAT** (ICLR 2020)                         | TGAT reference repos ([GitHub][8])     | **Wikipedia**, **Reddit**, **MOOC** ([Temporal Graph Benchmark][7])                                                |
| **CAW: Causal Anonymous Walks** (ICLR 2021)  | snap-stanford/**CAW** ([GitHub][10])   | **Wikipedia**, **Reddit**, **LastFM** (temporal interactions) ([Computer Science][11])                             |

---

## 4) Temporal Graph Generation

| Model (Venue, Year)                                                                       | Code                                                          | 3 datasets (as reported/evaluated)                                                                                                                                 |
| ----------------------------------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **MTM: Motif Transition Model** (KDD 2023)                                                | erdemUB/**KDD23-MTM** ([arXiv][12])                           | **Reddit (reply graph)**, **Email/communication networks**, **UCI/CollegeMsg-style temporal graphs** (typical in their evaluation; see paper) ([sariyuce.com][13]) |
| **DG-Gen: Deep Probabilistic Framework for CTDGs** (arXiv 2024)                           | ryienh/**DGGen** ([arXiv][14])                                | **5 temporal datasets** incl. social/comm. networks (reported in paper) ([arXiv][15])                                                                              |
| **Neural Temporal Walks (as a generator baseline / structure maintainer)** (NeurIPS 2022) | KimMeen/**Neural-Temporal-Walks** ([NeurIPS Proceedings][16]) | **Wikipedia/Reddit-style interaction logs**, **temporal contact networks**, **LastFM** (continuous-time dynamics benchmarks) ([NeurIPS Proceedings][16])           |

---

## 5) (Dynamic) Graph Clustering

| Model (Venue, Year)                                                     | Code                                               | 3 datasets                                                                               |
| ----------------------------------------------------------------------- | -------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| **Interpretable Clustering on Dynamic Graphs with RNN-GCN** (AAAI 2021) | yh-yao/**InterpretableClustering** ([AAAI][17])    | **Reddit**, **DBLP (3/5/Extended variants)**, **Brain networks** ([GitHub][18])          |
| **Deep Temporal Graph Clustering (TGC)** (ICLR 2024 poster)             | (code linked from arXiv page) ([arXiv][19])        | **Multiple temporal graph benches** (see arXiv; reports broad experiments) ([arXiv][19]) |
| **Dynamic Community Detection via Adversarial Temporal GNN** (2022)     | (paper, code often in project pages) ([arXiv][20]) | **Brain networks** and related temporal community datasets ([arXiv][20])                 |

---

## 6) (Dynamic) Graph Compression / Summarization

| Model (Venue, Year)                                                                    | Code                                                                             | 3 datasets                                                                                                                                             |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **PnC: Partition-and-Code (lossless neural compression)** (NeurIPS 2021)               | gbouritsas/**PnC** ([NeurIPS Proceedings][21])                                   | **MUTAG**, **PROTEINS**, **ZINC** (plus IMDB-B/M; see repo “Datasets”) ([GitHub][22])                                                                  |
| **SLUGGER: Lossless Hierarchical Summarization** (ICDE 2022)                           | KyuhanLee/**slugger** (datasets linked) ([GitHub][23])                           | **Massive real graphs** provided via authors’ dataset link (e.g., web/social), **protein**, etc. (see repo “Datasets and Contributors”) ([GitHub][23]) |
| **Mayfly: Neural Data Structure for Graph Stream Summarization** (ICLR 2024 Spotlight) | (paper page; implementations referenced via authors) ([proceedings.iclr.cc][24]) | **Graph streams** from communication/transaction logs (as evaluated in paper) ([proceedings.iclr.cc][24])                                              |

---

### Notes & caveats

* Where a paper spans multiple tasks (e.g., **TGN/TGAT** support both node classification and link prediction), I placed them under the task they’re most used for and referenced datasets accordingly. ([memgraph.com][25])
* For **classification/link‐prediction** datasets, the **Temporal Graph Benchmark (TGB, NeurIPS 2023 & 2024)** is now the de-facto source of modern, large-scale temporal datasets and leaderboards (e.g., **tgbl-wiki**, **tgbl-review**, **tgbl-coin**, **tgbl-comment**, **tgbl-flight**, and node tasks **tgbn-trade/genre/reddit/token**). Consider using TGB when reproducing recent results. ([Temporal Graph Benchmark][7])

If you want, I can turn this into a small **repro template** (one script per task that downloads a dataset from TGB or traffic repos and runs a baseline) — just say the word and name your preferred frameworks (PyG/DGL).

[1]: https://cdn.aaai.org/ojs/20587/20587-13-24600-1-2-20220628.pdf?utm_source=chatgpt.com "Graph Neural Controlled Differential Equations for Traffic Forecasting"
[2]: https://github.com/GestaltCogTeam/D2STGNN?utm_source=chatgpt.com "Decoupled Dynamic Spatial-Temporal Graph Neural Network for Traffic ..."
[3]: https://arxiv.org/abs/2206.09112?utm_source=chatgpt.com "Decoupled Dynamic Spatial-Temporal Graph Neural Network for Traffic ..."
[4]: https://github.com/nnzhan/MTGNN?utm_source=chatgpt.com "GitHub - nnzhan/MTGNN"
[5]: https://github.com/nnzhan/MTGNN/blob/master/README.md?utm_source=chatgpt.com "MTGNN/README.md at master · nnzhan/MTGNN · GitHub"
[6]: https://github.com/twitter-research/tgn?utm_source=chatgpt.com "GitHub - twitter-research/tgn: TGN: Temporal Graph Networks"
[7]: https://tgb.complexdatalab.com/docs/linkprop/ "Dynamic Link Property Prediction | Temporal Graph Benchmark"
[8]: https://github.com/goyalkaraniit/TGAT-original?utm_source=chatgpt.com "GitHub - goyalkaraniit/TGAT-original"
[9]: https://github.com/CongWeilin/GraphMixer/blob/main/README.md?utm_source=chatgpt.com "GraphMixer/README.md at main · CongWeilin/GraphMixer · GitHub"
[10]: https://github.com/snap-stanford/CAW?utm_source=chatgpt.com "GitHub - snap-stanford/CAW"
[11]: https://cs.stanford.edu/people/jure/pubs/caw-iclr21.pdf?utm_source=chatgpt.com "INDUCTIVE REPRESENTATION LEARNING IN TEMPO RAL NETWORKS VIA CAUSAL ..."
[12]: https://arxiv.org/abs/2306.11190?utm_source=chatgpt.com "Using Motif Transitions for Temporal Graph Generation"
[13]: https://sariyuce.com/papers/sigkdd23.pdf?utm_source=chatgpt.com "Using Motif Transitions for Temporal Graph Generation"
[14]: https://arxiv.org/abs/2412.15582?utm_source=chatgpt.com "A Deep Probabilistic Framework for Continuous Time Dynamic Graph Generation"
[15]: https://arxiv.org/pdf/2412.15582?utm_source=chatgpt.com "A Deep Probabilistic Framework for Continuous Time Dynamic Graph Generation"
[16]: https://proceedings.neurips.cc/paper_files/paper/2022/hash/7dadc855cef7494d5d956a8d28add871-Abstract-Conference.html?utm_source=chatgpt.com "Neural Temporal Walks: Motif-Aware Representation Learning on ..."
[17]: https://cdn.aaai.org/ojs/16590/16590-13-20084-1-2-20210518.pdf?utm_source=chatgpt.com "Interpretable Clustering on Dynamic Graphs with Recurrent Graph Neural ..."
[18]: https://github.com/yh-yao/InterpretableClustering?utm_source=chatgpt.com "GitHub - yh-yao/InterpretableClustering"
[19]: https://arxiv.org/abs/2305.10738 "[2305.10738] Deep Temporal Graph Clustering"
[20]: https://arxiv.org/abs/2207.03580?utm_source=chatgpt.com "Dynamic Community Detection via Adversarial Temporal Graph ..."
[21]: https://proceedings.neurips.cc/paper/2021/file/9a4d6e8685bd057e4f68930bd7c8ecc0-Paper.pdf?utm_source=chatgpt.com "Partition and Code: learning how to compress graphs"
[22]: https://github.com/gbouritsas/PnC "GitHub - gbouritsas/PnC: Official repository for the paper \"Partition and Code: learning how to compress graphs\" (NeurIPS'21) https://arxiv.org/abs/2107.01952"
[23]: https://github.com/KyuhanLee/slugger "GitHub - KyuhanLee/slugger: SLUGGER: Lossless Hierarchical Summarization of Massive Graphs"
[24]: https://proceedings.iclr.cc/paper_files/paper/2024/hash/e7e506bc5a94768243083216fe51d98b-Abstract-Conference.html?utm_source=chatgpt.com "Mayfly: a Neural Data Structure for Graph Stream Summarization"
[25]: https://memgraph.com/docs/advanced-algorithms/available-algorithms/tgn?utm_source=chatgpt.com "temporal_graph_networks"
