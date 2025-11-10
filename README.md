# Files

* **AtLaS\_ARCHERy1dev\_BOS4.csv** (ARCHER dev subset): each row is one summary identified by `doc`,`id`. We compute **pairwise semantic similarity** among **7 texts** (source + 4 references + 2 MT systems(**1_primary** and **2_secondary**)) → **21 comparisons**.
* **AtLaS\_ARCHERy1test\_BOS4.csv** (ARCHER test): each row is one summary (`doc`,`id`) with source and **3 MT outputs**(**1_primary**, **2_secondary** and **3_secondary**); pairwise semantic similarity across available items.
* **mean\_BOS4\_AtLaS\_ARCHERy1dev.png**: Heatmap of mean BOS4 similarity computed from `AtLaS_ARCHERy1dev_BOS4.csv`.

# Method

We segment each summary into EDUs or sentences, embed the segments, and model the summary as a weighted probability measure. **BOS4** compares two summaries via the Wasserstein distance between these measures; we report a monotonic transform so larger BOS4 means greater semantic similarity. Unlike cosine-based baselines (single pooled embedding or greedy segment matching), which miss meaning spread through partial clause reuse and varied phrasings, BOS4 emphasizes semantics and is more robust to non-semantic surface variation.

# Analysis Heatmap

Cross-lingual pairs score lower than same-language pairs. The four references form a tight cluster suggesting very similar paraphrases. Both MT outputs lie close to the reference cluster, capturing the core semantics and appearing comparable—no clear winner.

# Contact

Soulaymane Loukili — [soulaymane.loukili@bsc.es](mailto:soulaymane.loukili@bsc.es)
Cedric Bhihe — [cedric.bhihe@bsc.es](mailto:cedric.bhihe@bsc.es)


# License

This work is licensed under the Creative Commons Attribution–NonCommercial 4.0 International (CC BY-NC 4.0) license. You are free to share and adapt for non-commercial purposes with appropriate attribution. See `LICENSE` for the full legal text, or https://creativecommons.org/licenses/by-nc/4.0/ for a human-readable summary.

Copyright © 2025 Soulaymane Loukili and Cédric Bhihe.

