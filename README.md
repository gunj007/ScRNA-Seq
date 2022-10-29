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
	   
       scRNAseq was performed on a total of thirteen samples: three human samples and ten mouse samples. The human tissue samples of triple negative breast tumors were provided by the NCI Cooperative Human Tissue Network. The murine breast tumor samples were harvested from mammary glands of two transgenic mouse models:
       a) MMTV-PyMT and b) C3(1)-Tag SV40. The pancreatic tumor came from the Ptf1⍺-CreERTM; LSL- KRASG12D strain. .
       They performed scRNA-seq analysis of fibroblasts from murine and human TNBCs.
       
# Vln plot of TNBC data
Draws a violin plot of single cell data
![image](https://user-images.githubusercontent.com/110597928/198852180-65960d0d-bef8-4a29-818a-4b148d80fa59.png)

![image](https://user-images.githubusercontent.com/110597928/198851662-cf6a1812-5586-4102-959c-bc37c6db31ef.png)
Find relationships between features: percent.mt and nCount_RNA
![image](https://user-images.githubusercontent.com/110597928/198851971-b9c1e5c5-d654-4c2a-b23d-0ab3949af93c.png)
where,  0.95 correlations between x-axis and y-axis

# plot variable features with and without labels:
![image](https://user-images.githubusercontent.com/110597928/198852109-327efa18-c8eb-4cb6-a611-d42cfbe06e78.png)

# Dimheatmap
	
	Draws a heatmap focusing on a principal component. Both cells and genes are sorted by their principal component scores. Allows for nice visualization of sources of heterogeneity in the dataset.
![image](https://user-images.githubusercontent.com/110597928/198852208-0cd0bd2f-f855-4122-ae2f-fe1d4632bd5a.png)
The PCHeatmap function (renamed DimHeatmap in Seurat v3) can be used to help determine the number of principal components to use in downstream analysis, as well as to visualize the top genes contributing to each PC.

Both cells and genes are ordered by their PC scores, and by default the 1 genes with the highest and 2 genes with the lowest PC loadings are displayed for each PC.

In our case with PC1 and PC23,  PC1 and PC3 both strongly separate different populations of cells. For PC1 there is a smaller population with very strong separation, and PC3 the cells roughly same.

![image](https://user-images.githubusercontent.com/110597928/198852224-034ecfb1-342a-4148-a020-4a097d0305f1.png)
#Elbow starts appearing by pc3-10 . So it indicates that first 10 PCs are acceptable as majority of true signal is captured in the first 10 PCs .

# Dimplot of clusters using UMAP
Using UMAP method clusters of cells with features that are very similar to each other are created
![image](https://user-images.githubusercontent.com/110597928/198852565-821b2338-5328-4ded-8a05-933947948ce4.png)
#Assign markers to the clustered data
![image](https://user-images.githubusercontent.com/110597928/198852625-4c88761d-8d0a-485a-9cdb-0aa14a224680.png)

Concluding that the Cell type identification based on single-cell RNA sequencing involves partitioning the data into “clusters” of single cells.
Based on this , 2 clusters were created .Based on those clusters , GM26917 and GM42418 are highly expressed genes in TNBC's single-cell RNA data .






