# PDplasticity
Repository of functions and data for the manuscript: Developmental history modulates adult olfactory behavioral preferences via regulation of chemoreceptor expression in C. elegans

Travis Kyani-Rogers, Alison Philbrook, Ian G. McLachlan, Steven W. Flavell, Michael P. O’Donnell and Piali Sengupta

Raw data are available in the /rawdata folder in this repository, organized by figure. Analyses and figure generation were performed in R and PRISM. Photomask designs for the dauer olfactory chip are available in the /supplementaryfiles folder.

The package needed to perform calcium imaging analyses on raw data files can be installed in R using devtools::install_github("SenguptaLab/HEXplasticity"). Depedency functions are located in the analysis R packages https://github.com/SenguptaLab/MF.matR.git

Raw RNA-Seq reads were quality checked, adapter trimmed, and aligned to the C. elegans genome using STAR ALIGNER (https://github.com/alexdobin/STAR). Principal component analyses were performed on the normalized read counts of the 10,000 most variable genes across all samples. Differential expression analysis was performed using DESeq2 with lfc shrinkage on with normal modeling. Differential expression was determined with a significance cut-off of 0.05 (adjusted p-value; Wald test with Benjamini-Hochberg corrections) and the indicated Log2 fold change cut off of either -1.5 and 1.5 or -2 and  2. AWA enrichment analysis was performed using the web-based Tissue Enrichment Analysis tool with default parameters (https://www.wormbase.org/tools/enrichment/tea/tea.cgi) (Angeles-Albores et al., 2016).
