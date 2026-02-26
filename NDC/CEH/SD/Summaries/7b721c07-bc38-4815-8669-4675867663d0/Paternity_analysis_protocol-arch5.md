# Paternity of Eschscholzia californica plants introduced to habitats comprising different floral cover

## Overview
- Dataset describes paternity of progeny from Eschscholzia californica plants introduced into habitats with varying floral cover.
- Collected in June 2015 at Hillesden estate, Buckinghamshire, UK.
- Plants genotyped at seven microsatellite markers; paternity assigned with Cervus; seeds scored as selfed or outcrossed.
- Part of a larger experiment on how floral resources influence pollination services to isolated plants.
- Complete dataset, collected and interpreted by T.M. Evans.

## Experimental design
- Greenhouse-origin plants grown and then introduced as experimental arrays:
  - Each array comprises three E. californica plants, 1 m apart, in a triangular formation.
  - 16 arrays across four 100 ha replicate blocks (>500 m apart).
  - Within each block, a central transect of four arrays: two in florally rich habitat and two in florally poor habitat (50 m spacing along 150 m transect).
- Field period:
  - All open flowers removed; one bud per plant covered to simulate a pollinator-excluded flower.
  - Field exposure lasted 16 days to ensure full flower maturation and multiple pollination events.
  - After exposure, fruits tagged to ensure field-originating development; plants stored under controlled glasshouse conditions until maturation.

## Data collection and laboratory methods
- Plant material and DNA:
  - 95 plants sampled; DNA extracted using Qiagen DNeasy 96 Plant kit.
  - DNA quantified, diluted to 10 ng/µl.
- Genotyping:
  - Seven non-overlapping microsatellite markers; PCR conditions specified; some loci multiplexed.
  - Fragment analysis conducted on ABI3130/3730; alleles scored with Genemarker V1.95.
  - Ambiguous alleles cloned and sequenced to confirm true alleles.
- Plant selection for field deployment:
  - 48 plants selected with distinct genotypes; arrays designed so three plants per array were homozygous for the same allele at a selected locus, with different alleles across arrays.
- Paternity and flowering details:
  - All flowers from the 48 plants removed prior to field placement; one bud per plant pollinator-excluded.
  - After field exposure, fruits were tagged to ensure only local field-origin pollen contributed to analysis.

## Data structure and contents
- Data stored in a single CSV: Paternity_analysis_of_introduced_Eschscholzia_californica_plants.csv
- Key columns:
  - Block: replicate block identifier (4 blocks)
  - Experimental_array: identity of each array (within a block)
  - Plant_identification_number: ID for each plant prior to field deployment
  - Fruit_number: identifier for each fruit analyzed; "Maternal" used for maternal samples
  - Habitat: habitat type where the array was placed
  - Treatment: additional contextual information (e.g., florally rich vs poor)
  - Sample_identification: sample IDs; samples ending with "M" are maternal
  - LociX_AlleleY: alleles at each of the seven loci (X = locus, Y = allele copy 1 or 2)
  - NA entries indicate unsuccessful amplification
  - Parentage: manual paternity assessment based on allelic fits
  - Paternity_analysis: paternal assignment from Cervus; “?” indicates <95% confidence
  - Distance_of_pollen_movement: meters between maternal and paternal locations; NA if unresolved
  - Habitat_crossed: habitat type involved in pollen movement

## Data quality and validation
- Allele calls validated by cloning/sequencing for ambiguous cases.
- Paternity assignments constrained to high confidence: only trio ∆ confidence > 95% accepted.
- Selfing vs outcrossing determined by comparison of progeny to maternal genotype across seven loci.
- Pollen movement distances and habitat-crossed data captured only for high-confidence paternal assignments.

## Governance, provenance, and usability notes for data stewards
- Provenance:
  - Data collected and interpreted by T.M. Evans; part of a broader experiment on floral resources and pollination.
- Metadata completeness:
  - Detailed experimental design, collection methods, loci, analytical approach, and data structure are documented within the dataset description.
- Data format and accessibility:
  - Single CSV file with explicit column definitions and standardized locus naming; clear handling of maternal vs progeny samples and NA values.
- Reuse considerations:
  - Contextual information available on habitat types, block design, and experimental setup aids reproducibility and meta-analyses.
  - High-confidence paternity results enable robust analysis of cross-habitat pollen movement and selfing rates.
- Limitations and caveats:
  - Distance and movement data are only available for assignments with high confidence; unresolved cases are annotated as NA.
  - Data represent a single species and a specific experimental context; applicability to other systems should consider ecological differences.

## Use-case relevance for data stewardship
- Supports governance of experimental genetics datasets by illustrating:
  - Clear linkage between field design and molecular data.
  - Rigorous QC steps in genotyping and paternity inference.
  - Comprehensive metadata enabling discovery, understanding, and reuse by researchers evaluating pollination dynamics and habitat effects.