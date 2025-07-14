
--------------------------------------------------------------------------------
 IPD-IMGT/HLA Database - Testing Branch
--------------------------------------------------------------------------------

The IPD-IMGT/HLA database is a specialist sequence database for sequences of the human histocompatibility complex. This directory contains test file formats or data for the IPD-IMGT/HLA database. 

--------------------------------------------------------------------------------
Testing Branch Disclaimer
--------------------------------------------------------------------------------
This branch is intended only for distribution of test files and formats. The files in this branch should not be used for clinical or diagnostic work and intended for testing purposes only. The files may contain errors or raise errors in any downstream processes. This is not a minimised branch and contains all files that are also found in the latest IPD-IMGT/HLA branch.

This branch contains no unreleased information and maintains the rigorous testing and requirements of the latest IPD-IMGT/HLA release branch. 

The updated files contained within the testing directory of this branch will be confined to new file formats or to syntactic file format changes.

--------------------------------------------------------------------------------
File Formats 
--------------------------------------------------------------------------------

Within the following folders, the various format types are explained briefly here:

### hla.xml.zip

The hla.xml.zip file has changed on this testing branch. Updates have been made to the `<hla_g_group>` and `<hla_p_group>` tags. The "status" attribute has now been removed and replaced with a "name" attribute containing the relevant group name and an "id" attribute with a unique identifier for each group.

Previously these tags appeared as:

```
      <hla_g_group status="A*01:01:01G">
      <hla_p_group status="A*01:01P">
```

An example of the new format is

```
      <hla_g_group name="A*01:01:01G" id="HGG00001"/>
      <hla_p_group name="A*01:01P" id="HPG00001"/>
```

The hla.xsd has been updated to reflect this change in the schema.

### Other Files

All other files are the same as the [Latest branch](https://github.com/ANHIG/IMGTHLA)

