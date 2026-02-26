# Dataset name, Details = Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) standing crop biomass on salt marsh sites at Morecambe Bay and Essex

## Overview
- dataset measuring standing crop biomass (kg DW m^-2) on salt marsh sites in Morecambe Bay and Essex
- biomass estimated from vegetation cut to ground level in a 50 cm × 25 cm area, dried at 60°C for 72 hours
- part of a general field campaign conducted in Winter and Summer 2013
- stored as an Excel workbook with detailed field descriptions and a dataset field table

## Location and site design
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- geographic coordinates provided for each site
- soil contrasts used to represent two soil types: clay soils (Essex) and sandy soils (Morecambe Bay)
- broader environmental differences noted (inundation frequency, creek structure, dominant vegetation)
- grazing regimes differ by site: Essex heavily hare- and Brent goose-grazed; Morecambe Bay heavily sheep-grazed with winter goose grazing; West Plain lightly grazed

## Sampling design and procedures
- plot level: 1 m × 1 m quadrats; biomass measured from a 50 cm × 25 cm subarea within each quadrat
- sampling seasons: Winter and Summer 2013
- standard procedure described for collecting and drying vegetation to estimate biomass
- notes indicate scaling of measurements to larger scales and potential use in simulations (details ambiguous in the text)

## Variables and data structure
- Primary variable: Biomass (Kg DW m^-2)
- Dataset fields provided:
  - Row Number: nominal sort key
  - Season: Winter (W) or Summer (S)
  - Location: Morecambe (M) or Essex (E)
  - Site: Morecambe – Cartmel Sands (CS), Warton Sands (WS), West Plain (WP); Essex – Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Habitat: Mudflat (MF) or Saltmarsh (SM)
  - Quadrat Number: 1–22
  - Scale: A = 1 m, B = 1–10 m, C = 10–100 m, D = 100 m and above
  - Biomass: numeric values (Kg DW m^-2)

## Data access and format
- format: Excel workbook
- metadata includes detailed field descriptions and coding for seasons, locations, sites, habitats, and scales

## Quality, limitations, and reuse considerations
- Calibration procedures: None reported
- Data include clear site, habitat, and grazing context, aiding cross-site comparison but require careful standardization due to differing environmental conditions and management
- Useful for data leaders to compare salt marsh biomass across sites, assess data discoverability and metadata quality, and inform data governance for ecosystem service assessments

## Relevance to data leadership and strategic use
- demonstrates end-to-end data capture: field collection, lab processing, and structured metadata
- highlights importance of descriptive metadata to enable reuse across networks and partners
- offers a case study for managing and harmonizing multi-site ecological data (soil types, grazing regimes, inundation differences) to support system-wide data strategies and stakeholder needs