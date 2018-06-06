# Plasmodiophora
==========
Commands used in the assembly and annotation of Brassica Club Root associated Plasmodiophora genomes


This document details the commands used to assemble and annotate minion genomes.

Note - all this work was performed in the directory:
/home/groups/harrisonlab/project_files/plasmodiophora

```bash
  mkdir -p /home/groups/harrisonlab/project_files/plasmodiophora
```

## Organising Data

### Moving illumina data onto the cluster


Firstly directories were made in the temporary storage area to hold the data

```bash
Species=""
Strain=""
mkdir -p /data/scratch/crowtw/raw_dna/illumina/paired/$Species/$Strain/F
mkdir -p /data/scratch/crowtw/raw_dna/illumina/paired/$Species/$Strain/R

Species=""
Strain=""
mkdir -p /data/scratch/crowtw/raw_dna/illumina/paired/$Species/$Strain/F
mkdir -p /data/scratch/crowtw/raw_dna/illumina/paired/$Species/$Strain/R

Species=""
Strain=""
mkdir -p /data/scratch/crowtw/raw_dna/illumina/paired/$Species/$Strain/F
mkdir -p /data/scratch/crowtw/raw_dna/illumina/paired/$Species/$Strain/R
```
Then data was copied into this area using from my local machine using SCP.
*Note* Best not to display IP address and username here

```bash
Species=""
Strain=""
scp <F_reads.fastq.gz> cluster:/data/scratch/crowtw/raw_dna/illumina/paired/$Species/$Strain/F/.
scp <R_reads.fastq.gz> cluster:/data/scratch/crowtw/raw_dna/illumina/paired/$Species/$Strain/R/.

Species=""
Strain=""
scp <F_reads.fastq.gz> cluster:/data/scratch/crowtw/raw_dna/illumina/paired/$Species/$Strain/F/.
scp <R_reads.fastq.gz> cluster:/data/scratch/crowtw/raw_dna/illumina/paired/$Species/$Strain/R/.

Species=""
Strain=""
scp <F_reads.fastq.gz> cluster:/data/scratch/crowtw/raw_dna/illumina/paired/$Species/$Strain/F/.
scp <R_reads.fastq.gz> cluster:/data/scratch/crowtw/raw_dna/illumina/paired/$Species/$Strain/R/.
```


### Calling MinION data

Basecalling was performed on local machines at the University of Warwick. Commands used to do this are summarised below:

```bash

```

Raw data was moved onto the NIAB-EMR cluster.

Firstly directories were made in the temporary storage area to hold the data

```bash
mkdir -p /data/scratch/crowtw/raw_dna/minion
```

Then data was copied into this area using from my local machine using SCP.
*Note* Best not to display IP address and username here

```bash
scp <basecalled_data.tar.gz> cluster:/data/scratch/crowtw/raw_dna/minion/.
```

This data was temporarily un-tarballed on the cluster.

```bash
cd /data/scratch/crowtw/raw_dna/minion
tar -zxvf <basecalled_data.tar.gz>
```

## Assembly
