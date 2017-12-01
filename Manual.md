--------------------------------------------------------------------------------
IPD-IMGT/HLA HLA.dat User Manual
--------------------------------------------------------------------------------

This document describes the format and conventions used in the IPD-IMGT/HLA flat files. These files are included in the ftp directory on the EBI website. The formatting of the flat files and documentation below is based on guidelines provided by the EMBL Nucleotide User Manual.

The IPD-IMGT/HLA Database is composed of sequence entries. Each entry corresponds to a single contiguous sequence as contributed or reported in the literature. In some cases, entries have been assembled from several papers reporting overlapping sequence regions. Conversely a single paper often provides data for several entries.

### Structure of an Entry

The entries in the database are structured so as to be usable by human readers as well as by computer programs. The explanations, descriptions, classifications and other comments are in ordinary English, and the symbols and formatting employed for the base sequences themselves have been chosen for readability. Wherever possible, symbols familiar to molecular biologists have been used. At the same time, the structure is systematic enough to allow computer programs easily to read, identify, and manipulate the various types of data included.

Each entry in the database is composed of lines. Different types of lines, each with its own format, are used to record the various types of data which make up the entry. In general, fixed format items have been kept to a minimum, and a more syntax-oriented structure adopted for the lines. The two exceptions to this are the sequence data lines and the feature table lines, for which a fixed format was felt to offer significant advantages to the user. Users who write programs to process the database should not assume anything about the column placement of items on lines other than these two: all other line types are free-format.

Note that each line begins with a two-character line code, which indicates the type of information contained in the line. The currently used line types, along with their respective line codes, are listed below:

* ID - identification (begins each entry; 1 per entry)
* AC - accession number (1 per entry)
* DT - date (3 per entry)
* DE - description (>=1 per entry)
* KW - keyword (>=1 per entry)
* OS - organism species (1 per entry)
* OC - organism classification (1 per entry)
* RN - reference number (>=1 per entry)
* RC - reference comment (>=0 per entry)
* RP - reference positions (>=1 per entry)
* RX - reference cross-reference (>=0 per entry)
* RA - reference author(s) (>=1 per entry)
* RT - reference title (>=1 per entry)
* RL - reference location (>=1 per entry)
* DR - database cross-reference (>=1 per entry)
* FH - feature table header (>=1 per entry)
* FT - feature table data (>=0 per entry)
* CC - comments or notes (1 per entry)
* XX - spacer line (many per entry)
* SQ - sequence header (1 per entry)
* bb - (blanks) sequence data (>=1 per entry)
* // - termination line (ends each entry; 1 per entry)

A sample entry is shown below:

