## Details of data structure for the dataset Soil carbon data in the Conwy catchment in North Wales (2013 and 2014) as detailed in the table Turf2Surf_Soil _data.csv

- This document is a supplement to the Turf2Surf WP2 supporting documentation and describes the data structure for Turf2Surf_Soil_data.csv, which contains soil carbon data from the Conwy catchment, North Wales, for 2013 and 2014.
- The dataset has 644 rows and 48 additional columns beyond the first nine shared columns with related datasets (plant structural measurements, plant biomass, soil measurements, and plant physiology) across 2013–2014 (and 2016 for related datasets).
- The first nine columns (A–I) are common across the related datasets and capture site metadata and sampling design:
  - A: Unique site number
  - B–C: Habitat information and detailed habitat description
  - D: Site name
  - E: Ecosystem component (plant, soil, or roots)
  - F: If the component is Plant, the plant species (otherwise NA)
  - G–H: Plot number (1–4) and replicate number
  - I: Soil depth interval for the soil and root components
- Missing values are indicated as NA (e.g., due to restricted soil depths, limited replicates, or outliers). Roots were measured at fewer sites.

- The 48 additional columns (J onward) cover a broad suite of soil- and plant-related measurements, including:
  - Loss on ignition (LOI) and carbon in LOI fraction
  - Soil water content and bulk density
  - pH (in water) and electrical conductivity
  - Nitrate and ammonium (soil inorganic N)
  - Exchangeable cations (Na, K, Ca)
  - Various phosphorus pools (Olsen P, CaCl2-extractable P, citrate-extractable P, enzyme-extractable P, HCl-extractable P)
  - Dissolved organic carbon and total dissolved nitrogen
  - Bulk soil carbon and nitrogen
  - Root biomass and fine root biomass
  - A wide range of extractable elements and trace metals (Al, Si, P, S, Cl, K, Ca, Ti, V, Cr, Mn, Fe, Ni, Cu, Zn, Ga, Rb, Y, Ba, La, Ce, Pr, Nd, Pb, Th, U)
- Specific notes on the column content:
  - The table lists headers, units, and descriptions for each column (e.g., LOI in % dry weight; pH in water; mg L−1 or mg kg−1 for various solutes; g m−2 for biomass; mg kg−1 for trace elements).
  - Some columns’ descriptions appear to be aligned with multiple phosphorus extractable pools and related proxies (e.g., citrate-extractable P, enzyme-extractable P, HCl-extractable P, etc.) as part of soil P pool characterization.
- NA appears for measurements not performed at a given site (and root measurements were taken at fewer sites).

- Purpose and use for analysts:
  - The detailed column information enables data integration with the related Turf2Surf datasets via the first nine common columns.
  - The wide range of soil chemistry and biomass measures supports analyses of soil carbon dynamics, nutrient pools, and their relationships with plant performance across sites and depths.
  - The data require careful handling of missing values and attention to site- and depth-specific coverage, especially for root measurements.