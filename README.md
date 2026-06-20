Overview

This project performs a comprehensive single-cell RNA sequencing (scRNA-seq) analysis of the publicly available GSE241385 Long COVID Brain Fog dataset. The workflow includes data preprocessing, quality control, dimensionality reduction, clustering, cell-type annotation, visualization, and Gene Ontology (GO) enrichment analysis.

The objective is to identify cellular heterogeneity and biological pathways associated with Long COVID and brain fog pathology using transcriptomic profiling at single-cell resolution.

Dataset

Dataset: GSE241385

Source: NCBI GEO Database

Study Focus: Long COVID-associated neurological symptoms (Brain Fog)

Technology: Single-cell RNA Sequencing (scRNA-seq)

Workflow
1. Data Loading
Import scRNA-seq dataset
Read expression matrices
Create AnnData objects
2. Preprocessing
Quality control filtering
Gene filtering
Cell filtering
Normalization
Log transformation
3. Feature Selection
Identification of Highly Variable Genes (HVGs)
4. Dimensionality Reduction
Principal Component Analysis (PCA)
UMAP visualization
5. Clustering
Neighborhood graph construction
Leiden clustering
Cluster identification
6. Cell-Type Annotation

Cell populations identified include:

Monocytes
T Cells
B Cells
NK Cells
Dendritic Cells
Other immune cell populations
7. Visualization

Generated figures include:

UMAP Cell Type Visualization
Cell Type Distribution Plot
Marker Gene Dot Plot
GO Enrichment Bar Plot
8. Functional Enrichment Analysis

Gene Ontology (GO) enrichment analysis was performed on Monocyte marker genes using Enrichr.

Top enriched biological processes include:

Antigen Processing and Presentation
Immunoglobulin-Mediated Immune Response
Positive Regulation of Lymphocyte Activation
Immune System Activation
Adaptive Immune Response

These findings suggest significant immune dysregulation in Long COVID-associated monocyte populations.

Project Structure
scRNA_project/
│
├── Data/
│   ├── Raw/
│   └── Processed/
│       ├── GSE241385_processed.h5ad
│       ├── GSE241385_clustered.h5ad
│       └── GSE241385_annotated.h5ad
│
├── Notebook/
│   ├── 01_Data_Loading.ipynb
│   └── 01_Load_and_Merge_Data.ipynb
│
├── Figures/
│   ├── celltype_counts_FIXED.png
│   ├── GO_Monocyte_Barplot_FIXED.png
│   ├── dotplot_ifn_dotplot.png
│   └── umap_celltypes.png
│
├── GO_Monocytes/
│   ├── Enrichr.human.enrichr.reports.pdf
│   └── Enrichr.human.enrichr.reports.txt
│
├── Results/
├── Reports/
└── README.md
Key Findings
Cell-Type Composition

The dataset revealed distinct immune cell populations with Monocytes representing an important cell cluster for downstream functional analysis.

GO Enrichment Results

Significantly enriched biological processes include:

GO Term	Adjusted P-value
Antigen Processing and Presentation	5.36 × 10⁻¹²
Immunoglobulin Mediated Immune Response	7.45 × 10⁻¹²
Positive Regulation of Lymphocyte Activation	7.45 × 10⁻¹²

These results indicate enhanced antigen presentation and immune activation pathways in monocyte populations.

Technologies Used
Python
Scanpy
Pandas
NumPy
Matplotlib
Seaborn
Enrichr
Jupyter Notebook
Output Files
Processed Datasets
GSE241385_processed.h5ad
GSE241385_clustered.h5ad
GSE241385_annotated.h5ad
Figures
Cell Type Distribution Plot
UMAP Visualization
Marker Gene Dot Plot
GO Enrichment Bar Plot
Functional Analysis
GO Enrichment Report (PDF)
GO Enrichment Report (TXT)
Future Work
Differential Gene Expression Analysis
Cell-Cell Communication Analysis
Pathway Enrichment Analysis
Integration with additional Long COVID datasets
Machine Learning-based cell state prediction
