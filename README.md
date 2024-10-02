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
For more details and code for how each of these files were generated see: https://github.com/McTavishLab/AvesTreeCode 
* dates_citations.txt <-input studies used to estimate dates  
* tree_citations.txt <- input studies used to estimate tree  
* OpenTree_synth <- folder containing the direct outputs of OpenTree Synthesis  
    - full tree  
    - phylo only tree  
    - dated tree  
    - many nitty gritty internal synthesis outputs. These are detailed in depth in the index.html file contained in the OpenTree synth folder
* A folder for each year of the Clements taxonomy folder:
    - phylo_only.tre <- OpenTree Id labeled tree including only tips with phylogenetic information
    - phylo_only_clements_labels.tre  <- Clements labeled tree including only tips with phylogenetic information
    - phylo_only_clements_labels_ultrametric.tre <- ultrametric tree which is the input for the taxon addition step
    - taxon_addition_treeset.tre <- set of 100 complete trees from 100 stochastic taxon addition replicates
    - dated_rand_sample_clements.tre <- dated taxon addition tree cloud, 100 topologies from the taxon addition treeset using random selections from the node dates age for each dated node calibration.  
    - dated_mean_sample_clements.tre <- dated taxon addition tree cloud, 100 topologies from the taxon addition treeset using the mean node age for each node calibration. 
    - MCC.tre <- Maximim clade credibility tree including all taxa in this version of the taxonomy summarized from the dated trees using random selections for the node calibrations. Labelled with Clements taxonomy labels.
            




