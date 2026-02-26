# Map showing land-use/land-cover and floral cover across an arable landscape centred on the Hillesden Estate, Buckinghamshire, UK

- Purpose and scope
  - Provides a land-use/land-cover (LULC) map for a 20 km2 arable landscape around the Hillesden Estate, with added floral cover data from field surveys.
  - Integrates remote sensing (LiDAR and hyperspectral) with targeted field observations to assess habitat value for pollinators, led by the Centre for Ecology and Hydrology under the Insect Pollinators Initiative.

- Data provenance and authorship
  - Authors: John W. Redhead; Sarah Hulmes; Lucy Hulmes; Sam Amy; Gemma Baron; Matthew S. Heard; Roselle Hyman; Rachel MacDonald; Jodey Peyton; Joanna Savage; Claire Carvell.
  - Funded by the Insect Pollinators Initiative; data collection by NERC ARSF; processing and QA/validation by CEH staff.

- Data collection and methods
  - Remote sensing base: ARSF flight on 28 August 2007 under full leaf canopy.
  - Sensors and resolution:
    - LiDAR: Optech 3033 ALTM; 1 pulse/m2; canopy height model derived from surface elevation.
    - Hyperspectral: AISA EAGLE with 252 bands (selected 22 bands for vegetation discrimination).
    - Final spatial resolution: 0.5 x 0.5 m grids.
  - LULC derivation:
    - 30 classes from spectral data using maximum likelihood; integrated with LiDAR height to separate spectrally similar habitats (e.g., hedges vs. trees; roads vs. buildings).
    - Simplified to 10 final LULC classes: crop, short grass, mixed low vegetation, deciduous trees, field margin, road, hedge, building, water, bare soil/mud.
  - Field surveys and updates:
    - 2011: July–August field surveys of every mapped habitat parcel to estimate percentage cover and flowering for target plant groups.
    - 2011–2012: Spring mapping via stratified random sub-sampling; data used to estimate flowering in unsampled parcels for summer values.
    - Updates to polygon extents were made in ArcGIS based on field data and landowner information.
  - Floral data and metrics:
    - 28 plant groups assessed for vegetative cover and proportion in flower; floral cover (%) computed as cover x flowering proportion.
    - Floral cover summarized for subsets: all, non-crop, worker-visited, worker-preferred plants (summer); all (Sp_all), queen-visited plants (Sp_QV) for spring.
    - Area covered: 18.7 km2 surveyed; 6.5% unsurveyed (access restrictions) with floral data imputed using mean values from surrounding parcels of the same LULC class within 500 m.

- Data structure and format
  - Output format: ArcGIS shapefile (EIDC shapefile) with 7562 polygons, each representing a habitat parcel.
  - Core attributes:
    - FID: unique feature ID
    - Shape: Polygon geometry
    - Full_Code: field survey link to floral data
    - LULC: land-use class (Arable, Bare ground, Gardens and urban vegetation, Mixed vegetation, No Data, Roads and Buildings, Short grass, Sown floral habitat, Water/Waterside, Woody)
    - Floral cover attributes: Su_all, Su_NC, Su_WV, Su_WP (summer); Sp_all, Sp_QV (spring)
  - Metadata and compatibility:
    - Projections: British National Grid
    - Data type: vector (polygons) with associated .dbf table readable in Excel or GIS

- Data processing and QA
  - Software:
    - ERDAS Imagine (v9.0) for initial raster processing
    - ArcGIS (v9.3–v10.1) for map updates and attribute calculations
  - QA/validation:
    - Error checks against aerial photography and field survey data
    - CEH staff review of floral data
    - Manual updates to reflect field observations and landowner information

- Quality statements and limitations
  - Strengths: integration of high-resolution LiDAR and hyperspectral data with ground-truth field surveys; explicit QA steps.
  - Limitations:
    - Some areas inaccessible (6.5%) required estimation from nearby parcels, introducing uncertainty.
    - 2007 remote sensing baseline may not reflect subsequent land-use changes; updates occurred through 2011–2012 fieldwork.
    - Vectorization from raster and bespoke workflow may affect interoperability with some systems.

- Access, reuse, and related references
  - Data structure designed for GIS interoperability; shapefile and accompanying attributes suitable for habitat and pollinator analyses.
  - Related reference: Broughton et al. (2014) on agri-environment schemes and pollinator/fauna responses, providing context for the floral habitat classification used.

- Key takeaways for data stewardship
  - Clear provenance: remote sensing data, field surveys, and manual updates documented; QA procedures specified.
  - Rich metadata: detailed LULC class definitions, floral cover metrics, and spatial extent; explicit attribute meanings.
  - Governance and maintenance: updates linked to field surveys and landowner information; ongoing potential to refresh with new imagery or surveys.
  - Accessibility considerations: shapefile format supports broad GIS use; note potential limitations due to non-interoperable bespoke processing steps.