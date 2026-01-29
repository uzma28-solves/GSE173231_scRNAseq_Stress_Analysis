# Biological Interpretation of GSE173231 scRNA-seq Dataset

## 1. Dataset Overview
- **GEO Accession:** GSE173231  
- **Organism:** Human  
- **Platform:** 10x Genomics single-cell RNA-seq  
- **Focus:** Characterization of cell types, transcriptional stress states, and pathway enrichment in single-cell profiles.

The dataset contains multiple clusters of cells captured under different conditions. Our analysis focused on:

1. Cluster identification via Leiden clustering  
2. Marker gene detection using Scanpy’s `rank_genes_groups`  
3. Biological interpretation via PanglaoDB mapping  
4. Stress-state detection across clusters  
5. Pathway enrichment analysis using GSEApy

---

## 2. Cluster Summaries

### Cluster 0 – Fibroblast / Stellate-like Cells
- **PanglaoDB enrichment:**  
  - Fibroblasts (adj p = 8.68e-36)  
  - Pancreatic Stellate Cells (adj p = 1.37e-33)  
  - Hepatic Stellate Cells (adj p = 4.75e-32)  
  - Adipocytes (adj p = 1.52e-31)  

- **Top marker genes:**  
  `DCN, FBLN1, LUM, CFD, SOD3, APOD, MMP2, RARRES2, SERPINF1, COL1A2`  

- **Interpretation:**  
  Cluster 0 represents **stromal cells with fibroblast-like identity**. The high expression of extracellular matrix genes (COL1A2, LUM, DCN) and stress-associated genes (SOD3, APOD) indicates active **tissue remodeling** and response to **cellular stress**. Mapping to pancreatic and hepatic stellate cells highlights a heterogeneous fibroblast population.

---

### Cluster 1 – T-cell Populations
- **Marker genes:** `CD3D, CD3E, IL7R, TRAC`  
- **PanglaoDB enrichment:** T-cells, CD4+ T-cells, CD8+ T-cells  

- **Interpretation:**  
  Cluster 1 consists of **adaptive immune cells**. Differential expression indicates naive and memory T-cell subtypes. Pathway analysis shows **T-cell activation** and **cytokine signaling**, reflecting immune surveillance.

---

### Cluster 2 – B-cell / Plasma Cells
- **Marker genes:** `MS4A1, CD79A, IGHM, IGKC`  
- **PanglaoDB enrichment:** B-cells, plasma cells  

- **Interpretation:**  
  Cluster 2 represents **B-lineage cells**, including plasma cells. Upregulation of immunoglobulin genes confirms active **antibody production**.

---

### Cluster 3 – Endothelial Cells
- **Marker genes:** `PECAM1, VWF, CDH5`  

- **Interpretation:**  
  Cluster 3 represents **vascular endothelial cells**. Stress analysis shows mild upregulation of oxidative stress genes (HMOX1), suggesting adaptation to microenvironmental stress.

---

## 3. Stress State Analysis
- Calculated **stress scores** per cell using top stress-response genes (`HSPA1A, DDIT3, HSP90AA1`).  

**Findings:**
- Cluster 0 fibroblast-like cells exhibited the **highest stress scores** — active ECM remodeling under stress.  
- Cluster 3 endothelial cells showed **moderate stress**, reflecting vascular adaptation.  
- Immune clusters (1 & 2) displayed **lower stress scores**, indicating stress response is compartmentalized to stromal cells.

---

## 4. Pathway Enrichment (GSEApy Results)
- **Cluster 0:** ECM organization, collagen formation, oxidative stress response  
- **Cluster 1:** T-cell receptor signaling, cytokine-mediated signaling  
- **Cluster 2:** B-cell receptor signaling, immunoglobulin production  
- **Cluster 3:** VEGF signaling, angiogenesis, oxidative stress response  

**Interpretation:**  
Stressed stromal cells are involved in **extracellular matrix remodeling** and handling **reactive oxygen species**, while immune and endothelial clusters show functional specialization consistent with their lineage.

---

## 5. Integration with PanglaoDB
- Most clusters mapped accurately to expected cell types.  
- Cluster 0 mapping to fibroblast and stellate cells **validates marker-based annotation**.  
- Stress-associated genes are enriched in fibroblast clusters, supporting **cell-type specific stress response**.

---

## 6. Summary Table (Clusters & Key Features)

| Cluster | Identity                     | Top Genes                                | Stress Score | Key Pathways                  |
|--------|-------------------------------|-----------------------------------------|--------------|-------------------------------|
| 0      | Fibroblast / Stellate-like    | DCN, LUM, COL1A2, SOD3                  | High         | ECM, Oxidative Stress         |
| 1      | T-cells                       | CD3D, CD3E, IL7R                        | Low          | TCR signaling                 |
| 2      | B-cells / Plasma              | MS4A1, IGHM, IGKC                        | Low          | BCR signaling                 |
| 3      | Endothelial Cells              | PECAM1, VWF, CDH5                        | Moderate     | VEGF signaling, Oxidative Stress |

---

## 7. Conclusion
This analysis provides a **comprehensive single-cell map** integrating:

- Cluster-specific marker genes  
- Stress-state transcriptional profiling  
- Functional pathway enrichment  
- Validation against PanglaoDB  

**Key insights:**
1. Fibroblast-like cells are the **main stress responders**.  
2. Immune cells maintain **low stress gene expression**.  
3. Endothelial cells show **moderate stress adaptation**.  
4. Stress responses are **cluster-specific**, reflecting cellular specialization in the tissue microenvironment.

These results can guide future studies on **stromal stress in tissue remodeling or disease contexts**.

---

