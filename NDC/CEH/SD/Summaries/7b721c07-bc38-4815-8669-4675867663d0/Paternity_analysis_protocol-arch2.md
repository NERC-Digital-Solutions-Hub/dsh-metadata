# Paternity of Eschscholzia californica plants introduced to habitats comprising different floral cover

## Objective and context
- Dataset details the paternity of progeny from Eschscholzia californica plants introduced to habitats with different floral cover.
- Part of a larger experiment examining how floral resources affect pollination services to isolated plants.
- Collected and interpreted by T.M. Evans; aims to enable assessment of pollination dynamics across habitat types.

## Study design and site
- Location: Hillesden estate, Buckinghamshire, UK; field work conducted in June 2015.
- Experimental framework: four 100 ha replicate blocks (total of 4 blocks), each containing four experimental arrays (16 arrays total).
- Habitat treatment: arrays positioned along a 150 m transect crossing the boundary between an established wildflower patch (florally rich) and bare fallow ground or grazed grassland (florally poor); within each block, two arrays in florally rich habitat and two in florally poor habitat.
- Spatial arrangement: arrays consist of three plants, 1 m apart in a triangular formation; blocks separated by >500 m.

## Experimental setup
- Plant material: Eschscholzia californica grown from seed in glasshouse conditions; 48 plants selected with distinct genotypes and placed across the landscape.
- Field preparation: all open flowers removed; one bud per plant covered with muslin to simulate pollinator exclusion; field exposure lasted 16 days to allow full anthesis and multiple pollination events.
- Deployment: fruits were tagged post-exposure to ensure only experiment-derived fruit was analyzed.
- Storage: plants stored under controlled glasshouse conditions until fruit maturation.

## Genotyping and plant selection
- Prior to field deployment, 95 plants were sampled for DNA extraction (50 mg leaf tissue each).
- DNA quantified and diluted; seven non-overlapping microsatellite loci amplified via PCR (some loci multiplexed).
- Alleles scored using Genemarker; ambiguous alleles validated by sequencing (TOPO TA cloning).
- From the genotyped set, 48 plants with distinct genotypes were deployed; where possible, triplets in arrays were homozygous for different alleles at a chosen locus to aid paternity assignment.

## Progeny collection and paternity analysis
- For each field-exposed maternal plant, approximately 10 progeny (mean ~9.5) were genotyped at seven loci.
- Selfing vs outcrossing determined by comparing progeny alleles to maternal genotype:
  - Selfed: progeny matches maternal genotype at all loci or is homozygous for a maternal allele.
  - Outcrossed: presence of novel alleles not found in the maternal genotype.
- Paternity assignment: Cervus 3.0.7 used with a trio analysis (mother, potential father, offspring); delta score (∆) used to identify the most likely father.
- Confidence threshold: only assignments with trio ∆ confidence > 95% retained.
- Outputs recorded: habitat of pollen movement, distance traveled (metres), and whether pollen crossed between habitats.

## Data structure and content
- Single CSV file: Paternity_analysis_of_introduced_Eschscholzia_californica_plants.csv
- Key columns:
  - Block: block identifier (four 100 ha replicates)
  - Experimental_array: array identifier within a block
  - Plant_identification_number: plant identity before field transfer
  - Fruit_number: fruit analyzed (or "Maternal" for maternal samples)
  - Habitat: location type (florally rich vs florally poor)
  - Treatment: experimental treatment designation
  - Sample_identification: sample IDs (samples ending with M are maternal)
  - Loci_X_Allele_Y: allele sizes for each of the seven loci
  - Parentage: manual paternity assessment from allele data
  - Paternity_analysis: paternal assignment from Cervus (or a “?” for <95% confidence)
  - Distance_of_pollen_movement: metres moved (NA if undetermined)
  - Habitat_crossed: habitat type crossed by the pollen
- All data are stored in one CSV; NA indicates unsuccessful amplification or undetermined results.

## Outputs, provenance, and accessibility
- Dataset is complete and was collected and interpreted by Evans, T.M.
- Designed to quantify selfing rates, paternal origins, and pollen dispersal distances across differing floral resource environments.
- Data format and standardized analysis facilitate sharing and integration with other environmental monitoring datasets.