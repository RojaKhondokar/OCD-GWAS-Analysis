# AI Usage Documentation

## Project
Identification and Functional Annotation of OCD-Associated Variants Using Published GWAS Summary Statistics

## AI Tool Used
ChatGPT (OpenAI)

## Purpose of AI Assistance

ChatGPT was used as a supporting tool during the development of this computational genomics project.

### 1. Project Planning
AI assistance was used to refine the research question, organize the methodology and identify appropriate computational approaches.

### 2. Python Programming
ChatGPT assisted with writing and explaining Python code for analyzing GWAS summary statistics in Google Colab.

Assistance included:
- Reading compressed GWAS data using pandas.
- Checking data quality and identifying invalid records.
- Filtering SNPs using genome-wide significance thresholds.
- Generating Manhattan and Q-Q plots.
- Calculating the genomic inflation factor.

### 3. Troubleshooting
ChatGPT helped interpret error messages, troubleshoot computational steps, and identify alternative annotation resources when Ensembl VEP was unavailable.

### 4. Results Interpretation
AI assistance was used to explain statistical results, identify limitations, and interpret preliminary functional annotations obtained from NCBI dbSNP.

## Verification of AI-Assisted Outputs

AI-generated code was executed in Google Colab, and its outputs were inspected during the analysis.

The number of significant SNPs, quality-control results, p-values, odds ratios, and genomic inflation factor were checked against the notebook's computational outputs.

Functional annotations were examined using NCBI dbSNP records. Interpretations were limited to the available evidence, and statistical associations were not treated as proof of causality.

## Data Privacy and Ethical Considerations

Only publicly available GWAS summary statistics were analyzed. No individual-level participant records or personally identifiable genetic information were used.

AI was used to support computational work, not to replace verification of results.

