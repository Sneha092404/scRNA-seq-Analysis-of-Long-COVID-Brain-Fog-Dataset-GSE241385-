# Single-Cell RNA Sequencing Analysis of Long COVID Brain Fog Dataset (GSE241385)

## Overview

This project presents a comprehensive single-cell RNA sequencing (scRNA-seq) analysis of the publicly available GSE241385 Long COVID Brain Fog dataset. The workflow was developed using Python and Scanpy to investigate immune cell heterogeneity and biological pathways associated with Long COVID neurological symptoms.

The analysis includes data preprocessing, quality control, normalization, dimensionality reduction, clustering, cell-type annotation, visualization, and Gene Ontology (GO) enrichment analysis.

---

## Research Objective

Long COVID is associated with persistent neurological symptoms commonly referred to as "brain fog". Understanding the cellular and molecular mechanisms underlying these symptoms requires analysis at single-cell resolution.

The primary objectives of this project were:

* Perform quality control and preprocessing of scRNA-seq data.
* Identify distinct immune cell populations.
* Visualize cellular heterogeneity using dimensionality reduction techniques.
* Annotate cell types based on marker gene expression.
* Investigate immune-related biological processes through Gene Ontology enrichment analysis.

---

## Dataset Information

**Dataset ID:** GSE241385

**Source:** NCBI Gene Expression Omnibus (GEO)

**Data Type:** Single-cell RNA Sequencing (scRNA-seq)

**Biological Context:** Long COVID-associated neurological symptoms (Brain Fog)

---

## Analysis Workflow

### 1. Data Loading and Processing

* Imported scRNA-seq count matrices.
* Created AnnData objects using Scanpy.
* Merged and organized datasets for downstream analysis.

### 2. Quality Control

Quality control was performed to remove low-quality cells and genes.

Metrics evaluated:

* Number of genes detected per cell
* Total counts per cell
* Percentage of mitochondrial gene expression

Filtering steps:

* Removal of low-quality cells
* Removal of genes expressed in very few cells
* Mitochondrial content filtering

### 3. Data Normalization

* Library-size normalization
* Log transformation of expression values

### 4. Highly Variable Gene Selection

Highly Variable Genes (HVGs) were identified to capture the most informative biological variation in the dataset.

### 5. Dimensionality Reduction

Principal Component Analysis (PCA) was performed to reduce dimensionality.

Uniform Manifold Approximation and Projection (UMAP) was used for visualization of cellular populations.

### 6. Clustering Analysis

Leiden clustering was performed to identify transcriptionally distinct cellular populations.

### 7. Cell-Type Annotation

Clusters were annotated using known marker genes.

Identified cell populations include:

* Monocytes
* CD4 T Cells
* Activated T Cells
* Cytotoxic T Cells
* Activated Cytotoxic T Cells
* B Cells
* NK Cells
* Dendritic Cells
* Activated Immune Cells
* IFN-high Cells

### 8. Visualization

The following visualizations were generated:

* UMAP Cell Type Map
* Cell Type Distribution Plot
* Marker Gene Dot Plot
* GO Enrichment Bar Plot

### 9. Functional Enrichment Analysis

Gene Ontology (GO) enrichment analysis was performed using Enrichr on monocyte marker genes.

Significantly enriched biological processes included:

* Antigen Processing and Presentation
* Immunoglobulin-Mediated Immune Response
* Positive Regulation of Lymphocyte Activation
* Immune System Activation
* Adaptive Immune Response

These findings suggest enhanced immune activation and antigen presentation mechanisms within monocyte populations.

---

## Project Structure

scRNA_project/

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

│   ├── umap_celltypes.png

│   ├── celltype_counts_FIXED.png

│   ├── dotplot_ifn_dotplot.png

│   └── GO_Monocyte_Barplot_FIXED.png

│

├── GO_Monocytes/

│   ├── Enrichr.human.enrichr.reports.pdf

│   └── Enrichr.human.enrichr.reports.txt

│

├── Results/

├── Reports/

├── README.md

└── requirements.txt

---

## Key Findings

### Cell-Type Composition

The dataset revealed multiple immune cell populations, with monocytes representing the largest population identified in the analysis.

### Gene Ontology Enrichment

GO enrichment analysis of monocyte marker genes identified significant enrichment of pathways related to:

* Antigen presentation
* Immune activation
* Adaptive immune response
* Lymphocyte activation

These results support the involvement of immune dysregulation in Long COVID pathology.

---

## Technologies Used

* Python
* Scanpy
* AnnData
* Pandas
* NumPy
* Matplotlib
* SciPy
* GSEApy / Enrichr
* Jupyter Notebook

---

## Output Files

### Processed Data

* GSE241385_processed.h5ad
* GSE241385_clustered.h5ad
* GSE241385_annotated.h5ad

### Figures

* UMAP Cell Type Visualization
* Cell Type Distribution Plot
* Marker Gene Dot Plot
* GO Enrichment Bar Plot

### Functional Analysis

* GO Enrichment PDF Report
* GO Enrichment Text Report

---

## Future Directions

Potential extensions of this work include:

* Differential Gene Expression Analysis
* Pathway Enrichment Analysis
* Cell-Cell Communication Analysis
* Multi-dataset Integration
* Machine Learning-based Cell State Classification

---

## Author
 sneha galimotu                                                                                                                                                        
##Data Avalability
The original dataset (GSE241385) and processed .h5ad files are not included in this repository because of GitHub file size limitations.

Dataset source:
https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE241385                    
