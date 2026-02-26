# Map showing land-use/land-cover and floral cover across an arable landscape centred on the Hillesden Estate, Buckinghamshire, UK

- Purpose and scope
  - LULC map of a 20 km2 agricultural landscape centered on the Hillesden Estate, Buckinghamshire, UK.
  - Integrates remote sensing data (LiDAR and hyperspectral) with field-derived floral cover data.
  - Funded by the Insect Pollinators Initiative; produced as part of CEH-led project.

- Remote sensing data and processing
  - Data collected 28 August 2007 under full leaf canopy using:
    - Optech 3033 LiDAR (1 pulse/m2, 20° scan, provides height data; converted to canopy height model).
    - AISA EAGLE hyperspectral sensor (252 bands; 400–970 nm).
  - Sensors processed into 0.5 x 0.5 m grids; height information used to separate spectrally similar covers.
  - 30 land cover classes derived from 22 hyperspectral bands via maximum likelihood classification; combined with LiDAR height to distinguish features (e.g., hedges vs trees, roads vs buildings).
  - Final LULC map reduced to 10 classes: crop, short grass, mixed low vegetation, deciduous trees, field margin, road, hedge, building, water, bare soil/mud.
  - Software: ERDAS Imagine (v9.0) and ESRI ArcGIS (v10.1).

- Field surveys and floral data
  - 2011 field surveys: every mapped habitat parcel polygon surveyed to estimate percentage vegetative cover and percentage in flower for 28 plant groups.
  - Floral cover calculation: floral_cover_group = vegetative_cover (%) x proportion_in_flower; summed across groups to yield:
    - Su_all, Su_NC, Su_WV, Su_WP for summer (July–August).
  - Spring flowering: Sp_all and Sp_QV (queen-visited) values derived from a stratified subsample (April 2011–2012) and used to estimate on unsampled parcels.
  - Survey coverage: 18.7 km2 surveyed; remaining 6.5% (mostly pasture/edge areas) imputed using mean values from the same LULC class within 500 m.
  - Floral data updates to the LULC map were done manually in ArcGIS based on field observations and landowner information.

- Data structure and accessibility
  - Spatial units: discrete habitat parcels represented as polygons; 7,562 polygons in the EIDC shapefile.
  - Attributes include:
    - LULC class (10 categories, including Sown floral habitat)
    - Full_Code linking to remote-sensed data
    - Floral cover subsets: Su_all, Su_NC, Su_WV, Su_WP, Sp_all, Sp_QV
  - Projection: British National Grid.
  - Data format: vector shapefile with associated .dbf for tabular data; designed for compatibility with common GIS tools.

- Analytical workflow and validation
  - Remote sensing processing in ERDAS Imagine; map updates and habitat delineation in ArcGIS.
  - Data converted from raster to vector to enable calculation of floral attributes per polygon.
  - Validation and quality control included error checking against aerial photography and field survey data; manual updates integrated with landowner information.

- Limitations and considerations for analysis
  - 6.5% of study area not surveyed; floral data imputed from surrounding parcels within the same LULC class.
  - Potential scale limitations when correlating floral cover with pollinator activity; spatial gaps exist due to access restrictions.
  - Data are tied to the Hillesden Estate landscape and may require careful extrapolation to other areas.

- References and context
  - Broughton et al. (2014) cited for related agri-environment scheme impacts on pollinators, providing context for interpreting floral habitat data in ecological analyses.