```ID   HLA00001; SV 1; standard; DNA; HUM; 3503 BP.
XX
AC   HLA00001;
XX
SV   HLA00001.1
XX
DT   01-AUG-1989 (Rel. 1.0.0, Created, Version 1)
DT   10-NOV-2017 (Rel. 3.30.0, Last Updated, Version 1)
XX
DE   HLA-A*01:01:01:01, Human MHC Class I sequence
XX
KW   Human MHC; HLA; Class I; HLA-A; Allele; HLA-A*01:01:01:01;
XX
OS   Homo Sapiens (human)
OC   Eukaryota; Metazoa; Chordata; Vertebrata; Mammalia; Eutheria; Primates;
OC   Catarrhini; Hominidae; Homo.
XX
CC   --------------------------------------------------------------------------
CC   IPD-IMGT/HLA Release Version 3.30.0
CC   --------------------------------------------------------------------------
CC   Copyrighted by the IPD-IMGT/HLA Database, Distributed under the Creative
CC   Commons Attribution-NoDerivs License, see;
CC   http://www.ebi.ac.uk/ipd/imgt/hla/licence.html for further details.
CC   --------------------------------------------------------------------------
XX
RN   [1]
RP   1-3503
RX   PUBMED; 3375250.
RA   Parham P, Lomen CE, Lawlor DA, Ways JP, Holmes N, Coppin HL, Salter RD,
RA   Wan AM, Ennis PD;
RT   "Nature of polymorphism in HLA-A, -B, and -C molecules";
RL   Proc Natl Acad Sci U S A 85:4005-9(1988).
XX
RN   [2]
RP   1-3503
RX   PUBMED; 2251137.
RA   Girdlestone J;
RT   "Nucleotide sequence of an HLA-A1 gene";
RL   Nucleic Acids Res 18:6701-6701(1990).
XX
RN   [3]
RP   1-3503
RX   PUBMED; 9349617.
RA   Laforet M, Froelich N, Parissiadis A, Pfeiffer B, Schell A, Faller B,
RA   Woehl-Jaegle ML, Cazenave JP, Tongio MM;
RT   "A nucleotide insertion in exon 4 is responsible for the absence of
RT   expression of an HLA-A*01 allele";
RL   Tissue Antigens 50:347-50(1997).
XX
RN   [4]
RP   1-3503
RX   PUBMED; 15140828.
RA   Stewart CA, Horton R, Allcock RJ, Ashurst JL, Atrazhev AM, Coggill P,
RA   Dunham I, Forbes S, Halls K, Howson JM, Humphray SJ, Hunt S, Mungall AJ,
RA   Osoegawa K, Palmer S, Roberts AN, Rogers J, Sims S, Wang Y, Wilming LG,
RA   Elliott JF, de Jong PJ, Sawcer S, Todd JA, Trowsdale J, Beck S;
RT   "Complete MHC haplotype sequencing for common disease gene mapping";
RL   Genome Res 14:1176-87(2004).
XX
RN   [5]
RP   1-3503
RX   PUBMED; 18193213.
RA   Horton R, Gibson R, Coggill P, Miretti M, Allcok RJ, Almeida J, Forbes S,
RA   Gilbert JGR, Halls K, Harrow JL, Hart E, Howe K, Jackson DK, Palmer S,
RA   Roberts AN, Sims S, Stewart CA, Traherne JA, Trevanion S, Wilming L, Rogers
RA   J, de Jong PJ, Elliott JF, Sawcer S, Todd JA, Trowsdale J, Beck S;
RT   "Variation analysis and gene annotation of eight MHC haplotypes: The MHC
RT   Haplotype Project";
RL   Immunogenetics 60:1-18(2008).
XX
RN   [6]
RP   1-3503
RX   PUBMED; 19735485.
RA   Zhu F, He Y, Zhang W, He J, He J, Xu X, Yan L;
RT   "Analysis of the complete genomic sequence of HLA-A alleles in the Chinese
RT   Han population.";
RL   Int J Immunogenet 36:351-360(2009).
XX
RN   [7]
RP   1-3503
RX   PUBMED; 24673518.
RA   Lu L, Xu YP;
RT   "Genomic full-length sequence of two HLA-A alleles, A*01:01:01:01 and
RT   A*01:03, identified by cloning and sequencing.";
RL   Tissue Antigens 83:423-424(2014).
XX
CC   --------------------------------------------------------------------------
CC   The sequence below is the official allele sequence as approved by the
CC   WHO Nomenclature Committee for Factors of the HLA System.
CC   Any cross references may differ from the sequence shown below.
CC   --------------------------------------------------------------------------
XX
DR   EMBL; AJ278305; AJ278305.1.
DR   EMBL; AL645935; AL645935.0.
DR   EMBL; CR759913; CR759913.0.
DR   EMBL; EU445470; EU445470.0.
DR   EMBL; GU812295; GU812295.0.
DR   EMBL; HG794373; HG794373.0.
DR   EMBL; M24043; M24043.1.
DR   EMBL; X55710; X55710.1.
DR   EMBL; Z93949; Z93949.1.
XX
FH   Key             Location/Qualifiers
FH
FT   source          1..3503
FT                   /organism="Homo sapiens"
FT                   /mol_type="genomic DNA"
FT                   /db_xref="taxon:9606"
FT                   /ethnic="Oriental, Caucasoid"
FT                   /cell_line="7550800303"
FT                   /cell_line="APD"
FT                   /cell_line="B4702"
FT                   /cell_line="COX"
FT                   /cell_line="LCL721"
FT                   /cell_line="MOLT-4"
FT                   /cell_line="PP"
FT   CDS             join(301..373,504..773,1015..1290,1870..2145,2248..2364,
FT                   2807..2839,2982..3029,3199..3203)
FT                   /codon_start=1
FT                   /gene="HLA-A"
FT                   /allele="HLA-A*01:01:01:01"
FT                   /product="MHC Class I HLA-A*01:01:01:01 sequence"
FT                   /translation="MAVMAPRTLLLLLSGALALTQTWAGSHSMRYFFTSVSRPGRGEPR
FT                   FIAVGYVDDTQFVRFDSDAASQKMEPRAPWIEQEGPEYWDQETRNMKAHSQTDRANLGT
FT                   LRGYYNQSEDGSHTIQIMYGCDVGPDGRFLRGYRQDAYDGKDYIALNEDLRSWTAADMA
FT                   AQITKRKWEAVHAAEQRRVYLEGRCVDGLRRYLENGKETLQRTDPPKTHMTHHPISDHE
FT                   ATLRCWALGFYPAEITLTWQRDGEDQTQDTELVETRPAGDGTFQKWAAVVVPSGEEQRY
FT                   TCHVQHEGLPKPLTLRWELSSQPTIPIVGIIAGLVLLGAVITGAVVAAVMWRRKSSDRK
FT                   GGSYTQAASSDSAQGSDVSLTACKV"
FT   UTR             1..300
FT   exon            301..373
FT                   /number="1"
FT   intron          374..503
FT                   /number="1"
FT   exon            504..773
FT                   /number="2"
FT   intron          774..1014
FT                   /number="2"
FT   exon            1015..1290
FT                   /number="3"
FT   intron          1291..1869
FT                   /number="3"
FT   exon            1870..2145
FT                   /number="4"
FT   intron          2146..2247
FT                   /number="4"
FT   exon            2248..2364
FT                   /number="5"
FT   intron          2365..2806
FT                   /number="5"
FT   exon            2807..2839
FT                   /number="6"
FT   intron          2840..2981
FT                   /number="6"
FT   exon            2982..3029
FT                   /number="7"
FT   intron          3030..3198
FT                   /number="7"
FT   exon            3199..3203
FT                   /number="8"
FT   UTR             3204..3503
SQ   Sequence 3503 BP; 666 A; 1012 C; 1070 G; 755 T; 0 other;
     caggagcaga ggggtcaggg cgaagtccca gggccccagg cgtggctctc agggtctcag        60
     gccccgaagg cggtgtatgg attggggagt cccagccttg gggattcccc aactccgcag       120
     tttcttttct ccctctccca acctacgtag ggtccttcat cctggatact cacgacgcgg       180
     acccagttct cactcccatt gggtgtcggg tttccagaga agccaatcag tgtcgtcgcg       240
     gtcgctgttc taaagtccgc acgcacccac cgggactcag attctcccca gacgccgagg       300
     atggccgtca tggcgccccg aaccctcctc ctgctactct cgggggccct ggccctgacc       360
     cagacctggg cgggtgagtg cggggtcggg agggaaaccg cctctgcggg gagaagcaag       420
     gggccctcct ggcgggggcg caggaccggg ggagccgcgc cgggaggagg gtcgggcagg       480
     tctcagccac tgctcgcccc caggctccca ctccatgagg tatttcttca catccgtgtc       540
     ccggcccggc cgcggggagc cccgcttcat cgccgtgggc tacgtggacg acacgcagtt       600
     cgtgcggttc gacagcgacg ccgcgagcca gaagatggag ccgcgggcgc cgtggataga       660
     gcaggagggg ccggagtatt gggaccagga gacacggaat atgaaggccc actcacagac       720
     tgaccgagcg aacctgggga ccctgcgcgg ctactacaac cagagcgagg acggtgagtg       780
     accccggccc ggggcgcagg tcacgacccc tcatccccca cggacgggcc aggtcgccca       840
     cagtctccgg gtccgagatc caccccgaag ccgcgggact ccgagaccct tgtcccggga       900
     gaggcccagg cgcctttacc cggtttcatt ttcagtttag gccaaaaatc cccccgggtt       960
     ggtcggggcg gggcggggct cgggggactg ggctgaccgc ggggtcgggg ccaggttctc      1020
     acaccatcca gataatgtat ggctgcgacg tggggccgga cgggcgcttc ctccgcgggt      1080
     accggcagga cgcctacgac ggcaaggatt acatcgccct gaacgaggac ctgcgctctt      1140
     ggaccgcggc ggacatggca gctcagatca ccaagcgcaa gtgggaggcg gtccatgcgg      1200
     cggagcagcg gagagtctac ctggagggcc ggtgcgtgga cgggctccgc agatacctgg      1260
     agaacgggaa ggagacgctg cagcgcacgg gtaccagggg ccacggggcg cctccctgat      1320
     cgcctataga tctcccgggc tggcctccca caaggagggg agacaattgg gaccaacact      1380
     agaatatcac cctccctctg gtcctgaggg agaggaatcc tcctgggttt ccagatcctg      1440
     taccagagag tgactctgag gttccgccct gctctctgac acaattaagg gataaaatct      1500
     ctgaaggagt gacgggaaga cgatccctcg aatactgatg agtggttccc tttgacaccg      1560
     gcagcagcct tgggcccgtg acttttcctc tcaggccttg ttctctgctt cacactcaat      1620
     gtgtgtgggg gtctgagtcc agcacttctg agtctctcag cctccactca ggtcaggacc      1680
     agaagtcgct gttcccttct cagggaatag aagattatcc caggtgcctg tgtccaggct      1740
     ggtgtctggg ttctgtgctc tcttccccat cccgggtgtc ctgtccattc tcaagatggc      1800
     cacatgcgtg ctggtggagt gtcccatgac agatgcaaaa tgcctgaatt ttctgactct      1860
     tcccgtcaga cccccccaag acacatatga cccaccaccc catctctgac catgaggcca      1920
     ccctgaggtg ctgggccctg ggcttctacc ctgcggagat cacactgacc tggcagcggg      1980
     atggggagga ccagacccag gacacggagc tcgtggagac caggcctgca ggggatggaa      2040
     ccttccagaa gtgggcggct gtggtggtgc cttctggaga ggagcagaga tacacctgcc      2100
     atgtgcagca tgagggtctg cccaagcccc tcaccctgag atggggtaag gagggagatg      2160
     ggggtgtcat gtctcttagg gaaagcagga gcctctctgg agacctttag cagggtcagg      2220
     gcccctcacc ttcccctctt ttcccagagc tgtcttccca gcccaccatc cccatcgtgg      2280
     gcatcattgc tggcctggtt ctccttggag ctgtgatcac tggagctgtg gtcgctgccg      2340
     tgatgtggag gaggaagagc tcaggtggag aaggggtgaa gggtggggtc tgagatttct      2400
     tgtctcactg agggttccaa gccccagcta gaaatgtgcc ctgtctcatt actgggaagc      2460
     accttccaca atcatgggcc gacccagcct gggccctgtg tgccagcact tactcttttg      2520
     taaagcacct gttaaaatga aggacagatt tatcaccttg attacggcgg tgatgggacc      2580
     tgatcccagc agtcacaagt cacaggggaa ggtccctgag gacagacctc aggagggcta      2640
     ttggtccagg acccacacct gctttcttca tgtttcctga tcccgccctg ggtctgcagt      2700
     cacacatttc tggaaacttc tctggggtcc aagactagga ggttcctcta ggaccttaag      2760
     gccctggctc ctttctggta tctcacagga cattttcttc ccacagatag aaaaggaggg      2820
     agttacactc aggctgcaag taagtatgaa ggaggctgat gcctgaggtc cttgggatat      2880
     tgtgtttggg agcccatggg ggagctcacc caccccacaa ttcctcctct agccacatct      2940
     tctgtgggat ctgaccaggt tctgtttttg ttctacccca ggcagtgaca gtgcccaggg      3000
     ctctgatgtg tctctcacag cttgtaaagg tgagagcttg gagggcctga tgtgtgttgg      3060
     gtgttgggtg gaacagtgga cacagctgtg ctatggggtt tctttgcgtt ggatgtattg      3120
     agcatgcgat gggctgttta aggtgtgacc cctcactgtg atggatatga atttgttcat      3180
     gaatattttt ttctatagtg tgagacagct gccttgtgtg ggactgagag gcaagagttg      3240
     ttcctgccct tccctttgtg acttgaagaa ccctgacttt gtttctgcaa aggcacctgc      3300
     atgtgtctgt gttcgtgtag gcataatgtg aggaggtggg gagagcaccc cacccccatg      3360
     tccaccatga ccctcttccc acgctgacct gtgctccctc tccaatcatc tttcctgttc      3420
     cagagaggtg gggctgaggt gtctccatct ctgtctcaac ttcatggtgc actgagctgt      3480
     aacttcttcc ttccctatta aaa                                              3503
//
```

