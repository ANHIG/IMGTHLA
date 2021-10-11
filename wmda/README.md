--------------------------------------------------------------------------------
IPD-IMGT/HLA WMDA Read ME
--------------------------------------------------------------------------------

At the request of the IT Working Group of the World Marrow Donor Association (WMDA), we are making a number of computer readable files available. These files will document: the official WHO HLA Nomenclature, the relationships between serologically defined antigens and the relationships between HLA allele sequences and their serologically defined antigens. Updated versions of these files will be released every three months at the time new versions of the IPD-IMGT/HLA Database become available.
If you are regular user of these files and would like to be kept updated of any changes to the files, please email hla [at] alleles [dot] org and ask to be added to our WMDA mailing list.
Files for each individual release are located within appropriately named branch, for example files for Release 3.17.0 are located in the 3170 branch.

All five files have a short header with six lines of information, indicating:

* File Name
* Date file produced (YYYY-MM-DD)
* Version (IPD-IMGT/HLA Version Number)
* Origin of file (URL)
* Repository (URL)
* Author

--------------------------------------------------------------------------------
hla_nom.txt
--------------------------------------------------------------------------------

This file contains details of all current and deleted HLA antigens and alleles, and is sorted by locus and antigen/allele number:

* HLA Locus
* HLA Antigen or Allele name
* Date assigned (YYYYMMDD)
* Date deleted, if the name has now been abandoned (YYYYMMDD)
* Antigen or Allele that the deleted allele was shown to be identical to
* Reason for the Antigen or Allele to be deleted

This file includes six fields of information, each separated by a semi-colon (;). Please note that for HLA Antigen names assigned before November 1987, the dates given are only approximate.

--------------------------------------------------------------------------------
hla_nom_g.txt
--------------------------------------------------------------------------------

The use of Sequence Based Typing (SBT) as a method for defining the HLA type is well documented, most SBT typing strategies currently employed use the exon 2 and exon 3 sequences for HLA class I analysis and exon 2 alone for HLA class II analysis. Due to the heterozygous nature of the SBT analysis the combinations of many pairs of alleles may give an ambiguous typing result. This document includes a list of all alleles which are identical over exons 2+3 for HLA class I and exon 2 for HLA class II, in addition all ambiguous results obtained when using all alleles in the current release.

From 01 April 2010, all groups of HLA alleles that have identical nucleotide sequences across the exons encoding the peptide binding domains (exon 2 and 3 for HLA class I and exon 2 only for HLA class II alleles) are designated by an upper case ‘G’ which follows the three-field allele designation of the lowest numbered allele in the group.

The algorithm used to generate the G groups does include alleles that contain unsequenced regions. For these alleles the sequence of an alternate allele has been used to extend the sequence over this region. Where possible a genomic or silent variant of the unsequenced allele is used. When this is not possible an alternate allele from within the same first field group is used and only used when there is a high probability that the sequence used would be shown to be correct if the region was fully sequenced. The list of alleles containing unsequenced regions and the alternate alleles used to infer the missing sequence are detailed in this document. We recognise that future sequencing of unsequenced regions may reveal disparity between the predicted sequence and the newly sequenced region. We therefore welcome any further information, which will help improve analysis of these regions. Following the modification or deletion of an allele sequence a G group may contain only a single allele. In these cases the G group is retained and can refer to single allele, the G group may expand at a later date if new alleles are shown to have an identical nucleotide sequences across the exons encoding the peptide binding domains.

From IPD-IMGT/HLA Release 3.30, the generation of G groups and ambiguous combinations of DRB alleles was extended to include the complete sequences of exon 2. Previous versions contained only the sequence from nucleotides 101 to 356 due to a polymorphism at position 357 that could not be accurately predicted. Phylogenetic analysis of the increased number of DRB exon 2 sequences has been used to allow us to predict this position in alleles that are unsequenced for position 357. The extension of the sequence analysed has meant that a number of G groups previously assigned are no longer present in the output due to polymorphisms found between nucleotides 357 to 370. The following groups are no longer listed in the DRB tables as they now contain only a single allele. The identification of new alleles may cause these groups to be included in the tables again at a later date. 

DRB1\*03:05:01G, DRB1\*04:17:01G,  DRB1\*08:04:02G, DRB1\*11:01:03G, DRB1\*11:08:01G, DRB1\*11:10:01G, DRB1\*11:65:01G, DRB1\*13:12:01G, DRB1\*13:14:01G, DRB1\*13:23:01G, DRB1\*13:33:02G, DRB1\*13:66:01G, DRB1\*14:07:01G, DRB1\*14:12:01G

