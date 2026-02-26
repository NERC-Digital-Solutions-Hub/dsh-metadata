# Extensive_Vegetation_and_Soil_Data.csv

## Purpose and scope
- Describes a stratified survey of ecological and soil states to map fine-scale covariation between vegetation and edaphic characteristics.
- Sites located in Yukon (2013) and Northwest Territories (2014), Canada.
- Data file uses data codes described in Table 1; 24–30 x 1 m2 plots per site to capture variability.

## Data variables and codes
- Key variables included:
  - ALD: Late August thaw depth (active layer depth/thickness) from moss base.
  - slope: Ground surface incline angle (degrees).
  - Tree_LAI: Leaf Area Index of tree canopy.
  - Understorey_LAI (LAI U): LAI for understory vegetation (not moss layer).
  - OM_thick: Thickness of organic matter layer.
  - Moss_thickness: Moss layer thickness (living + dead moss).
  - OM_and_Moss_thickness: Combined thickness from moss surface to mineral layer.
  - DeepMoist: Deeper soil moisture (11–16 cm below moss/soil surface).
  - SurfMoist: Surface soil moisture (upper 0–6 cm).
  - Height: Mean understory vegetation height.
  - Region, Site, Plot: Spatial identifiers; GPS coordinates.
  - LAI: Total Leaf Area Index.
- Data codes and definitions are described in Table 1 of the dataset.

## Methods and data collection
- Tree canopy LAI (LAI Tree): Measured with Nikon D5000 DSLR and hemispherical lens; nine photos per plot, processed with CAN-EYE; sunlight conditions controlled via per-photo thresholding.
- Understory LAI (LAI U): Measured with LI-COR LAI2000 Plant Canopy Analyzer; one measurement above, four measurements at plot corners; shading controlled with cap and, if needed, tarpaulins.
- Understorey height: Measured at five points per plot (four corners and center) in a 0.5 x 0.5 m quadrat; mean used in analyses.
- Moss thickness: Determined by removing moss/organic material and measuring from moss surface to where dead moss loses identifiable structure.
- Surface moisture (SurfMoist): Measured in upper moss/soil layer using ML3 ThetaKit; readings reflect moss layer properties.
- Deeper moisture (DeepMoist): Measured at ~11–16 cm depth; four readings per plot over season; mean used; factory calibration applied due to calibration challenges.
- OM thickness: Measured with soil corer to base of O horizon; moss thickness subtracted.
- Slope: Assessed along steepest gradient using a 50 cm wooden plank and digital angle meter.
- Active Layer Thickness (ALT): Measured with a stainless steel probe plus temperature verification; plots with non-frozen soil excluded.
- Reference: Fisher et al. (2016) for related methodology.

## Sites and contextual details
- Detailed site information provided in Table 2, including:
  - Site names and abbreviations (e.g., FFB, FFU, BF, MB, MU, BB, BS).
  - Location data: city, country (Whitehorse, Yukon; Yellowknife, Northwest Territories), latitude, longitude, elevation.
  - Vegetation Zone: Boreal across all sites.
  - Vegetation descriptions: post-fire establishment, ground cover patterns, understory composition variations.
  - Disturbance/Hydrology: upland vs. wetlands, recent fire status where applicable.
  - Permafrost Zone (PF Zone): sporadic or discontinuous across sites.
  - Time of data collection: specific windows for vegetation and soil data (e.g., early August 2013; late July 2013; August 2014).
- Sites capture post-fire conditions, varying disturbance histories, and permafrost considerations to explore environmental health indicators.

## Temporal scope and data provenance
- Field data collected across two seasons:
  - 2013 (Yukon) and
  - 2014 (Northwest Territories).
- Data are organized with clear temporal markers for vegetation vs. soil sampling.

## Data quality, metadata, and access considerations
- Data described by coded variables (Table 1) and site details (Table 2) to enable reproducibility.
- Metadata gaps can arise when verifying dataset suitability; experts are encouraged to consult the accompanying tables and Fisher et al. (2016) for methodological context.
- Public sharing of underlying data is part of the framework, aligning with data governance practices common to monitoring outputs, though specific sharing barriers are noted in the archetype’s challenges (e.g., metadata adequacy, data silos).

## Relevance to monitoring framework authors
- Demonstrates a structured, field-based approach to environmental health monitoring:
  - Stratified plot design and comprehensive variable suite (vegetation structure, soil moisture, organic layer properties, permafrost context).
  - Standardized measurement protocols with controls for environmental conditions (sunlight, shading).
  - Integration of remote sensing-inspired LAI methods with ground-based validation.
  - Clear documentation of data codes, site metadata, and sampling timelines to support transparency and reuse.
- Highlights practical data governance considerations:
  - Need for thorough metadata and data sharing arrangements.
  - Challenges of data calibration, especially for soil moisture probes in organic soils.
  - Importance of documenting disturbance history and permafrost context for policy-relevant assessments.