# Turf2Surf WP2 Supporting documentation for data

## Overview and Purpose
- Focus: Coupled nutrient cycling in terrestrial and freshwater ecosystems; nitrogen and phosphorus impacts on carbon exchange between land and atmosphere.
- Context: Data intended to support understanding of how plant and soil nutrients influence above- and belowground processes and to parameterize the JULES model.
- Timeframe: Measurements primarily 2013–2015 (NPP, biomass, photosynthesis, leaf traits); soil analyses conducted around spring 2014; TXRF and other analyses follow-up.

## Project and Data Stewardship
- Project members and data responsibilities are specified (names and affiliations for data responsibility across sections: NPP, photosynthesis, leaf traits, soils, TXRF).
- Authors and corresponding contact: Sabine Reinsch (corresponding author); other contributors listed; data processing and methodological references provided.
- Dataset aims: Ensure measurables are linked to ecosystem processes and to JULES parameters; standardization and reproducibility are emphasized.
- Versioning: Document versions dated 01/06/2016; 25/08/2016; 04/11/2016.
- Data provenance: Detailed methodology per data type, with references and scripts or workflows where applicable (e.g., GitHub link for photosynthesis modeling).

## Data Components and Measurement Types
- Aboveground Net Primary Productivity (NPP) and Standing Biomass (3.1.1)
  - 4 plots per site representing dominant species; winter cutting with grazing exclusion where applicable.
  - Aboveground biomass: herbaceous in 1 m x 1 m plots; woodland biomass from 200 m² plots plus tree cores and litter biomass.
  - NPP measured 2013–2015; life-cycle adjustments applied for different species.
- Plant Photosynthesis Measures (3.1.2)
  - Parameters: Asat, Vcmax, Jmax (at 25°C); field and lab measurements using CIRAS-I, Conifer chamber, and LICOR 6400.
  - CO2 concentration treatments (400 and 2000 ppm; 50–2000 ppm curves); data processed with Farquhar model and temperature corrections.
  - Data processing scripts and model fitting available; linked to JULES integration.
- Leaf Traits and Plant Community Traits (3.1.3)
  - Traits: leaf N and P (%), leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
  - LMA: measured on ten leaves per area; leaf area via ImageJ; N and P analyzed via standardized lab methods.
- General Soil Measures (3.2.1)
  - Soil cores to 1 m depth across 17 habitats; depth intervals defined (0–15, 15–30, etc.).
  - Measurements: soil water content (SWC), bulk density (BD), LOI and LOI-C, pH, EC, total C and total N.
  - QA/QC and multi-operator involvement; data processing aligned with Turf2Surf aims.
- Phosphorus Fractions and Related Analyses (3.2.2)
  - Olsen P, Root-P, Complex-P, Enzyme-P, Proton-P using standardized colorimetric methods and extractions (Malachite Green method variances).
  - Detailed extraction protocols and reagent preparations provided; emphasis on cross-method comparability.
- Available Carbon and Nitrogen in Soil (3.2.3)
  - Extraction with 0.5 M K2SO4; NO3 and NH4 via colorimetric microplate methods; DOC and TDN measurements at CEH Bangor.
  - NO3: vanadate-based method; NH4: salicylate-nitroprusside method.
  - DOC/TDN measured with Thermalox 5003 (total carbon) and related QA/QC procedures.
- Soil Available Cations (3.2.4)
  - Ca, Na, K extracted with 0.5 M acetic acid; analysis via flame photometry.
- Root Biomass and Growth (3.2.5)
  - Total and fine root biomass at 6 sites; soil cores (0–15 cm depth intervals); root scanning with WinRhizo; in-growth root cores for growth assessment.
  - Biomass calculations include dry weights; growth cores recovered and analyzed.
- Soil Elements by TXRF (3.2.6)
  - TXRF analysis (S2 PICOFOX) for a broad suite of elements (Al, Fe, Ca, K, etc.) across all 17 sites.
  - Sample prep includes grinding, suspension in TritonX, and disc deposition; internal standard used; limitations noted in separate file.
  - Laboratory work conducted by specified team; data analysis and calculations documented.

## Dataset Structure and Files (4.0)
- Five data files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Common schema across files:
  - Column A: Site number (matches Table 1).
  - Column B: Habitat.
  - Column C: Detailed Habitat description.
  - Column D: Site name.
  - Column E: Ecosystem Component (Plant, Soil, Roots).
  - Column F: For Plant components, species; otherwise NA.
  - Column G: Plot number (1–4).
  - Column H: Replicate number (for non-co-located measurements based on dominant species).
  - Column I: Soil depth interval (for Soil and Roots).
- Data notes:
  - Missing values are indicated as NA.
  - Depth intervals and replicates are used to align measurements across habitats.
- Purpose and use:
  - Data are organized to support linking plant- and soil-derived parameters to ecosystem processes and JULES model parameters.
  - Documentation aims to ensure traceability, reproducibility, and compatibility with downstream analyses.

## Metadata, Quality, and Accessibility
- Detailed methodology available for each data type, including references and, where applicable, data processing scripts or links (e.g., GitHub for photosynthesis modeling scripts).
- Emphasis on QA/QC for key measurements (e.g., C, N, P fractions, TXRF and TXRF limitations documented in related file).
- Data intended for upload to relevant data portals and for subsequent integration with ecosystem-process models.
- Contact points for data stewardship and methodology:
  - Data responsible individuals per section (NPP, photosynthesis, leaf traits, soils, TXRF).
  - Corresponding author and project leads provided for coordination, updates, and data requests.

## Practical Considerations for Data Stewards
- Ensure consistent metadata mapping to the five data files and the common site/plot/replicate schema.
- Maintain provenance by linking to methodological references and scripts; preserve version history (as in the document’s version dates).
- Monitor completeness across sites (17 habitats) and address gaps indicated by NA values.
- Validate cross-file compatibility for site numbers, habitat descriptions, and depth intervals to support integrated analyses and JULES parameterization.
- Plan for ongoing data sharing and portal deposition, with clear licensing and usage guidelines aligned to Turf2Surf project goals.