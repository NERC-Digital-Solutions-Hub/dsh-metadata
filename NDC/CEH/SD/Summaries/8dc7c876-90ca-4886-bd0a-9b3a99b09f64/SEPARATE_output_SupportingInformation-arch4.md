# Source apportionment of annual nutrients and sediment loads to rivers in England and Wales modelled with SEPARATE

## Overview
- A national-scale dataset that apportions annual loads of total nitrogen, total phosphorus, dissolved phosphorus, and sediment to rivers in England and Wales.
- Covers both diffuse sources (agriculture, urban, river banks, atmospheric deposition, groundwater) and point sources (STWs, septic tanks, CSOs, storm tanks) using SEPARATE version 2.
- Aims to support Water Framework Directive policy delivery by providing waterbody-scale emissions.

## What data are included
- Source categories and pollutants:
  - Diffuse: agricultural, urban, river channel banks, atmospheric deposition, groundwater.
  - Point: Sewage treatment works (STWs), septic tanks, combined sewer overflows (CSOs), storm tanks.
- Pollutants per source: total nitrogen, total phosphorus, dissolved phosphorus, and sediment (with local vs. cumulative totals).
- Agricultural inputs include mitigated vs. unmitigated scenarios.
- Data summarize emissions to the aquatic environment for non-coastal waterbodies (Cycle 2).

## Data structure and format
- Format: CSV with the ability to map to WFD River Waterbody Catchment Cycle 2 shapefiles.
- Key mapping column: waterbody ID (EA_WB_ID or wb_ID in shapefiles).
- Columns include:
  - Region, catchment, waterbody name and ID, local area, cumulative area.
  - For each pollutant/source: local (L) and cumulative (C) tonnes per year, and local (L_p) and cumulative (C_p) percentages.
  - Examples of variable prefixes: X_au_L_t (agricultural unmitigated), X_be_L_t (bank erosion), X_ur_L_t (urban diffuse), X_sw_L_t (STWs), X_to_L_t (waterbody total), plus corresponding mitigated, cumulative, and percentage columns.
- Supporting documentation and links provided for data provenance and methodology.

## Data sources and modelling approach
- SEPARATE framework: sector pollutant apportionment for England and Wales; summarised by cycle-2 waterbodies.
- Diffuse agricultural emissions:
  - Based on the ADAS Agricultural Pollutant Transfer (APT) framework, built on PSYCHIC and NIPPER models.
  - Inputs include soils, daily weather, elevation, crop data, field boundaries, manure distribution, and fertiliser practices.
- Diffuse urban emissions:
  - Derived from annual urban runoff (Wallingford Modified Rational Method) and event mean concentrations.
- River channel bank emissions:
  - Estimated via a national-scale bank erosion index tied to river regime, flow, and geomorphology.
- Direct atmospheric deposition:
  - Nitrogen via NEAP-N; phosphorus via rainfall-derived concentrations and rainfall data.
- Sewage treatment works (STWs):
  - Based on a national register of consented discharges with measured flows and concentrations (2010–2012 data).
- Septic tanks:
  - Emissions drawn from Environment Agency studies.
- Combined sewer overflows (CSOs) and storm tanks:
  - CSOs modelled using SAGIS framework assumptions (discharge when rainfall triggers exceed certain thresholds).
  - Storm tanks treated similarly, with retention before discharge.
- References and supporting methodology details are provided in the linked documentation.

## Uncertainty, limitations, and scope
- Intended for national-scale policy support with local-scale decision relevance; uncertainties increase for smaller waterbodies.
- Approximately 43% of waterbodies have areas <25 km²; results for these should be treated with caution due to data and modelling limitations.
- Agricultural emissions are presented as baselines with and without mitigation; STW emissions reflect monitoring data but may have gaps for smaller works.
- STW emissions to estuarine/coastal environments are not included.
- Channel bank contributions do not account for margin protection works.
- Temporal coverage is not perfectly uniform across sectors (e.g., 2010 for agriculture vs. 2010–2012 for STWs).

## Usage and practical application
- Enables policy-makers and data leaders to:
  - Assess relative importance of different sources to waterbody nutrient and sediment loads.
  - Compare mitigated vs. unmitigated scenarios for agricultural impacts.
  - Map and prioritise actions at waterbody level using the provided CSV and GIS-compatible formats.
- Encourages careful interpretation at local scales due to identified uncertainties and data alignment issues.

## Access, provenance, and references
- Supporting documentation and data provenance are provided, including a link to additional resources and a comprehensive reference list with methodological sources (PSYCHIC, NIPPER, SAGIS, NEAP-N, etc.).