# Source apportionment of annual nutrients and sediment loads to rivers in England and Wales modelled with SEPARATE

## Overview
- Presents SEPARATE (SEctor Pollutant AppoRtionment for the AquaTic Environment) as a framework to apportion annual loads of nitrogen, phosphorus, and fine-grained sediment to rivers in England and Wales at the Water Framework Directive (WFD) waterbody scale.
- Data are summarized by non-coastal WFD Cycle 2 waterbodies, covering both diffuse and point sources.
- Dataset accompanies policy-oriented research on cross-sector contributions to river pollution and supports monitoring and decision-making under the WFD.

## What the dataset covers
- Apportionment of pollutant emissions to rivers for:
  - Diffuse sources: agriculture, urban, river channel banks, atmospheric deposition, groundwater.
  - Point sources: sewage treatment works (STWs), septic tanks, combined sewer overflows (CSOs), storm tanks.
- Pollutants included: total nitrogen (N), total phosphorus (P), dissolved phosphorus, and sediment (for each source category).

## SEPARATE framework and modelling approaches
- SEPARATE is a multi-pollutant source apportionment screening framework for England and Wales; data are aligned with non-coastal WFD Cycle 2 waterbodies.
- Emission calculations are broken down by source category, with distinct modelling approaches and input data per category (see details below).

## Source categories and key inputs
- Diffuse agricultural emissions
  - Inputs generated with the APT framework, built on PSYCHIC and NIPPER models.
  - Required data: NSRI Natmap soils, UK Met Office daily weather, elevation, 2010 agricultural census crops, field boundaries, MANURE-GIS manure loadings, 2010 Fertiliser Practice data.
- Diffuse urban emissions
  - Derived from annual urban runoff using the Wallingford Modified Rational Method and representative event mean concentrations (EMCs).
  - Inputs: rainfall and land cover/soil data.
- Diffuse river channel bank emissions
  - Estimated using a national-scale bank erosion index accounting for river regime and sinuosity.
  - Inputs: river flow, HOST soil classification, Detailed River Network (DRN).
- Direct atmospheric deposition
  - Nitrogen deposition estimated with NEAP-N; phosphorus deposition based on rainfall-derived concentrations from ECN monitoring sites.
- Sewage treatment works (STWs)
  - Emissions estimated from a national register of consented discharges with measured flows and pollutant concentrations (2010–2012); very small works (<3 m3 daily) or lacking data excluded.
- Septic tanks
  - Emissions taken from a recent EA study on phosphorus losses.
- Combined sewer overflows (CSOs)
  - Discharges estimated using the SAGIS framework; CSOs assumed to discharge when rainfall, sewer capacity, and surface permeability permit, with six times dry weather flow as a baseline.
- Storm tanks
  - Emissions estimated similarly to CSOs, with retention of three times the dry weather flow before discharge.
- Groundwater
  - Included as a separate pathway for certain pollutants; specific modelling details are aligned with the overall framework inputs.

## Uncertainty and limitations
- Results reflect national-scale integration with local-scale decision-making in mind; waterbody-level results for areas <25 km2 should be treated with caution (approx. 43% of waterbodies).
- Agricultural emissions represent baseline 2010–2012 conditions, with a separate baseline scenario (no prior mitigation) included; STW emissions reflect tightened permits and nutrient stripping over time, with uncertainties for small STWs.
- Estimation gaps: estuarine/coastal STW outfalls excluded; channel bank contributions do not account for margin protection works.
- Temporal coverage is not perfectly aligned across sources (e.g., agriculture 2010 vs. 2010–2012 for STWs); data reflect the latest available inputs used in the study.

## Data format and GIS use
- Stored as CSV files; can be mapped to WFD River Waterbody Cycle 2 shapefiles by joining on the Waterbody ID (EA_WB_ID).
- File structure includes:
  - Table 1: Modelled pollution sources (source categories)
  - Table 2: Modelled pollutants (N, P, dissolved P, sediment) by source
  - Table 3: CSV column descriptions and naming conventions for regional, catchment, waterbody, and pollutant columns
- Columns provide both local (per waterbody) and cumulative (upstream + waterbody catchment) values; include unmitigated and mitigated agricultural components and percentage-based mitigation indicators for local and cumulative scales.

## Implications for policy monitoring and framework authors
- Provides a transparent, auditable mechanism to attribute river pollutant loads to specific sectors and pathways, supporting targeted policy interventions and progress tracking under the WFD.
- Facilitates national-to-local decision-making by delivering load estimates in a format compatible with standard GIS workflows and waterbody-scale reporting.
- Emphasizes the importance of metadata, data provenance, and interoperability across datasets to enable replication and governance of monitoring approaches.

## Supporting references
- Zhang, Y.; Collins, A.L.; Murdoch, N.; Lee, D.; Naden, P.S. (2014) Cross sector contributions to river pollution in England and Wales: Updating waterbody scale information to support policy delivery for the Water Framework Directive. Environmental Science & Policy, 42, 16-32.
- Key methodological sources cited include PSYCHIC, NIPPER, ADAS-APT frameworks, Wallingford runoff method, NEAP-N deposition estimates, SAGIS framework, and UKWIR/EA data sources.