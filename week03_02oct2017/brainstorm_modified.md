
# Part 1 - Brainstorm: Statistics

## Distributions
### e.g., Gaussian, Poisson, ..

## Statistical Models
## Methods for Estimation
## Methods for Hypothesis Testing

# Part 2 - Brainstorm: Technologies in Biology

## microarray, sequencing, etc.

## In-class exercise 1 (1 technology for each row): microarray, Illumina sequencing, 3rd generation sequencing, cytometry, mass spectrometry

### Goal: 
#### produce a 2-3 point summary
#### links to a few (<5) good resources
#### create a markdown file for it; we will try a "group assignment" via GitHub

# Part 3 - Brainstorm: Applications in genomics 

### e.g., gene expression

# Part 4 - Brainstorm: Linking Technologies to Applications to Statistics (mainstream)

## e.g., microarray -> gene expression -> normally distributed (log intensities)

## In-class exercise 2 (in groups/rows): 
### Goal: make the link between technologies, what is measured, statistical models used
### For example:
##### RNA-seq: sequencing -> gene expression -> ?
##### BS-seq: bisulphite + sequencing -> DNA methylation -> ?
##### ChIP-seq: sequencing -> protein/DNA interactions -> ?

GBS(Genotyping by Sequencing) -> Illumina Sequencing -> MLM (Mixed Linear Model)

# Part 5 - Brainstorm: Methods/algorithms/data structures that are associated more to computer science

### Part 6: Microarrays

## Background and application 

A microarray is the convergence of DNA hybridization, fluorescence microscopy, and solid surface DNA capture. The setup consists of DNA oligonucleotide probes which are immobilized on a solid surface and capture the complementary sequences contained in the sample. The two main applications of this technology are the quantification of gene expression and the detection of SNPs (single nucleotide polymorphisms) between samples. 
 
## Technology -> application -> statistics
* Technology: Microarray
* Application: Testing if expression profiles between samples differ for selected genes.
* Statistics: Sum of squared univariate t-statistics, number of genes univariately significant at α level.
https://brb.nci.nih.gov/techreport/CIT_course_McShanePolley_May162011.pdf


## Links 

#### (Mark's edit: I'm not sure I understand this one)  Technology=microarray Application:? Statistics:?

Expression quantification: https://www.cs.nyu.edu/cs/faculty/mishra/COURSES/01.COBIO/expprof-Trent1999.pdf
SNP array: http://www.genomics.liv.ac.uk/tryps/Key_Papers/paperofmonthmay1.pdf
Data processing: http://www.cs.cmu.edu/~zivbj/class05/reading/norm.pdf

#### By: cstatzer, sorjuela





### Flow cytometry -> Cell developement -> Wanderlust algorithm

#### Summary

