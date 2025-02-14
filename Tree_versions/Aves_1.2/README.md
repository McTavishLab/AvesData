README.md

* dates_citations.txt <-input studies used to estimate dates  
* tree_citations.txt <- input studies used to estimate the phylogeny tree  
* all_node_ages.json <- a json file storing the age estimates for each internal node in the phylogeny only tree, with the metadata about what input study suggested that node age.
* OpenTree_synth <- folder containing the direct outputs of OpenTree Synthesis  (this is identical between Aves 1.2 and Aves 1.3) 
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


