# DilutionExperiment
This GitHub repository holds the R code for analysis of data from the 'dilution experiment' that was conducted during the DeepDOM cruise in April/May 2013. These files provide details on (1) the peak picking parameters used in XCMS to convert from mzML files into a set of aligned features, and (2) the options selected for the WGCNA analysis that linked the FT-MS data and the TSQ data.
The raw data and experimental metadata are available from MetaboLights: http://www.ebi.ac.uk/metabolights/MTBLS461
Krista Longnecker, klongnecker@whoi.edu

Analysis steps
* Run the dilution experiment (at sea)
* Store filters with intracellular metabolites at -80C until extraction can occur in a land-based laboratory
* Extract the intracellular metabolites using the methods described in Kido Soule et al. (2015)
* Analyze the extracts using (1) targeted mass spectrometry and (2) untargeted mass spectrometry methods, both as described in Kido Soule et al. (2015)
* Process the targeted mass spectrometry data to obtain concentrations of known organic compounds within the samples
* Use DilutionExperiment_XCMSpeakpicking.Rmd to obtain the set of aligned mzRT features in the untargeted mass spectrometry data
* Use DilutionExperiment_WGCNAanalysis.Rmd to conduct the WGCNA analysis that merges the targeted and untargeted mass spectrometry data.

References cited:
Kido Soule, M. C., Longnecker, K., Johnson, W. M., & Kujawinski, E. B. (2015). Environmental metabolomics: analytical strategies. Marine Chemistry, 177, Part 2, 374-387. doi: doi:10.1016/j.marchem.2015.06.029
