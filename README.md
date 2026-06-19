# HapFinder

## Haplotype-Based Genotyping and Analysis for Forensic Genetics

HapFinder is an open-source R package for microhaplotype genotyping, forensic statistical analysis, DNA mixture interpretation, population frequency estimation, and EuroForMix-compatible data conversion.

The package supports next-generation sequencing (NGS) data and provides both command-line functions and an interactive Shiny graphical user interface (GUI) for forensic genetic analyses.

---

# Overview

Microhaplotypes are emerging forensic genetic markers with high polymorphism, low mutation rates, and excellent performance for individual identification, kinship analysis, ancestry inference, and mixture deconvolution.

HapFinder provides a complete workflow for:

* Microhaplotype genotyping from BAM files
* DNA mixture interpretation
* Population frequency estimation
* Forensic parameter calculation
* EuroForMix-compatible data generation
* Interactive data analysis through Shiny

---

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

# Applications

HapFinder can be applied to:

* Forensic individual identification
* DNA mixture interpretation
* Kinship analysis
* Population genetic studies
* Microhaplotype database construction
* EuroForMix workflows
* Targeted sequencing panel analysis
* Next-generation sequencing (NGS) data analysis
* Forensic research and education

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
