# Materials and methods, and metadata for Freshwater Particulate Organic Radiocarbon for Four Major UK Catchments, 2013-2014. Data taken from 'Aged riverine particulate organic carbon in four UK catchments' Adams et al, 2015 Science of the Total Environment.

## Overview
- Presents materials, methods, and metadata for freshwater particulate organic radiocarbon (PO14C) across four UK catchments (Ribble, Conwy, Hampshire Avon, Dee) for 2013–2014.
- Data derived from riverine particulate organic carbon analyses (aged riverine POC).
- Emphasises data provenance, measurement techniques, calibration, and metadata standards to enable data discovery, reuse, and integration into broader data systems.

## Field sites
- Ribble catchment (north-west England): population density 989 persons/km²; includes Rivers Hodder and Calder; upper catchment shows rapid response to rainfall; Calder has extensive conurbations and historical industrial activity.
- Conwy catchment (North Wales): major drainage system in the region; catchment exhibits mountainous topography with strong river response during storms.
- Hampshire Avon catchment (south England): population density 108 persons/km²; largely groundwater-dominated with chalk aquifers; tidal limit shows limited response to rainfall.
- River Dee catchment (north-east Scotland): population density 4 persons/km² above tidal limit; upper tributary Gairn in mountainous area with rapid response to rainfall/snowmelt.

## River sampling and analysis
- Water samples (5 L) collected at tidal limits of the four catchments; additional upstream samples in Ribble and Dee.
- Suspended particulate matter (SPM) extracted by repeated centrifugation (9600 rpm for 30 min) until ~100 mL of sediment-water mixture remains.
- Organic carbon content of SPM measured using two approaches:
  - Filter a known water aliquot through pre-weighed, pre-combusted GF/F filters; dry and reweigh to determine [SPM], then analyze total carbon with:
    - Vario EL elemental analyser (Ribble, Conwy, Avon) and
    - Thermo Flash 2000 elemental analyser (James Hutton Institute).
- Graphite targets for AMS 14C analysis prepared by quantitative carbon recovery in sealed quartz tubes, followed by cryogenic CO2 separation and iron/zinc reduction to iron/graphite.
- δ13C measured on a subsample of CO2 using a dual-inlet mass spectrometer (Thermo Fisher Delta V) for δ13C correction of 14C data.
- Laboratories:
  - Most 14C analyses conducted at SUERC (Scottish Universities Environmental Research Centre AMS Laboratory, East Kilbride).
  - Three measurements on samples <500 μg C performed at UCIAMS (Keck Carbon Cycle AMS Laboratory, UC Irvine).
- Calibration and accuracy:
  - Size-matched process background materials and age standards used to check accuracy and precision.
  - Results reported as absolute % modern (pMC), with adjustments relative to the ONGOING radiocarbon standard since AD 1950 (Stuiver and Polach, 1977). 100% modern defined as oxalic acid standard value in AD 1950; samples can exceed 100 pMC due to bomb carbon.
  - Radiocarbon enrichment reported as percentage of 14C activity relative to modern standard; analytical precision stated as 1σ.

## Radiocarbon analysis and calibration (14C and δ13C)
- 14C content measured as pMC (percent modern carbon) with corrections for isotopic fractionation using δ13C.
- δ13C correction expressed relative to VPDB (-‰).
- Samples calibrated to conventional radiocarbon ages using standard reference materials and international references; precision and lab provenance recorded (SUERC or UCIAMS) in dataset metadata.
- Bomb carbon scenarios recognized (pMC > 100) where applicable.

## Data and metadata
- Data product: Riverine_PO14C_Raw_Data (columnar dataset) with detailed metadata to support discovery and reuse.
- Column heading explanations (examples of fields):
  - Catchment: name of the study catchment.
  - Catchment, Units: plain text.
  - Site: name of river within the catchment.
  - Flow: qualitative condition of river at sampling (e.g., High, Low).
  - Lat/Long: geographic coordinates.
  - Publication code: unique code assigned at analysis stage.
  - Date: sampling date.
  - d13CVPDB‰: stable carbon isotope content.
  - 14C pMC: radiocarbon content relative to modern standard.
  - ±/‑ 1σ PMC: analytical error (1σ) in pMC.
  - [SPM]: suspended particulate matter concentration (mg/L).
  - %OC: organic carbon content (percent).
- Data provenance notes:
  - Includes both field data and laboratory-derived measurements, with explicit lab provenance (SUERC, UCIAMS) and publication codes.
  - Metadata capture supports data discoverability, discoverable formats, and cross-lab integration.
  - Units and abbreviations standardized across the dataset (e.g., pMC, mg/L, ‰).

## Data quality and governance (implied)
- Multi-lab validation and cross-checking (SUERC and UCIAMS) to ensure accuracy and consistency.
- Use of standardized calibration, reference materials, and clearly documented metadata to enable reproducibility and reuse.
- Clear data schema with explicit column explanations to reduce ambiguity and facilitate integration with other data systems.

## References
- Boutton, T.W., et al. 1983. Comparison of quartz and pyrex tubes for combustion of organic samples for stable carbon isotope analysis.
- Slota Jr., P.J. 1987. Preparation of small samples for 14C accelerator targets by catalytic reduction of CO.
- Xu, S., et al. 2004. Capabilities of the SUERC 5MV AMS facility for 14C dating.
- Stuiver, M., Polach, H.A. 1977. Reporting of 14C data.