Wanderlust is a graph-based trajectory detection algorithm that receives multiparameter single-cell events as input and maps them onto a one-dimensional developmental trajectory. Cells are ordered along a trajectory that represents their most likely placement along a developmental path. [Source](https://www.c2b2.columbia.edu/danapeerlab/html/wanderlust.html)

#### By: s-a-m-u, martinholub



### BS-seq: bisulphite + sequencing -> DNA methylation -> Beta-binomial distribution 

#### Summary

Bisulfite sequencing uses bisulfite treatment of DNA to determine its pattern of methylation. The methylated read counts are often modeled by a beta-binomial distribution, which accounts for both the biological and sampling variations. 

#### Source:

[Using beta-binomial regression for high-precision differential methylation analysis in multifactor whole-genome bisulfite sequencing experiments.](https://www.ncbi.nlm.nih.gov/pubmed/24962134)

[Differential methylation analysis for BS-seq data under general experimental design](https://academic.oup.com/bioinformatics/article/32/10/1446/1743267)

#### By: churchillcui


### Technology (TAm Seq - Tagged-amplicon deep sequencing )

#### What is it?
TAM-Seq allows targeted two-step amplification and deep sequencing of entire genes to detect mutations in ctDNA.

First a general amplification step is performed using primers that span the entire gene of interest in 150-200bp sections. Then, a microfluidics system is used to attached adaptors with a unique identifier to each amplicon to further amplify the DNA in parallel singleplex reactions. 

It is a low-cost, high-throughput method could facilitate analysis of circulating DNA as a noninvasive "liquid biopsy" for personalized cancer genomics.

![TAm Sequencing. (Taken from paper: Analytical performance and validation of an
enhanced TAm-Seq™ circulating tumour DNA
sequencing assay across two laboratories
Poster 29 NCRI, November 2016)](tamseq.png)

#### Technique used

Pre-amplification, Single-plex PCR(Polymerase chain reaction)/Amplicon PCR, Barcoding PCR

#### What is measured?

Sensitivity, Specificity, Mutation.

For eg: To assess sensitivity, Horizon Tru-Q 6 (Low input,
undiluted, AF majority at 2%-2.5%) and Tru-Q 7 samples
(Medium, undiluted AF majority at 1%-1.25% & High,
diluted to AF 0.25%-0.3125%) were sheared to ~200bp to
mimic fragmented cfDNA. Dilutions were prepared
using Horizon Tru-Q 0 wild-type DNA as diluent.

* TAm-Seq technique was shown to successfully identify mutations scattered in the TP53 tumor suppressor gene in advanced ovarian cancer patients. The sensitivity of this technique is 1 in 50.

#### What are the statistical models used?

Poisson Distribution

Measured: Co-relation, false discovery rate, RMS error rate, Mean, Variance.

Reference standards and plasma DNA controls are also used to demonstrate the sensitivity, specificity and quantitative accuracy of this ctDNA analysis platform.

#### Application
* TAm-Seq can be used to noninvasively identify the origin of metastatic relapse in a patient with multiple primary tumors. 
* It also helped to identify, an EGFR mutation  in plasma, not found in an initial ovarian biopsy. 
* TAm-Seq can be used to monitor tumor dynamics.

#### Sources
[http://www.medicinalgenomics.com/wp-content/uploads/2011/12/Circ_tumor_DNA-Sci-Transl-Med-2012-Forshew-136ra68.pdf]

[http://stm.sciencemag.org/content/4/136/136ra68]

[http://www.inivata.com/wp-content/uploads/2016/11/inivata-ncri-poster.pdf]

[http://cancerres.aacrjournals.org/content/76/14_Supplement/3639]

#### By: dhivyaCS



### Hi-C

This technique is used to analyze the 3-dimensional spatial organization of chromatin. It quantifies the number of interactions between genomic loci that are nearby in 3D space but may be separated by many necleotides in the linear genome. The spatial proximity maps of chromatin confirms the presence of chromosome territories like compartment A/B and topological associated domains(TADs).

#### Link

Hi-C seq: formaldehyde + sequencing -> three-dimensional chromosome architecture -> Bayesian model(Bayesian 3D constructor for Hi-C data), Markow-chain Monte Carlo methods

#### Details

Statistical model: The read counts between a pair of loci are inversely proportional to the spatial distance between the two loci and the read counts follow a poisson distribution. The chromosome is modeled as a piecewise linear curve in a 3D space, specified by a spherical dot for each fragment or locus. 
Overview of Hi-C: cells are crosslinked with formaldehyde; DNA is digested with a restriction enzyme that leaves a 5′ overhang; the 5′ overhang is filled, including a biotinylated residue; and the resulting blunt-end fragments are ligated under dilute conditions that favor ligation events between the cross-linked DNA fragments. The resulting DNA sample contains ligation products consisting of fragments that were originally in close spatial proximity in the nucleus, marked with biotin at the junction. A Hi-C library is created by shearing the DNA and selecting the biotin-containing fragments with streptavidin beads. The library is then analyzed by using massively parallel DNA sequencing, producing a catalog of interacting fragments.
#### By: dandanpeng






### Ribosome Profiling

Ribosome profiling, or Ribo-Seq (also named Ribosome footprinting), is an adaptation  to work with next generation sequencing that uses specialized messenger RNA (mRNA) sequencing to determine which mRNAs are being actively translated. It produces a “global snapshot” of all the ribosomes active in a cell at a particular moment, known as a translatome. Consequently, this enables identifying the location of translation start sites, the complement of translated ORFs in a cell or tissue, the distribution of ribosomes on a messenger RNA, and the speed of translating ribosomes.

#### Linking Technologies to Applications to Statistics 

Ribo seq -> Identifying translated mRNA -> normally distributed

#### By: pmeili, stusas

#### References:
[1: http://science.sciencemag.org/content/324/5924/218](http://science.sciencemag.org/content/324/5924/218)








### technology -> application -> statistics
#### Illumina sequencing -> GWAS (Genome Wide Association Study) -> Linear Mixed Model

Next-generation-sequencing data has been utilized in many different researches, such as gene prediction and genome wide association study, which based on linkage disequilibrium. In GWAS, rather than only focus on a specific genetic region which researchers thought is related to targeted trait, researchers use SNPs (Single Nucleotide Polymorphisms) as marker, and take the whole genome-wide region into account. They compare the sequencing data of samples which have a particular trait between samples without this trait to identify SNPs which are associated with the trait. GWAS usually performs efficient in human genome, but when researchers use GWAS in plant genomes, the population structure often hinders our analysis. Hence, Linear Mixed Model is an usedful statistics tool to reduce the influence of population structure, and control false positives in results.

#### Reference:
 [1] Yu J, Pressoir G, Briggs W H, et al. A unified mixed-model method for association mapping that accounts for multiple levels of relatedness.[J]. Nature Genetics, 2006, 38(2):203.
 [2] Atwell S, Huang Y S, Vilhjálmsson B J, et al. Genome-wide association study of 107 phenotypes in Arabidopsis thaliana inbred lines.[J]. Nature, 2010, 465(7298):627-31.
 [3] Vanraden P M. Efficient methods to compute genomic predictions.[J]. Journal of Dairy Science, 2008, 91(11):4414.

#### By: LeaveLeaves








### RT-qPCR
Quantitative reverse transcription PCR (RT-qPCR) is used when the starting material is RNA. In this method, RNA is first transcribed into complementary DNA (cDNA) by reverse transcriptase from total RNA or messenger RNA (mRNA). The cDNA is then used as the template for the qPCR reaction. RT-qPCR is used in a variety of applications including gene expression analysis, RNAi validation, microarray validation, pathogen detection, genetic testing, and disease research.[from ThermoFisher](https://www.thermofisher.com/us/en/home/brands/thermo-scientific/molecular-biology/molecular-biology-learning-center/molecular-biology-resource-library/basic-principles-rt-qpcr.html)

#### link (technology -> application -> statistics)
RT-qPCR: RNA reverse transcription + qPCR reaction(cDNA as template) >-  gene regulation  >- Median normalization[Reference paper](http://www.sciencedirect.com/science/article/pii/S1046202310000472)
RT-qPCR: RNA reverse transcription + qPCR reaction(cDNA as template) >-  data quality control  >- simple linear regression model[Reference link](http://qrt-pcr-applications.com)

#### By: TaoDFang, orangelc1221, uraniumyo







### CirSeq

#### Link

CirSeq -> Virus mutation frequency analysis -> Standard error of binomial distribution

#### Method Summary

Circle sequencing (CirSeq) is a method used to reduce errors of next generation sequencing by circularizing RNA and reverse transcribing it to cDNA. While sequencing errors will not be shared between repeats, the mutations of the viral RNA should be present in all of them. This results in a framework to remove PCR and reverse transcription errors (by majority vote) and is used to calculate much more accurate viral mutation frequency.

#### Statistical analysis

From [1] :

Measurement accuracy of individual mutation frequencies at each position of the genome is affected by:

* depth of coverage at the position
* its true mutation frequency.

The error can be approximated by standard error of binomial distribution

$SE = \sqrt{\frac{p(1-p)}{n}}$ ,

|                       Where                     
|-----|:------------------------------------------ 
|  n  | coverage depth                            
|  p  | mutation frequency measured by sequencing 


##### **References**

[1] Acevedo A, Brodsky L, Andino R. Mutational and fitness landscapes of an RNA virus revealed through population sequencing. Nature. 2014 Jan 30;505(7485):686.   
[2] Posada-Cespedes S, Seifert D, Beerenwinkel N. Recent advances in inferring viral diversity from high-throughput sequencing data. Virus research. 2016 Sep 28.   
[3] Simple introduction: http://www.virology.ws/tag/cirseq/   

#### By: jugne

