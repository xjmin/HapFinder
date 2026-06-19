# HapFinder

HapFinder is an open-source R package for microhaplotype genotyping, mixture interpretation, population frequency estimation, forensic statistical analysis, and EuroForMix-compatible data conversion.

## Features

### Microhaplotype Genotyping

* Direct genotyping from BAM files
* Supports paired-end (PE) and single-end (SE) sequencing data
* Read-level haplotype reconstruction
* CIGAR and MD-tag based variant parsing
* Quality filtering at both read and base levels

### Mixture Analysis

* Microhaplotype calling for mixed DNA samples
* Allele count and haplotype frequency estimation
* Compatible with forensic mixture interpretation workflows

### Population Genetics

* Population haplotype frequency estimation
* Generation of allele frequency databases
* Calculation of forensic parameters

### Forensic Statistics

Automatically calculates:

* Expected Heterozygosity (He)
* Polymorphism Information Content (PIC)
* Effective Number of Alleles (Ae)
* Discrimination Power (DP)
* Probability of Exclusion (PE)
* Shannon Information Index

### EuroForMix Integration

* Convert population frequencies into EuroForMix database format
* Generate EuroForMix mixture input files
* Generate individual reference profiles

### Interactive GUI

A Shiny-based graphical interface allows:

* Data upload
* Parameter configuration
* Genotyping analysis
* Result visualization
* Export of reports

# Main Functions

| Function                      | Description                          |
| ----------------------------- | ------------------------------------ |
| MicrohapCalling               | Individual microhaplotype genotyping |
| MixMicrohapCall               | Mixture microhaplotype analysis      |
| analyzeMicrohaplotypeResults  | Zygosity and ACR analysis            |
| computeForensicStatsDetailed  | Forensic statistics                  |
| popMicroHapFreq               | Population frequency estimation      |
| recalculateMHcallsByThreshold | Threshold optimization               |
| toEuroForMixFreqData          | EuroForMix frequency database        |
| toEuroforMixInput             | EuroForMix mixture input             |
| toIndReference                | Individual reference profiles        |
| runHapFinder                  | Launch Shiny GUI                     |

---

# Applications

HapFinder can be applied to:

* Forensic individual identification
* DNA mixture interpretation
* Population genetic studies
* Kinship analysis
* Microhaplotype database construction
* EuroForMix workflows
* Targeted sequencing panels
* Next-generation sequencing (NGS) data analysis

---

# License

GPL-3 License
