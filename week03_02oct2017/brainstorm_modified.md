
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

[1] [https://liorpachter.wordpress.com/seq/](https://liorpachter.wordpress.com/seq/)

### Introduction

Hi-C technique is used to analyze the 3-dimensional spatial organization of chromatin. It quantifies the number of interactions between genomic loci that are nearby in 3D space but may be separated by many necleotides in the linear genome. The spatial proximity maps of chromatin confirms the presence of chromosome territories like compartment A/B and topological associated domains(TADs).

### Link

Hi-C seq: formaldehyde + sequencing -> three-dimensional chromosome architecture -> Bayesian model(Bayesian 3D constructor for Hi-C data), Markow-chain Monte Carlo methods

### Details

Overview of Hi-C: cells are crosslinked with formaldehyde; DNA is digested with a restriction enzyme that leaves a 5′ overhang; the 5′ overhang is filled, including a biotinylated residue; and the resulting blunt-end fragments are ligated under dilute conditions that favor ligation events between the cross-linked DNA fragments. The resulting DNA sample contains ligation products consisting of fragments that were originally in close spatial proximity in the nucleus, marked with biotin at the junction. A Hi-C library is created by shearing the DNA and selecting the biotin-containing fragments with streptavidin beads. The library is then analyzed by using massively parallel DNA sequencing, producing a catalog of interacting fragments.

Statistical model: The read counts between a pair of loci are inversely proportional to the spatial distance between the two loci and the read counts follow a poisson distribution. The chromosome is modeled as a piecewise linear curve in a 3D space, specified by a spherical dot for each fragment or locus. 

github username: dandanpeng



