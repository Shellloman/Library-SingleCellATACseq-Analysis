# CisTopic

---

## Steps in the analysis

---

1. define regions based on peak calling from either a reference bulk  ATAC-seq profile or an aggregated single-cell ATAC-seq profile  ( reads overlapping bins are counted )

2. Binarization of read counts is used. Binarization is advantageous in alleviating challenges arising from sequencing depth or PCR amplification artifacts

3. cisTopic uses latent Dirichlet allocation (LDA) to generate two  distributions including topic-cell distribution and region-topic  distribution. Choosing the top topics based on the topic-cell distribution reduces the dimensionality