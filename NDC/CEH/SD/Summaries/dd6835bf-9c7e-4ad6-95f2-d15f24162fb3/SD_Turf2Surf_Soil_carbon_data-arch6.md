# Soil carbon data in the Conwy catchment in North Wales (2013 and 2014) as detailed in the table Turf2Surf_Soil_carbon_data.csv

- This document is a supplement to the supporting documentation for data series described in Turf2Surf_WP2_Supporting_documentation.rtf.
- Focus: Details of the data structure for soil carbon data in the Conwy catchment (2013 and 2014), as captured in Turf2Surf_Soil_carbon_data.csv.
- Purpose for data work: Provide a consistent, identifiable structure to enable data discovery, integration with related datasets, quality assurance, and creation of end-user data products.

Overview of data structure and shared fields

- The following datasets share the first 9 columns, enabling cross-dataset joins on key identifiers:
  - Plant structural measurements (North Wales and Northwest England; 2013–2014)
  - Plant aboveground and belowground standing biomass (Conwy catchment; 2013–2014)
  - Plant physiological measurements (North Wales, Northwest England; 2013–2016)
  - Plant aboveground and belowground standing biomass (Conwy catchment; 2013–2014)
  - Soil physical, chemical and biological measurements (Conwy catchment; 2013–2014)
- Column A (Site Number) uniquely identifies a site.
- Columns B–C provide Habitat and a more detailed Habitat description.
- Column D is the Site name.
- Column E describes the ecosystem Component (plant, soil, or roots); for soil/roots, Column F is NA.
- Column F contains plant species information (when applicable); otherwise NA.
- Columns G–H provide Plot number (1–4) and Replicate number (for non-co-located measurements by dominant species).
- Column I indicates the Soil depth interval for soil and roots components.
- Missing values are indicated as NA, representing data not available due to depth restrictions, limited replicates, or other constraints.

Column-by-column description (A–J)

- A. Site Number: Unique identifier for each data row.
- B. Habitat: General habitat category for the site.
- C. Habitat description: More detailed habitat description.
- D. Site name: Name of the site.
- E. Ecosystem Component: Plant, soil, or roots.
- F. Plant species (if component is Plant); NA for soil/roots.
- G. Plot number: 1–4 (where applicable).
- H. Replicate number: Used when measurements are not co-located with plots.
- I. Soil depth interval: Depth interval applicable to soil/roots measurements.
- J. Soil carbon (kg C m-2): Carbon stock at the specified depth interval; NA if not measured at that site/depth.

Data quality, missing values, and dataset size

- Missing values are marked as NA, due to restricted soil depths, limited number of cores/replicates, or data not collected.
- The dataset comprises 469 rows, including the header row.

Practical implications for data work and analytics

- The consistent first 9 columns across related datasets supports easy merging, filtering by site, habitat, plot, replicate, and depth for multi-dataset analyses.
- Depth-aggregate and depth-specific carbon calculations can be performed using Column I and Column J.
- NA indicators require considerations for data cleaning, imputation decisions, or exclusion when conducting analyses.
- The data can be used to explore soil carbon variation across habitats, depths, and sites, and to integrate soil carbon with plant biomass and physiological datasets for broader ecosystem analyses.
- As a supplement to the main Turf2Surf WP2 documentation, this structure supports the development of dashboards, reports, and self-service data exploration tools while guiding data curation and propagation of outputs.