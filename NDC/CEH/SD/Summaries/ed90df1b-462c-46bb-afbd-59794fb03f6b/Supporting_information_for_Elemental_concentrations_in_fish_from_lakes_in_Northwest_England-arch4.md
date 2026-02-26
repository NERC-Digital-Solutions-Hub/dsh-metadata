# Material and methods and metadata

## Study Overview
- Research conducted in 2012 and 2013 as part of CEH monitoring studies.
- Sampling locations: Windermere, Bassenthwaite Lake, and Derwent Water in the English Lake District, UK.
- Target species: Roach (Rutilus rutilus), Perch (Perca fluviatilis), Ruffe (Gymnocephalus cernuus), Brown trout (Salmo trutta), Pike (Esox lucius), Vendace (Coregonus albula).

## Sample Handling and Preparation
- Samples frozen at -20°C as soon as possible after collection.
- Processing: defrost, weigh, gut, then ashed at 500°C.
- Ashed material weighed; results reported as mg kg-1 fresh weight after conversion from ash weight using a sample-specific fresh-to-ash ratio.

## Chemical Analysis
- Digestion: ashed samples digested with aqua regia (3:1 HNO3:HCl) at 175°C for 12 minutes using a microwave (CEM MarsXpress).
- Analytical techniques: ICPMS (Inductively Coupled Plasma Mass Spectrometry) or ICPOES (Inductively Coupled Plasma Optical Emission Spectrometry).
- ICPMS operation modes:
  - Quantitative: external calibration with internal standards (Ga, In, Re) to correct drift and matrix effects.
  - Semi-quantitative: kinetic energy discrimination (KED) mode with helium for broader mass range extrapolation.
- Calibration and detection: Limits of detection (LODs) derived from reagent blanks; method LODs account for digestion dilution. For some elements in semi-quantitative mode where LODs could not be derived from blanks, LODs were estimated (0.001 µg L-1, equivalent to a mean method LOD of 0.001 mg kg-1).

## Data Processing and LOD Handling
- Concentrations reported as mg kg-1 fresh weight (converted from ash weight using sample-specific fresh-to-ash ratios).
- Non-detects denoted with "<" in respective columns; a separate scheme addresses LODs for different measurement modes.

## Data Structure, Metadata, and Provenance
- Laboratory and sample identifiers: Laboratory_id (CEH centralised chemistry laboratory), Sample_id (CEH Radiochemistry laboratory unique sample identifier).
- Metadata fields include: Lake, Fish_species_common_name, Fish_species_latin_name, Site_name_or_number, Date_fish_sampled, Gutted_ashed_fish_mass_in_grams, Gutted_fresh_fish_mass_in_grams, Ratio_of_wet_fish_mass_to_ashed_fish_mass.
- Elemental data columns span ICPMS and ICPOES results, with naming conventions such as Li_mg_kg_quantitative, Be_< for below-LOD, Na_ICPOES_mg_kg_quantitative, Fe_ICPOES_mg_kg_quantitative, etc., covering a wide range of elements and measurement modes (quantitative and semi-quantitative).
- Data dictionary structure provided to define each field (e.g., Lake, Date_fish_sampled, element-specific concentration columns, and their units).

## Use and Applications
- Data intended for model validation in radioecological wildlife transfer contexts (reference: Beresford et al., 2015, Journal of Environmental Radioactivity, "Making the most of what we have: application of extrapolation approaches in radioecological wildlife transfer models").
- Metadata-rich dataset supports reproducibility, discoverability, and integration within broader data ecosystems and partner networks.

## Data Quality, Standards, and Governance
- Emphasis on robust documentation of sampling, preparation, analytical methods, calibration, LOD treatment, and data fields to support data quality and reuse.
- Acknowledges potential challenges such as detection limits, data standardization across elements and modes, and the need for clear metadata to ensure correct interpretation and integration across datasets and sectors.