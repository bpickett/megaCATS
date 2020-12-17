# megaCATS

##Background
The megaCATS code implements an iterative version of the meta-CATS algorithm [https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5040469/]. Briefly, this algorithm implements a chi-square test of independence AND a chi-square goodness of fit test. The p-values that are generated indicate aligned columns that contain a significant skew in the distribution of nucleotides or amino acids between 2 (or more) groups of sequences.

##Input
The algorithm requires a multiple sequence alignment in fasta format, as well as a table with the first column containing the same string name that is used in the alignment file. Subsequent columns indicate the metadata category as well as the assignment for each sample. **Note that the end of line characters in both files are required to be Unix-friendly and the metadata table should be tab-delimited.

Lines 15 and 16 of the metadata_parser.pl script need to be modified based on the name of the alignment and metadata file for each run.

##Running
Perl version <5.18 must be installed. Then use the command: 'perl metadata_parser.pl'

Sample data is provided in the folder such that directly running the metadata_parser.pl script should generate the appropriate output files.

##Results
All of the required intermediate files should be automatically generated and output files will be labeled appropriately.
