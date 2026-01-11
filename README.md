# RNAseq-Differential-Expression-R
RNA Expression by Abdullah Alvi
  ## Requirements
  
  The analysis is performed in **R (≥ 4.2)** using the following packages:
  
  - DESeq2  
- edgeR  
- ggplot2  
- pheatmap  
- matrixStats  

All packages are from Bioconductor or CRAN.

---
  
  ## Analysis Workflow
  
  ### 1. Quality Control
  The QC step evaluates raw count data by examining:
  - Library sizes (total reads per sample)
- Distribution of log-transformed gene counts

These checks help identify technical biases, sequencing depth issues, or problematic samples before downstream analysis.

---
  
  ### 2. Normalization
  Normalization is performed using two widely accepted RNA-seq methods:
  
  - **DESeq2 size factor normalization**
  - **edgeR TMM (Trimmed Mean of M-values)**
  
  Normalization corrects for library size and compositional differences, enabling accurate comparison of gene expression across samples.

---
  
  ### 3. Differential Expression Analysis
  Differentially expressed genes (DEGs) are identified independently using:
  - DESeq2
- edgeR

Significance thresholds:
  - Adjusted p-value < 0.05
- Absolute log2 fold change > 1

Genes passing these criteria are considered biologically significant and condition-associated.

---
  
  ## Visualization and Interpretation
  
  ### Volcano Plot
  The volcano plot displays:
  - Log2 fold change on the x-axis
- −log10 adjusted p-value on the y-axis

Upregulated genes appear on the right, downregulated genes on the left. Genes with higher statistical confidence appear higher on the plot.

---
  
  ### Heatmap
  The heatmap visualizes expression patterns of the top differentially expressed genes across samples. Hierarchical clustering highlights co-regulated genes and similarities between biological conditions.

---
  
  ### PCA Plot
  Principal Component Analysis (PCA) reduces data dimensionality and summarizes global expression patterns. Clear separation between conditions indicates strong biological signal and consistency among replicates.

---
  
  ## Biological Interpretation
  Consistent results across DESeq2 and edgeR strengthen confidence that observed expression changes are driven by the experimental condition rather than technical noise. This workflow mirrors best practices used in published RNA-seq studies.

---
  
  ## Reproducibility
  - Simulated data ensure the workflow runs identically on any system
- Fixed random seed (`set.seed()`) guarantees reproducible results
- Modular scripts allow independent or sequential execution

---
  
  ## Author
  **Abdullah**  
  Undergraduate Biotechnology Student  
Interest areas: RNA-seq analysis, computational biology, and applied bioinformatics

---
  
  ## License
  This project is released for academic and educational use.