### The ID Line

The ID (IDentification) line is always the first line of an entry. The general form of the ID line is:

`ID   entryname  dataclass; molecule; division; sequence length BP`

Entryname: The entry name is a unique identifier generated by the IPD-IMGT/HLA Database. This is used to identify each allele and to provide an accession number. EMBL accession numbers are not used, as although the sequence is derived from an EMBL entry the data is not the same and so new identifiers have been provided for the IPD-IMGT/HLA . The identifier follows the form 'HLA' then a six digit code.

Sequence Version Number: The sequence version included in this file.

Dataclass: The class of each entry is indicated on the first (ID) line of the entry. Entries distributed and made publicly available are of dataclass 'standard'.

Molecule Type: All entries are of the molecular type "DNA".

Database division: This indicates to which division the entry belongs. All entries are of the division "HUM".

Sequence length: The last item on the ID line is the length of the sequence (the total number of bases in the sequence). This number includes base positions reported as present but undetermined (coded as "N").

An example of a complete identification line is shown below:

`ID   HLA00001; SV 1; standard; DNA; HUM; 3503 BP.`

### The AC Line

The AC (ACcession number) line lists the accession number associated with the entry. An example of an accession number line is shown below:

`AC   HLA00001;`

Each accession number is terminated by a semicolon. Accession numbers are the primary means of identifying sequences providing a stable way of identifying entries from release to release. Accession numbers allow unambiguous citation of database entries.

