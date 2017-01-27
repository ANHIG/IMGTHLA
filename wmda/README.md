--------------------------------------------------------------------------------
IPD-IMGT/HLA WMDA Read ME
--------------------------------------------------------------------------------

At the request of the IT Working Group of the World Marrow Donor Association (WMDA), we are making a number of computer readable files available. These files will document: the official WHO HLA Nomenclature, the relationships between serologically defined antigens and the relationships between HLA allele sequences and their serologically defined antigens. Updated versions of these files will be released every three months at the time new versions of the IPD-IMGT/HLA Database become available.
If you are regular user of these files and would like to be kept updated of any changes to the files, please email hla [at] alleles [dot] org and ask to be added to our WMDA mailing list.
Files for each individual release are located within appropriately named branch, for example files for Release 3.17.0 are located in the 3170 branch.

All five files have a short header with six lines of information, indicating:

File Name
Date file produced (YYYY-MM-DD)
Version (IPD-IMGT/HLA Version Number)
Origin of file (URL)
Repository (URL)
Author

--------------------------------------------------------------------------------
hla_nom.txt
--------------------------------------------------------------------------------

This file contains details of all current and deleted HLA antigens and alleles, and is sorted by locus and antigen/allele number:

HLA Locus
HLA Antigen or Allele name
Date assigned (YYYYMMDD)
Date deleted, if the name has now been abandoned (YYYYMMDD)
Antigen or Allele that the deleted allele was shown to be identical to
Reason for the Antigen or Allele to be deleted

This file includes six fields of information, each separated by a semi-colon (;). Please note that for HLA Antigen names assigned before November 1987, the dates given are only approximate.

--------------------------------------------------------------------------------
hla_nom_g.txt
--------------------------------------------------------------------------------

HLA alleles that have identical nucleotide sequences across the exons encoding the peptide binding domains (exon 2 and 3 for HLA class I and exon 2 only for HLA class II alleles) will be designated by an upper case ‘G’ which follows the first 3 fields of the allele designation of the lowest numbered allele in the group. The full list of these groups is available at the G Groups page. A computer readable version is also available, this file includes three fields of information, each separated by a semi-colon (;). Please note that several DRB alleles are not sequenced for the dimorphic nucleotide at position 357. It would therefore be inaccurate to assign a base to these sequences at this position. For this reason the sequences have been truncated to include only nucleotides 101 to 356, in the DRB analysis.

--------------------------------------------------------------------------------
hla_nom_p.txt
--------------------------------------------------------------------------------

This file contains details of all HLA Sequences having the same antigen binding domains. This analysis is performed on the polypeptide sequence, and for HLA Class I alleles, identity in the 'antigen binding domains' is based on identical protein sequences as encoded by exons 2 and 3. For HLA Class II alleles this is based on identical protein sequences as encoded by exon 2. HLA alleles having nucleotide sequences that encode the same protein sequence for the peptide binding domains (exon 2 and 3 for HLA class I and exon 2 only for HLA class II alleles) will be designated by an upper case ‘P’ which follows the 2 field allele designation of the lowest numbered allele in the group. The full list of these groups is available at the P Groups page. A computer readable version is also available, this file replaces the file previously called abdm.txt and includes three fields of information, each separated by a semi-colon (;). Several DRB alleles are not sequenced for the dimorphic nucleotide at position 357. It would therefore be inaccurate to assign a base to these sequences at this position. For this reason the sequences have been truncated to include only the translated sequence of nucleotides 101 to 356, in the DRB analysis.

--------------------------------------------------------------------------------
rel_ser_ser.txt 
--------------------------------------------------------------------------------

This file lists the relationships between all current serologically defined HLA antigens: broad antigens, split antigens and associated antigens.

HLA Locus
HLA Antigen name
Split Antigen
Associated Antigen

This file includes four fields of information, each separated by a semi-colon (;). The file lists only those antigens for which split or associated antigens exist. Multiple values are separated by a forward slash (/).

--------------------------------------------------------------------------------
rel_dna_ser.txt 
--------------------------------------------------------------------------------

This file contains details of all current HLA alleles and where known their unambiguous, possible or assumed serologically equivalent antigens.

Details of the unambiguous serology is defined from submissions to the WHO Nomenclature Committee for Factors of the HLA System (1) at the time an allele is submitted for naming, or from the WMDA HLA Dictionary 2004 (2). For Null alleles a value of zero (0) is given and for alleles with no corresponding antigen a question mark (?) is given.

In cases where an allele has been shown to be associated with more than one serologically defined antigen, these are indicated in the 'Possible Serology' field. Multiple values are separated by a forward slash (/). In cases where there is currently no information about the serological equivalent of an allele, the 'Assumed Serology' field contains the antigen equivalent as expected by the first two digits of the allele name.

This file contains details of all current HLA antigens and alleles, and is sorted by locus and allele number:

HLA Locus
HLA Allele Name
Unambiguous Serological Antigen associated with allele
Possible Serological Antigen associated with allele
Assumed Serological Antigen associated with allele
Expert assigned exceptions in search determinants of some registries

This file includes five fields of information, each separated by a semi-colon (;).

--------------------------------------------------------------------------------
md5checksum.txt 
--------------------------------------------------------------------------------

This file contains an md5 fingerprint for each file allowing verification of the downloads.

--------------------------------------------------------------------------------
Release Archive
--------------------------------------------------------------------------------

The release archive is now maintained as a git repository and available at https://github.com/ANHIG/IMGTHLA. This repository contains a branch for each database release and a Latest branch which contains the most recent files.