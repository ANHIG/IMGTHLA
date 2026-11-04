# HLA XML Beta Branch

> [!CAUTION]
> This is a development branch providing early access to potential new features that are being considered, there is no expected release date for these files.

Once a decision is made to include any of these proposed changes into the standard releases files, the testing branch would be updated one release before inclusion into the Latest branch.  
>
> All files in this directory are subject to change, and as such users should be aware they may change at any time.

These files are designed purely for testing purposes and to get feedback on new features, and are **not for clinical use**.
>
> If you have feedback on improvements or further updates to these files, please contact the IPD team at [ipdsubs@anthonynolan.org](mailto:ipdsubs@anthonynolan.org)

## Overview
Following user feedback and requests for features from the wider HLA community we are considering making updates to the database XML files.

This development branch contains proposed updates to the hla.xml, the inclusion of a new hla_alignment.xml and relevant information related to both files.

## Proposal

The proposed changes to the XML file format, and the new files, are described in [`hla_xml_proposal.md`](hla_xml_proposal.md).

## Contents

This branch contains only one directory with the following structure:

```
<xml_beta>/
├── README.md
├── hla_xml_proposal.md # Our proposal document
└── <xml_files>/
	├── hla.xml # Updated HLA XML file
	├── hla.xsd # Schema for hla.xml
	├── hla_alignment.xml # New XML file containing alignment information
	└── hla_alignment.xsd # Schema for hla_alignment.xml
```

The files contained within the `<xml_files>/` subdirectory only contain a subset of alleles and are not representative of the whole database. This was done to allow the structure to be reviewed rather than the data.

> [!CAUTION]
>
> Please note that this branch only contains the updated structure XML files and no other database information.
