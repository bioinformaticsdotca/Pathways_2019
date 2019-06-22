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

By Veronique Voisin, Ruth Isserlin, Gary Bader

## Goal of the exercise

**Create an enrichment map and navigate through the network**

During this exercise, you will learn how to create an EnrichmentMap from gene-set enrichment results. The enrichment tool chosen for this exercise is g:Profiler but an enrichment map can be created from various gene-set tools using the generic format or the more specific GSEA or BinGO interface.


## Data

The data used in this exercise is a list of frequently mutated genes that we used in previous exercise. 
Pathway enrichment analysis has been run using g:Profiler and the results have been downloaded as a GEM format.


## EnrichmentMap

*	A circle (node) is a genee-set (pathway) enriched in genes that we used as input in g:Profiler (frequently mutated genes).

*	edges (lines) represent genes in common between 2 pathways (nodes).

*	A cluster of nodes represent overlapping and related pathways and may represent a common biological process.

*	Clicking on a node will display the genes included in each pathway.

## Description of this exercise

We run and save the g:Profiler results using different parameters. 
An enrichment map represents the result of enrichment analysis as a network where significantly enriched gene-sets that share a lot of genes in common will form identifiable clusters. The visualization of the results as these biological themes will ease the interpretation of the results. 

The goal of this exercise is to learn how to:
1) upload g:Profiler results into Cytoscape EnrichmentMap to create a map.
2) upload several g:Profiler results at the same time to create one map and learn how to distinguish the results.
3) to compare the differences resulting from the use of different g:Profiler parameters at the enrichment map level. 


## Start the exercise

To start the lab practical section, first create a gprofiler_files directoty on your computer and download it the files below.

Five files are needed to create the enrichment maps for this exercise (please download these files on your computer):

