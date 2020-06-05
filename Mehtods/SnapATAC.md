# SnapATAC

---

## Steps in the analysis

---

1. SnapATAC segment the genomes into fixed-size bins (windows) and count features within each bin. ( reads overlapping bins are counted )

2. Binarization of read counts is used. Binarization is advantageous in alleviating challenges arising from sequencing depth or PCR amplification artifacts

3. convert the binary count matrix into a cell-pairwise Jaccard index similarity matrix

4. SnapATAC perform a read coverage bias correction to account for the influence of sample depth

5. SnapATAC uses a regression-based method to mitigate the coverage difference between cells.

6. PCA is the most commonly used method