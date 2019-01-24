--------------------------------------------------------------------------------
 IPD-IMGT/HLA Database
--------------------------------------------------------------------------------

This directory contains data for the IPD-IMGT/HLA database. The IPD-IMGT/HLA database is a specialist sequence database for sequences of the human histocompatibility complex. This directory contains the IPD-IMGT/HLA flat files and documentation. 

--------------------------------------------------------------------------------
Downloading and Cloning This Repository 
--------------------------------------------------------------------------------

Due to the increasing file sizes for the hla.dat and some of the compressed zip files, the repository now requires the Git LFS tools (https://git-lfs.github.com) which handle files over 100MB. Please use these when cloning to ensure the larger files are downloaded correctly. If Git LFS is not used then large files will contain pointers to the Git LFS location rather than the data required. 

--------------------------------------------------------------------------------
File Formats 
--------------------------------------------------------------------------------

The directory also contains the HLA sequences in a number of formats. Within the following folders, the various format types are explained briefly here:

### Alignments folder

Files designated “X_prot.txt”, where X is a locus or gene, contain protein sequences. Please note that alleles that contain non-coding variations may be identical at the protein level. 

Files designated “X_nuc.txt”, where X is a locus or gene, contain the nucleotide coding sequences (CDS). Please note that alleles that contain non-coding variations may be identical at the CDS level.

Files designated “X_gen.txt”, where X is a locus or gene, contain genomic DNA sequences. Please note that for alleles that do not possess genomic sequences there will be no entry in the file, or where there is only a single genomic sequence at the locus, a file will not be produced.  

For further information on the construction of these text files, please refer to the description available here: http://www.ebi.ac.uk/ipd/imgt/hla/nomenclature/alignments.html. To provide consistency in both formatting and to record versioning information, as of version 3.32.0, the header is designated by hash tags at the start of the line. 

A zip compressed archive of all the text-format alignment files is available from the top-level directory. 

### FASTA folder

All files in this folder are provided in the FASTA sequence format. Please note the FASTA format contains no alignment information.

Files designated “X_prot.fasta”, where X is a locus or gene, contain protein sequences. Please note that alleles that contain non-coding variations may be identical at the protein level. 

Files designated “X_nuc.fasta”, where X is a locus or gene, contain the nucleotide coding sequences (CDS). Please note that alleles that contain non-coding variations may be identical at the CDS level.

Files designated “X_gen.fasta”, where X is a locus or gene, contain genomic DNA sequences. Please note for alleles that do not possess genomic sequences, there will be no entry in the file.

### MSF Folder

All files in this folder are provided in the MSF sequence format. 

Files designated “X_prot.msf”, where X is a locus or gene, contain protein sequences. Please note that alleles that contain non-coding variations may be identical at the protein level. 

Files designated “X_nuc.msf”, where X is a locus or gene, contain the nucleotide coding sequences (CDS). Please note that alleles that contain non-coding variations may be identical at the CDS level.

Files designated “X_gen.msf”, where X is a locus or gene, contain genomic DNA sequences. Please note for alleles that do not possess genomic sequences, there will be no entry in the file.

### OID Folder

Further information on the OID files can be found in the dedicated README file in the oid directory. As of version 3.32.0, all list files have been converted to csv format, and contain a header. The header is donated by hash tags at the start of the line.  
https://github.com/ANHIG/IMGTHLA/blob/Latest/oid/README.md

### PIR Folder

All files in this folder are provided in the PIR sequence format. 

Files designated “X_prot.pir”, where X is a locus or gene, contain protein sequences. Please note that alleles that contain non-coding variations may be identical at the protein level. 

Files designated “X_nuc.pir”, where X is a locus or gene, contain the nucleotide coding sequences (CDS). Please note that alleles that contain non-coding variations may be identical at the CDS level.

Files designated “X_gen.pir”, where X is a locus or gene, contain genomic DNA sequences. Please note for alleles that do not possess genomic sequences, there will be no entry in the file.

### TCE Folder

The files in this folder provide a listing of the T-Cell Epitope Group Assignments for DPB1 proteins. The assignments are taken from the algorithms used for the online tools at https://www.ebi.ac.uk/ipd/imgt/hla/dpb.html. The file formart is as follows;

* DPB1 allele, DPB1 protein, Version 1 Assignment, Version 2 Assignment, Comments

Alleles which have yet to be assigned a TCE group using either version are left blank.  

### WMDA Folder

Further information on the WMDA files can be found in the dedicated README file in the wmda directory. 
https://github.com/ANHIG/IMGTHLA/blob/Latest/wmda/README.md

### XML Folder

Please refer to the relevant XSD file for information regarding the XML files, which can be found here: https://github.com/ANHIG/IMGTHLA/blob/Latest/xml/hla_ambigs.xsd

### Other Files

The top-level directory contains the following files; 

* Alignments_Rel_XXXX.zip - a compressed archive of the alignments folder, where the XXXX in the file denotes a particular release.
* LICENSE.md - a file detailing the licensing of data included in the IPD-IMGT/HLA Database.
* Nomenclature_2009.txt - a file detailing pre-2010 allele nomenclature
* README.md - This README file
* hla.dat - An EMBL-ENA style format file containing data from the IPD-IMGT/HLA Database, see http://www.ebi.ac.uk/ipd/imgt/hla/docs/manual.html for further details. Please note as of version 3.35.0 this file has been uploaded using Git LFS, and when downloading or cloning may not be retrieved properly. We recommend downloading directly from the raw file link provided at Github.
* hla_gen.fasta - a copy of the file in the fasta directory, includes the DNA sequence for all alleles, which have genomic sequences available. 
* hla_nuc.fasta - a copy of the file in the fasta directory, includes the DNA sequence for the CDS sequence of all alleles. 
* hla_prot.fasta - a copy of the file in the fasta directory, includes the amino acid sequence for all alleles. 
* md5checksum.txt - a file detailing md5 checksums for all files in the top-level directory

The top-level directory contains the following lists, in order to provide consistency in both formatting and to record versioning information, as of version 3.32.0, all list files have been converted to csv format, and contain a header. The header is designated by hash tags at the start of the line.  

* Allele_status.txt - a csv file detailing for each allele how many times it has been submitted, from how many cells, the unconfirmed/confirmed status of the allele, if the CDS is fully sequenced and if the allele is cDNa or gDNA sequence.
* Allelelist.txt and Allelelist.XXXX.txt - a csv file listed all alleles named at the time of the release, the XXXX in the file denotes a particular release. Allelelist.txt is a copy of the latest version.
* Allelelist_history.txt - a csv file detailing for each allele the official name used in each release of the database. 
* Deleted_alleles.txt - a csv file detailing all deleted allele names, with reasons for the deletion. This list also includes details of any suffix changes. 


--------------------------------------------------------------------------------
 CONTACTS
--------------------------------------------------------------------------------

For information on the IPD-IMGT/HLA Database please see the website at:
http://www.ebi.ac.uk/ipd/imgt/hla

Additional information on sequence file formats is available from:
http://www.ebi.ac.uk/ipd/imgt/hla/download.html

For any other information please contact hla@alleles.org.

--------------------------------------------------------------------------------
 COPYRIGHT NOTICE
--------------------------------------------------------------------------------

We have chosen to apply the Creative Commons Attribution-NoDerivs License to all
copyrightable parts of our databases, which includes the sequence alignments.
This means that you are free to copy, distribute, display and make commercial
use of the databases in all legislations, provided you give us credit by citing
the following;

Robinson J, Halliwell JA, Hayhurst JH, Flicek P, Parham P, Marsh SGE:
The IPD and IPD-IMGT/HLA Database: allele variant databases
Nucleic Acids Research (2015), 43:D423-431

Robinson J, Malik A, Parham P, Bodmer JG, Marsh SGE:
IMGT/HLA - a sequence database for the human major histocompatibility complex
Tissue Antigens (2000), 55:280-287

We are strongly opposed to the mirroring of the data contained on our sites, both
hla.alleles.org and the IPD-IMGT/HLA Database, and would ask that rather than mirror
the information, appropriate links are provided where applicable.

If you intend to distribute a modified version of our data, you must ask us for
permission first, please contact hla [at] alleles [dot] org for further details
of how modified data can be reproduced.

--------------------------------------------------------------------------------
 FUNDING
--------------------------------------------------------------------------------

The development of the IPD-IMGT/HLA Database was funded by an EU BIOTECH grant. The
work of maintaining and updating the database has been supported in the past by
the Imperial Cancer Research Fund, the National Institute of Health, the
National Marrow Donor Program (NMDP) and more recently by the Anthony Nolan
Trust. The continual maintenace and any further development of the database
relies on alternate sources of financial support, which are actively been sought
for the continued maintenance of the database. The Sequence.org initiative at
the NMDP has solicited funds from institutions and companies who produce HLA
typing reagents, typing systems, and instrumentation or that otherwise utilise
these databases in critical components of their business. To learn more about
how your business can support the IPD-IMGT/HLA Database, please contact: Todd Peterson
(Email: Todd [dot] Peterson [at] nmdp [dot] org).

If you intend to use any of the data found on our sites for commercial use, we
would ask you to consider funding the database and the work we do. Without
continued funding the database cannot be maintained.

--------------------------------------------------------------------------------
 DISCLAIMER
--------------------------------------------------------------------------------

Where discrepancies have arisen between reported sequences and those stored in
the database, the original authors have been contacted where possible, and
necessary amendments to published sequences have been incorporated. Future
sequencing may identify errors and the WHO Nomenclature Committee would welcome
any evidence that helps to maintain the accuracy of the database. We therefore
make no warranties regarding the correctness of the data, and disclaim liability
for damages resulting from its use. We cannot provide unrestricted permission
regarding the use of the data, as some data may be covered by patents or other
rights. Any medical or genetic information is provided for research, educational
and informational purposes only. It is not in any way intended to be used as a
substitute for professional medical advice, diagnosis, treatment or care.

We reserve the right to use information about visitors (IP addresses), date/time
visited, page visited, referring website, etc. for site usage statistics and to
improve our services.
