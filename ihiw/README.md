# Reference alleles for HML Genotyping reports for the 18th IHIW

This directory contains selected reference sequences for the [18th International HLA and Immunogenetics Workshop.](https://www.ihiw18.org/) These reference sequences were selected using a set of python scripts, which choose the lowest-numbered full-length sequence available in a given IPD-IMGT/HLA release. For these purposes, "full length" refers to the 'genomic' sequences curated by the IPD-IMGT/HLA Database, which include sequence for all exons and introns, and the 5' and 3' untranslated regions (UTRs). This reference allele catalog was created for use in generating and aligning consensus sequences and describing novel sequence variation in HML Genotyping documents. 

The python code for generating this list, and guidelines for generation of HML documents can be found at the IHIW Git Repository:

* https://github.com/IHIW/bioinformatics

## Loci

Reference alleles are provided for each HLA locus (HLA-A, -B, -C, -E, -F, -G, -DPA1, -DPB1, -DQA1, -DQB1, -DRA, -DRB1, -DRB3, -DRB4 and -DRB5) Sequences are also provided for the MICA and MICB loci, as well as HLA-DMA, -DMB, -DOA, -DOB, when these sequences are available in hla.xml

For each release starting with 3.26.0, this catalog is available in this folder in two files:

* A list of alleles, ordered by locus and allele name (.._Reference_Alleles.txt)
* A fasta formatted file containing the reference sequence (.._ReferenceSequences.fasta)

## References

Matern BM, Mack SJ, Osoegawa K, Maiers M, Niemann M, Robinson J, Heidt S, Spierings E\
Standard Reference Sequences for Submission of HLA Genotyping for the 18th IHIW\
Manuscript Submitted for Publication

Milius RP, Heuer M, Valiga D, Doroschak KJ, Kennedy CJ, Bolon YT, Schneider J, Pollack J, Kim HR, Cereb N, Hollenbach JA, Mack SJ, Maiers M.\ 
Histoimmunogenetics Markup Language 1.0: Reporting next generation sequencing-based HLA and KIR genotyping.\
Human Immunology (2015) doi: 10.1016/j.humimm.2015.08.001. \
http://schemas.nmdp.org

Robinson J, Barker DJ, Georgiou X, Cooper MA, Flicek P, Marsh SGE\
The IPD-IMGT/HLA Database\
Nucleic Acids Research (2020) 43:D948-D955

## Contact
Questions about the designated IHIW reference sequences should be directed to Ben Matern\
B.M.Matern@umcutrecht.nl