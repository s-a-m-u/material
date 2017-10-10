
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

# CirSeq

## Link

CirSeq -> Virus mutation frequency analysis -> Standard error of binomial distribution

## Method Summary

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


By Ugne Jankauskaite (jugne on github).

