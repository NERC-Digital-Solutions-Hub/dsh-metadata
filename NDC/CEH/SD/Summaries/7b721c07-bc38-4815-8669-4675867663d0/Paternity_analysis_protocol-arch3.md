# Paternity of Eschscholzia californica plants introduced to habitats comprising different floral cover

## Overview
- A dataset from a 2015 field experiment in Hillesden estate, Buckinghamshire, UK, examining how floral resources influence pollination services to isolated Eschscholzia californica plants.
- Focuses on paternity and mating system outcomes (selfing vs outcrossing) across habitat types with differing floral cover.
- Data collected, processed, and interpreted by T.M. Evans; data available as a single CSV with rich metadata.

## Experimental design
- Four 100-hectare replicate blocks, each >500 m apart.
- Sixteen experimental arrays (four per block), each array containing three E. californica plants spaced 1 m apart in a triangular arrangement.
- At block centers, four arrays positioned along a 150 m transect crossing between florally rich wildflower patches and florally poor ground (bare/fallow or grazed grassland), ensuring two arrays in each habitat type per block.
- Field exposure duration: 16 days to ensure full anthesis and multiple pollination events.
- About 48 plants with distinct genotypes deployed across the landscape, selected to maximize homozygosity within arrays for a chosen locus.

## Collection methods
- Plants grown from seed under controlled glasshouse conditions; DNA extracted from leaf tissue of 95 plants using Qiagen DNeasy 96 kit.
- Seven non-overlapping microsatellite loci genotyped; PCR with fluorescently labeled primers; fragment analysis on ABI3730; allele scoring in Genemarker.
- Ambiguous alleles verified by cloning and sequencing; four plants per array ensured genotype differentiation across loci.
- Flowers removed prior to field placement; one bud per plant protected to simulate pollinator exclusion; field remained in place for 16 days.
- After field exposure, fruits tagged and plants stored under controlled glasshouse conditions until maturation.

## Analytical methods
- Progeny genotyped (~10 per plant; mean ≈ 9.5) to detect pollination events.
- Selfing vs outcrossing determined by comparing progeny genotypes to maternal genotype across seven loci.
- Paternity assigned for progeny using Cervus 3.0.7; trio-based likelihoods with a Delta score to identify the most likely paternal parent.
- Only assignments with high confidence (Delta confidence > 95%) were retained.
- For each paternal assignment, recorded habitat of pollen movement and distance traveled; data indicate whether pollen crossed habitat types.

## Data structure and contents
- All data stored in a single CSV: Paternity_analysis_of_introduced_Eschscholzia_californica_plants.csv.
- Key columns:
  - Block: replicate block identifier.
  - Experimental_array: array identifier within a block.
  - Plant_identification_number: plant ID prior to field transfer.
  - Fruit_number: fruit analyzed; “Maternal” for maternal samples.
  - Habitat / Treatment: location type (florally rich/poor) and experimental treatment.
  - Sample_identification: sample IDs; ends with M for maternal samples; others are progeny.
  - LociX_AlleleY: allele sizes for each of seven loci (X = locus 1–7; Y = allele 1 or 2).
  - Parentage: manual paternity assessment from allele data.
  - Paternity_analysis: paternal ID as determined by Cervus; “?” if confidence < 95%.
  - Distance_of_pollen_movement: metres between maternal and paternal samples.
  - Habitat_crossed: habitat type of pollen movement; NA when paternity could not be assigned with confidence.
- Data quality notes: some loci entries NA where amplification failed; all data are intended to support inferences about pollination dynamics and pollen flow.

## Data provenance and sharing
- Dataset is described as complete and was collected and interpreted by Evans (T.M. Evans).
- Metadata-rich structure supports transparency, verification, and reuse for monitoring and policy evaluation purposes.
- Uses standard, reportable genetic-analysis tools (Genemarker for allele scoring; Cervus for paternity).

## Relevance for monitoring frameworks
- Demonstrates a genetics-based approach to quantify pollination services as environmental health indicators.
- Provides a structured data model to capture spatially explicit pollen movement and habitat effects on reproduction.
- Illustrates integration of field design, molecular methods, and analytical pipelines for monitoring policy-relevant outcomes.
- Highlights the importance of high-confidence assignments, metadata completeness, and clear documentation for data governance and public sharing.

## Limitations and considerations
- Some data points marked NA due to unsuccessful amplification.
- Paternity inferences rely on a 95% confidence threshold; lower-confidence assignments are excluded, which may limit completeness in some contexts.
- Specific to a single estate and habitat configurations; extrapolation should consider site-specific factors.