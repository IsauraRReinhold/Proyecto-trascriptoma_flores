# Flower Transcriptome


In this respository you will find the raw data from *Idesia polycarpa Maxim. var. vestita* Diels s male flowers downloaded from NCBI 4th may 2018 (https://www.ncbi.nlm.nih.gov/sra/?term=SRR6958534), and a serie of analyses to make the preprocess of sequences  with fastQC and Trimmomatic and *de novo* assembly using Trinity.

### Objective

The objective of this repository is make an excercise to practice command line and R using RNA-seq data.

- - -




## Data

All the analysis described below were run in Ubuntu 14.06

**Download sequences**

The data used in this ecxercise were downloaded from NCBI 4th may 2018.

SRX3901489: Early data of Idesia polycarpa Maxim. var. vestita Diels s male flowers
1 ILLUMINA (Illumina HiSeq 2000) run: 22.6M spots, 6.8G bases.


In the `data` directory all the sequences are in fastq format.


For download the data first you need install sra-tool kit with the command

`wget ftp://ftp-trace.ncbi.nlm.nih.gov/sra/sdk/current/sratoolkit.current-centos_linux64.tar.gz` 

For download the raw sequences the command is


`./fast-dump --split-files accession code -O dirname.fastq`

- - -


## Sequencing files

All raw FASTQ sequences are in `data/seqs/raw_data` :

SRR6958534_1.fastq

SRR6958534_2.fastq

**Quality control steps**

In order to check the high quality of sequences I do the next steps

1. Run fastQC 0.11

2. Then i check the results

3. Also trimm the adapters 

4. And the poor quality bases 

**Programs** :

fastQC 0.11

trimmomatic V0.36 (http://www.usadellab.org/cms/?page=trimmomatic)

All results from fastQC and trimmomatic are in `FlowerProject/analysis`

- - -

### the novo assembly

The assembly are in `analysis/Trinity_assembly`

### Scripts

In the directory Scripts you will find all the scripts generated to make the analysis