An accession number is dropped from the database only when the data to which it was assigned have been completely removed from the database.

### The SV Line

The SV (Sequence Version number) line lists the version of the nucleotide sequence associated with the entry. An example of an SV line is shown below:

`SV   HLA00001.1;`

### The DT Line

The DT lines list when the allele was first assigned an official name. This corresponds to a date in the previous HLA DB. The DT lines also record the latest updates to an allele. There are two kinds of update, sequence and annotation. The DT line records when each of these was last updated and is displayed as follows: :

```DT   DD-MON-YYYY (Rel. #, Created, Version #)
DT   DD-MON-YYYY (Rel. #, Sequence Updated, Version #)
DT   DD-MON-YYYY (Rel. #, Current Release, Version #)
```

### The DE Line

The DE (Description) lines contain general descriptive information about the sequence stored. This may include the designations of genes for which the sequence codes, the region of the genome from which it is derived, or other information which helps to identify the sequence. This is derived from the EMBL description line, but a standard format is used for all entries. The format for a DE line is:

`DE   description`

### The KW Line

The KW (KeyWord) lines provide information which can be used to generate cross-reference indexes of the sequence entries based on functional, structural, or other categories deemed important. The keywords chosen for each entry serve as a subject reference for the sequence. The IPD-IMGT/HLA keywords include;

