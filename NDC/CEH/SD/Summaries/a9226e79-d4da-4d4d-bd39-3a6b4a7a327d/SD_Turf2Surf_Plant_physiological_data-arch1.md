# Plant physiological measurements in North Wales and Northwest England (2013, 2014 and 2016)

- Purpose and scope
  - Supplement detailing the data structure for plant physiological measurements across North Wales and Northwest England, covering 2013, 2014, and 2016.
  - Data described in Turf2Surf_Plant_physiological_data.csv; part of datasets linked to Turf2Surf WP2 supporting documentation.

- Data structure: shared first 9 columns (A–I)
  - Column A: Unique Site Number (as introduced in Table 1 of the supporting documentation).
  - Column B: Habitat.
  - Column C: Habitat Description (more detailed).
  - Column D: Site name.
  - Column E: Ecosystem Component (plant, soil, or roots).
  - Column F: If Component is Plant, plant species; otherwise NA.
  - Column G: Plot number (1–4).
  - Column H: Replicate number (used when photosynthesis measurements are tied to the dominant species rather than exact plots).
  - Column I: Soil depth interval (for soil/roots components).

- Missing values and sampling notes
  - NA indicates data not available.
  - At sites 5, 7, 14, and 19, leaves were sampled in 2015 for re-analysis of foliar nitrogen and phosphorus content only.

- Dataset size for the shared structure
  - The dataset described has 96 rows beyond the first 9 columns (total 96 rows with the 9 additional columns).

- Additional measurements: columns J–R
  - Column J: Year of measurement.
  - Column K: Vcmax — Maximum rate of carboxylation at 25°C (µmol m^-2 s^-1).
  - Column L: Jmax — Electron transport capacity at 25°C (µmol m^-2 s^-1).
  - Column M: Asat — Photosynthetic rate at saturating irradiance and 400 ppm CO2 at 25°C (µmol m^-2 s^-1).
  - Column N: Leaf mass area — leaf mass per leaf area (g m^-2).
  - Column O: Foliar nitrogen content (%).
  - Column P: Foliar phosphorus content (%).
  - Column Q: Specific leaf area (cm^2 g^-1).
  - Column R: Comments (none).

- Context and applicability
  - The first 9 columns are common to multiple datasets:
    - Plant structural measurements (North Wales & Northwest England, 2013–2014).
    - Plant aboveground and belowground biomass in the Conwy catchment (2013–2014).
    - Soil carbon data in the Conwy catchment (2013–2014).
    - Soil physical, chemical, and biological measurements in the Conwy catchment (2013–2014).
    - Plant aboveground and belowground biomass in the Conwy catchment (2013–2014).
  - The plant physiological data extend this structure to include year-specific measurements (2013, 2014, 2016) with detailed photosynthesis-related traits and leaf chemistry.

- Data quality, provenance, and usage
  - Data are supplemented by the broader Turf2Surf WP2 documentation and should be analysed in conjunction with the supporting documentation.
  - The 9 additional columns (J–R) provide key physiological and leaf trait metrics suitable for correlation analyses and predictive modeling related to plant function across sites.
  - Data traceability is supported by explicit metadata for each site, plot, replicate, and sampling year.