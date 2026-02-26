# Paternity of Eschscholzia californica plants introduced to habitats comprising different floral cover

## Overview
- Dataset on paternity of progeny from Eschscholzia californica plants introduced into habitats with differing floral cover.
- Collected in June 2015 at the Hillesden estate, Buckinghamshire, UK.
- Plants were genotyped at seven microsatellite markers and deployed in experimental arrays across a landscape to study pollination services.

## Experimental design and study area
- Four 100-hectare replicate blocks, each separated by more than 500 meters.
- Within each block, four experimental arrays (triplets of E. californica plants) placed at 50-meter intervals along a 150-meter transect near the boundary between florally rich habitat and florally poor habitat (bare/fallow or grazed grassland).
- Each array comprised three plants arranged in a triangular formation (1 meter between plants).

## Data collection and genetic methods
- Plants grown in glasshouse conditions; 50 mg of fresh leaf tissue from 95 plants used for DNA extraction.
- DNA quantified and diluted; seven non-overlapping microsatellite markers used (some amplified in multiplex).
- Fragment analysis performed; alleles scored; ambiguous alleles verified by cloning/sequencing.
- From 48 plants with distinct genotypes, field deployments were established; all open flowers removed except one bud per plant to simulate pollinator-excluded flowers for a subset.
- Field exposure lasted 16 days to ensure anthesis and multiple pollination events.
- Seeds collected and stored for maturation under controlled glasshouse conditions.

## Paternity analysis and assignment
- Progeny genotyped (approximately 10 per maternal plant) to detect selfing versus outcrossing.
- Selfing determined by exact maternal genotype matches across loci; outcrossing indicated by novel alleles not present in the mother.
- Paternity assigned with Cervus 3.0.7, comparing progeny to potential paternal samples within the same block while accounting for self-fertilisation.
- Only high-confidence paternity (Delta score > 95% and trio confidence) recorded.
- For each paternal assignment, recorded habitat crossed and distance of pollen movement (in meters); samples where paternity could not be determined are marked accordingly.

## Data structure and file format
- Single CSV file: Paternity_analysis_of_introduced_Eschscholzia_californica_plants.csv.
- Key fields include:
  - Block: replicate block identifier.
  - Experimental_array: array identifier within a block (three plants per array).
  - Plant_identification_number: plant ID prior to field transfer.
  - Fruit_number: identifying number for each analyzed fruit; "Maternal" for maternal samples.
  - Habitat and Treatment: location context of arrays.
  - Sample_identification: lab sample IDs; ends with "M" for maternal samples.
  - Loci alleles: columns lociX_AlleleY with allele sizes (NA if not amplified).
  - Parentage: manual paternity assessment based on alleles.
  - Paternity_analysis: paternal ID from Cervus; "?" if below 95% confidence.
  - Distance_of_pollen_movement: pollen transfer distance (meters); NA if undetermined.
  - Habitat_crossed: habitat type inferred for the pollen movement path.

## GIS relevance and potential map-based uses
- Spatial layout documented as discrete blocks, transects, and arrays, enabling:
  - Visualization of pollen movement distances between maternal and paternal plants.
  - Comparison of selfing vs outcrossing rates across florally rich vs. florally poor habitats.
  - Habitat-based analysis of pollination dynamics and cross-habitat pollen flow within replicate blocks.
- Data can be integrated into GIS workflows to produce maps of pollen flow, pollination services, and habitat effects, with future potential to link to geographic coordinates if location metadata are expanded.

## Data quality, provenance, and notes
- Alleles verified through cloning/sequencing to confirm true alleles.
- Field exposure and sampling designed to ensure robust assessment of pollination over a fixed period.
- High-confidence paternity only included in the final dataset, enhancing reliability for spatial analyses.