Human MHC
HLA
Class
Locus
Allele
The format for a kW line is:

```KW   keyword[; keyword ...].
```

### The OS and OC Lines

The OS and OC lines are set for all entries. The database currently contains only human sequences and so these lines are preset. The format of the OS and OC line is:

```OS   Homo Sapiens (human)
OC   Eukaryota; Metazoa; Chordata; Vertebrata; Mammalia; Eutheria; Primates;
OC   Catarrhini; Hominidae; Homo.
```
     
### The Reference Lines (RN, RP, RX, RA, RT, RL)

The references cited for an entry should be considered a pointer to the literature and not as assigning scientific credit for the elucidation of the sequence. These lines comprise the literature citations within the database. The citations provide access to the papers from which the data has been abstracted. The reference lines for a given citation occur in a block, and are always in the order RN, RP, RX, RA, RT, RL. Example of reference :

```RN   [1]
RP   1-1098
RX   PUBMED; 3375250.
RA   Parham P, Lomen CE, Lawlor DA, Ways JP, Holmes N, Coppin HL, Salter RD,
RA   Wan AM, Ennis PD;
RT   "Nature of polymorphism in HLA-A, -B, and -C molecules";
RL   PNAS USA 85:4005-4009(1988).
```

The RN (Reference Number) line gives a unique number to each reference Citation within an entry. The reference number is always enclosed in square brackets.

