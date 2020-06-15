# SnapATAC

---

## Steps in the analysis

---

1. SnapATAC segment the genomes into fixed-size bins (windows) and count features within each bin. ( reads overlapping bins are counted )
2. Binarization of read counts is used. Binarization is advantageous in alleviating challenges arising from sequencing depth or PCR amplification artifacts
3. convert the binary count matrix into a cell-pairwise Jaccard index similarity matrix
4. SnapATAC perform a read coverage bias correction to account for the influence of sample depth
5. SnapATAC uses a regression-based method to mitigate the coverage difference between cells.
6. uses of Diffusion map for dimension reduction 

## Step in the Dimension Reduction 

---

**Appear in step 5 : runDiffusionMaps function**

1. Compute Jaccard similarity matrix : calcul d'un matrice de similarte de jaccard 

   ex :https://i2.wp.com/ewouddt.github.io/RcmdrPlugin.BiclustGUI/img/bibitworkflow_images/HeatmapJI_example.png?w=450

2. fit regression model : calculate the expected jaccard index matrix given the read depth && estimate the global scaling factor. 

3. normalize the data (divise toute la matrice par un facteur commun)

4. comput eigen decomposition