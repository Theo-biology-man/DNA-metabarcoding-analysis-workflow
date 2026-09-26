DNA metabarcoding analysis workflow
================

**Introduction and Background**

This project presents an R-based workflow for processing and analysing DNA metabarcoding data to investigate
how pollinators of cocoa (*Theobroma cacao*) utilise the habitat around cocoa farms. 

DNA metabarcoding is a high-throughput molecular technique that combines next-generation sequencing (NGS) with DNA barcoding
to identify species in complex biological samples. In the case of cocoa pollinators, it allows for identification of 
icryptic nsect taxa that are present in cocoa farms that may be missed due to the limitations of traditional ecological capture techniques.
As cocoa flowers are particularly small, pollinator species need to be small to access the flowers. 

Ceratopogonidae is considered the primary pollinator in Africa and the Americas (Adjaloo and Oduro, 2013,
Vandromme et al., 2023), with numerous studies trying to understand how midges use
the farm environment with the goal of developing pollination-boosting practices
(Jaramillo et al., 2024). 

The focus on Ceratopogonidae as the 'main' pollinator, however,
masks the role of other pollinators (Vandromme et al., 2023). Most notably,
Cecidomyiidae (gall midges) due to their similar morphology (small size, pollen carrying
body) to Ceratopogonidae and presence on cocoa flowers (Winder, 1978, Toledo-Hernández et al., 2017). 

Other small insects from the Dipterans and the
Hymenopterans (Chumacero de Schawe, 2016, Toledo-Hernández et al., 2017,
Vandromme et al., 2023) have also been shown to visit cocoa flowers leading to their
proposal as potential pollinators

**Analysis Workflow**

The R markdown worflow includes:

1. Data processing and quality control

* Importing Illumina sequencing results
* Organising OTU read counts
* Identifying potential contaminants using the decontam package 
* Removing contaminant and unwanted taxonomic assignments 

2. Taxonomic filtering 

* Restricing analysis to insect taxa 
* Identifying candidate pollinator families across Diptera, Hymenoptera and Hemiptera

3. Community analysis 

* Relative read abundance (RRA)
* Frequency of occurrence (FOO)
* Candidate family richness 
* Comparison between substrate and farm types 

4. Community composition 

* Presence/absence transformation 
* Jaccard distance
* Non-metric multidimensional scaling (NMDS)
* PERMANOVA to investigate differences in community composition between substrates

5. Visualisation 

* Taxonomic composition 
* Candidate pollinator family abundance 
* Frequency of occurrence
* Substrate-level comparisons 
* Farm-level comparisons 
* Community ordination plot

Tools and Packages 

The analysis was conducted in R using:

* readxl
* dplyr
* tidyr
* ggplot2
* decontam
* vegan
* tidyverse
* gridExtra

The analysis is presented as an R Markdown workflow to combine reproducible code,
analysis and visualisation.

**Repository Structure**

├── .gitignore\
├── README.md\
├── dna-metabarcoding-visualisation-and-analysis.Rmd\
├── dna-metabarcoding-visualisation-and-analysis.html\
└── Figures/

**Files**

* README.md - Overview of project, methods and analysis workflow
* .Rmd - Complete R Markdown source code
* .html - Rendered HTML report containing the analysis and visualisations.
* Figures/ - Rendered plots 

**Data Availability**

The original sequencing data set is not currently included in the repository due 
data sharing regulations. 


**References**

Adjaloo, M.K. and Oduro, W. (2013) Insect assemblage and the pollination system in cocoa
ecosystems. Journal of Applied Biosciences, 62, pp.4582–4594.
https://doi.org/10.4314/jab.v62i0.86070

Adjaloo, M.K., Owusu-Ansah, E., Oduro, W. and Fleischer, T. (2017)
Preference of cocoa pollinators for different breeding substrates in a
cocoa-agroecosystem: a proxy approach. Ghana Journal of Forestry, 33,
pp. 38–47. Available at:
<https://www.researchgate.net/publication/333320170_Preference_of_cocoa_pollinators_for_bre>
eding_substrates_PREFERENCE_OF_COCOA_POLLINATORS_FOR_DIFFERENT_BREEDING_SUB
STRATES_IN_A_COCOA-AGROECOSYSTEM_A_PROXY_APPROACH#fullTextFileContent