The RP (Reference Position) indicates which part(s) of the sequence are covered by the reference. Note that the numbering scheme is for the sequence as presented in the database entry (i.e. from 5' to 3' starting at 1), not the scheme used by the authors in the reference should it differ.

The RX (reference cross-reference) line type is a optional line type which contains a cross-reference to an external citation or abstract database. For example, if a journal citation exists in the PUBMED database, there will be an RX line pointing at the relevant PUBMED identifier.

The RA (Reference Author) lines list the authors of the paper (or other work) cited. All of the authors are included, and are listed in the order given in the paper. The names are listed surname first followed by a blank followed by initial(s) with periods. The author names are separated by commas and terminated by a semicolon. As many RA lines as necessary are included for each reference.

The RT (Reference Title) lines give the title of the paper (or other work) as exactly as is possible given the limitations of computer character sets. Note that the form used is that which would be used in a citation rather than that displayed at the top of the published paper. The title is enclosed in double quotes, and may be continued over several lines as necessary. The title lines are terminated by a semicolon.

The RL (Reference Location) line contains the conventional citation information for the reference. In general, the RL lines alone are sufficient to find the paper in question. They include the journal, volume number, page range and year for each paper. Journal names are abbreviated according to existing ISO standards (International Standard Serial Number). The format for the location lines is:

`RL   journal vol:pp-pp(year).`

### The DR Line

The DR (Database Cross-reference) line cross-references other databases which contain information related to the entry in which the DR line appears. For example, if the protein translation of a sequence exists in the UniProtKB/Swiss-prot database there will be a DR line pointing to the relevant UniProtKB/Swiss-prot entry. The format of the DR line is as follows:

`DR  database_identifier; primary_identifier; secondary_identifier.`

The first item on the DR line, the database identifier, is the abbreviated name of the data collection to which reference is made. The second item on the DR line, the primary identifier, is a pointer to the entry in the external database to which reference is being made. The third item on the DR line is the secondary identifier, if available, from the referenced database.
Feature Table Definitions

The feature table contains information about genes and gene products, as well as regions of biological significance reported in a sequence. It contains information on regions of the sequence that code for proteins and RNA molecules. The IPD-IMGT/HLA format is based on the EMBL flat file format. Currently the database provides only feature keys and qualifiers already used by the EMBL system.

### The FH Line

The first two lines of the feature table in the IPD-IMGT/HLA entries are feature header (FH) lines, specific to the EMBL flat file format. The FH (Feature Header) lines are present only to improve readability of an entry when it is printed or displayed on a terminal screen. The lines contain no data and may be ignored by computer programs. The format of these lines is always the same:

```
FH   Key             Location/Qualifiers
FH
```

The first line provides column headings for the feature table, and the second line serves as a spacer. If an entry contains no feature table (i.e. no FT lines - see below), the FH lines will not appear.

### The FT Line

The FT (Feature Table) lines provide a mechanism for the annotation of the sequence data. Regions or sites in the sequence which are of interest are listed in the table. In general, the features in the feature table represent signals or other characteristics reported in the cited references. In some cases, ambiguities or features noted in the course of data preparation have been included. The feature table is subject to expansion or change as more becomes known about a given sequence.

Features appear on FT lines. The line type code FT appears in columns 1-2 and columns 3-5 are blank. The feature key begins in column 6 and may be no more than 15 characters in length. The location begins in column 26. Feature qualifiers begin on subsequent FT lines at column 26. Location, qualifier, and continuation lines may extend from column 26 to 80. Each qualifier is added on a new line.

The first item on an FT line is the feature key. It starts in column 6 and can continue to column 24. The features provided in the first release of IPD-IMGT/HLA flat files contain only a small amount of information. Further feature keys will be added as annotation of entries progresses. Currently the feature keys listed are the source, CDS and exon information.

