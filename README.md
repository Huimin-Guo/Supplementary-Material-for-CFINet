# Supplementary Material for CFINet

**Manuscript Title:** *CFINet: A Coarse–Fine Interaction Network for Gross Tumor Volume Segmentation in Esophageal Cancer Radiotherapy*

**Authors:** *Huimin Guo, Yin Gu, Ming Cui, Deyu Sun, Wei Qian, Alessandro Perelli and He Ma*

## Overview

This supplementary material provides additional methodological details, experimental results, and analyses supporting the main manuscript. It documents the training and evaluation procedures, offers expanded comparisons with baseline methods, and examines the spatial response characteristics and geometric implications of GTV segmentation. The supplement is organized into six sections.

## Contents

| Section | Title | Description |
|---|---|---|
| **S1** | **Experimental Setup** | Dataset and annotation details, preprocessing and augmentation, patient-level five-fold evaluation, temporally held-out testing, baseline configurations, and evaluation metrics. |
| **S2** | **Performance and Efficiency** | Additional performance comparisons on Dataset A, paired statistical analyses, model complexity and inference measurements, and qualitative GTV segmentation examples. |
| **S3** | **Ablation and ERF Analysis** | Controlled comparisons of grouped self-attention (GSA), grouped cross-attention (GCA), cross-scale feature fusion (CSFF), and Path-2 patch size, together with attention-efficiency and effective receptive field (ERF) analyses. |
| **S4** | **Temporal Testing and Failure Modes** | Patient-level results on Dataset B, comparisons of cohort characteristics, and representative segmentation errors in Datasets A and B. |
| **S5** | **GTV-to-CTV/PTV Geometry** | Fixed-margin GTV expansions, comparisons with GTV-centered portions of physician-defined clinical target volumes, margin sensitivity, local target coverage, and volume outside the clinical PTV. |
| **S6** | **SegTHOR Evaluation** | Detailed thoracic organ-at-risk segmentation results, including per-organ measurements and qualitative comparisons on the public SegTHOR dataset. |

## Evaluation Scope

**Dataset A** is the internal cohort used for patient-level five-fold evaluation. **Dataset B** was collected later at the same institution and was held out from model development. It should not be interpreted as an independent-institution test set.

The GTV-to-CTV/PTV analysis in **S5** evaluates the geometry of fixed-margin expansions against GTV-centered regions of clinical contours. These measurements do not establish the accuracy of complete clinical CTV/PTV delineation or the dosimetric suitability of the expanded regions.

The **SegTHOR** experiments in S6 evaluate segmentation of thoracic organs at risk. They provide a complementary cross-task benchmark, not an external test of esophageal cancer GTV segmentation.

## Reading Guide

The main manuscript presents the central methodology and findings. Refer to **S1–S2** for implementation and comparison details, **S3** for module-level and ERF analyses, **S4** for temporal testing and error characteristics, **S5** for downstream geometric evaluation, and **S6** for the public organ-segmentation benchmark. Figures and tables are cited within their corresponding sections.

## Abbreviations

GTV, gross tumor volume; CTV, clinical target volume; PTV, planning target volume; OAR, organ at risk; DSC, Dice similarity coefficient; HD95, 95th-percentile Hausdorff distance; ASSD, average symmetric surface distance; ERF, effective receptive field.