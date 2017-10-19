
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

# Part 6 - Pick another "technology" (from those above, from [1] or another technology) to briefly describe

## In-class exercise 3 (in groups): 
### Goal: 
#### write ~2 sentences about what the method does
#### again, make the link (technology -> application -> statistics)
#### list the github usernames of everyone in your group
#### submit a pull request to brainstorm_modified.md



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


