# ScRNA-Seq
Single cell transcriptome sequencing (single cell RNA sequencing,
single cell RNA-seq, or scRNA seq) scRNA-seq measures the RNA molecules within each cell of a given sample.
This information provides a snapshot of the transcriptome (the genes that were being transcribed) when the cells were harvested
# Why scRNA-seq?
    It is used to determine transcriptional activity across thousands of cells to discover complex and rare cell populations and gain further insight
    into the dynamic nature of the transcriptome.
 # Analysis of scRNA-seq data using R:
 Seurat is an R package designed for QC, analysis, and exploration of single-cell RNA-seq data. Seurat aims to enable 
 users to identify and interpret sources of heterogeneity from single-cell transcriptomic measurements, and to integrate diverse types of single-cell data
 
# Dataset 
https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi
custom file GSM5974488_TNBC3.filtered_feature_bc_matrix.tar.gz
	   
       scRNAseq was performed on a total of thirteen samples: three human samples and ten mouse samples. The human tissue samples of triple negative breast tumors were provided by the NCI Cooperative Human Tissue Network. The murine breast tumor samples were harvested from mammary glands of two transgenic mouse models: a) MMTV-PyMT and b) C3(1)-Tag SV40. The pancreatic tumor came from the Ptf1⍺-CreERTM; LSL- KRASG12D strain. .
       
# Vln plot of TNBC data
![image](https://user-images.githubusercontent.com/110597928/198851662-cf6a1812-5586-4102-959c-bc37c6db31ef.png)
Find relationships between features: percent.mt,nCount_RNA
![image](https://user-images.githubusercontent.com/110597928/198851971-b9c1e5c5-d654-4c2a-b23d-0ab3949af93c.png)

![image](https://user-images.githubusercontent.com/110597928/198851948-fe9bb0a6-d59a-4577-975c-6e5a7bbe1fe8.png)


