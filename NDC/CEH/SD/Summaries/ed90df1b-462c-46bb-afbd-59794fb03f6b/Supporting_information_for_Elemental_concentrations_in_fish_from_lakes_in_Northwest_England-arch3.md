# Material and methods and metadata

## Overview
- Describes fish sampling and chemical analysis performed in 2012–2013 as part of CEH monitoring studies.
- Locations: Windermere, Bassenthwaite Lake, and Derwent Water in the English Lake District.
- Species collected: Roach (Rutilus rutilus), Perch (Perca fluviatilis), Ruffe (Gymnocephalus cernuus), Brown trout (Salmo trutta), Pike (Esox lucius), and Vendace (Coregonus albula).
- Purpose: provide data for model validation in radioecological wildlife transfer studies; results intended to support extrapolation approaches and model evaluation.

## Sampling and specimen processing
- Fish samples were collected in 2012–2013 and preserved by freezing at −20°C as soon as possible.
- Post-collection processing: defrost, weigh, gut, and ashing at 500°C.
- Ashed samples were digested with aqua regia (3:1 HNO3:HCl) at 175°C for 12 minutes using a microwave.
- Masses reported as mg/kg fresh weight (converted from ash weight using fresh-to-ash mass ratios).

## Laboratory analysis
- Analytes measured by ICPMS (ICP-Mass Spectrometry) or ICPOES (Inductively Coupled Plasma Optical Emission Spectrometry).
- Quantitative measurements: external calibration with internal standards (Ga, In, Re) to correct drift/matrix effects.
- Semi-quantitative measurements: ICPMS in kinetic energy discrimination (KED) mode with helium for broader mass range extrapolation.
- Instrument detection limits (LODs): calculated from reagent blanks; method LODs account for digestion dilution; for some elements, LODs were not derivable from blanks and were set to 0.001 µg/L (equivalent to 0.001 mg/kg fresh weight).
- Data presentation: results as mg/kg fresh weight.
- Data structure: includes a variety of fields for sample identification, lake/site, species, date, and detailed element concentrations.

## Data collection and metadata structure
- Key identifiers: Laboratory_id (CEH centralised chemistry laboratory), Sample_id (CEH Radiochemistry laboratory), Lake, Site_name_or_number, Date_fish_sampled.
- Biological details: Fish_species_common_name, Fish_species_latin_name.
- Sampling metadata: Gutted_ashed_fish_mass_in_grams, Gutted_fresh_fish_mass_in_grams, Ratio_of_wet_fish_mass_to_ashed_fish_mass.
- Element concentration fields: numerous columns across quantitative and semi-quantitative measurements (e.g., Li_mg_kg_quantitative, Be_mg_kg_quantitative, Na_ICPOES_mg_kg_quantitative, Fe_ICPOES_mg_kg_quantitative, Cd_mg_kg_quantitative, Pb_mg_kg_quantitative, U_mg_kg_quantitative, etc.), with some entries marked as "<" to indicate below the limit of detection.
- Data labeling: many columns indicate the measurement method (ICPMS quantitative, ICPMS semi-quantitative, ICPOES quantitative/semi-quantitative) and associated units (mg/kg).
- Metadata emphasis: explicit documentation of each field’s meaning and unit, enabling traceability and reproducibility.

## Data handling, QA, and governance
- Quality assurance/isolation: clear QA steps implied by use of internal standards, calibration methods, blanks, and LOD determinations.
- Data transparency: detailed metadata and column explanations to verify data provenance and suitability for analysis.
- governance considerations (relevant to monitoring frameworks): explicit plan for sharing underlying data, and notes on how data management standards are established at the data source; data handling supports reproducibility and potential reuse in broader monitoring contexts.

## Data usage and references
- Primary use: support model validation in radioecological wildlife transfer research (e.g., extrapolation approaches in wildlife transfer models).
- Reference example: Beresford et al., 2015, Journal of Environmental Radioactivity, for model validation approaches.
- Output focus: dataset designed to enable transparent interpretation of contaminant concentrations in fish and to underpin comparative evaluations and monitoring-driven policy decisions.