# Ultrafast_Memory_Efficient_Genome_Sequence_Aligner
Ultrafast and memory-efficient genome aligning with Bowtie 2 and visualization with Samtools

Next Generation Sequencing affords high-throughput genome sequencing via library automation, low DNA input samples, capture hybridization multiplexing and application of ultrafast and memory-efficient read mapping tools, including Bowtie 2. The driving function of Bowtie 2 is the Burrows-Wheeler transform, which lexographically reverse permutates the characters of a string (e.g. nucleotides) to render the data more compressible, thus optimized for further processing.

This repository describes the process of taking a .fasta file of DNA sequences, aligning them with Bowtie 2, and visualizing and analyzing them with Samtools.

**Requirements**
* Linux OS (I used Windows Subsystem for Linux (WSL) in Visual Studio Code in Windows 10)
