# Source apportionment of annual nutrients and sediment loads to rivers in England and Wales modelled with SEPARATE

- Purpose: quantify annual loads of nitrogen, phosphorus and fine-grained sediment from both diffuse and point sources to rivers at Water Framework Directive (WFD) waterbody scale, using SEPARATE version 2.
- Coverage: non-coastal WFD cycle 2 waterbodies across England and Wales; provides both individual and cumulative waterbody data.
- Outputs: pollutant emissions broken down by source and by pollutant type; supports policy delivery and monitoring under the Water Framework Directive.

## SEPARATE description

- SEPARATE (SEctor Pollutant AppoRtionment for the AquaTic Environment) is a multi-pollutant source apportionment framework.
- Data are summarised by non-coastal WFD Cycle 2 waterbodies, for both individual waterbodies and cumulative catchments.
- Emissions come from diffuse sources (agriculture, urban, river channel banks, atmospheric deposition, groundwater) and point sources (sewage treatment works, septic tanks, CSOs, storm tanks).

## Pollutant emission sources

- Diffuse agricultural
  - Inputs from agricultural losses modelled with the ADAS Agricultural Pollutant Transfer framework, built on PSYCHIC and NIPPER models for phosphorus, sediment, and nitrogen respectively.
  - Key inputs: soils data, daily weather, elevation, crop data, field boundaries, manure distribution (MANURE-GIS), fertiliser practices.
- Diffuse urban
  - Inputs produced by combining annual urban runoff (Wallingford Modified Rational Method) with representative event mean concentrations (EMCs) from published data.
- River channel bank sources
  - Erosion inputs estimated with a national-scale bank erosion index, accounting for river regime, excess shear stress, and channel network density.
- Direct atmospheric deposition
  - Nitrogen deposition: NEAP-N; phosphorus deposition: based on rainfall-derived concentrations from ECN sites.
- Sewage treatment works (STWs)
  - Emissions estimated from a national register of consented discharges with measured flow and pollutant concentrations (2010–2012 data); very small STWs removed due to data gaps.
- Septic tanks
  - Emissions sourced from recent Environment Agency phosphorus studies.
- Combined sewer overflows (CSOs)
  - Discharges modelled using SAGIS framework, assuming CSOs discharge when rainfall and sewer capacity conditions exceed thresholds.
- Storm tanks
  - Emissions estimated similarly to CSOs, with retention before overflow.
- Groundwater
  - Inputs for nitrogen, phosphorus, and sediment via groundwater pathways (where applicable).

## Uncertainty and limitations

- National-scale results must be interpreted with local decision-making in mind; caution for waterbodies smaller than ~25 km2 (about 43% of waterbodies) due to data limitations.
- Agricultural baseline represents 2010–2012 with mitigation; STW emissions reflect tightened permits and nutrient stripping (not all small outfalls reliably captured).
- STW data may have multiple outfalls/permits needing alignment; STW emissions to estuarine/coastal zones are not included.
- Channel bank contributions do not account for any mitigation works along margins.
- Temporal coverage is not uniform across sectors (e.g., agriculture 2010 vs 2010–2012 for STWs).

## Format and how to use the dataset

- Format: CSV files; can be mapped in GIS by joining to WFD River Waterbody Cycle 2 shapefiles using EA_WB_ID.
- Structure: Table 3 describes the file columns, including regional identifiers, waterbody details, and per-source/per-pollutant load figures (local and cumulative) in tonnes per year and percentages for mitigated vs unmitigated (local) and cumulative.
- Columns capture multiple pollutants: X (nutrients/sediment), with specific sub-columns for total nitrogen, total phosphorus, dissolved phosphorus, and sediment, plus direct deposition and other components.
- Mapping and usage: join CSVs to WFD Cycle 2 shapefiles to visualise pollution loads by waterbody; supports national policy assessment and local decision support, with a baseline and mitigation scenarios for agriculture and other sectors.

## Supporting information and references

- Supporting documentation available, including methodology and data sources used for SEPARATE framework and pollutant transfer models.
- Key references and data sources span PSYCHIC, NIPPER, ADAS frameworks, urban runoff models, bank erosion indices, atmospheric deposition datasets, STW discharge registers, SAGIS CSO framework, and various UK hydrological datasets.