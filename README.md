# OCD GWAS Analysis

## Project Overview

This project identifies genome-wide significant single-nucleotide polymorphisms (SNPs) associated with obsessive-compulsive disorder (OCD) and investigates their predicted functional consequences using publicly available genome-wide association study (GWAS) summary statistics.

## Research Question

Which genetic variants show genome-wide significant associations with OCD, and what are their predicted functional consequences?

## Dataset

- **Source:** Psychiatric Genomics Consortium (PGC), Strom et al. (2025)
- **Dataset:** `daner_OCD_full_wo23andMe_190522.gz`
- **Sample size:** 23,493 OCD cases and 1,114,613 controls
- **Number of variant records:** 6,791,632
- **Reference genome:** GRCh37
- **Data access:** https://www.med.unc.edu/pgc/download-results/

The publicly available dataset excludes 23andMe data.

## Tools and Methods

The analysis was conducted in Google Colab using Python.

Libraries included:
- pandas
- NumPy
- Matplotlib
- SciPy

The workflow included:

1. Inspection and quality control of GWAS summary statistics.
2. Identification of significant SNPs using P < 5 × 10⁻⁸.
3. Generation of Manhattan and Q-Q plots.
4. Calculation of the genomic inflation factor.
5. Preliminary functional annotation using NCBI dbSNP.

## Preliminary Results

Three SNPs passed the genome-wide significance threshold:

| SNP | Chromosome | P-value | Gene | Predicted consequence |
|---|---|---|---|---|
| rs13262595 | 8 | 6.902 × 10⁻¹⁰ | TSNARE1 | Intron variant |
| rs4129585 | 8 | 9.990 × 10⁻¹⁰ | TSNARE1 | Intron variant |
| rs10098073 | 8 | 2.992 × 10⁻⁸ | TSNARE1 | Intron variant |

The genomic inflation factor was λGC = 1.1882.

These three SNPs are closely positioned and have not been established as independent association signals. Their annotations do not establish causality.

## Repository Contents

- `OCD_GWAS_Analysis.ipynb` — Google Colab notebook containing the computational analysis.
- `OCD_significant_SNPs.csv` — Table of genome-wide significant SNPs.
- `OCD_Manhattan_Plot.png` — Manhattan plot of GWAS association results.
- `OCD_QQ_Plot.png` — Q-Q plot of observed and expected association statistics.
- `README.md` — Project description and instructions.
- `ai_usage.md` — Documentation of AI assistance.

## Reproducing the Analysis

1. Download the publicly available summary-statistics dataset from the PGC.
2. Open `OCD_GWAS_Analysis.ipynb` in Google Colab.
3. Upload the downloaded `.gz` dataset into the Colab environment.
4. Ensure the notebook's dataset path matches the uploaded filename.
5. Run the notebook cells in sequence to reproduce the quality-control summaries, significant SNP table, and plots.

The original GWAS dataset is not included in this repository because of its large file size.

## Limitations

The public summary statistics exclude 23andMe data and may not reproduce all findings from the complete published meta-analysis. The analysis does not include formal linkage disequilibrium testing or experimental functional validation.

## References

Strom, N. I., et al. (2025). Genome-wide analyses identify 30 loci associated with obsessive–compulsive disorder. *Nature Genetics*. https://doi.org/10.1038/s41588-025-02189-z

Psychiatric Genomics Consortium: https://www.med.unc.edu/pgc/download-results/

NCBI dbSNP: https://www.ncbi.nlm.nih.gov/snp/
