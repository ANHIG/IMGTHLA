--------------------------------------------------------------------------------
 IPD-IMGT/HLA Database
--------------------------------------------------------------------------------

This directory contains data for the IPD-IMGT/HLA database. The IPD-IMGT/HLA database is a specialist sequence database for sequences of the human histocompatibility complex. This directory contains the IPD-IMGT/HLA flat files and documentation. 

### Cloning the Repository

#### From April 2024, Release 3.56.0

As of Release 3.56.0, due April 2024, all large files (>100MB) will be provided as compressed files rather than utilise Git LFS, which was previously required. This includes the hla.dat, xml/hla.xml and xml/hla_ambigs.xml in the next release. This has been done to simplify the cloning process and also due to escalating and unpredictable costs in providing the files using Git LFS from a public repository. All compressed files will use the [ZIP format](https://en.wikipedia.org/wiki/ZIP_(file_format)). This formatting change will be applied to all branches.

#### Up to April 2024

Previously the repository has required the use of the Git LFS tools (https://git-lfs.github.com) to handle files over 100MB in size. Whilst all hla.dat files are now provided as a zipped file, any pulls from previous commits for Release 3.55.0 and earlier will still require Git LFS. Please use this when cloning the repository to ensure the larger files are downloaded correctly. If Git LFS is not used then large files will contain pointers to the Git LFS location rather than the data required.

--------------------------------------------------------------------------------
File Formats 
--------------------------------------------------------------------------------

The directory also contains the HLA sequences in a number of formats. Within the following folders, the various format types are explained briefly here:

### Alignments folder

Files designated “X_prot.txt”, where X is a locus or gene, contain protein sequences. Please note that alleles that contain non-coding variations may be identical at the protein level. 

Files designated “X_nuc.txt”, where X is a locus or gene, contain the nucleotide coding sequences (CDS). Please note that alleles that contain non-coding variations may be identical at the CDS level.

Files designated “X_gen.txt”, where X is a locus or gene, contain genomic DNA sequences. Please note that for alleles that do not possess genomic sequences there will be no entry in the file, or where there is only a single genomic sequence at the locus, a file will not be produced.  

For further information on the construction of these text files, please refer to the description available here: https://www.ebi.ac.uk/ipd/imgt/hla/alignment/help/. To provide consistency in both formatting and to record versioning information, as of version 3.32.0, the header is designated by hash tags at the start of the line. 

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

Please note in release 3.60.0, the TCE tools introduced version 3 which now includes core/non-core assignments. An updated dpb_tce.csv file containing Version 3 Assignment is provided.

The files in this folder provide a listing of the T-Cell Epitope Group Assignments for DPB1 proteins. The assignments are taken from the algorithms used for the online tools at https://www.ebi.ac.uk/ipd/imgt/hla/matching/. The file formart is as follows;

* DPB1 allele, DPB1 protein, Version 1 Assignment, Version 2 Assignment, Version 3 Assignment, Comments

Alleles which have yet to be assigned a TCE group using either version are left blank.  

### WMDA Folder

Further information on the WMDA files can be found in the dedicated README file in the wmda directory. 
https://github.com/ANHIG/IMGTHLA/blob/Latest/wmda/README.md

### XML Folder

Please refer to the relevant XSD file for information regarding the XML files, which can be found here: https://github.com/ANHIG/IMGTHLA/blob/Latest/xml/hla_ambigs.xsd

Please note in release 3.43.0, there are three XML files for the release, hla.xml, hla_ciwd.xml and hla_ambigs.xml. The hla_ciwd.xml file is an updated version of the hla.xml file and includes the addition of new information from the Common, intermediate and well‐documented HLA alleles in world populations: CIWD version 3.0.0 (https://doi.org/10.1111/tan.13811). This is as new elements have been required to incorporate this data, and the CWD version 2.0.0 data has been recoded to the same structure. In release 3.44.0 and onwards, hla_ciwd.xml will replace hla.xml, and the older format archived.

Please note in release 3.53.0, there was a change made to the hla.xml. The releaseversions tag attribute releasestatus has been changed to a binary flag containing either "Public" or "Deleted" to allow for easier filtering of deleted alleles. In addition a releasecomments attribute has been added containing information about changes to this allele with this verison of the database, this contains the information previously stored in the releasestatus attribute.

Please note in release 3.55.0, there are three XML files for the release, hla.xml, hla_new.xml and hla_ambigs.xml. The hla_new.xml is an updated version of the hla.xml and includes a new release tag containing version and date information for the release. In release 3.56.0 and onwards, hla_new.xml will replace hla.xml, and the older format archived.

### Allele List Folder

Lists of alleles for different versions of the database are now included in this single folder due to the large number of files.

These filenames take the format Allelelist.XXXX.txt with the XXXX in the file denotes a particular release. These files are a csv format detailing for each allele the official name used in each release of the database.

### Other Files

The top-level directory contains the following files; 

* Alignments_Rel_XXXX.zip - a compressed archive of the alignments folder, where the XXXX in the file denotes a particular release.
* LICENSE.md - a file detailing the licensing of data included in the IPD-IMGT/HLA Database.
* Nomenclature_2009.txt - a file detailing pre-2010 allele nomenclature
* README.md - This README file
* hla.dat.zip - An EMBL-ENA style format file containing data from the IPD-IMGT/HLA Database, see (https://github.com/ANHIG/IMGTHLA/blob/Latest/Manual.md) for further details. 
* hla_gen.fasta - a copy of the file in the fasta directory, includes the DNA sequence for all alleles, which have genomic sequences available. 
* hla_nuc.fasta - a copy of the file in the fasta directory, includes the DNA sequence for the CDS sequence of all alleles. 
* hla_prot.fasta - a copy of the file in the fasta directory, includes the amino acid sequence for all alleles. 
* md5checksum.txt - a file detailing md5 checksums for all files in the top-level directory

The top-level directory contains the following lists, in order to provide consistency in both formatting and to record versioning information, as of version 3.32.0, all list files have been converted to csv format, and contain a header. The header is designated by hash tags at the start of the line.  

* Allele_status.txt - a csv file detailing for each allele how many times it has been submitted, from how many cells, the unconfirmed/confirmed status of the allele, if the CDS is fully sequenced and if the allele is cDNa or gDNA sequence.
* Allelelist.txt  - a csv file listing all alleles named at the time of the latest release.
* Allelelist_history.txt - a csv file detailing for each allele the official name used in each release of the database. 
* Deleted_alleles.txt - a csv file detailing all deleted allele names, with reasons for the deletion. This list also includes details of any suffix changes. 
* release_version.txt - a plain text file which denotes the current release version.
* sversion_history.txt - a csv file detailing for each allele the Sequence Version used in each release of the database.

### Versioning

The database version number, IPD-IMGT/HLA 3.44.0 2021-04-20 b9d9ef7, can be interpreted as;

* Database Name
* Major release number (nomenclature version, quarterly release, sequence version)
* Date
* Latest commit for ANHIG/IMGTHLA/Latest branch

The major release number contains three key fields, the first is the nomenclature version, which is currently 3. The second is the quarterly release number, which is incremented by 1 every January, April, July and October with each subsequent release. The final third number represents the sequence version. A '0' is used for the primary quarterly release, and only incremented if any subsequent interim path or update contains a change to a valid base (not a * or a .) in either the nucleotide (both cDNA and gDNA) or protein sequence. Changes to the positioning of indels, or unsequenced bases are not included if the raw sequence remains unchanged.

--------------------------------------------------------------------------------
 CONTACTS
--------------------------------------------------------------------------------

For information on the IPD-IMGT/HLA Database please see the website at:
http://www.ebi.ac.uk/ipd/imgt/hla

Additional information on sequence file formats is available from:
http://www.ebi.ac.uk/ipd/imgt/hla/download/

For any other information please contact ipdsubs@anthonynolan.org.

--------------------------------------------------------------------------------
 COPYRIGHT NOTICE
--------------------------------------------------------------------------------

We have chosen to apply the Creative Commons Attribution-NoDerivs License to all
copyrightable parts of our databases, which includes the sequence alignments.
This means that you are free to copy, distribute, display and make commercial
use of the databases in all legislations, provided you give us credit by citing
the following;

Barker D, Maccari G, Georgiou X, Cooper M, Flicek P, Robinson J, Marsh SGE
The IPD-IMGT/HLA Database
Nucleic Acids Research(2023), 51(D1): D948-D955

Robinson J, Barker D, Marsh SGE
25 years of the IPD-IMGT/HLA Database.
HLA(2024),103(6): e15549

Robinson J, Malik A, Parham P, Bodmer JG, Marsh SGE:
IMGT/HLA - a sequence database for the human major histocompatibility complex
Tissue Antigens (2000), 55:280-287

We are strongly opposed to the mirroring of the data contained on our sites, both
hla.alleles.org and the IPD-IMGT/HLA Database, and would ask that rather than mirror
the information, appropriate links are provided where applicable.

If you intend to distribute a modified version of our data, you must ask us for
permission first, please contact ipdsubs [at] anthonynolan [dot] org for further details
of how modified data can be reproduced.

--------------------------------------------------------------------------------
 FUNDING
--------------------------------------------------------------------------------

The development of the IPD-IMGT/HLA Database was funded by an EU BIOTECH grant. The
work of maintaining and updating the database has been supported in the past by
the Imperial Cancer Research Fund, the National Institute of Health, the NMDP and 
more recently by Anthony Nolan. The continual maintenace and any further development 
of the database relies on alternate sources of financial support, which are actively 
been sought for the continued maintenance of the database. The Sequence.org initiative at
the NMDP has solicited funds from institutions and companies who produce HLA
typing reagents, typing systems, and instrumentation or that otherwise utilise
these databases in critical components of their business. To learn more about
how your business can support the IPD-IMGT/HLA Database, please contact:
Benjamin Hester, (Email: bhester [at] nmdp [dot] org), NMDP.

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
