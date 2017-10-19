
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

Overview of Hi-C: cells are crosslinked with formaldehyde; DNA is digested with a restriction enzyme that leaves a 5′ overhang; the 5′ overhang is filled, including a biotinylated residue; and the resulting blunt-end fragments are ligated under dilute conditions that favor ligation events between the cross-linked DNA fragments. The resulting DNA sample contains ligation products consisting of fragments that were originally in close spatial proximity in the nucleus, marked with biotin at the junction. A Hi-C library is created by shearing the DNA and selecting the biotin-containing fragments with streptavidin beads. The library is then analyzed by using massively parallel DNA sequencing, producing a catalog of interacting fragments.

Statistical model: The read counts between a pair of loci are inversely proportional to the spatial distance between the two loci and the read counts follow a poisson distribution. The chromosome is modeled as a piecewise linear curve in a 3D space, specified by a spherical dot for each fragment or locus. 


#### By: dandanpeng
