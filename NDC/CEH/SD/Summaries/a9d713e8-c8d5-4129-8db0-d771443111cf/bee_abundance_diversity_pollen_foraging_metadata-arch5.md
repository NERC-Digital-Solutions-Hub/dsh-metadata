# Metadata taken from 'Providing foraging resources for solitary bees on farmland: current schemes for pollinators benefit a limited suite of species' by T.J. Wood, J.M. Holland and D. Goulson, 2016

## Overview
- Describes metadata and data files for a study comparing pollinator resources on Higher Level Stewardship (HLS) and Entry Level Stewardship (ELS) farms in Hampshire and West Sussex, UK (2013–2015).
- Data cover flora abundance and richness, bee abundance and richness, bee foraging behavior, plant-pollinator interactions, and pollen loads from solitary bees.
- Data collection followed standardized bee walk methodologies across multiple years and sampling rounds, with careful documentation of habitat types and management regime.

## Study design and data collection context
- Study area: nine HLS and ten ELS farms; HLS farms had a pollinator-focused habitat component for at least three years; ELS farms served as controls.
- Habitats surveyed: pollinator-focused flower-rich schemes, non-agricultural grass margins, hedgerows, and woodland edges; crops and agricultural grassland were not surveyed.
- Survey technique: standardized 3 km transects (varying by year) with bee activity recorded within 2 m of the recorder; plant species visited and purpose (pollen/nectar) noted.
- Timing: multiple rounds per year (2013–2014 distance-based transects; 2015 fixed-time surveys). All surveys conducted by a single operator (TJW) to minimize bias.
- Pollen sampling: foraging solitary bees captured in 2015; pollen loads quantified by volume and corrected for load size; pollen identified to species/genus using a reference library and standard microscopy.

## Datasets included (file-level descriptions)
- 2013_2014_floral_abundance_data.csv
  - Farm, Type (ELS/HLS), Round, Year, Species, Nature (wild or sown), Abundance (flowering units)
- 2013_2015_floral_richness_data.csv
  - Farm, Type, Round, Year, Species
- 2013_2014_bee_abundance_data.csv
  - Farm, Type, Round, Date, Species, Number
- 2013_2015_bee_richness_data.csv
  - Farm, Type, Round, Date, Species
- 2013_2015_flower_visitation_data.csv
  - Farm, Type, Round, Date, Species (bee), Number, Caste, Visiting (plant), Status (wild/sown/crop), Purpose (pollen/nectar), Family
- 2015_pollen_load_data.csv
  - Farm, Type, Round, Date, Species, Load (relative fullness), Netted on (plant species), Plant pollen (identified), Status, Proportion, Weight

## Variable definitions and data fields
- Key fields across datasets:
  - Farm: farm identifier
  - Type: ELS or HLS
  - Round: sampling round
  - Year/Date: sampling period
  - Species: plant or bee species
  - Nature/Status: wild, sown, or crop plant status
  - Abundance/Richness/Number: counts
  - Visiting/Purpose: bee visitation context (pollen or nectar)
  - Proportion/Weight: pollen load composition and calculated weights
- Pollen identification and counting:
  - Pollen loads analyzed by light microscopy; proportional volumes estimated along three lines across the cover slip.
  - Species represented <1% excluded; where identification was uncertain, genus-level classification used.
  - Brassica pollen largely treated as crop-derived and excluded from sown vs wild comparisons when appropriate.

## Data processing and analysis workflow
- Pollen data: load proportions converted to final weights; volume-based weighting to reflect pollen volume per species.
- Floristic and bee data: standardized to enable comparisons across farm types and years.
- Statistical analyses (described in metadata):
  - Generalised Linear Mixed-Effect Models (GLMMs) in R (v3.1.1) using lme4; negative binomial or Poisson distributions; year as random factor; management type as fixed factor.
  - Analyses include: bee and plant abundance and richness by management type; relationships between plant species richness and bee diversity/diet breadth; pollen species richness in relation to plant richness; pollen load composition relative to sown vs wild flora; correlations between sown-flower proportion and pollinator visitation.
  - Observational and pollen-load datasets analyzed separately; seven common polylectic bee species analyzed in detail with ~30 loads per species.
- Data integrity approaches:
  - All field work conducted by a single observer to minimize bias.
  - Sampling conditions standardized (time of day, temperature thresholds, weather prerequisites).

## Data quality, limitations, and governance notes
- Limitations noted in methods include potential over- or underestimation of pollen use due to collection timing and the difficulty of pollen identification for certain species; Hylaeus visits recorded as visits due to pollen transfer mechanisms.
- Crop pollen (Brassica) treated cautiously to avoid misattributing wild pollen use; some taxa identified only to genus level when species-level resolution was not possible.
- Data are organized with explicit farm-level identifiers and a clear distinction between sown, wild, and crop plant status, enabling transparency for reuse while maintaining site-level context.

## Data sharing, documentation, and provenance
- Metadata explicitly documents file structures and column headings (including Appendix S1–S3 references for full taxonomic lists and methods).
- Provided data are in CSV format with self-contained descriptions of fields and statuses to support reproducibility and secondary analyses.
- Acknowledges funding and references a broad body of supporting literature, indicating alignment with established pollinator and agri-environment scheme research.

## Practical guidance for data stewards and users
- Ensure consistent interpretation of “Nature/Status” fields (wild, sown, crop) across analyses and downstream datasets.
- Maintain linkage between floral abundance/richness data and corresponding bee data by Farm, Round, and Year to support longitudinal analyses.
- Use pollen-load Weight and Proportion fields to reconstruct species-level pollen contributions in polylectic bee diets, while excluding negligible (<1%) taxa as appropriate.
- Leverage the detailed methodology (survey rounds, timing, and conditions) to assess comparability with other years or regions and to calibrate future data collection efforts.
- Monitor for potential biases introduced by single-observer data collection and consider replication or cross-validation in future studies.