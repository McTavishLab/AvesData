README:

# Data stucture
## Taxonomy:
This directory contains folders for each year of the Clements taxonomy.  
- Clements_2021  
- Clements_2022  
- Clements_2023  

Each taxonomy_year directory contains:  
- OTT_crosswalk_YEAR.csv
a CSV file mapping species from the [Clements taxonomy](https://www.birds.cornell.edu/clementschecklist/introduction/updateindex/october-2023/download/?__hstc=60209138.b9804d29db01561a7e696935f1b2fe77.1722097297040.1727728190990.1728510098461.4&__hssc=60209138.1.1728510098461&__hsfp=3468990387&_ga=2.238563136.176428784.1728510098-449536986.1722097296) for that taxonomy year to [OpenTreeTaxonomy (OTT)](https://tree.opentreeoflife.org/taxonomy/browse?name=Aves) identifiers (e.g. OTT_crosswalk_2021.csv).
Also includes mapping from species in Clements to their Avibase id, and to the names for those taxa in the [IOC World Bird List v14.1](https://www.worldbirdnames.org/new/) , [Birdlife/HBW 8](https://datazone.birdlife.org/species/taxonomy), and the [Howard and Moore v4 taxonomy](https://www.aviansystematics.org/the-howard-and-moore-complete-checklist)"

- Column names and contents
    * TAXON_ORDER <- from Clements Checklist csv
    * SPECIES_CODE <- from Clements Checklist csv
    * TAXON_CONCEPT_ID <- Avibase id imported from Clements Checklist csv
    * PRIMARY_COM_NAME <- from Clements Checklist csv
    * SCI_NAME <- from Clements Checklist csv
    * ORDER1 <- from Clements Checklist csv
    * FAMILY <- from Clements Checklist csv
    * ott_id <- id for that species in OTT
    * ott_name <- name for that species in OTT
    * ott_tax_sources <- sources for that taxon name in OTT
    * ott_match_type <- how link was made from Clements name to OTT id. (may be 'canonical_match', 'synonym_match', 'new_taxon_addition', or 'NA' for no match, as well some other idiosyncratic match types for hand corrections)
    * H_M_name <- best match name or names in the Howard and Moore v4 taxonomy(if multiple names matched they are a semi-colon seperated list)
    * H_M_match_type <- how the the avibase taxon concepts map between the Clements and Howard and Moore names. One of 'concepts_match', 'child_of', 'parent_of', 'overlaps', or 'missing'. 
    * Birdlife_name <- best match name or names in the Birdlife/HBW taxonomy(if multiple names matched they are a semi-colon seperated list)
    * Birdlife_match_type <- how the the avibase taxon concepts map between Clements and Birdlife names
    * IOC_name <- best match name or names in the Birdlife/HBW taxonomy(if multiple names matched they are a semi-colon seperated list)
    * IOC_match_type <- how the the avibase taxon concepts map between Clements and IOC names



- a taxon addition file capturing a suggested placement for species for which we do not yet have phylogenetic information  

- a copy of the ebird taxonomy file for that year. 
                    
## Trees:
This directory contains folders for each synth tree run, labelled by their version identifier (e.g. Aves_1.0) 

- Aves_1.3 

The most recent tree is Aves_1.3 and that directory contains all of these files. 
(Older trees folders have most of these files, and have a readme inculded in each folder)

For more details and code for how each of these files were generated see: https://github.com/McTavishLab/AvesTreeCode 
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




