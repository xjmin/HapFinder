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

---

# Installation

# Workflow

```text
BAM File
   │
   ▼
MicrohapCalling()
   │
   ▼
Microhaplotype Genotypes
   │
   ├── analyzeMicrohaplotypeResults()
   │
   ├── computeForensicStatsDetailed()
   │
   ├── popMicroHapFreq()
   │
   ├── toEuroForMixFreqData()
   │
   └── toEuroforMixInput()
```

---

# Quick Start

## Individual Sample Analysis

```r
result_file <- MicrohapCalling(
    MH_info = "MH_info.txt",
    bam.file = "sample.bam",
    wd_link = "./results",
    lian_qual = 20,
    base_qual = 30,
    base_qual_include = "F",
    other_snp_threshold = 0.01,
    MH_read_threshold = 10,
    MH_ratio_threshold = 0.25,
    SNP_ratio_threshold = 0.25,
    PE_data = "T"
)
```

---

## Mixture Analysis

```r
mix_result <- MixMicrohapCall(
    MH_info = "MH_info.txt",
    bam.file = "mixture.bam",
    wd_link = "./results",
    lian_qual = 20,
    base_qual = 30,
    base_qual_include = "F",
    MH_read_threshold = 10,
    PE_data = "T"
)
```

---

## Analyze Calling Results

```r
summary_result <- analyzeMicrohaplotypeResults(
    "Test_MHCalling.txt"
)
```

Outputs include:

* Zygosity
* Haplotype depth
* Allele Coverage Ratio (ACR)
* ACR quality category

---

## Calculate Forensic Statistics

```r
computeForensicStatsDetailed(
    c(0.4,0.3,0.2,0.1)
)
```

Returns:

* He
* PIC
* Ae
* DP
* PE
* Shannon Index

---

## Population Frequency Estimation

```r
popMicroHapFreq(
    input_link = "./input/",
    MH_info = "./MH_info.txt",
    ind_file = "./individuals.txt",
    out_link = "./output/"
)
```

---

## Generate EuroForMix Database

```r
toEuroForMixFreqData(
    popfreq = "MH_haplotypes_popFreq.txt",
    out_link = "./EuroForMix/"
)
```

---

## Generate EuroForMix Mixture Input

```r
toEuroforMixInput(
    result_mix = mix_result,
    mix_name = "Case001",
    Mix_read_threshold = 10,
    wd_link = "./EuroForMix/"
)
```

---

# Launch Shiny Application

```r
HapFinder::runHapFinder()
```

Default:

```text
http://127.0.0.1:3838
```

---

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

# Citation

If you use HapFinder in your research, please cite:

```text
Xue J, et al.
HapFinder: an open-source R package for microhaplotype
genotyping and forensic genetic analysis.
(Manuscript in preparation)
```

---

# License

GPL-3 License

---

# Contact

Jiaming Xue

Department of Forensic Biology,
West China School of Basic Medical Sciences and Forensic Medicine,
Sichuan University, China

Email: [xuejiaming@scu.edu.cn](mailto:xuejiaming@scu.edu.cn)
GitHub: https://github.com/qushengqiu2020
