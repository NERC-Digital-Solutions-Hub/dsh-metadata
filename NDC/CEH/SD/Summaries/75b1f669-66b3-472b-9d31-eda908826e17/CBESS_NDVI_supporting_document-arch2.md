# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) Normalised Difference Vegetation Index (NDVI) in saltmarsh and mudflat habitats

## Purpose and scope
- Standardised dataset to monitor environmental health through NDVI (vegetation index) in saltmarsh and mudflat habitats.
- Supports scrutiny of environmental health and policy performance over time using established CBESS monitoring approaches.

## Data collection and variables
- NDVI derived from surface reflectance measurements; capture with a OceanOptics USB2000 spectrometer.
- Measurements taken 1.5 m above ground; reflectance logged with OOIBase32.
- Field protocol includes white reference, dark measurement, and checks for stable ambient light; measurements under variable light conditions discarded.
- NDVI calculated in Matlab using FSFPostProcessing toolbox.
- Sampling design: random 1x1 m quadrats; 22 quadrats per site across four spatial scales (A: 1 quadrat; B: 3 quadrats; C: 6 quadrats; D: 12 quadrats).

## Sites and habitats
- Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS).
- Habitats: saltmarsh and mudflat; contrasting soil types (Essex: clay soils; Morecambe: sandy soils) and sediment characteristics.
- Essex saltmarsh and mudflat differ in inundation frequency, creek structure, and dominant vegetation; Morecambe similarly contrasts with sandy sediments and variable sediment mobility.

## Temporal design and sampling schedule
- Part of the general CBESS field campaign conducted in winter and summer 2013.
- No repeat sampling planned for quadrats sites.

## Data processing, quality control
- Quadrats allocated randomly with R to specify spatial scales (A–D).
- NDVI values generated prior to any destructive sampling.
- Measurement protocol includes multiple steps per quadrat (white reference, dark, reflectance) and re-measurement if ambient conditions change.
- Number of OOBase files and percentage cloud/water coverage recorded for each quadrat.
- Dataset indicates missing data with NA in appropriate fields.

## Data formats and metadata
- Primary data format: CSV.
- Dataset field descriptions include: Row Number, Season, Location, Site, Habitat, Quadrat Number, Scale, NDVI.
- Evidence of data quality indicators (e.g., cloud and water cover) linked to each quadrat measurement.

## Data management and accessibility
- Procedures emphasize data verification, quality assurance, and standardised storage.
- Data are prepared in interoperable formats (CSV) and designed to be stored, uploaded to appropriate portals, and accessible for reuse alongside other related data.

## Outputs and potential uses
- Provides a comparable, standardized NDVI dataset across contrasting coastal habitats.
- Enables environmental health assessment, habitat monitoring, and integration with broader biodiversity and ecosystem service analyses.
- Facilitates data discovery and interoperability to support policy evaluation and environmental management decisions.