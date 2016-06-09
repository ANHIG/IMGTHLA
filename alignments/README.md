## Sequence Alignment Helpfile

In order to provide standardised sequences for any loci, the following numbering system has been established that accurately represents the sequence at both the nucleotide and protein level. We have looked at the HUGO Gene Nomenclature Committee recommendations proposed for the numbering of genomic sequences, and use a similar model for the HLA sequences held in the IPD-IMGT/HLA Sequence Database. Many of their proposals already match our current strategy. HUGO recommends that for all nomenclature systems a standard reference sequence should be used for each locus. In the case of HLA sequences a standard reference sequence is already established for each gene. The remaining recommendations for nucleotide sequences are as follows;

### Nucleotide Sequence Numbering.

The numbering of the nucleotides in the reference sequence should remain constant.
* For both gDNA and cDNA the A of the ATG initiator Methionine codon has been denoted nucleotide +1. In some non-expressed genes this codon is not present and in these cases the first base of the reference sequence has been denoted as nucleotide +1.
* The nucleotide immediately preceding the A of the ATG initiator Methionine codon has been denoted nucleotide -1. Note: that there is no nucleotide 0.
cDNA sequences are numbered consecutively from the A of the ATG initiator Methionine codon.
* Nucleotide sequences may be displayed in codons, in this case the numbering follows that for protein sequences.

The following recommendations are used for describing mutations in nucleotide sequences;

* Nucleotide substitutions are designated using the nucleotide number, followed by the substitution. For example; 997G>T denotes a substitution of G to T at position 997 of the DNA sequence.
* Deletions are designated by 'del' after the nucleotide number. For example; 997delT denotes the deletion of a T at position 997 of the DNA. For deletions of a number of consecutive bases the mutation should be described as 997-998delTG which denotes a deletion of TG at positions 997 and 998 of the DNA.
* Insertions are designated by 'ins' after the nucleotide numbers bordering the insertion. For example; 997-998insT, represents an insertion of T between bases 997 and 998 of the DNA. In the alignments produced this will be represented by a period (.), but the numbering of the reference sequence will not be altered to include this base. Insertions of multiple bases are designated using the same form, 997-998insTG denotes an insertion of TG between positions 997 and 998 of the DNA.

### Protein Sequence Numbering

* For amino acid-based systems, the start codon of the mature protein is labeled codon 1.
* The codon 5' to this is numbered -1.
* All numbering is based on the reference sequence.
* The single letter amino acid code is used in all protein alignments.
* Nucleotide sequences may be displayed in codons, in this case the numbering follows that for protein sequences.
* To avoid confusion with the nucleotide numbering p. may be added to the nomenclature to denote a protein sequence.

Mutations in protein sequences follow a similar format;

* For amino acid nomenclature the reference amino acid is listed first followed by the codon and then the mutation. For example; Y97S represents a substitution of the Tyrosine at codon 97 for a Serine.
* Stop codons are always designated by X. For example; T97X represents a Threonine substituted for a stop codon.
* Deletions are again designated used 'del'. For example; T97del is the deletion of a Threonine at codon 97.
* Insertions again follow the 'ins' convention. For example; T97-98ins represents a Threonine inserted between codons 97 and 98

### Alignment Conventions

The following conventions are used in the sequence alignments to represent identity and mismatches.

* The entry for each allele is displayed in respect to the reference sequences.
* Where identity to the reference sequence is present the base will be displayed as a hyphen (-).
* Non-identity to the reference sequence is shown by displaying the appropriate base at that position.
* Where an insertion or deletion has occurred this will be represented by a period (.).
* If the sequence is unknown at any point in the alignment, this will be represented by an asterisk (*).
* In protein alignments for null alleles, the 'Stop' codons will be represented by a hash (X).
* In protein alignments, sequence following the termination codon, will not be marked and will appear blank.
* These conventions are used for both nucleotide and protein alignments.
* A pipe (|) represents an exon or intron border.