The second item on the FT line designates the location of the feature in the sequence. The location begins at column 26. Several conventions are used to indicate sequence location. Base numbers in locations refer to the numbering in the entry, which may differ from the official alignment sequences. The first base in the presented sequence is numbered base 1. Sequences are presented in the 5' to 3' direction. Locations can be described by either a single base or a contiguous span of bases. This is indicated by separating the start and end position by two periods (e.g., 23..79).

Feature qualifiers provide additional information about the individual feature key. The qualifiers take the form of a slash (/) followed by a name and, if applicable, an equal sign (=) and the qualifier value.

The qualifiers can convey many types of information. Text qualifier values are enclosed in double quotation marks. Citation or reference numbers for an entry are enclosed in square brackets ([]) to distinguish them from other numbers. A literal sequence of bases (e.g., "atgcatt") is enclosed in quotation marks. Literal sequences are distinguished from free text by context. Qualifiers that take free text as their values do not take literal sequences, and vice versa. The '/label=' qualifier takes a feature label as its qualifier. Although feature labels are optional, they allow unambiguous references to features. The feature label identifies a feature within an entry; when combined with the accession number and the name of the data bank from which it came, it is a unique tag for that feature.

The first release of the IPD-IMGT/HLA Database used only those qualifiers found in the EMBL feature qualifier definitions. These qualifiers are still used until additional specific qualifiers for the IPD-IMGT/HLA Database are implemented. The first release of the IPD-IMGT/HLA Database using the following feature qualifiers;

* organism - The scientific name of the organism that provided the sequenced genetic material, in all cases this is listed as Homo sapiens (human)
* cell_line - Cell line from which the sequence was obtained. The primary name given to the cell in accompanying HLA cell database.
* ethnic - Possible ethnic origin of the cells sequenced for this allele. This qualifier is devised from only the sequenced cells available.
* codon_start	Indicates the offset at which the first complete codon of a coding feature can be found, relative to the first base of that feature
* product - A general description of the gene product.
* partial - Differentiates between complete and partial region.
* pseudo - Used to mark up sequence that maps to an exon but is not expressed in the CDS
* translation - Translation provides a protein translation of the nucleotide sequence.
* number - A number to indicate the order of genetic elements (e.g., exons or introns) in the 5' to 3' direction.
* note - General qualifier for text descriptions, contains any comments or additional information

### The SQ Line

The nucleotide sequence data is generally present in the database as they have been submitted or published, subject to some conventions which have been adopted for the database as a whole. The sequences are always listed in the direction 5' to 3', regardless of the published order. Bases are numbered sequentially beginning with 1 at the 5' end of the sequence. Where possible a genomic sequence is provided, constructed from a number of different source sequence entries. The SQ (SeQuence header) line marks the beginning of the sequence data and gives a summary of its content. The sequence data line has a line code consisting of two blanks. The sequence is written 60 bases per line, in groups of 10 bases separated by a blank character, beginning at position 6 of the line. Columns 73-80 of each sequence line contain base numbers for easier reading and quick location of regions of interest. The numbers are right justified and indicate the number of the last base on each line. An example is:

```SQ   Sequence 1859 BP; 609 A; 314 C; 355 G; 581 T; 0 other;```

As shown, the line contains the length of the sequence in base pairs followed by its base composition. Bases other than A, C, G and T are grouped together as "other". An example of a data line is:

```     aaacaaacca aatatggatt ttattgtagc catatttgct ctgtttgtta ttagctcatt        60```

### The XX Line

The XX (spacer) line contains no data or comments. Its purpose is to make an entry easier to read on a page or terminal screen by setting off the various types of information in appropriate groupings. XX is used instead of blank lines to avoid confusion with the sequence data lines. The XX lines can always be ignored by computer programs.

### The CC Line

CC lines are free text comments about the entry, and may be used to convey any sort of information thought to be useful.

### The // Line

The // (terminator) line also contains no data or comments. It designates the end of an entry.

### Further Information

For more information about the database, queries (including website) or to subscribe to the IPD mailing lists please contact IPD Support. Please see our licence for our terms of use.
