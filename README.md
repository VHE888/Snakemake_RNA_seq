# RNA-seq Pipeline with Snakemake

## Overview

This Snakemake workflow performs quality control, contamination assessment, and genome alignment for paired-end bulk RNA-seq data.

The pipeline includes:

- Raw read quality assessment
- Read trimming
- Quality assessment after trimming
- PhiX contamination detection
- rRNA contamination detection and removal
- Genome alignment
- Microbial contamination detection
- MultiQC summary report

*Note: PhiX, rRNA, Microbial contamination detection are optional if you have processed data from facility.*

---

## Workflow

Raw Reads

↓

FastQC

↓

Trimmomatic

↓

FastQC (Trimmed Reads)

↓

PhiX Contamination Check

↓

rRNA Contamination Detection and Removal

↓

STAR Genome Alignment

↓

Microbial Contamination Detection

↓

MultiQC Report

---

## Input

The pipeline requires paired-end FASTQ files as input.

Reference files include:

- Reference genome
- STAR genome index
- Gene annotation (GTF)
- rRNA reference
- PhiX reference
- Kraken database

---

## Output

The workflow generates:

- FastQC reports
- Trimmed FASTQ files
- PhiX contamination report
- rRNA contamination report
- rRNA-filtered FASTQ files
- STAR alignment results
- Microbial contamination report
- MultiQC summary report

---

## Software

- Snakemake
- FastQC
- Trimmomatic
- STAR
- Bowtie2
- BWA
- SAMtools
- KrakenUniq
- MultiQC
