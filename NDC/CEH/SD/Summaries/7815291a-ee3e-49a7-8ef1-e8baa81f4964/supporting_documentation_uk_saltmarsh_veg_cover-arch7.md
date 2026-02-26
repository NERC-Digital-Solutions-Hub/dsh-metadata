# Saltmarsh vegetation composition data produced from 460 quadrats across 33 UK saltmarshes, 2018 - 2021.

- Project and scope
  - Part of the Carbon Storage in Intertidal Environments (C-SIDE) project.
  - Funded by NERC (NE/R010846/1).
  - Dataset describes saltmarsh vegetation composition across 33 UK saltmarshes, collected between 2018 and 2021.
  - Data resource ID: UK_saltmarsh_veg_cover.csv.

- Data producers and collaborators
  - Research team includes: Cai J.T. Ladd (University of Glasgow), Lucy C. Miller (University of St Andrews), Lucy McMahon (University of York), Glenn M. Havelock (University of York), Craig Smeaton (University of St Andrews), Angus Garbutt (UK CEH), Martin W. Skov (Bangor University), William E.N. Austin (University of St Andrews/Scottish Association of Marine Science).

- Spatial and temporal extent
  - Geographic coverage: United Kingdom (predominantly Scotland; sites chosen to reflect saltmarshes, sediment types, and organic carbon content within Scotland; coordinates include decimal degrees and projected coordinates).
  - Location formats: Latitude/Longitude (WGS84), X_Easting, Y_Northing; elevation above ordnance datum (m).
  - Survey period: 2018–2021.
  - Site and marsh type diversity: includes Natural, Historic Breach, and Managed Realignment marsh types.
  - Nations represented: England, Scotland, Wales.

- Data content and structure
  - Observations: 460 quadrats (1 x 1 m) across 33 UK saltmarshes.
  - Variables per quadrat (per-site data resource description):
    - Marsh_ID, Site_ID, Marsh_Type, Nation.
    - Location: Latitude_Dec_Degree, Longitude_Dec_Degree, X_Easting, Y_Northing, Elevation_above_OD_m.
    - Survey_Date.
    - Mean_Plant_Height_cm, Plant_Height_SD.
    - Plant_species_richness, Plant_S-W_diversity (Shannon-Wiener index).
    - Plant_Species (percentage cover for 58 plant species), Plant_total_cover.
  - Data formats: Primary file is CSV (UK_saltmarsh_veg_cover.csv).
  - Description of attributes: Includes per-quadrat vegetation cover by species, height measurements from 10 random points per quadrat, and derived metrics (mean height, richness, diversity).

- Measurement and data processing methods
  - Vegetation coverage: estimated by eye within each 1 m² quadrat.
  - Plant height: measured at 10 random points per quadrat; mean and standard deviation calculated.
  - Species richness: number of species per quadrat.
  - Diversity: Shannon-Wiener index calculated using species abundances.
  - Calibration: expert judgment used to estimate species coverage; two team members independently conducted surveys for quality assurance.
  - Data quality checks: specific QA procedures not detailed (marked as NA for some entries).

- Notable metadata and references
  - Primary data is linked to saltmarsh carbon stock research context (Ford et al., 2019) and diversity methodology (Pielou, 1966) references.
  - Field methods and sampling design designed to capture variation across marsh zones along transects perpendicular to the coastline.

- Usage in GIS and potential applications
  - Suitable for map-based visualization of vegetation composition, species distribution, and diversity across UK saltmarshes.
  - Can be integrated with spatial layers (e.g., marsh type, coastlines, soil type, elevation, carbon stock models) to analyze spatial patterns and support coastal management decisions.
  - Enables cross-site comparisons and temporal trend analysis across 2018–2021.

- Limitations and considerations
  - Coverage based on visual estimation of species cover, which may introduce observer bias.
  - Some metadata fields show NA for certain QA aspects; users should consider calibration notes when performing analyses.
  - Data density varies by site; ensure appropriate spatial handling when aggregating.

- References for further context
  - Ford, H., Garbutt, A., Duggan-Edwards, M., Harvey, R., Ladd, C., Skov, M.W. (2019). Large-scale predictions of salt-marsh carbon stock based on simple observations of plant community and soil type. Biogeosciences, 16(2), 425-436.
  - Pielou, E.C. (1966). Shannon's formula as a measure of specific diversity: its use and misuse. The American Naturalist, 100(914), 463-465.