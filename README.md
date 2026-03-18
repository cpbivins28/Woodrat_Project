Woodrat Project
ITS1 fecal metabarcoding of big-eared woodrats (Neotoma macrotis) in California foothill oak woodlands. This repository contains the sequence processing pipeline, analytical code, and working data tables used in the study.

Repository Structure
Code_for_sequence_processing/
Code covering the full pipeline from raw Illumina MiSeq reads to analysis-ready data tables.

Trimming_and_AMPtk_processing — Adapter and quality trimming with Trimmomatic, followed by OTU clustering, taxonomy assignment, and denoising with AMPtk.
Post_AMPtk_R_code — Imports the AMPtk .biom file into R as a phyloseq object, cleans taxonomy columns, assigns functional guilds using FungalTraits, converts raw read counts to relative abundance and presence/absence matrices, and exports the guild table, raw OTU table, relative abundance OTU table, and metadata table.
Custom_BLAST_Analysis — Improves OTU taxonomic assignments using a custom local voucher-based ITS database combined with the California statewide FUNDIS ITS database.
Collapse_redundant_OTUs_and_update_taxonomy_and_primary_lifestyles_based_on_BLAST_results — Collapses redundant OTUs identified during the BLAST analysis, then updates taxonomy and primary lifestyle assignments in the guild table accordingly.

Code_for_figures_and_tables/
R code for the major statistical analyses in the study and Python code for generating figures.
Working_data/
The analysis-ready data tables used throughout the study:

Metadata table
Guild table (taxonomy and functional lifestyle assignments per OTU)
Raw read count OTU table (with collapsed OTUs, post-BLAST)
Relative abundance OTU table (read counts transformed to proportions summing to 100 per sample)
