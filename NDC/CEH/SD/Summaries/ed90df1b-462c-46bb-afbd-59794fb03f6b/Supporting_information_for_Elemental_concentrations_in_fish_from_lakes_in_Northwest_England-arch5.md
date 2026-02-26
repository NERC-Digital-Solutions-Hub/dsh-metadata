# Material and methods and metadata

## Purpose and scope
- Documents the sampling, analytical methods, and metadata for fish samples collected in 2012–2013 from Windermere, Bassenthwaite Lake, and Derwent Water in the English Lake District.
- Species included: Roach, Perch, Ruffe, Brown trout, Pike, and Vendace.
- Data intended to support model validation in radioecology (e.g., wildlife transfer models).

## Sampling and specimen handling
- Samples collected during CEH monitoring studies; stored frozen at -20°C as soon as possible after collection.
- Processing: defrost, weigh, gut, ashing of whole fish at 500°C, and weigh ash.
- Fresh samples converted to ash-based measurements for reporting; results expressed as mg/kg fresh weight (mg/kg FW).

## Analytical methods and QA/QC
- Digestion: aqua regia (3:1 HNO3:HCl) at 175°C for 12 minutes using a microwave.
- Measurements: ICPMS or ICPOES.
  - Quantitative mode: external calibration with internal standards (Ga, In, Re) to correct drift and matrix effects.
  - Semi-quantitative mode (ICPMS with kinetic energy discrimination and He): uses a concentration-to-intensity curve for broad mass-range extrapolation.
- Limits of detection (LODs):
  - Calculated from reagent blanks (mean + 3 SD) and adjusted for dilution.
  - For some semi-quantitative cases where blanks couldn’t determine LODs, an instrument LOD of 0.001 µg/L was assigned.
- Data reporting: results as mg/kg fresh weight; conversion from ash via lake-specific fresh-to-ash mass ratio.
- Provenance of data: results linked to CEH centralised chemistry laboratory identifiers (Laboratory_id, Sample_id) for traceability.
- Reference usage: dataset intended for model validation work (citation provided in the text).

## Metadata and data dictionary (structure and fields)
- Key identifiers and context:
  - Laboratory_id and Sample_id: CEH centralised chemistry laboratory identifiers.
  - Lake and Site_name_or_number: origin of the lake site.
  - Date_fish_sampled: sampling date (dd/mm/yyyy).
  - Fish_species_common_name and Fish_species_latin_name: species names.
  - Site_name_or_number: CEH Lake ecosystems group site identifier.
- Physical characteristics:
  - Gutted_ashed_fish_mass_in_grams: mass of ashed fish sample with gut removed.
  - Gutted_fresh_fish_mass_in_grams: mass of fresh fish sample with gut removed.
  - Ratio_of_wet_fish_mass_to_ashed_fish_mass: conversion factor from fresh to ash mass.
- Measurement data (element-specific, method-dependent):
  - Quantitative (e.g., Li_mg_kg_quantitative, Be_mg_kg_quantitative, Na_ICPOES_mg_kg_quantitative, etc.): concentrations in mg/kg fresh weight.
  - Semi-quantitative (e.g., S_mg_kg_semi_quantitative, Br_mg_kg_semi_quantitative, etc.): concentrations in mg/kg fresh weight.
  - < indicators (e.g., Be_<, Al_<, Co_<, etc.): concentration at or below the limit of detection.
  - Unit consistency: mg per kg for most element measurements; grams and other fields noted where relevant.
- Coverage:
  - Includes a broad suite of elements measured by ICPMS or ICPOES, with a mix of quantitative, semi-quantitative, and censored (<) entries.
- Documentation style:
  - Explicit explanations accompany many fields, outlining the measurement method, units, and interpretation of below-LOD values.

## Data governance, sharing, and provenance
- Rich, machine-actionable metadata and a detailed data dictionary enhance findability, understandability, and reusability.
- Provenance is maintained via laboratory and sample identifiers, lake/site metadata, and clear method descriptions (instrument mode, internal standards, LOD methodology).
- Data suitable for deposition in portals and for reuse in scientific analyses; work can be documented and updates managed while respecting any sharing restrictions.

## Practical implications for reuse
- Researchers can filter by lake/site, fish species, date, or element to reproduce or validate models.
- The combination of raw mass data, ash conversions, and element concentrations supports transparent QA/QC and traceable data lineage.
- The dataset’s explicit LOD handling and method details support robust interpretation of non-detects and measurement uncertainties.