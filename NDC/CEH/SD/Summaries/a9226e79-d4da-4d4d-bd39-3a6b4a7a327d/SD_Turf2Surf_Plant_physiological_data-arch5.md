# Details of data structure for the dataset Plant physiological measurements in North Wales and Northwest England (2013, 2014 and 2016) as detailed in the table Turf2Surf_Plant_physiological_data.csv

## Overview
- This document supplements Turf2Surf WP2 supporting documentation and describes the data structure for plant physiological measurements in North Wales and Northwest England (2013, 2014, 2016).
- Several datasets share the first 9 columns, enabling cross-dataset linkage (e.g., plant structure, biomass, soil data in Conwy catchment).
- The dataset comprises 96 rows and 9 additional columns (J–R) beyond the initial identifying columns (A–I).
- Some sites include re-analysis of foliar nutrients in 2015 (sites 5, 7, 14, and 19).

## Data fields and interpretation (A–R)

- A. Site Number — unique site identifier.
- B. Habitat — broad habitat category.
- C. Habitat Description — more detailed habitat description.
- D. Site name — name of the site.
- E. Ecosystem Component — plant, soil, or roots.
- F. Plant species — species name; NA for soil/roots.
- G. Plot — plot number (1–4).
- H. Replicate — replicate number (for non-coincident measurements with plots).
- I. Soil depth interval — depth range (for soil/roots).
- J. Year — year of measurement.
- K. Vcmax — maximum rate of carboxylation at 25°C; unit: µmol m⁻² s⁻¹.
- L. Jmax — electron transport capacity at 25°C; unit: µmol m⁻² s⁻¹.
- M. Asat — photosynthetic rate at saturating irradiance and 400 ppm CO₂ at 25°C; unit: µmol m⁻² s⁻¹.
- N. Leaf mass area — leaf mass per leaf area; unit: g m⁻².
- O. Foliar nitrogen content — foliar N content; unit: %.
- P. Foliar phosphorus content — foliar P content; unit: %.
- Q. Specific leaf area — area per unit leaf mass; unit: cm² g⁻¹.
- R. Comments — free-text notes; unit: none.

## Data quality and metadata notes
- Missing values are indicated as NA (e.g., unavailable measurements, restricted depths, limited replicates).
- At sites 5, 7, 14, and 19, leaves were sampled in 2015 for re-analysis of foliar nitrogen and phosphorus content only.
- The 9 initial columns (A–I) provide core identifiers to enable cross-dataset linking with related datasets (e.g., plant structure, biomass, soil properties in Conwy catchment for 2013–2014).
- The 9 additional columns (J–R) document measurement specifics, units, and descriptive context for comparability and reuse.

## Data management and sharing implications for Data Stewards
- Ensure consistent metadata across all Turf2Surf data series by maintaining a shared data dictionary for A–R fields.
- Verify and confirm units and nomenclature (e.g., Vcmax, Jmax, Asat, leaf metrics) across datasets to support interoperability.
- Track data provenance and versioning, particularly noting the 2015 foliar N/P re-analysis at specified sites.
- Prepare for ingestion into data portals with complete metadata, including descriptions, units, and any site-specific caveats (e.g., NA values, depth restrictions).
- Document any data processing steps (e.g., quality assurance, transformation) and decisions to support future reuse.

## Practical considerations and potential challenges
- Aligning metadata across multiple datasets that share the first 9 columns to enable seamless discovery and integration.
- Managing incomplete data due to NA values and differences in data availability by site, plot, or year.
- Handling format and system diversity when sharing or updating datasets, given the broader Turf2Surf data ecosystem.
- Maintaining up-to-date records when re-analysis data (2015 foliar N/P) are incorporated for select sites.