Chumacero de Schawe, C., Kessler, M., Hensen, I. and Tscharntke, T., 2018. Abundance and diversity of flower visitors on wild and cultivated cacao (Theobroma cacao L.) in Bolivia. Agroforestry Systems, 92(1), pp. 117–125. Available at: https://doi.org/10.1007/s10457-016-0019-8.

Claus, G., Vanhove, W., Damme P.V., Smagghe, G. (2018) Challenges in
Cocoa Pollination: The Case of Côte d’Ivoire. Pollination in Plants.
InTech. Available at: <http://dx.doi.org/10.5772/intechopen.75361>.

Deagle, B. E., Thomas, A. C., McInnes, J. C., Clarke, L. J., Vesterinen, E. J., Clare, E. L., Kartzinel, T.
R., & Eveson, J. P. (2019). Counting with DNA in metabarcoding studies: How should we convert
sequence reads to dietary data? Molecular Ecology, 28(2), 391–406.
https://doi.org/10.1111/mec.14734

Espinosa Prieto, A., Hardion, L., Debortoli, N., Bournonville, T., Marescaux, J., van der Zon, K.A.E.
and Beisel, J. (2025) Environmental DNA metabarcoding for catchment-scale detection of
aquatic plants, invasive species, and land-use indicators in a large river. Ecological Indicators,
178, 113943. https://doi.org/10.1016/j.ecolind.2025.113943

Forbes, S.J. and Northfield, T.D. (2017) Increased pollinator habitat
enhances cacao fruit set and predator conservation. Ecological
Applications, 27(3), pp.887–899. <https://doi.org/10.1002/eap.1491>

Jaramillo, M.A., Reyes-Palencia, J. and Jiménez, P. (2024) Floral
biology and flower visitors of cocoa (Theobroma cacao L.) in the upper
Magdalena Valley, Colombia. Flora, 313, 152480.
<https://doi.org/10.1016/j.flora.2024.152480>

Kennerley, W.L., Clucas, G.V. and Lyons, D.E. (2024) Multiple methods of diet assessment reveal
differences in Atlantic puffin diet between ages, breeding stages, and years. Frontiers in Marine
Science, 11, 1410805. https://doi.org/10.3389/fmars.2024.1410805

Lander, T.A., Atta-Boateng, A., Toledo-Hernández, M., Wood, A., Malhi,
Y., Solé, M., Tscharntke, T. and Wanger, T.C. (2025) Global chocolate
supply is limited by low pollination and high temperatures.
Communications Earth & Environment, 6(1), 97.
<https://doi.org/10.1038/s43247-> 025-02072-z

Toledo-Hernández, M., Wanger, T.C. and Tscharntke, T. (2017) Neglected
pollinators: Can enhanced pollination services improve cocoa yields? A
review. Agriculture, Ecosystems & Environment, 247, pp.137–148.
<https://doi.org/10.1016/j.agee.2017.05.021>

Vandromme, M., Van de Sande, E., Pinceel, T., Vanhove, W., Trekels, H. and Vanschoenwinkel, B.
(2023) Resolving the identity and breeding habitats of cryptic dipteran cacao flower visitors in a
neotropical cacao agroforestry system. Basic and Applied Ecology, 68, pp.35–45.
https://doi.org/10.1016/j.baae.2023.03.002

Winder, J.A. (1978) Cocoa Flower Diptera: their identity, pollinating activity, and breeding sites.
PANS: Pest Articles & News Summaries, 24(1), pp.5–18.
https://doi.org/10.1080/09670877809414251

Young, A. M. (1982). Effects of Shade Cover and Availability of Midge
Breeding Sites on Pollinating Midge Populations and Fruit Set in Two
Cocoa Farms. Journal of Applied Ecology, 19(1), 47–63.
<https://doi.org/10.2307/2402990>
