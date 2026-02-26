# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) net primary productivity (NPP) on salt marsh sites at Morecambe Bay and Essex

## Overview
- Dataset captures CBESS net primary productivity (NPP) on salt marsh sites in Morecambe Bay and Essex, focusing on the 2013 growing season.
- NPP measured as above-ground vegetation mass within grazer-exclusion cages, then scaled to kg of dry weight per square meter per year (kg DW m^-2 yr^-1).
- Principal staff: Hilary Ford.
- Monitoring conducted as part of the CBESS field campaign during Winter and Summer 2013; measurements taken at the end of the 2013 growing season (summer 2013 campaign).

## Locations and habitat
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Geographic coordinates provided for each site (Essex and Morecambe Bay).
- Habitat: saltmarsh chosen to represent two contrasting soil types—clay soils in Essex and sandy soils in Morecambe Bay.
- Regional differences beyond soil type: inundation frequency, creek structure, and dominant vegetation differ between Essex and Morecambe Bay.
- Grazing regimes differ by site:
  - Essex: hare-grazed sites, with heavy grazing by Brent geese at AH and FW.
  - Morecambe Bay: intensive sheep grazing at CS and WS; winter grazing by pink-footed geese; WP lightly grazed.

## Methods and data processing
- NPP measurement method: above-ground vegetation sampled in 50 cm x 25 cm plots inside grazer exclusion cages during Summer 2013; measurements reflect the growing season after winter vegetation removal.
- Calculation: dry mass scaled to kg DW per cup area, then converted to kg DW m^-2 yr^-1.
- Sample processing: vegetation dried at 60°C for 72 hours and weighed.
- Calibration: none reported.
- Data treatment: scaling from 50 cm x 25 cm quadrats to larger area; statistical treatment minimal (scaling rather than complex models).
- File format: CSV.
- Data quality and checks: QA procedures in place; some data missing due to loss of grazing exclosures in Morecambe Bay; NA indicates missing data.

## Dataset structure and fields
- Key fields include:
  - Season (Winter or Summer; with some textual variants)
  - Location (Essex or Morecambe)
  - Site (AH, FW, TM; CS, WS, WP)
  - Habitat (Mudflat or Saltmarsh)
  - Quadrat Number (1–22, or numeric)
  - Scale (A-D, with corresponding meter ranges)
  - NPP (Net primary productivity, kg DW m^-2 yr^-1)
  - Additional descriptive fields such as header, row number, and dataset field descriptions (metadata descriptors)

## Data quality, limitations, and considerations
- Notable missing data: grazing exclosures in Morecambe Bay were lost, leading to gaps.
- Data are described as representing the whole growing season, even though measurements occurred in Summer 2013; careful interpretation required when treating as strictly "summer" data.
- Some fields contain multiple entries/labels (e.g., Season, Location) that may require harmonization during analysis.
- Potential biases due to grazing intensity and habitat differences across sites.

## Practical implications for analysis
- Enables comparisons of NPP across soil types (clay vs. sandy) and between different grazing regimes.
- Facilitates assessment of how inundation, creek structure, and vegetation type influence productivity in saltmarsh ecosystems.
- Useful for modeling ecosystem productivity and informing coastal habitat management within CBESS.