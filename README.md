# GSE173231_scRNAseq_Stress_Analysis
Detailed analysis of GSE173231 dataset
# scRNAseq_stress_gene_analysis
Detailed analysis of GSE173231 dataset
# 🧬 scRNA-seq Analysis of GSE173231: Stress State, Pathways & Cell Identity

This repository contains a full single-cell RNA-seq analysis workflow for the GEO dataset **GSE173231**, with a focus on:

- Quality control & filtering  
- Normalization and feature selection  
- Clustering and visualization  
- Marker gene discovery  
- Cell type annotation  
- **Stressed vs non-stressed cellular state analysis**  
- **Pathway enrichment using GSEApy**  
- **Cell identity validation using PanglaoDB**

The analysis is performed using **Scanpy (Python)** following best practices for reproducible scRNA-seq workflows.

---

## 📌 Dataset

**GEO Accession:** GSE173231  
**Platform:** 10x Genomics scRNA-seq  
**Organism:** Human  

Raw data was downloaded from NCBI GEO and processed into AnnData (`.h5ad`) format.

---

## 🔬 Analysis Workflow

1. QC & Filtering  
2. Normalization & HVGs  
3. PCA → Neighbors → UMAP  
4. Leiden Clustering  
5. Marker Gene Detection (`rank_genes_groups`)  
6. Cell Type Annotation  
7. Stress State Analysis  
8. Pathway Enrichment (GSEApy)  
9. PanglaoDB Mapping  

---

## 🧪 Key Biological Questions

- Which clusters show a transcriptional stress response?  
- What genes define the stressed state?  
- What pathways are activated under stress?  
- Do PanglaDB annotations agree with manual marker logic?  

---

## 📁 Repository Structure

```text
notebooks/   → Step-by-step analysis  
scripts/     → Reusable functions  
results/     → Figures & tables  
data/        → Processed AnnData  
docs/        → Biological interpretation  
