# DilutionExperiment
This GitHub repository holds the R code described in Longnecker and Kujawinski (2020). The code analyzes data from a dilution experiment conducted during the DeepDOM cruise in April/May 2013. These files provide details on (1) the peak picking parameters used in XCMS to convert from mzML files into a set of aligned features, and (2) the options selected for the WGCNA analysis that linked the FT-MS data and the TSQ data. WGCNA (Weighted Correlation Network Analysis) is an R package that seeks to find paramters that co-vary and thus may be regulated by similar factors (Langfelder and Horvath, 2008). In this project, we used WGCNA to link untargeted and targeted mass spectrometry data from intracellular organic matter extracted from seawater.

The raw data and experimental metadata are available from MetaboLights: http://www.ebi.ac.uk/metabolights/MTBLS461

Krista Longnecker, klongnecker@whoi.edu

## Analysis steps
* Run the dilution experiment (at sea)
* Store filters with intracellular metabolites at -80 degrees Celsius until extraction can occur in a land-based laboratory
* Extract the intracellular metabolites using the methods described in Kido Soule et al. (2015)
* Analyze the extracts using (1) targeted mass spectrometry and (2) untargeted mass spectrometry methods, both as described in Kido Soule et al. (2015)
* Process the targeted mass spectrometry data to obtain concentrations of known organic compounds within the samples
* Use `DilutionExperiment_XCMSpeakpicking.Rmd` to obtain the set of aligned mzRT features in the untargeted mass spectrometry data
* Use `DilutionExperiment_WGCNAanalysis.Rmd` to conduct the WGCNA analysis that merges the targeted and untargeted mass spectrometry data. 

## Data files provided on GitHub
* `DilutionExperiment_FTLCdata.csv` - the complete set of mzRT features from the untargeted mass spectrometry data
* `DilutionExperiment_FTLCdata_annotation.csv` - mzRT feature information used in the visualization of the WGCNA results
* `DilutionExperiment_FTLCsequenceInformation.xlsx` - the sample information for the FTLC data, used in the peak picking steps to help organize the data
* `DilutionExperiment_TSQdata.csv` - the results from the targeted mass spectrometry data in a format that can be read into R for the WGCNA analysis.

## References cited
* Kido Soule, M. C., Longnecker, K., Johnson, W. M., & Kujawinski, E. B. (2015). Environmental metabolomics: analytical strategies. Marine Chemistry, 177, Part 2, 374-387. doi: doi:10.1016/j.marchem.2015.06.029
* Langfelder, P., & Horvath, S. (2008). WGCNA: an R package for weighted correlation network analysis. BMC Bioinformatics, 9(1), 559. 
* Longnecker, K. and E. B. Kujawinski (2020). Intracellular metabolites in marine microorganisms during an experiment evaluating microbial mortality. Metabolites 10(3): 105. DOI: 10.3390/metabo10030105.
