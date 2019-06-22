---
layout: tutorial_page
permalink: /Pathways_2019_Module3_Lab-EM_GProfiler
title: Pathways
header1: Workshop Pages for Students
header2: Pathways and Network Analysis of -Omics Data 2019
image: /site_images/CBW_pathway_icon.jpg
home: https://bioinformaticsdotca.github.io/Pathways_2019
author: Veronique Voisin
modified: June 26th, 2018
---

**This work is licensed under a [Creative Commons Attribution-ShareAlike 3.0 Unported License](http://creativecommons.org/licenses/by-sa/3.0/deed.en_US). This means that you are able to copy, share and modify the work, as long as the result is distributed under the same license.**

# Network Visualization and Analysis with Cytoscape: Enrichment Map from g:Profiler results

By Veronique Voisin

## Goal of the exercise:

**Create an EnrichmentMap and navigate through the network**

During this exercise, you will learn how to create an EnrichmentMap from gene-set enrichment results. The enrichment tool chosen for this exercise is g:Profiler but an enrichment map can be created from various gene-set tools using the generic format or the more specific GSEA or BinGO interface.


## Data

The data used in this exercise is a list of frequently mutated genes that we used in previous exercise. 
Pathway enrichment analysis has been run using g:Profiler and the results have been downloaded as a GEM format.


## EnrichmentMap

*	A circle (node) is a genee-set (pathway) enriched in genes that we used as input in g:Profiler (frequently mutated genes).

*	edges (lines) represent genes in common between 2 pathways (nodes).

*	A cluster of nodes represent overlapping and related pathways and may represent a common biological process.

*	Clicking on a node will display the genes included in each pathway.

## Goal of this exercise:

We run and save the g:Profiler results using different parameters. 
An enrichment map represent the result of enrichment analysis as a network where significantly enriched gene-sets that share a lot of genes in common will form identifiable clusters. These visualization of the results as biological themes and will ease the interpretation of the results. 

The goal of this exercise is to learn how to:
1) upload g:Profiler results into Cytoscape EnrichmentMap to create a map.
2) upload several results at the same time to create one map and how to distinguish the results.
3) to compare the differences resulting from the use of different g:Profiler parameters at the enrichment map level. 


## Start the exercise

To start the lab practical section, first create a gprofiler_files directoty on your computer and download it the files below.

Five files are needed to create the enrichment maps for this exercise (please download these files on your computer):

Enrichment result 1: [gprofiler_results_mesenchymal.txt](https://github.com/bioinformatics-ca/bioinformatics-ca.github.io/raw/master/2016_workshops/pathways/module3_lab/EM_gProfiler_data/gprofiler_results_mesenchymal.txt)

Enrichment result 2: [gprofiler_results_mesenchymal.txt](https://github.com/bioinformatics-ca/bioinformatics-ca.github.io/raw/master/2016_workshops/pathways/module3_lab/EM_gProfiler_data/gprofiler_results_mesenchymal.txt)

Enrichment result 3: [gprofiler_results_mesenchymal.txt](https://github.com/bioinformatics-ca/bioinformatics-ca.github.io/raw/master/2016_workshops/pathways/module3_lab/EM_gProfiler_data/gprofiler_results_mesenchymal.txt)


Pathway database 1 (.gmt):[hsapiens.pathways.NAME.gmt.zip](https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/hsapiens.pathways.NAME.gmt)

Pathway database 1 (.gmt):[hsapiens.pathways.NAME.gmt.zip](https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/hsapiens.pathways.NAME.gmt)

## Exercise 1a 

## Step 1

Launch Cytoscape and open the EnrichmentMap App

1a. Double click on Cytoscape icon

1b. Open EnrichmentMap App

*	In the Cytoscape top menu bar:

  *	Click on Apps -> EnrichmentMap

<img src="https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/img/EM1.png?raw=true"  />

 * A 'Create Enrichment Map' window is now opened.

## Step 2

Create an enrichment map from 3 datasets and with no gmt file 

2a. In the 'Create Enrichment Map window' , drag and drop the 3 enrichment files.  

2b. Specify the following parameters:

*	Name: use default or choose a name of your choice like 'g:Profiler network'

* Analysis Type: Generic/gProfiler

* Enrichments: gprofiler_results_mesenchymal.txt TIP: only field that is not optional


## Step 3

Create an enrichment map with a gmt file 







<img src="https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/img/EMgprofilerinput.png?raw=true"  width="750"/>
 
2c. Click on *Build* button at the bottom of the Enrichment Map Input panel.

Unformatted results

![EM18](https://github.com/bioinformaticsdotca/HT-Biology_2017/blob/master/Pathways/img/EM18v2.png?raw=true) 

 * In the Cytoscape menu bar, select 'View" and 'Show Graphic Details' to display node labels. Zoom in to be able to read the labels and navigate the network using the bird eye view.

## Step 3 

Select a node and visualize the *Table Panel*

3a. Click on a node

For this example the node *"MESENCHYME DEVELOPMENT"* has been selected. Tip: you can type it in the search bar, quotes are important.

When the node is selected, it is highlighted in <font color="yellow">yellow</font>.

3b. In Table Panel:

*	Click on the Sort Column on "Ranks Data Set1"

*	Set Expressions to *Row Norm*

* Set Compress to -None- (tip: select the field and use the keyboard arrows up to select it)

You can now visualize the genes in the MESENCHYME DEVELOPMENT pathway that are higher expressed in the mesenchymal samples when compared to the immunoreactive samples. 

 <img src="https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/img/EMgprofilerheatmap.png?raw=true"  width="750" />

## OPTIONAL
 
 * Create a subnetwork : select nodes connected to the "MESENCHYME DEVELOPMENT" node by looking at the Cytoscape toolbar and selecting the correct icon (2 houses). Once the nodes that are connected to "MESENCHYME DEVELOPMENT" are highlghted in yellow, create a subnetwork by selecting the appropriate icon on the left side on the previous icon. Redo the layout and manually move the nodes so the labels are not overlapping.
 
  
 <img src="https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/img/button.png?raw=true"  />
 
 
 <img src="https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/img/EMgprofilersubnetwork.png?raw=true"  />
 

 * Use the AutoAnnotate App to create annotated clusters. Use the instructions from the GSEA lab.
 

#### SAVE YOUR FILE ! ####


