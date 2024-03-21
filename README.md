--------------------------------------------------------------------------------
 IPD-IMGT/HLA Database - Testing Branch
--------------------------------------------------------------------------------

This directory contains test data for the IPD-IMGT/HLA database. The IPD-IMGT/HLA database is a specialist sequence database for sequences of the human histocompatibility complex. 

### Cloning the Repository

Prior to 2024-03-21 large files required Git LFS to download, this branch does not require Git LFS, but other branches may depending on which files and commits are downloaded. 

#### From April 2024, Release 3.56.0

As of 2024-03-21 the Testing Branch and as of Release 3.56.0, due April 2024 for the latest branch, all large files (>100MB) will be provided as compressed files rather than utilise Git LFS. This includes the hla.dat, xml/hla.xml and xml/hla_ambigs.xml in the next release. This has been done to simplify the cloning process and also due to escalating and unpredictable costs in providing the files using Git LFS from a public repository. All compressed files will use the [ZIP format](https://en.wikipedia.org/wiki/ZIP_(file_format)). This formatting change will be applied to all branches.

--------------------------------------------------------------------------------
Testing Directory Disclaimer
--------------------------------------------------------------------------------

This directory is intended only for distribution of test files and formats. The files in this repository should not be used for clinical or diagnostic work and intended for testing purposes only. The files may contain errors or raise errors in any downstream processes.

The contents of this branch have been minimised to only contain those files under active development.

--------------------------------------------------------------------------------
File Formats 
--------------------------------------------------------------------------------

Within the following folders, the various format types are explained briefly here:

### XML Folder

Please refer to the relevant XSD file for information regarding the XML files, which can be found here: https://github.com/ANHIG/IMGTHLA/blob/Latest/xml/hla_ambigs.xsd

Please note in release 3.43.0, there are three XML files for the release, hla.xml, hla_ciwd.xml and hla_ambigs.xml. The hla_ciwd.xml file is an updated version of the hla.xml file and includes the addition of new information from the Common, intermediate and well‐documented HLA alleles in world populations: CIWD version 3.0.0 (https://doi.org/10.1111/tan.13811). This is as new elements have been required to incorporate this data, and the CWD version 2.0.0 data has been recoded to the same structure. In release 3.44.0 and onwards, hla_ciwd.xml will replace hla.xml, and the older format archived.

Please note in release 3.53.0, there was a change made to the hla.xml. The releaseversions tag attribute releasestatus has been changed to a binary flag containing either "Public" or "Deleted" to allow for easier filtering of deleted alleles. In addition a releasecomments attribute has been added containing information about changes to this allele with this verison of the database, this contains the information previously stored in the releasestatus attribute.

Please note in release 3.55.0, there are three XML files for the release, hla.xml, hla_new.xml and hla_ambigs.xml. The hla_new.xml is an updated version of the hla.xml and includes a new release tag containing version and date information for the release. In release 3.56.0 and onwards, hla_new.xml will replace hla.xml, and the older format archived.

### Other Files

The top-level directory contains the following files; 

* LICENSE.md - a file detailing the licensing of data included in the IPD-IMGT/HLA Database.
* README.md - This README file
* hla.dat.zip - An EMBL-ENA style format file containing data from the IPD-IMGT/HLA Database, see (Manual.md) for further details. 

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

For any other information please contact hla@alleles.org.

--------------------------------------------------------------------------------
 COPYRIGHT NOTICE
--------------------------------------------------------------------------------

We have chosen to apply the Creative Commons Attribution-NoDerivs License to all
copyrightable parts of our databases, which includes the sequence alignments.
This means that you are free to copy, distribute, display and make commercial
use of the databases in all legislations, provided you give us credit by citing
the following;

Barker DJ, Maccari G, Georgiou X, Cooper MA, Flicek P, Robinson J, Marsh SGE:
The IPD-IMGT/HLA Database.
Nucleic Acids Research (2023), 51:D1053-60

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
how your business can support the IPD-IMGT/HLA Database, please contact:
Anna Bedard, (Email: abedard [at] nmdp [dot] org), Be The Match Foundation.

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