Enrichment result 1: [gProfiler_hsapiens_GEM1.txt](https://github.com/bioinformaticsdotca/Pathways_2019/blob/master/Module3/newgprofilerEM/data/gProfiler_hsapiens_GEM1.txt) 
In g:Profiler, the parameters that we used were: GO_BP no electronic annotation, Reactome, Benjamini-HochBerg FDR 0.05. 


Enrichment result 2: [gProfiler_hsapiens_gs250.gem.txt](https://github.com/bioinformaticsdotca/Pathways_2019/blob/master/Module3/newgprofilerEM/data/gProfiler_hsapiens_gs250.gem.txt) 
In g:Profiler, the parameters that we used were: GO_BP no electronic annotation, Reactome, Benjamini-HochBerg FDR 0.05. The results were filtered using the g:Profiler Term size slidebar and **only the enriched gene-sets that contain equal or less than 250 genes per gene-set** were included in the result file (gProfiler_hsapiens_gs250.gem.txt).


Enrichment result 3: [gprofiler_results_mesenchymal.txt](https://github.com/bioinformatics-ca/bioinformatics-ca.github.io/raw/master/2016_workshops/pathways/module3_lab/EM_gProfiler_data/gprofiler_results_mesenchymal.txt)


Pathway database 1 (.gmt):[hsapiens_GO_REAC.gmt](https://github.com/bioinformaticsdotca/Pathways_2019/blob/master/Module3/newgprofilerEM/data/hsapiens_GO_REAC.gmt)
This file has been created by concatenating the hsapiens.GO/BP.name.gm and the hsapiens.REAC.name.gmt files contained in the g:Profiler gprofiler_hsapiens.name folder. 

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

Create an enrichment map from 2 datasets and with a gmt file.

2a. In the 'Create Enrichment Map window' , drag and drop the 2 enrichment files gProfiler_hsapiens_GEM1.txt and 
gProfiler_hsapiens_gs250.gem.txt.

<img src="https://github.com/bioinformaticsdotca/Pathways_2019/blob/master/Module3/newgprofilerEM/images/gem0.png?raw=true" alt="workflow" width="750" />

2b. In the white box, click on "gProfiler_hsapiens_gs250.gem (Generic/gProfiler) 

2c. On the right side, go to the *GMT* field, click on the 3 radio button (...) and locate the file hsapiens_GO_REAC.gmt that you have saved on your computer to upload it.

<img src="https://github.com/bioinformaticsdotca/Pathways_2019/blob/master/Module3/newgprofilerEM/images/gem1.png?raw=true" alt="workflow" width="750" />

2d. In the white box, click on "gProfiler_hsapiens_GEM1 (Generic/gProfiler) 

2e. On the right side, go to the *GMT* field, click on the 3 radio button (...) and locate the file hsapiens_GO_REAC.gmt that you have saved on your computer to upload it.

2f. Locate the *FDR q-value cutoff* field and set the value to 0.001

2g. Select the *Connectivity* slide bar to *sparse*. 

2h. Click on *Build*.

<img src="https://github.com/bioinformaticsdotca/Pathways_2019/blob/master/Module3/newgprofilerEM/images/gem2.png?raw=true" alt="workflow" width="750" />


<img src="https://github.com/bioinformaticsdotca/Pathways_2019/blob/master/Module3/newgprofilerEM/images/gem3.png?raw=true" alt="workflow" width="750" />


## Step3: Explore the results:

In the EnrichmentMap control panel located at the left:
 * check the 2 Data Sets (checked by default)
 * set Chart Data o *Color by Data Set*
 * check *Publication Ready* to remove gene-set label to have a global view of the map. Tip: uncheck this box when you explore the map in details to see the gene-set names. 
 
 <img src="https://github.com/bioinformaticsdotca/Pathways_2019/blob/master/Module3/newgprofilerEM/images/gem3a.png?raw=true" alt="workflow" width="750" />

On the map, a node that has both green and blue color is a gene-sets that was present in the 2 gProfiler result file that we have been uploaded. A node that is blue is a gene-set that was present only in the file *gProfiler_hsapiens_GEM1* . A blue edge represents genes that overlap between gene-sets included in the file *gProfiler_hsapiens_GEM1* and a green edge represents genes that overlap between gene-sets included in the file gProfiler_hsapiens)gs250.gem. 

 <img src="https://github.com/bioinformaticsdotca/Pathways_2019/blob/master/Module3/newgprofilerEM/images/gem6.png?raw=true" alt="workflow" width="750" />


# Explore Detailed results 

 * In the Cytoscape menu bar, select 'View" and 'Show Graphic Details' to display node labels. Zoom in to be able to read the labels and navigate the network using the bird eye view.

 * Select a node and visualize the *Table Panel*
   * Click on a node

   * For this example the node *"MESENCHYME DEVELOPMENT"* has been selected. Tip: you can type it in the search bar, quotes are important.

When the node is selected, it is highlighted in <font color="yellow">yellow</font>.

3b. In Table Panel:

*	Click on the Sort Column on "Ranks Data Set1"

*	Set Expressions to *Row Norm*

* Set Compress to -None- (tip: select the field and use the keyboard arrows up to select it)

You can now visualize the genes in the MESENCHYME DEVELOPMENT pathway that are higher expressed in the mesenchymal samples when compared to the immunoreactive samples. 

 <img src="https://github.com/bioinformaticsdotca/Pathways_2018/blob/master/module3_lab/img/EMgprofilerheatmap.png?raw=true"  width="750" />

## Exercise 1b

Create an enrichment map without a gmt file to compare the results with Exercise 1a.

 * Go to Control Panel and select the EnrichmentMap tab. 
 * Click on the "+" sign to re-open the *Create Enrichment Map* window.
 * In the white box, select the "gProfiler_hsapiens_gs250.gem (Generic/gProfiler) file 
 * Locate the GMT field and delete the file name , leaving it blank.
 * In the white box, select the "gProfiler_hsapiens_GEM1 (Generic/gProfiler) file 
 * Locate the GMT field and delete the file name , leaving it blank.
 * Use same parameters as in exercise 1a: FDR q-value cutoff of 0.001 and Connectivity to sparse.
 * Click on *Build*
 
  <img src="https://github.com/bioinformaticsdotca/Pathways_2019/blob/master/Module3/newgprofilerEM/images/gem5.png?raw=true" alt="workflow" width="750" />
 
 
 Explore the results:
 
 In the EnrichmentMap control panel located at the left:
 * check the 2 Data Sets (checked by default)
 * set Chart Data o *Color by Data Set*
 * check *Publication Ready* to remove gene-set label to have a global view of the map. Tip: uncheck this box when you explore the map in details to see the gene-set names. 
 
 <img src="https://github.com/bioinformaticsdotca/Pathways_2019/blob/master/Module3/newgprofilerEM/images/gem3a.png?raw=true" alt="workflow" width="750" />

On the map, a node that has both green and blue color is a gene-sets that was present in the 2 gProfiler result file that we have been uploaded. A node that is blue is a gene-set that was present only in the file *gProfiler_hsapiens_GEM1* . A blue edge represents genes that overlap between gene-sets included in the file *gProfiler_hsapiens_GEM1* and a green edge represents genes that overlap between gene-sets included in the file gProfiler_hsapiens)gs250.gem. 
 
 <img 
 src="https://github.com/bioinformaticsdotca/Pathways_2019/blob/master/Module3/newgprofilerEM/images/gem4.png?raw=true" alt="workflow" width="750" />
 







#

## Exercie 1c
 
 Create an enrichment map from the results of g:Profiler generated using the custom Baderlab gene-set file. 

 
 

#### SAVE YOUR CYTOSCAPE SESSION (.cys) FILE ! ####


