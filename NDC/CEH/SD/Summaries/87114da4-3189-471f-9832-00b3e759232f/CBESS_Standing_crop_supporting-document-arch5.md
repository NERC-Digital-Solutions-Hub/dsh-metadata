# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) standing crop biomass on salt marsh sites at Morecambe Bay and Essex.

## Overview
- A dataset of standing crop biomass (kg DW m^-2) from saltmarsh and associated habitats at six sites in Essex and Morecambe Bay, collected during Winter and Summer 2013 as part of the CBESS project.
- Staff responsible: Hilary Ford.

## Data content and structure
- Locations
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Habitats: Saltmarsh (SM) and Mudflat (MF)
- Site context
  - Essex sites represent clay soils; Morecambe Bay sites represent sandy soils
  - Essex region differing from Morecambe Bay in inundation frequency, creek structure, and dominant vegetation
  - Grazing regimes differ: Essex heavily grazed by Brent geese; Morecambe Bay heavily grazed by sheep with pink-footed geese in winter; West Plain lightly grazed
- Sampling design
  - General field campaign in Winter and Summer 2013
  - Quadrats: 1 m x 1 m per site, with sub-sampling area of 50 cm x 25 cm per quadrat
  - Biomass measurement: vegetation cut to ground level, dried at 60°C for 72 hours to determine standing crop biomass
  - Biomass unit: Kg DW m^-2
- Data format and fields
  - File format: Excel workbook
  - Dataset field descriptions include:
    - Row Number (numeric)
    - Season (Winter W, Summer S)
    - Location (Morecambe M, Essex E)
    - Site (CS, WS, WP for Morecambe; AH, FW, TM for Essex)
    - Habitat (MF, SM)
    - Quadrat Number (1–22)
    - Scale (A = 1 m, B = 1–10 m, C = 10–100 m, D = 100 – upper limit)
    - Biomass (Kg DW m^-2)
- Procedures and data handling
  - Procedures for observations: 50 cm x 25 cm area cut from each 1 m x 1 m quadrat in winter and summer
  - Quality control notes: present but no specific QC details provided
  - Calibration: none
  - Statistical treatment: mentions scaling up measurements from 50 cm x 25 cm area; details on the scaling approach are not fully specified
- Additional context
  - Year of data collection is 2013
  - The dataset includes explicit site and habitat codes and coordinates, enabling GIS alignment and cross-site comparisons

## Data quality and governance considerations
- Potential issues to address for stewardship
  - Clarify QC procedures and any calibration steps that were intended but not described
  - Resolve ambiguities in the scaling note (how measurements from 50 cm x 25 cm areas were upscaled)
  - Ensure coordinates and site codes are consistently mapped to GIS layers
- Data interoperability and sharing
  - Current format is an Excel workbook; consider providing CSV or an accompanying machine-readable data dictionary
  - Ensure complete metadata, including licensing and access rights, to facilitate reuse
- Versioning and updates
  - Dataset appears to be from a single field campaign (2013); plan for versioning if updates or expanded sites are added

## Actions for Data Stewards
- Validate and document QC steps and data processing methods
- Produce a detailed data dictionary and, if possible, export to open formats (CSV, JSON) to improve interoperability
- Confirm and standardize the scaling method used to extrapolate from 50 cm x 25 cm samples
- Provide precise site coordinates and unify site naming conventions across platforms
- Clarify licensing, access permissions, and any embargo or usage restrictions related to the dataset