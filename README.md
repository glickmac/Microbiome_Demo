# Microbiome_Demo

[![Build Status](https://travis-ci.org/glickmac/Microbiome_Demo.svg?branch=master)](https://travis-ci.org/glickmac/Microbiome_Demo)
![Python](https://img.shields.io/badge/python-v2.7%20%2F%20v3.6-blue.svg)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-orange.svg)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)


## Table of Contents
[What is the Microbiome?](#intro)     
[Workflow](#workflow)   
[Installing Tools](#install)    
[Workflow Usage](#usage)        

## <a name="intro"></a>What is the Microbiome?

The microbiome is a collection of all microorganisms in a niche. For the purposes of this demo, we focus solely on the bacterial microbiome. The bacterial microbiome is accessible via a universally conserved gene sequence called the 16s ribosomal RNA. 

## <a name="workflow"></a>Microbiome Workflow

To identify the bacterial taxa in a niche, a region of the 16s ribosomal RNA gene is amplified and sequenced. This repository stores two workflows to analyze the resulting 16s sequences though more information about the workflows and additional techniques can be found:

- [Dada2](http://benjjneb.github.io/dada2/index.html)

- [Qiime2](https://docs.qiime2.org)


## <a name="install"></a>Installing Items for Workflows

Software:

Optional but highly recommended to install Qiime


+ Anaconda: [download](https://blast.ncbi.nlm.nih.gov/Blast.cgi?CMD=Web&PAGE_TYPE=BlastDocs&DOC_TYPE=Download) 

+ Qiime w/ Anaconda (On Command-Line):
```
wget https://data.qiime2.org/distro/core/qiime2-2018.2-py35-osx-conda.yml
conda env create -n qiime2-2018.2 --file qiime2-2018.2-py35-osx-conda.yml

## Optional Cleanup 
rm qiime2-2018.2-py35-osx-conda.yml
```

+ Jupyter Notebook: 
```
pip install jupyter
```

+ Bioconductor (In R Environment): 
```
source("https://bioconductor.org/biocLite.R")
biocLite()
```

+ Dada2 and other packages:
```
source("https://bioconductor.org/biocLite.R")
biocLite("dada2")
biocLite("phyloseq")
install.packages("RColorBrewer")
install.packages("ggplot2")
```

+ R Kernal for Jupyter Notebook:
See installation instructions for IRKernel [here](https://irkernel.github.io/installation/) or directly from the [github repository](https://github.com/IRkernel/IRkernel)


Additional instructions for installing the required packages are found within the demo scripts. 


## <a name="usage"></a>Using Microbiome Workflows

This repository holds two jupyter workflows one in R (Dada2 & Phyloseq) and one in python (Qiime2). Download this repository and start a jupyter notebook within it to follow along with the scripts. 

