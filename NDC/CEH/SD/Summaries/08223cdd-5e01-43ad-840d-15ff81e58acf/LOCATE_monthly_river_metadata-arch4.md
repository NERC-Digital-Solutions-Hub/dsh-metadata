# Land Ocean Carbon Transfer (LOCATE) Monthly river sampling dataset

## Overview
- Multidisciplinary NERC project involving multiple UK institutions (NOC, BGS, CEH, Plymouth Marine Laboratory; collaborators from several universities and Environment Agency).
- Objective: improve understanding of carbon flow from land into the ocean, focusing on rivers (companion dataset covers estuaries).
- Dataset contains monthly measurements from 41 rivers across England, Scotland, and Wales in 2017 (with samples from November 2016); rivers selected to reflect different land-use types.

## Scope and sampling design
- Temporal scope: January–December 2017 (monthly); November 2016 treated as a trial period for some sites; Dorset Stour not sampled until April 2017.
- Sampling regime: fixed site on each river; majority of sites moved to HMS sites to facilitate data integration; coordination led by Andy Tye (BGS).
- Sampling cadence: field collection typically within a 2–3 day window per month; field protocols cover bottle types, filtration, storage, and in-field measurements.

## Parameters measured
- Physical/chemical: temperature, specific electrical conductivity (SEC), salinity.
- Nutrients: ammonium (NH4-N), nitrate (NO3-N), phosphate (PO4-P), total nitrogen (TN), total phosphate (TP).
- Organic carbon: non-particulate organic carbon (NPOC), total dissolved carbon (TDC).
- Particulate matter: particulate organic carbon (POC), particulate organic nitrogen (PON).
- Isotopes: 13C (POC), 15N (PON).
- Dissolved organic matter analyses: dissolved organic matter fluorescence (fDOM) and absorbance.
- Additional measures: alkalinity, pH.
- Molecular analyses: additional samples collected for molecular work (reported separately).

## Field sampling protocol (summary)
- In-field handling: most samples filtered and allocated to appropriate bottles in the field; samples kept dark and cold; specific protocols for salinity/temperature measurements; field weather/river condition notes recorded.
- Sample depth: collected from ~0–30 cm in the mid-channel when possible.
- Sampling sequence and bottle types detailed (filtration steps, rinsing procedures, storage conditions).
- Field blanks used selectively to test batches of filters; procedure blanks prepared for key analyses.

## Laboratory analyses and quality control
- Elemental and isotopic analysis: carbon and nitrogen concentrations (percent w/w) and δ13C/δ15N measured with an elemental analyser linked to an isotope ratio mass spectrometer (Flash EA 1112 + Conflo III + DeltaPlus XP).
- Calibration: international references USGS40/USGS41a; results aligned to VPDB and AIR-N2 scales; methods adhere to UKAS ISO 17025 framework; analyses treated with accreditation-like rigor though not formally accredited due to repeatability limitations.
- Quality control: long-term precision metrics provided for standard materials; approximately 5% of samples undergo internal checks; CEH Lancaster participates in the Aquacheck program for measurement accuracy.
- Fluorescence and absorbance analytics: fluorescence (excitation 200–400 nm, emission 250–500 nm; Raman units after correction) and absorbance (200–800 nm) measured with Varian instruments; PARAFAC modelling performed in Matlab (DOMFluor v1.7); blanks and standards (quinine sulfate) used for QA.
- Data calibration/normalization: fluorescence data corrected for absorbance; PARAFAC component loadings reported; internal blanks used to monitor instrument performance.

## Data structure, metadata, and provenance
- River and catchment context: land cover data derived from 2015 CEH Land Cover Map; includes catchment area, peat soil presence, arable/grassland/woodland types, various habitat classifications, and freshwater extent.
- Hydrological and landscape variables: Base Flow Index (BFI) derived from NRFA data; carbonate rock presence; mean altitude; rainfall indicators (standardized 1961–90 rainfall maps).
- Data file columns encompass: river identifiers, sampling times, site/trip metadata, volumes and filtration details, temperature/conductivity/salinity, weather comments, flow/level, nutrient and carbon measurements (with filtered/raw distinctions), pH/alkalinity, PARAFAC/component loadings, fluorescence indices, absorbance metrics, EEM peak metrics, and a comprehensive set of quality/control fields.
- Coordination and data management: sampling coordinated by BGS; shift to HMS sites to improve integration with EA modelling datasets; data intended for cross-lab integration and broader data-system usefulness.

## Implications for data strategy and reuse
- Rich, multi-parameter river water data with extensive metadata enables cross-site data integration and modelling of land-to-river carbon flux.
- Strong emphasis on documentation, standardization, and QA across labs, supporting reliability in multi-partner data environments.
- Data structure supports advanced analyses (e.g., PARAFAC modelling of DOM, isotopic tracing of carbon and nitrogen, coupling with land-cover and hydrological metrics).
- For data leaders, the dataset demonstrates effective governance in a collaborative science project, including clear provenance, standardized units, documented sampling protocols, and routine quality checks.