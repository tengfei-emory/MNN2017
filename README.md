# MNN

This folder contains R codes used to generate figures 1-5 in the manuscript "Correcting batch effects in single-cell RNA sequencing data by matching mutual nearest neighbours", as well as 1-6 supplementary figures.

1. To generate the simulation figure in the main text, first run the source file `simulateBatches.R`, then run the source file `plotCorrections.R` in the `Simulations/` folder.
This will also generate the simulation figure in the supplement involving batches with the same cell type composition.

2. To generate the haematopoietic data figures in the main text, first run the source file `preparedata.R`, then  run the source file `FourPlots_haem.R` in the Haematopoiesis folder.

3. Then, to generate the haematopoietic data figures in the supplement, run the source file `PCAs.R` in the Haematopoiesis folder.

4. First download gene expression data from the four public data sets (Gene X Cell matrices, meta data and highly variable gene lists) by running the bash script `DownloadData.sh`.  This will download a directory 'ftp2.cruk.cam.ac.uk', which contains two sub-directories; CELseq and Smartseq2.  These directories contain the data for the appropriate studies (denoted by GEO/ArrayExpress accession number detailed in the manuscript).

5. To generate any of the pancreas data sets results, you have to run the source file `preparedata.R` in the Pancreas folder first. You will need to create a directory called 'results', into which all figures and batch corrected data will be saved.

6. To correct the batch effects and generate t-SNE plots and the Silhouette boxplots for the pancreas data sets (Fig 4), run the source file `FourPlots_panc.R` in the Pancreas folder.

7. Then, to generate the pancreas PCA plots and the entropy of mixings boxplots in the supplement (Suppl. Fig.3), run the source file `entropyandPCAs.R` in the Pancrease folder.

8. To compare performance of MNN with locally variable batch effects versus a global batch effect settings (Suppl.Fig. 6), run the source file `local_global_batchvect.R` in the Pancrease folder.

9. Differential expression testing figures can be generated by running the R markdown document, `PancreasDE_analysis.Rmd` , contained in the PancreasDE directory.  The static version of the R notebook is also available as a html document that can be opened with any internet browser.

10. The sub-sampling differential expression analysis can be performed by running the script `pancreas_subsample_DE.R` in an open R session.  This script assumes the data are downloaded and the R markdown notebook `PancreadDE_analysis.Rmd` has been run.
