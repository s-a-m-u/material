
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

# Part 6 - Pick another "technology" (from those above, from [1] or another technology) to briefly describe

## In-class exercise 3 (in groups): 
### Goal: 
#### write ~2 sentences about what the method does
#### again, make the link (technology -> application -> statistics)
#### list the github usernames of everyone in your group
#### submit a pull request to brainstorm_modified.md

[1] [https://liorpachter.wordpress.com/seq/](https://liorpachter.wordpress.com/seq/)

### technology -> application -> statistics
#### Illumina sequencing -> GWAS (Genome Wide Association Study) -> Linear Mixed Model

Next-generation-sequencing data has been utilized in many different researches, such as gene prediction and genome wide association study, which based on linkage disequilibrium. In GWAS, rather than only focus on a specific genetic region which researchers thought is related to targeted trait, researchers use SNPs (Single Nucleotide Polymorphisms) as marker, and take the whole genome-wide region into account. They compare the sequencing data of samples which have a particular trait between samples without this trait to identify SNPs which are associated with the trait. GWAS usually performs efficient in human genome, but when researchers use GWAS in plant genomes, the population structure often hinders our analysis. Hence, Linear Mixed Model is an usedful statistics tool to reduce the influence of population structure, and control false positives in results.

#### Reference:
#### [1] Yu J, Pressoir G, Briggs W H, et al. A unified mixed-model method for association mapping that accounts for multiple levels of relatedness.[J]. Nature Genetics, 2006, 38(2):203.
#### [2] Atwell S, Huang Y S, Vilhjálmsson B J, et al. Genome-wide association study of 107 phenotypes in Arabidopsis thaliana inbred lines.[J]. Nature, 2010, 465(7298):627-31.
#### [3] Vanraden P M. Efficient methods to compute genomic predictions.[J]. Journal of Dairy Science, 2008, 91(11):4414.

### Github user name: LeaveLeaves