From IPD-IMGT/HLA Release 3.28.0 the G group DPA1\*02:02:01G was removed as the allele DPA1\*02:02:01G was shown to be deleted. The G group DPA1\*02:07:01G was added which contained DPA1\*02:07:01:01 and DPA1\*02:07:01:02, note the DPA1\*02:07 allele was previously included in the DPA1\*02:02:01G listing. 

Following the modification or deletion of an allele sequence an allele may be removed from a G or P group. This may result in the group only containing a single allele. In these cases the group is retained and can refer to single allele, the group may expand at a later date if new alleles are shown to belong to the group. If the allele that the group was initially named after is removed from the group, the group will retain the original name, and not be renamed to match the revised listing. If an allele is added to the group, with a lower number designation, the group will again retain it's original name, and not be revised to match the new listing. For this reason it is possible to have a G or P group designation that no refers to allele groups that are not represented by the group designation.

--------------------------------------------------------------------------------
hla_nom_p.txt
--------------------------------------------------------------------------------

This file contains details of all HLA Sequences having the same antigen binding domains. This analysis is performed on the polypeptide sequence, and for HLA Class I alleles, identity in the 'antigen binding domains' is based on identical protein sequences as encoded by exons 2 and 3. For HLA Class II alleles this is based on identical protein sequences as encoded by exon 2. HLA alleles having nucleotide sequences that encode the same protein sequence for the peptide binding domains (exon 2 and 3 for HLA class I and exon 2 only for HLA class II alleles) will be designated by an upper case ‘P’ which follows the 2 field allele designation of the lowest numbered allele in the group. The full list of these groups is available at the P Groups page. A computer readable version is also available, this file replaces the file previously called abdm.txt and includes three fields of information, each separated by a semi-colon (;). Several DRB alleles are not sequenced for the dimorphic nucleotide at position 357. It would therefore be inaccurate to assign a base to these sequences at this position. For this reason the sequences have been truncated to include only the translated sequence of nucleotides 101 to 356, in the DRB analysis.

Following the modification or deletion of an allele sequence an allele may be removed from a P group, please see the section above for further details. 

--------------------------------------------------------------------------------
rel_ser_ser.txt 
--------------------------------------------------------------------------------

This file lists the relationships between all current serologically defined HLA antigens: broad antigens, split antigens and associated antigens.

* HLA Locus
* HLA Antigen name
* Split Antigen
* Associated Antigen

This file includes four fields of information, each separated by a semi-colon (;). The file lists only those antigens for which split or associated antigens exist. Multiple values are separated by a forward slash (/).

--------------------------------------------------------------------------------
rel_dna_ser.txt 
--------------------------------------------------------------------------------

This file contains details of all current HLA alleles and where known their unambiguous, possible or assumed serologically equivalent antigens.

Details of the unambiguous serology is defined from submissions to the WHO Nomenclature Committee for Factors of the HLA System (1) at the time an allele is submitted for naming, or from the WMDA HLA Dictionary 2004 (2). For Null alleles a value of zero (0) is given and for alleles with no corresponding antigen a question mark (?) is given.

In cases where an allele has been shown to be associated with more than one serologically defined antigen, these are indicated in the 'Possible Serology' field. Multiple values are separated by a forward slash (/). In cases where there is currently no information about the serological equivalent of an allele, the 'Assumed Serology' field contains the antigen equivalent as expected by the first two digits of the allele name.

This file contains details of all current HLA antigens and alleles, and is sorted by locus and allele number:

* HLA Locus
* HLA Allele Name
* Unambiguous Serological Antigen associated with allele
* Possible Serological Antigen associated with allele, where multiple serologies are reported
* Assumed Serological Antigen associated with allele

This file includes five fields of information, each separated by a semi-colon (;).

--------------------------------------------------------------------------------
md5checksum.txt 
--------------------------------------------------------------------------------

This file contains an md5 fingerprint for each file allowing verification of the downloads.

--------------------------------------------------------------------------------
Release Archive
--------------------------------------------------------------------------------

The release archive is now maintained as a git repository and available at https://github.com/ANHIG/IMGTHLA. This repository contains a branch for each database release and a Latest branch which contains the most recent files.
