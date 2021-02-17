# Molecular Biology

### Computational analysis Project

*GROUP 11 - Dante Aviñó, Miguel Borge, Pol Segura*

------

The main objective of the project is to **annotate the genes** included in the contig and to **functionally characterize** the predicted proteins.

Download assigned contig from a nematode species.

```bash
# Using npm package manager we're going to install github-files-fetcher
# so we can download particular files from the github repo.
npm install -g github-files-fetcher

# Download contig sequence from repo
fetcher --url="https://github.com/dantekali/BioMol-Project/blob/main/Group11_contig_194888_195063.fa"  --out="~/Desktop/Project"
```

#### Genes annotation included in the contig

We will obtain gene predictions using the two types of methods and we will compare the results with Ensembl annotations.

- **ab-initio tools** to obtain a first prediction (select closest species in model)
  <!--Ab-initio methods: they use several elements in the genomic sequence (suchas donor and acceptor splice sites, branch site, initiation and termination codons)and codon usage to obtain a model based on a training set.-->
  - GeneID  prediction: https://genome.crg.cat/software/geneid/geneid.html
  - FGENESH: http://www.softberry.com/berry.phtml?topic=fgenesh&group=programs&subgroup=gfindYou
  - GENESCAN: http://argonaute.mit.edu/GENSCAN.html

- blast search to identify the putative proteins (more sensitive if protein level instead of nucleotides)
  - https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastp&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome

- **homology-based tools** with the annotations of  a closely related species (web-server/local)
<!--Gene predictions are based on alignments from known proteins (usually) from other genomes.-->
  - https://bio.tools/t?page=1&q=%27Homology-based%20gene%20prediction%27&sort=score
  - https://ibb.co/kxSt6K8

#### Functionally characterization of the predicted proteins

Functional annotation is an essential step in omics data analysis. It is defined as the process of attaching biological information to gene and protein sequences(such as those predicted using Ab-initio and Homology-based methods) and describing functional groups based on similarities.



#### Discuss the performance of the different methods. Can you guess to which species does your contig correspond?