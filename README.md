# VGICs

Reincarnation of our original work, that was published in Journal of Proteome Research ( DOI: 10.1021/acs.jproteome.9b00121), in Python.

## Pipeline

### Data Retrieval & Merging

1. Data regarding missense SNPs of human VGICs were retrieved from the FTP servers of UniProtKB & ClinVardb
2. A common reference code for the characterization of SNPs' clinical significance was adapted
3. The 2 datasets were merged to form a conlusive & non-redudant dataset of missense SNPs for human VGICs

### Mapping of SNPs on Biologically Significant Regions

Data regarding topological features of VGICs were retreived from UniProtKB/SwissProt. Regions of VGICs were grouped using the following reference code:
1. VSD (S1 - S4 transmembrane(tm) regions)
2. PL (pore loops, loops between 5th and 6th tm-segments)
3. S5 - S6 tm-regions
4. N-terminal
5. C-terminal
6. IL (intracellular loops)
7. EL (extracellular loops)

Using this “topological profile”, all polymorphisms, pathogenic, and unclassified SNPs were mapped on the sequences of VGICs.

### Categorize SNPs according to their biophysical attributes

SNPs and normal amino acid residues were grouped to each of the following groups according to their biophysical properties:
1. non-polar
2. polar 
3. charged

### Descriptive analysis

The following practices were applied to the final dataset of missense SNPs to evaluate the statistical significance of our findings:
1. Raw & normalized distribution of total polymorphisms & pathogenic SNPs per topological domain 
2. Normalization was conducted in respect to the length of each topological region (e.g if there are 5 SNPs in a region of 20 residues, after the normalizion it would be transformed to 25/100)
3. Two-way ANOVA with replication to examine the connection between an SNP’s pathogenicity status and its appearance in transmembrane regions
4. Binomial Generalized Linear Model Regression (GLM) to investigate the distribution of polymorphisms and pathogenic mutations in different topological regions of biological significance & distinquish the ones that statistically significant
5. Binomial Generalized Linear Model Regression(GLM) to investigate the distribution of polymorphisms and pathogenic mutations in different topological regions of biological significance & distinquish the ones that statistically significant
6. Random sampling with replacement (bootstrap) to examine the statistical significance of the amino acid substitutions

### Assocation of pathogenic SNPs with diseases

Data regarding impliaction with disease were retrieved from UniProtKB and ClinVar
Diseases were grouped to four categories according to the primary organ system that was affected:
1. ND : neuron disease
2. MD : muscle disease
3. HMD : heart muscle disease
4. Other
