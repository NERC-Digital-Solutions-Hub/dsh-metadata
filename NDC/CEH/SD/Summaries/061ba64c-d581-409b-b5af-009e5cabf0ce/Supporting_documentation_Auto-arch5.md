# Autotrophic and heterotrophic soil respiration fluxes from peatland plateaus and thawing peatland plateaus and from burnt and unburnt forests from permafrost in subarctic Canada

## Overview
- Study of CO2 respiration fluxes measured during summers 2013 and 2014.
- Compared peatland plateau vs thawing features and unburnt vs burnt black spruce forests, with additional sites included.

## Sites and Codes
- FFU: FireFox Unburnt (unburnt black spruce forest)
- FFB: FireFox Burnt (burnt in 1998)
- BLF: BlackFox
- WHF: WhiteFox
- TPP: Teslin Peatland Plateau
- TWMID: Teslin Wetland Mid (center of thawed plateau)
- TWM: Teslin Wetland Margin (margin of thawed plateau)
- MCU: Mosquito Creek Unburnt
- MCB: Mosquito Creek Burnt
- WTP: White Truck Plateau
- WTM: White Truck Moss (recently thawed plateau, moss-dominated)
- WTS: White Truck Sedge (recently thawed plateau, sedge/moss)
- WTW: White Truck Wetland (older collapse feature)
- BCB: Boundary Creek Birch
- BCS: Boundary Creek Spruce
- Note: Flux and soil-core datasets share coding conventions but originate from different locations; refer to GPS coordinates in each file.

## Field Methods and Measurements
- Collars and trenching
  - Heterotrophic respiration: PVC collars deployed deep into thaw depth (up to 40 cm); surface vegetation clipped.
  - Autotrophic+heterotrophic respiration: collars placed on the ground surface; edge sealed with putty to prevent leaks.
  - Trenching conducted to minimize autotrophic contributions in most sites; timing varied by site (some trenched prior to measurement year, others the measurement summer).
  - Replicates: 3 to 5 collars per site and respiration type.
  - Collar dimensions: varies by site (e.g., FFU/FFB/BLF/WHF/TPP/MCU/MCB/WTP/BCB/BCS with 160 mm diameter; 5 cm or 45 cm depth; TWMID/TWM/WTM/WTS with 315 mm diameter and 10–15 cm depth; 45 cm for heterotrophic respiration).
- Gas flux measurement
  - Instrumentation: EGM-4 Infrared Gas Analyzer (PP Systems); CPY-4 chamber used at several sites for dark conditions (suppress photosynthesis).
  - Procedure: chamber placed on collar; flux rate derived after 1.5–2 minutes; measurement repeated if initial vs final rates differed substantially.
  - For some sites (TWMID, TWM, WTM, WTS, WTW): PVC chambers 15–35 cm high placed over collars; inner tube prevents leakage; enclosure times usually ≤ 3 minutes; measurements recorded every ~10 seconds.
  - Volume calculations: headspace volume determined from collar-ground distance.
- Calculations and quality checks
  - Flux rates computed from the slope of linear CO2 concentration vs time.
  - Reported metrics include the slope (flux), intercept, and R^2 for regression where used.
  - Flux units: mg CO2 day^-1 m^-2 or mg CO2-C day^-1 m^-2.
- Environmental context measurements
  - Air temperature recorded on-site; soil temperature measured at 5 cm and 10 cm inside the collar after removing the chamber.
  - Volumetric soil moisture measured at the surface (0–6 cm) with ML3 ThetaKit.
  - Thaw depth measured with a metal rod; water-table depth recorded relative to a defined datum using a long rod inserted at the start of the season.

## Data Quality, Provenance, and Documentation
- Distinguishing notes
  - Flux data and soil core data use the same coding scheme but originate from different locations; refer to GPS coordinates in each file.
  - Example: soil profile information for soil core TPP1 does not spatially match the flux data for TPP1.
- Documentation implications for data stewards
  - Ensure clear linkage between flux datasets and corresponding site metadata, avoiding spatial misalignment.
  - Capture detailed protocol differences across sites (collar size/depth, trenching status, enclosure method) to support reproducibility and cross-site comparability.
  - Include complete environmental context (on-site air/table temperatures, soil moisture, thaw depth, and water table) to support interpretation of flux variations.

## Data Management and Sharing Considerations for Data Stewards
- Data organization and cataloging
  - Maintain separate but linked records for autotrophic vs heterotrophic fluxes, associated site codes, and corresponding soil-core data.
  - Record measurement specifics (collar dimensions, trenching status, chamber type, measurement duration) in metadata.
- Metadata and interoperability
  - Standardize units (flux in mg CO2 day^-1 m^-2 or mg CO2-C day^-1 m^-2) and clearly indicate which flux type each value represents.
  - Provide GPS coordinates for all sites; ensure files note any spatial mismatches between flux and soil-core datasets.
- Data quality assurance
  - Adopt explicit thresholds and QC steps (e.g., restarts when initial/final rates differ substantially; leakage prevention notes; regression diagnostics like R^2).
- Updates and versioning
  - Track versions of datasets and any reprocessing of flux calculations or environmental measurements.
  - Document any site-specific protocol changes across the 2013 and 2014 measurement campaigns and any future updates.

## Key Takeaways for Data Stewardship
- The dataset comprises multi-site, multi-year measurements of autotrophic and heterotrophic soil respiration under varying permafrost-affected forest and peatland conditions, with rich environmental context.
- Rigorous documentation of site-specific methodologies, measurement protocols, and data processing is essential to ensure comparability and reuse.
- Careful alignment between flux data and soil-core data, including explicit spatial metadata, is critical to prevent misinterpretation due to dataset disjunction.