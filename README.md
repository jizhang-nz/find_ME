# Find ME (Find Mobile Element)
Find ME is a program that could be used to find out if a Mobile Element (ME) is present in the whole-genome sequences of bacterial isolates.

## Motivation
Mobile Elements (MEs) such as prophage, plasmid and genomic island are common in bacterial whole-genome sequences. A tool is needed to detect if a ME is present in a fragmented whole-genome sequences (draft genomes).

## Summary of Algorithm

First the whole-genome sequences of a bacterial isolate were concatinated, and then used as a query to search in a protein sequences database with BLASTX. The protein sequence database comprised of translated coding sequences (CDSs) in the reference ME. For each hits in the database, if the alignment coverage (default 50%) and alignment identity percentage (default 80%) are both above cutoff values, then the program would conclude that the CDS is present in the query genome. A final score will be given by caculating the percentage of the positive reference CDSs in the reference ME, which could be used to signify the presence or absence of the ME in the genome.

## Prerequisites
Before start, you need to make sure the following three programs were full functional in your system:
   * [BLAST+](https://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/)

## Usage
Let's assume you have put the `find_ME.pl` file in your PATH. If not, or if you prefer, you could always put the `find_ME.pl` file along with your other input files, and use commands like:

    perl find_ME.pl -g list.genomes.txt -r list.reference.txt

Here are some example commands:
_coming soon_

## Citation
_coming soon_
