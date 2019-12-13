# lung_single_cell_2019


**Prerequisites:**  
[Cell Ranger 3.1](https://support.10xgenomics.com/single-cell-gene-expression/software/downloads/latest)  
[Loupe Cell Browser 3.1](https://support.10xgenomics.com/single-cell-gene-expression/software/downloads/latest)  
[Pre-made mouse genome reference 3.0](https://support.10xgenomics.com/single-cell-gene-expression/software/downloads/latest)  
[Seurat R package 3.0](https://satijalab.org/seurat/v3.0)  

Experimental design: two samples (cells from mouse lungs)    
Sample 1: hypoxia  
Sample 2: hypoxia treated with exosomes
Notes: each sample is a pool of 3 lungs from pups (male/female identity was not determined before pooling and sequencing)  


Pre-process data with Cell Ranger  
```bash 
#process hyperoxia sample
cellranger count --id=hyperoxia --transcriptome=./cellranger-3.1.0/reference/mm10_v3.0/ --fastqs=./scell/Hyperoxia/
#process hyperoxia_treated_with_exosomes sample
cellranger count --id=hyperoxia_treated --transcriptome=./cellranger-3.1.0/reference/mm10_v3.0/ --fastqs=./scell/Hyperoxia_plus_Exosomes/
```



