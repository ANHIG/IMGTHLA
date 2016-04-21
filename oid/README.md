## ISO HL7 OIDs

The IMGT/HLA Database allows you to retrieve information upon a specific HLA allele as named in the WHO Nomenclature Committee for Factors of the HLA System. All HLA alleles have now received ISO standard HL7 Registered IDs. The HL7 designations use the following syntax:

+ 2.16.840.1.113883.13.252; HL7 Registered Organisational OID
+ .1;  Gene System ID; . 1 for HLA 
+ .1; Resolution Level; i.e. 1 for allele level, 2 for antigen level [other resolutions are been investigated for example G-group designations, and may be added later] 
+ .1; Allele ID; The IMGT/HLA Database accession number with the HLA and leading zeroes removed. For example HLA-A*01:01:01:01 this would be 1, as the accession number is HLA00001

### Example OIDs are listed below;

+ HLA-A*01:01:01:01 (HLA00001) is assigned the OID 2.16.840.1.113883.13.252.1.1.1
+ HLA-B*15:01:01:01 (HLA00162) is assigned the OID 2.16.840.1.113883.13.252.1.1.162
+ HLA-C*04:09N (HLA01451) is assigned the OID 2.16.840.1.113883.13.252.1.1.1451
+ The serologically recognised HLA specificity A1 is assigned the OID 2.16.840.1.113883.13.252.1.2.1
+ The serologically recognised HLA specificity Bw4 is assigned the OID 2.16.840.1.113883.13.252.1.2.89
+ The serologically recognised HLA specificity DR51 is assigned the OID 2.16.840.1.113883.13.252.1.2.148

The ISO OIDs are listed in the allele reference pages of the IMGT/HLA Database and are be searchable using the OID in the URL:

http://www.ebi.ac.uk/cgi-bin/ipd/imgt/hla/get_allele.cgi?2.16.840.1.113883.13.252.1.1.1

Please see http://www.ebi.ac.uk/ipd/imgt/hla/isoid.html for further details.
