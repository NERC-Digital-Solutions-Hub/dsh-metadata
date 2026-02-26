# Details of data structure for the dataset Plant physiological measurements in North Wales and Northwest England (2013, 2014 and 2016) as detailed in the table Turf2Surf_Plant_physiological_data.csv

- Purpose and scope
  - Supplement to the supporting documentation for Turf2Surf data series (Turf2Surf_WP2_Supporting_documentation.rtf).
  - Describes the data structure for plant physiological measurements collected in North Wales and Northwest England during 2013, 2014, and 2016.
  - The dataset is part of a broader set of measurements across plant, soil, and root components within the Conwy catchment and surrounding sites.

- Data structure: common fields (first 9 columns)
  - A: Site Number (unique identifier; see Table 1 in supporting docs).
  - B: Habitat.
  - C: Habitat Description.
  - D: Site name.
  - E: Ecosystem Component (plant, soil, or roots).
  - F: If Ecosystem Component is Plant, the plant species; otherwise NA.
  - G: Plot number (1 to 4 possible).
  - H: Replicate number.
  - I: Soil depth interval (for soil and roots components).
  - Notes: Missing values are represented as NA when data are unavailable due to restricted depths, insufficient replicates, or outliers.

- Dataset size and content
  - The dataset includes 9 additional data columns beyond the first 9.
  - Total: 96 rows (records).

- Measurements and units (the 9 additional columns)
  - J: Year of measurement.
  - K: Vcmax — Maximum rate of carboxylation at 25°C (µmol m^-2 s^-1).
  - L: Jmax — Electron transport capacity at 25°C (µmol m^-2 s^-1).
  - M: Asat — Photosynthetic rate at saturating irradiance and 400 ppm CO2 at 25°C (µmol m^-2 s^-1).
  - N: Leaf Mass Area — leaf mass per leaf area (gm^-2).
  - O: Foliar nitrogen content (%).
  - P: Foliar phosphorus content (%).
  - Q: Specific leaf area (cm^2 g^-1).
  - R: Comments (free text).

- Special notes and data completeness
  - NA indicates measurements not performed for that site.
  - At sites 5, 7, 14, and 19, leaves were sampled in 2015 for re-analysis of foliar nitrogen and phosphorus content only.
  - The dataset is designed to be combined with other data series and used in standardized analyses for environmental monitoring.

- Relevance for environmental monitoring
  - Provides a uniform structure for plant physiological traits across multiple sites and years.
  - Facilitates cross-site comparisons of photosynthetic capacity and foliar chemistry.
  - Supports QA, cleaning, and transformation to enable monitoring outputs (reports, maps, charts) and integration into environmental data portals.