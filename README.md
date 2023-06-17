# TFM_Elvira_Marquez
This repository aims to store the code and data used for the analysis of the HDL proteome in subjects with metabolic syndrome.

## Script "deg_enrich_HDL_proteome.Rmd"
The aim of this script is to analyse the HDL proteome of patients with metabolic syndrome (MS) and healthy patients (H) to determine the proteins associated with this clinical condition. To this end, the first part of the script focuses on the pre-processing, log-transformation and exploratory analysis of the data. This is followed by differential expression analysis using the Bioconductor *Limma* package (http://bioconductor.org/packages/release/bioc/html/limma.html). Finally, the differentially expressed proteins are subjected to functional enrichment analysis using Bioconductor's *ClusterProfiler* package (https://bioconductor.org/packages/release/bioc/html/clusterProfiler.html). The visualisation of these results and the summary of ontological terms by REVIGO (http://revigo.irb.hr/) can be found at the end of the script.  

## Script "cor_glm_lm.Rmd"
This script has been performed following a differential expression analysis of the HDL proteome of healthy patients and patients with metabolic syndrome and has several objectives:
- To generate correlation heat maps between differentially expressed proteins and some biochemical variables of interest using Pearson's correlation coefficient, using the CRAN package ggplot2 (https://cran.r-project.org/web/packages/ggplot2/index.html) for visualisation.
- Fitting HDL functionality data to a logistic regression model to estimate the probability of the qualitative variable "sindrome metabolico".
- Fitting gene expression data to a linear regression model to explain the levels of the quantitative variable "cholesterol efflux".

## Script "sPLS-DA.Rmd"
This script aims to apply a supervised learning technique to develop a predictive model from proteomic data. It includes the visualisation of an initial PLS-DA, the tuning process of the model, the visualisation of its predictive capacity, and the evaluation of the final PLS-DA. The Bioconductor MixOmics package (https://www.bioconductor.org/packages/release/bioc/html/mixOmics.html) has been used for its elaboration.

## Data
Due to the ethical and legal issues supporting this research, and in order to ensure the privacy and confidentiality of the subjects of this study, the data for the execution of these scripts are not publicly available for viewing or downloading. Proteomics data (not clinical data) will be made available upon request to the author.
In the main directory you can find the scripts used for the analysis, in .Rmd format and in HTML format, as well as some files from their execution (REVIGO treemaps, tsv files with enriched GO terms, etc). 
