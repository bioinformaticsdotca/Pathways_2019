---
layout: tutorial_page
permalink: /Pathways_laptop_setup_instructions
title: Pathways
header1: Workshop Pages for Students
header2: Pathways and Network Analysis of -Omics Data 2019
image: /site_images/CBW_pathway_icon.jpg
home: https://bioinformaticsdotca.github.io/Pathways_2019
---

## Install these tools on your laptop before coming to the workshop:

1) A robust text editor.   

* For Windows/PC - [notepad++](http://notepad-plus-plus.org/)  
* For Linux - [gEdit](http://projects.gnome.org/gedit/)  
* For Mac – [TextWrangler](http://www.barebones.com/products/textwrangler/download.html)

2) A file decompression tool.  

* For Windows/PC – [7zip](http://www.7-zip.org/).  
* For Linux – [gzip](http://www.gzip.org).   
* For Mac – already there.

3) A robust internet browser such as Firefox or Safari (Internet Explorer and Chrome are not recommended because of Java issues).

4) Java -The software that we will be using (GSEA and Cytoscape) requires Java. Check if you have Java installed: https://www.java.com/verify/ and download Java if you do not have it installed. **You need Java 8. Do NOT install Java 10**.

5) A PDF viewer (Adobe Acrobat or equivalent).

6) Install [Cytoscape 3.7.1](https://cytoscape.org/download-platforms.html).  

Choose the version corresponding to your operating system (OS, Windows or UNIX) 
Cytoscape requires Java8: check your version at  https://www.java.com/verify/ and download Java8 if you do not have it installed. Contact your system administrator if you have trouble with Java installation. 

7) Within the Cytoscape program, install the following Cytoscape apps.  

From the menu bar, select ‘Apps’, then ‘App Manager’.
 
Within 'all apps', search for the following and install:  

 * EnrichmentMap 3.2.0
 * EnrichmentMap Pipeline Collection 1.0.0 (it will install ClusterMaker2, WordCloud and AutoAnnotate) 
 * GeneMANIA 3.5.1
 * IRegulon  1.3
 * ReactomeFIPlugin 7.2.0 - http://apps.cytoscape.org/apps/reactomefiplugin  
 * stringApp 1.4.2
 * yFiles Layout Algorithms	1.0.2	
 
 
8) Install the data set within GeneMANIA app.

From the menu bar, select 'Apps', hover over 'GeneMANIA', then select 'Choose Another Data Set'.  
From the list of available data sets, select the most recent (2017-07-13/13 July 2017) and under ‘Include only these networks:' select ‘all’. Click on ‘Download’.  
An ‘Install Data' window will pop-up. Select H.Sapiens Human (2589 MB). Click on ‘Install’.  
This requires time and a good network connection to download completely, so be patient (around 15mins).  

  
9) Install GSEA.  

 * Go to the [GSEA page](http://www.broadinstitute.org/gsea/index.jsp)    
 * Register  
 * Login  
 
 ############ option 1 recommended:
 
 * In menu, in the javaGSEA Desktop Application section, changed *Launch with" to *4GBG (for 64 bit Java only)*  
 * Click on the *Launch* button. This is downloading a gsea icon. Save it on your computer. Double click on this icon to 
 open GSEA.
 
  * Note 1: please try to lauch GSEA before the workshop (open).
  * Note 2: Most common issue with GSEA during the workshop is out of memory error because GSEA was launched with 1GB instead of 4 GB. Please make sure that you have downloaded the 4GB start icon as descrived above.
 
 

 ############# option 2 in case option 1 does not work on your computer:
 
 * In menu, choose Downloads 
 * Go to the javaGSEA Java Jar file section and download the gsea-3.0.jar file and save in your Documents folder (do not leave it in the “Downloads”folder).  
 
**MAC/Linux Computer** 

* On a MAC, the Terminal window is located in Applications/Utilities. Tip: add the terminal window to your dock so it is easy to open when needed.  
* At the prompt, type the command in your terminal window and hit enter:

```
java -Xmx4G -jar ~/Documents/gsea-3.0.jar
```

**PC/Windows Computer** 

* On Windows, go to the start icon and type cmd (for command prompt) in the search box.  
* At the prompt, type the following commands, hitting enter in between each command and waiting for the prompt before the next command:

```
cd Documents
java -Xmx4G -jar gsea-3.0.jar
```
