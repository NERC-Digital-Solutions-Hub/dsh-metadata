# Water chemistry of Welsh upland rivers

## Overview
- Dataset of stream water chemistry from 61 sites across Welsh upland rivers: 41 WAWS (Welsh Acid Water Surveys) sites and 20 Wye catchment sites.
- WAWS dataset includes detailed major ions; Wye dataset includes pH, alkalinity, conductivity, and major anions.
- Purpose: characterize variation in water chemistry along gradients of aquatic biodiversity, land-use, and recovery from acidification.

## Data Collection and Provenance
- In situ collection of filtered and unfiltered water samples using standardized procedures.
- WAWS: 41 sites; Wye catchment: 20 sites.
- Sampling campaigns:
  - WAWS: four samples per site during July/September 2012 and April/July 2013 (seasonal variation).
  - Wye: one sample collected in May 2013.
  - Two WAWS sites missing a sample on 01/07/2013 (DW20274 and DW57001).
- Project leadership: Dr Isabelle Durance (survey organization) and Dr Hugh Feeley (sample collection).
- Laboratory analysis at Forest Research Laboratories.
- Data handling: results entered into Excel, exported as CSV for ingestion into the Environmental Information Data Centre (EIDC).
- Project context: Diversity in Upland Rivers for Ecosystem Service Sustainability (DURESS), funded by NERC (NE/J014818/1).

## Analytical Methods (high-level)
- Ammonia in water: ISO 7150/2 (1986) Blue book method; indophenol colorimetric determination using salicylate/DIC; 50°C incubation; 650 nm detection; Chemlab instrument.
- Anions in water: US EPA Method 300.0; ion chromatography with Dionex system (columns, eluents, conductivity detector) details provided.
- Total Organic Carbon (TOC) and Dissolved Organic Carbon (DOC): Thermal oxidation to CO2; TOC measured without filtration; DOC measured after filtration and acidification with helium purge.
- pH and Conductivity: low-conductivity pH electrode and conductivity probe.

## Data Structure and Content
- WAWS data: 34 columns.
- Wye dataset: 13 columns (site_code, site_name, date, pH, Conductivity, Alkalinity_CaCO3, Alkalinity_eq, Cl, N(NO3), S(SO4), P(PO4), F, N(NO2)).
- WAWS columns include: site_code, site_name, date, pH, Conductivity, Alkalinity_CaCO3, Alkalinity_eq, DOC, Cl, N(NO3), S(SO4), P(PO4), F, N(NO2), K, Ca, Mg, Na, Al, Fe, Mn, P, S, B, Ba, Cd, Co, Cr, Cu, Ni, Pb, Si, Sr, Zn.
- Wye columns include: site_code, site_name, date, pH, Conductivity, Alkalinity_CaCO3, Alkalinity_eq, Cl, N(NO3), S(SO4), P(PO4), F, N(NO2).

## Supporting Documentation and Data Ingestion
- Supporting files:
  - DURESS_CU_site_description.csv: site description with coordinates and identifiers.
  - Plynlimon methods guidance: field methods reference.
- Notes on ingestion:
  - May consider ingesting WAWS and Wye data as two datasets due to differences in determinands analyzed.
  - Data are intended for ingestion into EIDC; details of analysis and field methods to be provided.

## Provenance and Project Context
- Lineage: samples collected in situ, analyzed at Forest Research Laboratory, results recorded in Excel, exported to CSV for EIDC.
- Keywords: diversity, aquatic invertebrates, land-use, benthic community, acidity.
- Related project: DURESS (NERC Biodiversity and Ecosystem Service Sustainability programme).