PBMC 10x scRNA‑seq Preprocessing and QC (Seurat + EmptyDrops + SoupX + scDblFinder)
This repository contains an R workflow for preprocessing and quality control of 10x Genomics PBMC single‑cell RNA‑seq data. The pipeline emphasizes rigorous droplet‑level QC, ambient RNA assessment, doublet detection, and standard Seurat‑based downstream analysis.

Overview
Input: Raw 10x raw_feature_bc_matrix directory (500 PBMC 3p LT Chromium X).

Main steps:

Load 10x counts into a Seurat object.

Detect true cells vs empty droplets with EmptyDrops (DropletUtils).

Estimate ambient RNA contamination with SoupX and decide whether correction is needed.


Apply cell‑level QC filters (UMI, genes, %MT, %ribo).

Normalize, find variable features, scale, PCA, clustering, UMAP.

Marker‑based cell‑type annotation using canonical PBMC markers.
