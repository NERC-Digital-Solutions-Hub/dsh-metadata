# Paternity of Eschscholzia californica plants introduced to habitats comprising different floral cover

- Purpose and context
  - Dataset on paternity of progeny from Eschscholzia californica introduced into habitats with varying floral cover to study pollination services to isolated plants.
  - Field site: Hillesden estate, Buckinghamshire, UK; collection in June 2015.
  - Part of a larger experiment examining how floral resources influence pollination.

- Experimental design
  - Genotyped plants formed experimental arrays: three E. californica plants per array, arranged in a triangle with 1 m spacing.
  - 16 arrays across four replicate blocks (each 100 ha) separated by >500 m.
  - Each block contains a transect with four arrays at 50 m intervals across the boundary between florally rich and florally poor habitats (two arrays in each habitat type).

- Plant deployment and collection
  - 48 plants with distinct genotypes selected and deployed; within blocks, arrays were arranged so that the three plants in an array were homozygous for different alleles at a chosen locus.
  - All open flowers removed; one bud per plant covered to simulate pollinator exclusion in a subset.
  - Field exposure lasted 16 days to ensure full anthesis and multiple pollination events.
  - Fruits were tagged and later collected for maturation in controlled glasshouse conditions.

- DNA collection and genotyping methods
  - Growth and DNA extraction: plants grown in compost under glasshouse; DNA from leaf tissue (about 50 mg per plant) using Qiagen DNeasy kit; DNA quantified and diluted for PCR.
  - Markers: seven non-overlapping microsatellite markers (DS-33 dye set); some primers multiplexed.
  - PCR and fragment analysis: standardized PCR protocol; products run on ABI3730; alleles scored using Genemarker; ambiguous alleles cloned and sequenced for verification.
  - Plant selection for field deployment: 48 plants with distinct genotypes; efforts to ensure within-array homozygosity for different alleles at a target locus.

- Progeny and paternity analysis
  - Progeny sampling: ~10 offspring per maternal plant field-exposed (mean ~9.5; range not specified).
  - Selfing vs outcrossing: determined by comparing progeny genotypes to maternal genotype; selfed if progeny matched maternal alleles at all loci, otherwise outcrossed if novel alleles appeared.
  - Paternity assignment: Cervus 3.0.7 used to assign paternal parentage from within-block potential fathers; accounts for selfing and uses likelihood-based delta scores.
  - Confidence threshold: only paternal assignments with delta score giving trio confidence >95% (high confidence) recorded.
  - Recorded data: for each progeny, habitat of pollen origin (the habitat crossed) and pollen movement distance.

- Data structure and contents
  - Single CSV file: Paternity_analysis_of_introduced_Eschscholzia_californica_plants.csv.
  - Key columns:
    - Block: replicate block identifier.
    - Experimental_array: array identifier within a block.
    - Plant_identification_number: plant IDs prior to field transfer.
    - Fruit_number: fruit identifiers; "Maternal" for maternal samples.
    - Habitat and Treatment: location and experimental treatment.
    - Sample_identification: sample IDs for each seed; maternal samples end with 'M'; progeny samples are others.
    - lociX_AlleleY: seven loci with two alleles each (mapped as X = locus, Y = allele number 1 or 2); NA if amplification failed.
    - Parentage: manual paternity scoring from alleles.
    - Paternity_analysis: paternal ID from Cervus; '?' if confidence <95%.
    - Distance_of_pollen_movement: metres between maternal and paternal plants; NA if undetermined.
    - Habitat_crossed: habitat type where the pollen originated.
  - All data documented as part of the study by Evans, T.M.

- Quality, provenance, and scope
  - Data collected and interpreted by Evans, T.M.
  - Allele verification included cloning/sequencing for ambiguous cases.
  - Data designed to enable analyses of selfing vs outcrossing rates, paternal pollen-source habitat, and pollen dispersal distances across floral-resource gradients.

- Uses and potential analyses
  - Quantify how floral resource availability affects pollination success and selfing rates.
  - Analyze spatial patterns of pollen movement between florally rich and poor habitats.
  - Compare paternal origins relative to habitat type and distance, within-block constraints.
  - Integrate genotype data with field exposure to model pollinator-mediated gene flow in fragmented or resource-variable landscapes.