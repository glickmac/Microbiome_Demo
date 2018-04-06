# Microbiome_Demo

[![Build Status](https://travis-ci.org/glickmac/Microbiome_Demo.svg?branch=master)](https://travis-ci.org/glickmac/Microbiome_Demo)
![Python](https://img.shields.io/badge/python-v2.7%20%2F%20v3.6-blue.svg)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-orange.svg)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)


## Table of Contents
[What is the Microbiome?](#intro)     
[Workflow](#workflow)   
[Installing Tools](#install)    
[Dada2 Usage](#usage)     
[Additional Functionality](#additional)    

## <a name="intro"></a>What is the Microbiome?

GRAB is short for Genomic Retrieval and Blast Database Creation. GRAB currently is only able to mine **bacterial** genomic information by taxonomy. GRAB consists of python scripts to mine the NCBI FTP sites for genomes, coding regions, or proteins of interest. 


## <a name="workflow"></a>GRAB Workflow

%<p align="center"><img src="https://github.com/glickmac/GRAB/blob/master/images/GRAB.png" 

 
[BLAST makeblastdb Example](https://www.haktansuren.com/blast-makeblastdb/) 

A helpful post on BLAST command makeblastdb 
   

## <a name="install"></a>Installing GRAB

Required software
+ NCBI-BLAST: [download](https://blast.ncbi.nlm.nih.gov/Blast.cgi?CMD=Web&PAGE_TYPE=BlastDocs&DOC_TYPE=Download) 
Must be in environmental path
+ Argparse & Pandas: 
```
pip install argparse
pip install pandas
```
[Argparse](https://pypi.python.org/pypi/argparse/)

## [Download GRAB](https://github.com/glickmac/GRAB/raw/master/GRAB.zip)

#### Unzip GRAB and CD into Directory

```
unzip GRAB.zip
cd GRAB
```

#### Other installations (Git)

```
git clone https://github.com/glickmac/GRAB
```



## <a name="usage"></a>Using 


+ GRAB.py Help: 

```
python GRAB.py -h
```

+ Build.py Help: 

```
python Build.py -h
```

### GRAB.py (Information Retrieval from NCBI)

Either -q or -f is required, however please use only one flag at a time

#### Required arguments :

| Option     | Description                                     |
|------------|-------------------------------------------------|
| **-q** or **-f**   | -q: -query seperated by commas **(no spaces)** or -f: -file with query seperated by new lines  |
| **-l**   | -level: Taxanomic level: options include *phylum, order, class, family, genus, species, or subspecies*  |


## <a name="additional"></a>Edge Cases

### Edge Cases
There exists edge cases which can affect the retrieval in taxonomic querying in GRAB.py. For example, at the species level if the search term Abscessus is used to find Mycobacterial Abscessus species, other bacteria with the term Abscessus will be present in the retreival. To counter, a user must enter the full search term in the query or file. 

For example:

```
python GRAB.py -m genomic -q 'Mycobacterium abscessus' -l species -o Abscessus_species
```

