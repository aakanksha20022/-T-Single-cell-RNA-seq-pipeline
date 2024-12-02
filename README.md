Gamma-delta-T-Cell-Single_cell-RNA-seq-pipeline
---
This repository contains the implementation of a single-cell analysis pipeline using ScanPy, focusing on a dataset of γδ T cells with three wild type (WT) samples and one knockout (KO) sample 
(β2 integrin-deficient mouse). The analysis replicates steps introduced in lectures and practicals, including quality control, integration, differential expression, and pseudotime trajectory analysis.

Pipeline Overview
1. Quality Control of 10X Chromium Data
- Evaluates mapping quality using IGV and Cell Ranger summary outputs.
- Identifies issues and suggest improvements for downstream analysis.
- Data Integration with ScanPy

2. Performs standard ScanPy integration for WT and KO samples.
- Optimizes dimension reduction and clustering parameters.
- Generates UMAPs, annotate clusters using marker genes, and visualize cell-type frequencies.
- Differential Expression (DE) Analysis

3. Compares DE in KO vs. WT within major clusters using:
- BBKNN method.
- Harmony integration.
- Pseudo-bulk analysis (DESeq2).
- Reports upregulated genes (p-value < 0.01, logFC > 0.5) and summarize methods.
- Pseudotime Trajectory Analysis

Uses PAGA to generate and interpret trajectories for major clusters.
Explore biological relevance and potential directions of cellular progression.
