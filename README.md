# Cross-Disorder Representation Learning for Neurodevelopmental Disorders using Multimodal Data

## Overview

Neurodevelopmental disorders such as **Attention Deficit Hyperactivity Disorder (ADHD)**, **Autism Spectrum Disorder (ASD)**, and **Dyslexia** are complex conditions characterized by overlapping behavioral, cognitive, and biological features. Traditional machine learning approaches often rely on single-modality data, limiting their ability to capture this complexity.

This project proposes a **multimodal representation learning framework** that integrates:
- Structural MRI (sMRI)
- Phenotypic (behavioral and clinical) data
- Genomic (GWAS-based pathway features)

The goal is to learn **shared and disorder-specific representations** across these conditions without requiring fully matched multimodal datasets.

---

## Key Contributions

- Developed a **cross-disorder multimodal learning framework** for neurodevelopmental disorders
- Designed **modality-specific encoders**:
  - ResNet for structural MRI
  - TabTransformer for phenotypic data
  - MLP for genomic features
- Proposed **disorder-level aggregation** to handle incomplete multimodal data
- Implemented **attention-based multimodal fusion** for adaptive integration of modalities
- Evaluated representations using:
  - SVM baseline (unimodal evaluation)
  - Prototype-based classification (multimodal evaluation)
- Demonstrated that multimodal fusion improves representation quality and generalization

---

## Methodology

### 1. Data Processing
- sMRI preprocessing (alignment, normalization, resampling)
- Phenomic data harmonization and feature engineering
- Genomic feature construction:
  - SNP → Gene mapping
  - Gene scoring
  - Pathway enrichment (GO, KEGG, Reactome)

### 2. Representation Learning
- sMRI → ResNet-based encoder
- Phenomic → TabTransformer
- Genomic → MLP projection

### 3. Multimodal Fusion
- Disorder-level aggregation
- Cross-modal attention mechanism
- Generation of fused embeddings

### 4. Evaluation
- Unimodal classification using SVM
- Multimodal evaluation using prototype-based classification
- Clustering, similarity analysis, and visualization

---

## Results

- Multimodal fusion achieved:
  - **Accuracy: ~84.5%**
  - **Weighted F1-score: ~0.84**
- Learned representations capture:
  - Shared patterns (e.g., ADHD–Dyslexia overlap)
  - Disorder-specific characteristics (e.g., strong ASD separability)
- Attention analysis shows adaptive modality contributions per disorder

---


---

## Reproducibility

- All major components of the pipeline are included
- Scripts are organized by modality and processing stage
- Results can be reproduced using the provided workflows

---

## Future Work

- Subject-level multimodal fusion (with matched datasets)
- Improved genomic data integration
- Advanced fusion architectures (e.g., transformers, graph-based models)
- Extension to additional neurodevelopmental disorders
