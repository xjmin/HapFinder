# HapFinder

## A Unified Framework for Haplotype Genotyping of Multivariant Genetic Markers

HapFinder is an open-source R framework for haplotype genotyping of multivariant genetic markers from both second- and third-generation sequencing data.

Unlike existing software that primarily focuses on SNP-based microhaplotypes (MHs) from targeted sequencing assays, HapFinder supports a broad spectrum of haplotype markers, including:

- SNP-based Microhaplotypes (MHs)
- Multi-InDel markers
- DIP-MHs
- Custom multivariant marker systems

The framework is compatible with both targeted sequencing panels and untargeted datasets such as whole-genome sequencing (WGS) and whole-exome sequencing (WES), enabling scalable haplotype analysis across diverse forensic and genetic applications.

In addition to haplotype genotyping, HapFinder integrates population frequency estimation, forensic statistical analysis, DNA mixture interpretation workflows, and data export modules compatible with established forensic software such as EuroForMix and Familias.

HapFinder is freely available and designed as an extensible platform for current and emerging haplotype-based forensic genetic analyses.

---

# Overview

HapFinder was developed by providing a unified and platform-agnostic framework for haplotype analysis. Key advantages include:

### Broad Marker Support

HapFinder supports multiple classes of multivariant genetic markers:

- Microhaplotypes (MHs)
- Multi-InDels
- DIP-MHs
- User-defined multivariant loci

### Multi-Platform Compatibility

Compatible with:

- Illumina sequencing
- MGI sequencing
- Oxford Nanopore sequencing
- Other BAM-based sequencing datasets

### Targeted and Untargeted Data Analysis

Supports:

- Targeted forensic sequencing panels
- Whole-genome sequencing (WGS)
- Whole-exome sequencing (WES)

### Integrated Forensic Workflows

Provides downstream tools for:

- Population frequency estimation
- Forensic parameter calculation
- DNA mixture interpretation
- EuroForMix database generation
- Familias-compatible outputs

### Interactive and Reproducible

- Command-line workflow
- Shiny graphical interface
- Open-source and fully reproducible

# Repository Contents

This repository contains the following files:

| File                                 | Description                                             |
| ------------------------------------ | ------------------------------------------------------- |
| **HapFinder_1.0.0.tar.gz**           | HapFinder R package source file for local installation  |
| **HapFinder_install_dependencies.R** | Script for installing all required package dependencies |
| **HapFinder.pdf**                    | Complete user manual and software documentation         |
| **README.md**                        | Project overview and installation guide                 |

---

# Installation

## Step 1. Download Repository Files

Download the following files from this repository:

```text
HapFinder_1.0.0.tar.gz
HapFinder_install_dependencies.R
HapFinder.pdf
```

---

## Step 2. Install Dependencies

Before installing HapFinder, install all required dependencies:

```r
source("HapFinder_install_dependencies.R")
```

This script automatically installs all required R packages.

---

## Step 3. Install HapFinder

Install the package locally:

```r
install.packages(
  "HapFinder_1.0.0.tar.gz",
  repos = NULL,
  type = "source"
)
```

Load the package:

```r
library(HapFinder)
```

---

## Step 4. Launch Shiny GUI

```r
HapFinder::runHapFinder()
```

The graphical interface will automatically open in your web browser.

---

# Main Features

## Microhaplotype Genotyping

* Direct genotyping from BAM files
* Supports paired-end (PE) and single-end (SE) sequencing data
* Read-level haplotype reconstruction
* CIGAR- and MD-tag-based variant parsing
* Quality filtering at both read and base levels

---

## DNA Mixture Analysis

* Microhaplotype calling for mixed DNA samples
* Allele count estimation
* Haplotype frequency estimation
* Mixture interpretation support

---

## Population Genetics

* Population haplotype frequency estimation
* Construction of frequency databases
* Population-level marker evaluation

---

## Forensic Statistics

Automatically calculates:

* Expected Heterozygosity (He)
* Effective Number of Alleles (Ae)
* Polymorphism Information Content (PIC)
* Discrimination Power (DP)
* Probability of Exclusion (PE)
* Shannon Information Index

---

## EuroForMix Integration

* Generation of EuroForMix-compatible frequency databases
* Generation of EuroForMix mixture input files
* Generation of reference individual profiles

---

## Interactive Shiny Interface

The built-in Shiny GUI supports:

* Data upload
* Parameter configuration
* Genotyping analysis
* Mixture analysis
* Result visualization
* Report export

---

# Main Functions

| Function                      | Description                              |
| ----------------------------- | ---------------------------------------- |
| MicrohapCalling               | Individual microhaplotype genotyping     |
| MixMicrohapCall               | Mixture microhaplotype analysis          |
| analyzeMicrohaplotypeResults  | Zygosity and ACR analysis                |
| computeForensicStatsDetailed  | Forensic statistical analysis            |
| popMicroHapFreq               | Population frequency estimation          |
| recalculateMHcallsByThreshold | Threshold optimization                   |
| toEuroForMixFreqData          | EuroForMix frequency database generation |
| toEuroforMixInput             | EuroForMix mixture input generation      |
| toIndReference                | Individual reference profile generation  |
| runHapFinder                  | Launch Shiny GUI                         |

---

# Documentation

A complete user manual is available in:

```text
HapFinder.pdf
```

The manual includes:

* Installation instructions
* Input file preparation
* Parameter descriptions
* Example datasets
* Function documentation
* Workflow tutorials
* EuroForMix integration examples

---

# License

GPL-3 License

---

# Contact

**Jiaming Xue**

Department of Forensic Biology
West China School of Basic Medical Sciences and Forensic Medicine
Sichuan University, Chengdu, China

Email: [xuejohn55@gmail.com](mailto:xuejohn55@gmail.com)

GitHub:
https://github.com/xjmin/HapFinder

---

# Acknowledgements

We thank all contributors and users of HapFinder for their support and feedback.

HapFinder is freely available for academic and research use.
