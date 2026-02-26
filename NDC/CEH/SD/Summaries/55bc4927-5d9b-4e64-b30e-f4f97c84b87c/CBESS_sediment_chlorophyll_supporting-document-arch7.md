# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment chlorophyll concentrations in saltmarsh and mudflat habitats

## Overview
- Dataset of chlorophyll concentrations in surface sediments (2 mm) from microphytobenthos (MPB) in saltmarsh and mudflat habitats.
- Measurements include chlorophyll a, b, and c1+c2 as micrograms per gram of sediment (µg g⁻¹).
- Winter and summer 2013 sampling with five replicates per quadrat.

## Spatial coverage and sampling design
- Regions/sites:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Exact locations provided as latitude/longitude for each site.
- Habitat types sampled at each site: saltmarsh and mudflat.
- Site selection aimed to represent contrasting habitats and sediment types (clay soils in Essex; sandy soils in Morecambe Bay; differing inundation, creek structure, and vegetation).
- Sampling framework: 22 randomly allocated 1x1 m quadrats per mudflat and per saltmarsh site.
- Temporal scope: winter and summer 2013.

## Data content and variables
- Primary variables:
  - Chl a (µg g⁻¹)
  - Chl b (µg g⁻¹)
  - Chl c1+c2 (µg g⁻¹)
- Additional fields (structure for GIS use):
  - Season (Winter or Summer)
  - Location (region/site)
  - Site (e.g., CS, WS, WP, AH, FW, TM)
  - Habitat (Mudflat or Saltmarsh)
  - Quadrat Number (1–22)
  - Scale (spatial scale code corresponding to quadrat/grouping)
  - Chl a, Chl b, Chl c1+c2 values with accompanying StDev
  - NA entries indicate missing data
- Data format: Comma-separated values (.csv)

## Sampling and laboratory procedures
- Sampling: surface sediment (2 mm) collected with a contact corer.
- Preservation: flash-frozen with liquid nitrogen; stored in darkness at ≤ -80°C.
- Processing: samples dried using freeze-dryer; chlorophyll extracted with acetone.
- Measurement: spectrophotometric analysis at 630, 647, 664, and 750 nm; concentrations derived from absorption data using standard equations.
- Calibration and quality control:
  - Scales calibrated according to lab protocols; spectrophotometer accuracy checked with standard chlorophyll solutions.
  - Random quadrat locations determined via R (statistical software).

## Data organization and formats
- File format: CSV containing:
  - Metadata fields (Season, Location, Site, Habitat, Quadrat Number, Scale)
  - Measurement fields (Chl a, Chl b, Chl c1+c2) and their standard deviations
  - Row numbering and descriptive headers
  - Indicators for missing data (NA)

## Quality, provenance, and metadata considerations
- Data checked by recording readings into spreadsheets; spectrophotometer software used for data capture.
- Documentation includes site descriptions, habitat distinctions, and sampling design details to support reproducibility and GIS integration.
- Explicit note on no planned repeat sampling beyond 2013 CBESS campaign.

## Temporal coverage
- Winter and Summer 2013 sampling period for all sites and habitats.

## GIS and data-use implications
- Rich geospatial dataset suitable for map-based visualization of MPB chlorophyll across habitat types and coastal sites.
- Can be integrated with other CBESS datasets to analyze spatial patterns of primary production, habitat health, or ecosystem services.
- Useful for comparative analyses across contrasting sediment types and inundation regimes.
- GIS considerations: ensure coordinate reference system alignment with site coordinates; leverage quadrat-level data for fine-scale mapping and spatial statistics.