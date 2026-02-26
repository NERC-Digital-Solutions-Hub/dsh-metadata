# DATASET: Stable water isotopes in Western Siberian inland waters

## Overview
- Part of the JPI/NERC SIWA project: Climate impact on the carbon emission and export from Siberian inland waters (grant NE/M019896/1).
- Collaborative data generation and analysis led by Northern Rivers Institute (UoA) with GET, TSU, and UU.
- Focus: stable water isotopes (δ2H and δ18O) across rivers, lakes, floodplains, and soils in the Western Siberian inland waters region.

## Data collection & sampling
- Sample types: rivers, lakes, floodplain (flood samples), soil solutions.
- Sampling methods:
  - River: grab samples from the middle of the channel (preferred from a bridge or bank) at ~0.5 m depth in flowing water.
  - Lakes: samples collected from a boat at ~0.5 m depth; thermokarst lakes are very shallow (0.5–1.0 m).
  - Soil: ceramic cup suction lysimeters at 20–50 cm depths (typically ~10 cm above permafrost), filtered in the field.
- Handling:
  - Filters used on site if water had excess organic matter; discard first 2 mL of filtrate.
  - Inundated areas sampled as grab samples from a boat.
- Sample storage pre-analysis: kept in the dark at 4–6 °C until analysis; archived after analysis.

## Laboratory analysis & QA
- Instrument: Los Gatos DLT-100 laser isotope analyser.
- Precision: δ2H ±0.4 ‰; δ18O ±0.1 ‰.
- Isotope reporting: δ-notation relative to Vienna Standard Mean Ocean Water (VSMOW).
- QA: samples analyzed in UoA isotope laboratory; quality control performed by Ala-aho; results compiled into a database.

## Data storage, provenance & archiving
- Storage: after analysis, samples stored in UoA facilities; traceable by analysis date and sample ID.
- Sample handling: archived according to analysis date and sample ID for easy traceability.
- Shipping/transfer: samples shipped to the University of Aberdeen for analysis; records maintained for traceability.

## Dataset structure & metadata
- File name: SIWA_stable_water_isotope_data.txt
- File encoding: UTF-16LE with BOM
- Structure: tabular data; each row represents a unique sample; each column a data field
- Key fields and descriptions:
  - T_ID: sample ID linking to vial
  - sample_ID: alternative sample ID
  - lat_N: latitude (WGS84, decimal degrees, North)
  - long_E: longitude (WGS84, decimal degrees, East)
  - sample_type: type of inland water (flood, lake, river, soil)
  - sample_description: detailed English/Russian description
  - name_engl: name of water body in English
  - sampling_date: date of collection (dd/mm/yyyy)
  - analysis_date: date of analysis (dd/mm/yyyy)
  - d2H: δ2H value (‰)
  - d18O: δ18O value (‰)
- Data semantics:
  - Lat/long provide geographic context for spatial analyses and mapping.
  - Sample_type and sample_description enable grouping by environment and water body characteristics.
  - Dates enable temporal analyses and alignment with sampling campaigns.
  - Isotope values enable hydrological and hydrometeorological interpretations.

## Usage & accessibility
- Dataset is structured to enable self-serve exploration: clear field definitions, units, and date formats facilitate joining with other datasets.
- Metadata supports traceability from sample collection through analysis to final data points.
- Cross-reference note: detailed sampling methods for some contexts are described in Raudina et al. (2017).

## Acknowledgements & authors
- Acknowledgement of lab analysis contributions: Jonathan J. Dick and Audrey Innes (UoA) for laboratory work.
- Full author list spans UoA, GET, TSU, and UU, reflecting a multi-institution collaboration.