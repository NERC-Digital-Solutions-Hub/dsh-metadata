# Water chemistry of Welsh upland rivers

## Overview
- A dataset of stream water chemistry from 61 sites across Welsh upland rivers (41 WAWS sites; 20 Wye catchment sites).
- WAWS samples collected in summer/autumn 2012 and spring/summer 2013; Wye samples collected in May 2013.
- Aims: characterize chemical variation along gradients in aquatic biodiversity, land-use impacts, and recovery from acidification.
- Data collected to support analysis of environmental settings and ecosystem responses; prepared for use in GIS-based visualization and analysis.

## Study design and sampling regime
- WAWS: 41 sites capturing acidity gradients across geological settings and acid episodes; major ion analysis emphasized.
- Wye: 20 sites along land-use gradient focusing on nutrient content.
- Sampling frequency: WAWS—four samples per site (Jul and Sep 2012; Apr and Jul 2013); two WAWS sites unavailable on 01/07/2013; Wye—one sample in May 2013.
- In situ collection with standardized procedures; samples sent to Forest Research Laboratory for analysis.

## Data collected and content
- Parameters (WAWS): pH, conductivity, alkalinity (as CaCO3 and in equivalents), major ions; additional variables laterally included (e.g., DOC).
- Wye dataset: identical variables where available, but provided with a reduced set of columns (13 columns vs. 34 for WAWS).
- Data structure differences noted between WAWS and Wye datasets.

## Data structure and formats
- WAWS data: 34 columns per site entry (comprehensive suite of chemical variables).
- Wye data: 13 columns (site_code, site_name, date, pH, Conductivity, Alkalinity_CaCO3, Alkalinity_eq, DOC, Cl, N(NO3), S(SO4), P(PO4), F, N(NO2), plus additional cations/anions as applicable).
- Site description file: separate CSV with 10 columns containing spatial identifiers and coordinates (Eastings, Northings, Grid, Latitude, Longitude, Elevation, etc.) and catchment details.

## Analytical methods
- Ammonia: Blue book method (ISO 7150/2-1986); automated spectrophotometric determination using salicylate/DIC with nitroprusside catalyst.
- Anions: US EPA Method 300.0; IC with Dionex equipment (CO3 removal and conductivity detection).
- Carbon: Total Organic Carbon (TOC) and Dissolved Organic Carbon (DOC) via thermal oxidation to CO2 with NDIR detection; TOC unfiltered, DOC filtered and acidified and purged with Helium.
- PH & Conductivity: Low conductivity pH electrode and conductivity probe.
- Instruments: Thermo Scientific/Analytical Sciences equipment referenced; field and lab procedures guided by provided documentation (e.g., Plynlimon methods).

## Data provenance and processing
- In situ sampling followed by laboratory analysis at Forest Research Laboratory.
- Results recorded in Excel; later exported as CSV for ingestion into the Environmental Information Data Centre (EIDC).
- Data described as potentially comprising two datasets due to differences in determinands analyzed; notes to finalise structure and column lists.

## Spatial and temporal coverage
- Geographic scope: Welsh upland rivers across WAWS catchments and the Wye catchment.
- Temporal scope: WAWS samples spanning 2012–2013; Wye samples from May 2013.
- Spatial attributes available via the Site Description file (coordinates, grid references, elevation).

## Supporting documentation and cautions for use
- Supporting docs available: site description CSV; Plynlimon methods; references to broader method guidance (CAST-like column lists) to aid data ingestion and standardization.
- Considerations for GIS use:
  - WAWS and Wye datasets differ in the number of columns and determinands; may need to treat as two related datasets.
  - Some dates/sites are missing (e.g., two WAWS sites on 01/07/2013); account for incomplete time series.
  - Seasonal variation is present; interpret results with sampling windows in mind.
  - Spatial accuracy relies on site description coordinates; cross-check against GIS basemaps.

## GIS-ready opportunities
- Map-based visualization of pH, conductivity, alkalinity, and major ion concentrations across catchments.
- Overlay with land-use data, biodiversity gradients, and acidification recovery indicators.
- Link to site metadata (coordinates, elevation) for spatial analyses and watershed-level modeling.