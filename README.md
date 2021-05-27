# COVID-19 Ultrafast, Memory-Efficient Genome Sequence Aligner
Ultrafast and memory-efficient genome aligning with Bowtie 2 and visualization with Interactive Genomics Viewer (IGV)

<a href="url"><img src="https://github.com/MattLondon101/Images/blob/master/samtools.png" align="center" height="422" width="723" ></a>

Next Generation Sequencing affords high-throughput genome sequencing via library automation, low DNA input samples, capture hybridization multiplexing and application of ultrafast and memory-efficient read mapping tools, including Bowtie 2. The driving function of Bowtie 2 is the Burrows-Wheeler transform, which lexographically reverse permutates the characters of a string (e.g. nucleotides) to render the data more compressible, thus optimized for further processing.

This repository describes the process of taking a .fasta file of DNA sequences, aligning them with Bowtie 2, and visualizing and analyzing them with Samtools.

**Requirements**
* Linux OS (I used Windows Subsystem for Linux (WSL) in Visual Studio Code in Windows 10)
* Conda: [Instructions for installation](https://conda.io/projects/conda/en/latest/user-guide/install/linux.html)
* Genome sequences: In this case, I will be using COVID-19 cDNA sequences from NCBI.

**Bowtie2**

In Linux terminal enter:
```
conda install bowtie2
```
In you working directory:
```
# build database
bowtie2-build -f nucleotide_all2056_NCBI.fasta covid_all_db
```
align sequences in .fasta and save as .sam
```
bowtie2 -f -x covid_all_db -U nucleotide_all2056_NCBI.fasta -S nucleotide_all2056_NCBI.sam
```
.sam to binary .bam
```
samtools view -Sb nucleotide_all2056_NCBI.sam > nucleotide_all2056_NCBI.bam
```
create .bai index file
```
samtools index nucleotide_all2056_NCBI.bam
```
View in IGV by loading both .bam and .bai



Updated 5/7/21


