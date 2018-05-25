
[TOC]

# Flower Transcriptome of *Idesia polycarpa*


In this respository you will find the raw data from *Idesia polycarpa* Maxim. var. *vestita* Diels  male flowers downloaded from NCBI 4th may 2018 (https://www.ncbi.nlm.nih.gov/sra/?term=SRR6958534), and a series of analyses to make the preprocess of sequences  with fastQC and Trimmomatic and *de novo* assembly using Trinity.

Data references :


Mei, L., Dong, N., Li F., Li. N. Yao M., Chen F., Tang L.(2017).Transcriptome analysis of female and male flowers buds of *Idesia polycarpa* Maxim. var. *vestita* Diels. *Electronic Journal of Biotechnology*, 29:39-46.

### Objective

The objective of this repository is to make an exercise to practice command line and R using RNA-seq data.

- - -




## Data



**Download sequences**

The data used in this exercise was downloaded from NCBI 4th may 2018.

SRX3901489: Early data of Idesia polycarpa Maxim. var. vestita Diels s male flowers
1 ILLUMINA (Illumina HiSeq 2000) run: 22.6M spots, 6.8G bases.


In the `data` directory all the sequences are in fastq format.


To download the data first you need to install sra-tool kit with the command

`wget ftp://ftp-trace.ncbi.nlm.nih.gov/sra/sdk/current/sratoolkit.current-centos_linux64.tar.gz` 

To download the raw sequences the command is


`./fast-dump --split-files accession code -O dirname.fastq`

- - -


## Sequencing files

All raw FASTQ sequences are in `data/seqs/raw_data` :

SRR6958534_1.fastq

SRR6958534_2.fastq

**Quality control steps**

In order to check the high quality of sequences I do the next steps.

1. Run fastQC 0.11

2. Then I check the results

3. Trimm the adapters 

4. And the poor quality bases 

**Programs** :

fastQC 0.11

trimmomatic V0.36 (http://www.usadellab.org/cms/?page=trimmomatic)

All results from fastQC and trimmomatic are in `FlowerProject/analysis`

- - -

### The novo assembly

The assembly is in `analysis/Trinity_Results`

### Scripts

All the analysis described below were run in Ubuntu 14.06.

In the directory Scripts you will find all the scripts generated to make the analysis

1. Descargar datos crudos.sh Script to download the raw data
2. fastqc.sh   Script to run fastqc
3. trimmomatic.sh Script to make the data clean
4. Trnity.sh  Script to make the data assembly
5. Mapa Idesia.R Script to make the Idesia map distribution
6. Gráfica de barras.R Script to make the bar plot of the percent and presence of Idesia in the world



