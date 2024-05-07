README:

# Data stucture
## Taxonomy:
This directory contains folders for each year of the Clements taxonomy.  
- Clements_2021  
- Clements_2022  
- Clements_2023  

Each taxonomy_year directory contains:  
- a CSV mapping species from that taxonomy year to OpenTreeTaxonomy (OTT) identifiers (e.g. OTT_crosswalk_2021.csv)  
- a taxon addition file capturing a suggested placement for species for which we do not yet have phylogenetic information  
    
                    
## Trees:
This directory contains folders for each synth tree run, labelled by their version identifier (e.g. Aves_1.0)  
Each tree version directory contains:  
* dates_citations.txt <-input studies used to estimate dates  
* tree_citations.txt <- input studies used to estimate tree  
* OpenTree_synth <- folder containing the direct outputs of OpenTree Synthesis  
    - full tree  
    - phylo only tree  
    - dated tree  
    - many nitty gritty internal synthesis outputs  
* TreeVersion_ClementsYear folders (e.g. Aves1.0_CLO2023) <- folder containing the compete tree matching that taxonomy year.  
    - phylo_only_dated.tre (dated Clements2021 labeled tree including only tips with phylogenetic information)  
    - dated taxon addition tree cloud (results of 100 random replicates of the taxon addition algorthim)  
    - MCC.tre (Maximim clade credibility tree including all taxa in this version of the taxonomy. taxa without phylogenetic information added using Clootl)  
            




