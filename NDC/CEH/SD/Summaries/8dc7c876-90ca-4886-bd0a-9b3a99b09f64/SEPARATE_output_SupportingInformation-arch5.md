# Source apportionment of annual nutrients and sediment loads to rivers in England and Wales modelled with SEPARATE

## Overview
- Dataset models annual loads of total nitrogen, total phosphorus, dissolved phosphorus, and fine-grained sediment to rivers at Water Framework Directive (WFD) waterbody scale in England and Wales.
- Covers both diffuse sources (agriculture, urban, river channel banks, atmospheric deposition, groundwater) and point sources (sewage treatment works, septic tanks, combined sewer overflows, storm tanks).
- Implemented using SEPARATE version 2 (SEctor Pollutant AppoRtionment for the AquaTic Environment) and linked to non-coastal WFD Cycle 2 waterbodies.

## Data content and structure
- Tables described:
  - Table 1: Modelled pollution sources (source descriptions per category).
  - Table 2: Modelled pollutant emissions by source.
  - Table 3: File column names in descriptions (CSV structure).
- Output format:
  - Stored as CSV files that can be mapped in GIS by joining to WFD Cycle 2 shapefiles (via EA_WB_ID or waterbody ID).
  - Columns include region, catchment, waterbody name and ID, local vs cumulative areas, and pollutant load values.
  - Pollutants represented with abbreviations (e.g., X_au_L_t for agricultural unmitigated load in tonnes/year; X_to_L_t for waterbody total; X_dd_L_t for direct deposition, etc.).
  - Local and cumulative totals, as well as mitigated vs unmitigated agricultural values and bank erosion, urban diffuse, and other source components.
- Documentation and supporting materials:
  - Supporting documentation available via CEH catalogue.
  - References section provides context for models and data sources.

## Methods and data sources
- SEPARATE framework:
  - A national-scale, multi-pollutant source apportionment model for England and Wales, summarised by WFD cycle 2 waterbodies.
  - Combines diffuse and point-source emissions to the aquatic environment.
- Diffuse source inputs:
  - Agricultural: uses the ADAS Agricultural Pollutant Transfer (APT) framework built on PSYCHIC (phosphorus and sediment) and NIPPER (nitrogen losses); inputs rely on soils, weather, elevation, agricultural census, field boundaries, manure distribution (MANURE-GIS), fertiliser practices, and other agronomic data.
  - Urban: combines annual runoff (Wallingford Modified Rational Method) with representative event mean concentrations (EMCs).
  - River channel banks: bank erosion index incorporating river regime, excess shear stress, channel density, and geomorphology.
  - Atmospheric deposition: nitrogen via NEAP-N; phosphorus via rainfall-based concentrations.
  - Groundwater: pollutant content for groundwater pathway.
- Point source emissions:
  - Sewage treatment works (STWs): uses a national register of consented discharges with measured flows and pollutant concentrations (2010–2012 data); excludes very small STWs.
  - Septic tanks: emissions from a recent EA study.
  - Combined sewer overflows (CSOs) and storm tanks: emissions estimated using SAGIS framework assumptions (CSOs discharge when rainfall triggers, with volumes dependent on rainfall, sewer capacity, permeability; storm tanks similar approach with retention before discharge).
- Uncertainty and scale considerations:
  - Outputs are at the WFD cycle 2 waterbody level; caution advised for waterbodies <25 km² (approx. 43% of waterbodies) due to data accuracy and regional averaging.
  - Agricultural emissions are baseline (2010–2012) with/without prior mitigation; STW emissions reflect tightening permits and nutrient stripping progression through directives (estimates exclude estuarine/coastal environments).
  - Channel bank contributions and some outfall details may be incomplete; temporal coverage varies (e.g., 2010 versus 2010–2012).

## Uncertainty, limitations, and scope
- Interpretations should consider national-scale integration with local decision-making needs.
- Waterbodies under 25 km² have higher uncertainty due to data limitations.
- STW data may have residual uncertainties for smaller works; some outfalls and permits require expert resolution.
- Estuarine and coastal environments are not included; channel margin protection works are not accounted for in bank erosion estimates.
- Temporal alignment across sectors is not fully uniform (e.g., some inputs are 2010, others 2010–2012).

## Format, access, and governance
- Format: CSV data with the option to map against WFD River Waterbody Cycle 2 shapefiles.
- Key identifiers: waterbody ID (EA_WB_ID) to join with shapefiles.
- Data governance notes for Data Stewards:
  - Clear provenance through multiple validated models (APT, PSYCHIC, NIPPER) and national datasets (MO weather, NSRI soils, various EA and DoE data sources).
  - Documentation and supporting references accompany the dataset for traceability.
  - Acknowledges uncertainties and provides baseline vs mitigated scenarios to support policy assessment and planning.
- Access to further documentation:
  - Supporting documentation and dataset context available via CEH catalogue links provided in the references.

## References and documentation
- Comprehensive methodological references for SEPARATE components, modelling approaches, and data sources (PSYCHIC, NIPPER, bank erosion indices, SAGIS framework, NEAP-N, Wallingford method, MANURE-GIS, BSFP, and EA data).
- Primary publication: Zhang et al. (2014) Environmental Science & Policy, updating waterbody-scale information to support Water Framework Directive policy delivery.