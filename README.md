## Example paper and data for summer school 2025

Data is from Proteomic Characterization of Caenorhabditis elegans Larval Development by [Xia et al 2017](https://analyticalsciencejournals.onlinelibrary.wiley.com/doi/10.1002/pmic.201700238) it contains quantitative proteomics across 4 larval stages of C. elegans development.

- The data is on [proteomexchange](https://proteomecentral.proteomexchange.org/cgi/GetDataset?ID=PXD006676) as .raw files.
- To obtain peptide level .txt file this would need to be re-processed with MaxQuant, Proteome Discoverer or other software.
- Protein level un-normalised data can be found in the supporting information with the paper in "Supporting Information Table 1. Proteins identified during C. elegans larval development by mass spectrometry–based proteomic analysis" the filename is `pmic12778-sup-0002-Table-S1.xlsx`.

### Project summary for participants 
(Suggestion from Hugo)

In this project, you will explore a mass spectrometry-based proteomics dataset generated from Caenorhabditis elegans sampled at four larval developmental stages (L1–L4). C. elegans is a nematode with a simple body organisation and a highly reproducible developmental lineage, which makes it an ideal model system for embryogenesis studies. While many transcriptomic studies have focused on embryonic or adult stages, proteomic profiling across larval development remains relatively underexplored. 

Your task will be to reproduce and expand on the analyses presented in this study, examining protein expression dynamics, identifying stage-specific proteins, and linking expression patterns to biological function.

Collaboration opportunity: This project can be paired with the bulk RNA-seq or single-cell RNA-seq projects, which examine gene expression across C. elegans development. While your focus is on protein-level changes during the larval stages, your colleagues will be analysing mRNA expression dynamics during embryogenesis. Together, you can explore the relationship between transcriptomic and proteomic regulation. 

For example:
- Compare stage-specific gene expression at the mRNA and protein levels.
- Are genes with strong mRNA dynamics during embryogenesis also dynamic at the protein level later in development?
- Identify genes with discordant RNA and protein profiles, which could indicate post-transcriptional regulation.
- Explore whether gene clusters found in your proteomics data correspond to known gene modules from RNA-seq studies

### Getting started
- Students can read in the un-normalised protein level data into R using `QFeatures` as they have done in the [earlier course](https://cambridgecentreforproteomics.github.io/course_expression_proteomics/)
- The peptide data is not available

### Considerations
- Data is protien level so some of the cleaning steps may not be applicable
- This is label-free (LFQ) data and processed using MaxQuant not proteome discoverer. Students should think about appropriate normalisation for LFQ and data missingness.
- Note NAs have been encoded as zeros in this data and should be converted back to NA using `zeroIsNA` function from `QFeatures`.
