# Computational Reanalysis of COVID-19 Single-Cell RNA Sequencing Data


# 🧬 Computational Reanalysis of COVID-19 Single-Cell RNA Sequencing Data

## 📌 Project Overview

This project performs a computational reanalysis of publicly available single-cell RNA-sequencing (scRNA-seq) data derived from COVID-19 patient samples. Using the **Seurat** package in R, I processed the raw count matrices, performed clustering, identified cell type–specific marker genes, and carried out **functional enrichment analysis (GO)** to highlight the biological pathways dysregulated during SARS-CoV-2 infection.

The goal is to demonstrate advanced **bioinformatics and computational biology skills** by reproducing and extending published datasets into a reproducible pipeline.

---

## 📂 Dataset

* Source: [GEO accession — GSM4557327](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM4557327)
* Format: `.rds` count matrix (with exon/intron/spanning annotations).
* Preprocessing: Extracted exon counts, created **Seurat object**, performed QC, normalization, clustering.

---

## 🛠️ Methods / Pipeline

1. **Data Import & Seurat Object Creation**

   * Read raw counts (exon matrix).
   * Created `Seurat` object with metadata.

2. **Quality Control (QC)**

   * Filtered cells by number of features & counts.
   * Calculated **percent mitochondrial genes** to remove low-quality cells.

3. **Normalization & Feature Selection**

   * Log normalization.
   * Identified top variable genes.

4. **Dimensionality Reduction & Clustering**

   * PCA for initial reduction.
   * **UMAP** for visualization.
   * Louvain clustering to identify cell populations.

5. **Marker Gene Identification**

   * Ran `FindAllMarkers()` to extract cluster-specific genes.
   * Highlighted genes like **S100A8, HBB, IFI27**.

6. **Functional Enrichment**

   * **GO Biological Process** enrichment of marker genes
---

## 📊 Results

* **UMAP clustering** revealed distinct immune cell populations.
* **Cluster markers** included inflammatory genes (*S100A8/S100A9*), interferon-induced genes (*IFI27*), and hemoglobin (*HBB*).
* **GO/KEGG enrichment** suggested activation of:

  * Immune response pathways.
  * Interferon signaling.
  * Inflammatory cascades.

> 📌 Plots are included in the `results/` directory:

* QC violin plots
* PCA/UMAP visualizations
* Cluster marker heatmaps
* GO enrichment dotplots

---

## 📁 Repository Structure

```
├── scripts/             # R scripts for each step of pipeline
├── results/             # Figures and tables generated
├── README.md            # Project overview (this file)

```

---

## 🔧 Tools & Packages

* **R (≥ 4.0)**
* [Seurat](https://satijalab.org/seurat/)
* [clusterProfiler](https://yulab-smu.top/biomedical-knowledge-mining-book/)
* tidyverse

---
## 🧑‍💻 Author

**Saman Israr**
📫 \samanisrar200@gmail.com
🔗 \www.linkedin.com/in/saman-israr-200baac | https://www.kaggle.com/samanisrar
---

✨ This project highlights expertise in **single-cell transcriptomics, statistical analysis, and reproducible bioinformatics workflows**.


