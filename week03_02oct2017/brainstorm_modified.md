
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