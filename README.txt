
# README: Cross-Species scRNA-seq Pipelines (Seurat & SCE)

## Requirements
- R 4.1+
- Install these packages before running:
  - Seurat, SingleCellExperiment, scater, scran
  - tidyverse, biomaRt, data.table, Matrix, patchwork

## Files
- SRC/seurat_pipeline.R → Seurat-based analysis
- SRC/sce_pipeline.R → SingleCellExperiment-based analysis
- DOC/writeup.txt → Project description

## How to Run
1. Edit each R script to set file paths (input CSVs for exon, intron, metadata).
2. Run in R using:
```R
source("SRC/seurat_pipeline.R")
source("SRC/sce_pipeline.R")
```

## Parameters Used
- Downsample: 2000 cells per species
- PCA dims: 10
- UMAP dims: 1:10
- Human mito pattern: "^MT-"
- Manual annotations applied to human clusters

## Expected Output
- Integrated objects with harmonized gene names
- UMAP plots grouped by species and manual labels
