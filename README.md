# An Introduction to the NCBI and BLAST

This module is a short introduction to the [National Center for Biotechnology Information](https://www.ncbi.nlm.nih.gov) - or "NCBI" for short - and an overview of the various tools available there to the public. Of these tools, we will focus mostly on BLAST - the Basic Local Alignment Search Toool. 

An outline for the module is below:

  * [What is the NCBI?](#What-is-the-NCBI?)
  * [What is BLAST?](#What-is-BLAST?)
  * How does BLAST work?
  * For what purposes would you use BLAST?
  * Let's BLAST something!
    * Example One: Find a transgene in the Papaya Genome.
    * Example Two: Finding novel sequences 
  * Designing and Validating Primers with BLAST

***

## What is the NCBI? 

The [National Center for Biotechnology Information](https://www.ncbi.nlm.nih.gov) is an important component of the [National Library of Medicine](https://www.nlm.nih.gov) that has two broadly defined functions. First, the NCBI is tasked with hosting and maintaining a series of databases relevant to biotechnology and biomedicine. Secondly, the NCBI also serves to both curate and develop a wide variety of bioinformatics tools and services for researchers to use. We will take a better look at these two functions below. For further reading, a good overview of the history of the NCBI can be found [here](https://www.ncbi.nlm.nih.gov/books/NBK148949/). 

***

#### NCBI Databases

 >Understanding nature's mute but elegant language of living cells is the quest of modern molecular biology. From an alphabet of only four letters representing the chemical subunits of DNA emerges a syntax of life processes whose most complex expression is man. The unraveling and use of this "alphabet" to form new "words and phrases" is a central focus of the field of molecular biology. The staggering volume of molecular data and its cryptic and subtle patterns have led to an absolute requirement for computerized databases and analysis tools. - *from the NCBI mission statement*


<p align="center">
<kbd>
  <img src="SequencingData.png"/>
 </kbd>
 </p>
 <p align="center"
  <em>The Explosion of Sequencing Data - <i>National Library of Medicine</i></em>
</p>

***

With the rapid expansion of the availability of biological data in the Twentieth Century came the need for tools and software to both structure and query this data. This need brought together computer scientists, biologists, and government officials to help design and launch a variety of databases and protocols to assist researchers in both curating new knowledge and validating the old. For further reading, an interesting overview of the general history of bioinformatics (as related to computational structures) can be found [here](http://web.bf.uni-lj.si/bi/biokemija/bioinfo/2007/Material/Uvod1.pdf). 

Though there are many different databases avialable for users, Some of the more well-known databases at the NCBI include:

  * [GenBank](https://www.ncbi.nlm.nih.gov/genbank/): An annotated collection of all publically available nucloetide sequences and their protein translations. 
  * [PubMed](https://www.ncbi.nlm.nih.gov/pubmed): A search engine for accessing a variety of research publications (and their associated data) on life sciences and biomedical topics.
  * [Sequence Read Archive](https://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?): Also known as the "Short Read Acrhive", the SRA is a bioinformatics database that provides a repository for sequencing data generated by next-generation, high-throuput sequencing - such as data generated for [RNA-Seq](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2949280/) or [ChIP-seq](http://bitesizebio.com/13541/an-introduction-to-chip-seq/) experiments. 

A full list of the available resources and tools may be found [here](https://www.ncbi.nlm.nih.gov/guide/all/).

These different databases are all linked together by the [Entrez](https://en.wikipedia.org/wiki/Entrez) search engine. Entrez (French for "Come in") allows users to search many of the different databases hosted by NCBI all at the same time, thus allowing for simple queries to produce very wide-ranging results. As an example: if we search the string **CFTR** (a gene responsible for encoding a protein important to the pathology of cystic fibrosis in *Homo sapiens*):

<p align="center">
<kbd>
  <img src="EntrezExample.png"/>
</kbd>
</p>

As shown above: the query returend a rich selection of results that could be used to answer a variety of different scientific questions. If we were interested in DNA or RNA sequences, we would find them in the **Genome** database. If we were looking for human variations of the gene, we'd be able to find this in the **ClinVar** database, and so on. This kind of information retrieval is only possible because of the unified structures that exist between the databases and the Entrez search engine. 

***

## CHALLENGE

Search for the gene symbol **POMC**, look up information about the gene in *Homo sapiens*, and report three known phenotypic variations associated with this particular gene. 

***

First, navigate to [Entrez](https://www.ncbi.nlm.nih.gov/gquery/) and search for the gene symbol **POMC**. Then click "Search". When your results are returned, click "Gene".

<p align="center">
<kbd>
  <img src="EntrezSearchExampleOne.png"/>
</kbd>
</p>

**NOTE**: If you'd like to search specifically for a gene symbol you can use the search term **POMC[sym]**.


Next, look for the entry in the query results that is for the gene found in *Homo sapiens*. When you find it, click the gene symbol.

<p align="center">
<kbd>
  <img src="EntrezSearchExampleTwo.png"/>
</kbd>
</p>


This page returns a large amount of information about the **POMC** gene. 

<p align="center">
<kbd>
  <img src="EntrezSearchExampleThree.png"/>
</kbd>
</p>


Importantly, many genes have thorough summaries that can provide the user with a quick overview of the scientific knowledge of the gene in question. Upon inspecting the information available in the summary for **POMC**, we can see that mutations in this gene have been identified with the following phenotypic variations in human beings:
  
  * Early onset obesity
  * Adrenal insufficiency
  * Read hair

Fascinating! There's a wide vairety of information to be found amongst the various databases that the NCBI has to offer. Take a few moments to explore the information available about the **POMC** gebe before moving on. 

From James Watson, Nobel laureate and co-discoverer of the structure of DNA:

>One gene fascinates me: POMC, on chromosome 2, which is a recipe for a protein called ­pro-opiomelanocortin. In the body it gets broken up into different proteins, including melanotropin, which makes the skin darker when you’ve been in the sun, and beta-endorphin, a natural opioid that makes you feel satisfied after eating and also causes the ‘runner’s high.’ It’s the only gene I know whose very structure is an implicit biological message: Happiness is a reward for doing what we should be doing—for being in the sun and making vitamin D, for exercising and for bringing nutrients into our bodies. Eons ago these messages were delivered by the genes of our vertebrate ancestors on this planet. Now they are passed down to us. 


***

#### NCBI Tools

<p align="center">
<kbd>
  <img src="Tools.png"/>
</kbd>
</p>
<p align="center"
  <em>The painful reality of some tools in bioinformatics - <i>XKCD</i></em>
</p>

***

The tools available on the NCBI website provide users with a wide variety of ways to manipulate, investigate, and visualize biological data. An exhaustive list of these tools is avialable [here](https://www.ncbi.nlm.nih.gov/home/analyze.shtml). Some of the more popular tools provided by the NCBI include: The Open Reading Frame Finder (ORF Finder), Electronic PCR (e-PCR), and the Genome Workbench. However, the most popular tool by far is BLAST (and its many variations). What BLAST is, how it works, and what it's used for are the topics of the nesxt section.

***

## What is BLAST?
