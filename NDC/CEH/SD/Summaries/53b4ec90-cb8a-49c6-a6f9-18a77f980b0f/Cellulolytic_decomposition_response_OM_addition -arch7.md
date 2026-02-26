# Cellulolytic decomposition of Welsh upland rivers in response to organic matter addition

## Aim
- Describe a BACI-based study assessing how organic matter addition (leaf litter) affects cellulolytic decomposition in Welsh upland streams.
- Produce data suitable for map-based visualization and spatial analysis of stream sites, treatments, and outcomes.

## Study design and setting (GIS-relevant context)
- Experimental design: before-after-control-impact (BACI) with each stream split into:
  - Upstream reference zone (control)
  - Downstream experimental zone (treatment)
- Zone separation: 20–50 m between reference and experimental zones to maintain independence
- Habitat and site characteristics similar across zones (riffle, glide, pool structure; slope; flow; substratum; land use)
- Time periods:
  - Before period (T1): 61–65 days, early Nov 2012 to early Jan 2013
  - After period (T2): 57–62 days, early Jan to March 2013
- Treatment during T2: leaf litter addition to the experimental zone (simulating natural senescence/abscission)
  - Leaf litter: 1 tonne bags containing oak, birch, alder; proportionally divided by experimental zone area
  - Additional leaf litter: 630 kg (wet weight) added on 12 Feb and 5 Mar 2013 after storm events
  - Leaf packs maintained within the experimental reach using poles; leaf packs degraded slowly to maintain coverage

## Data collection and sampling regime (how data would map in GIS)
- Experimental units: six cotton strips placed randomly in each experimental reach before and after manipulation
- Sample processing:
  - Strips retrieved at end of T1 and T2, frozen at -20°C
  - In the lab: rinsed, oven-dried (65°C), and tensile strength measured with a Hounsfield machine
  - One breaking-strain value per strip
  - Three untreated control strips used to account for transport and washing losses
- Data produced per site/reach: tensile strength and comparative loss metrics linked to exposure (Before/After)

## Data structure and content (GIS-ready attributes)
- Data files are flatbed CSVs
- Core dataset (Cellulolytic decomposition data) contains 10 columns:
  - site_code: Code of the sampling site
  - region: Stream basin
  - date: Date of sampling
  - time: Before or After manipulation
  - landuse: Basin land-use
  - reach: Experimental or Control site
  - replicate: Replicate code (A–F)
  - exposure: Number of days exposed
  - breaking_strain: Tensile strength in Newtons
  - %_loss: Percent loss of tensile strength relative to control
- Supporting site metadata (DURESS_CU_site_description.csv) contains 10 columns:
  - Site_description, Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment
  - Location details include Welsh National Grid references and geographic coordinates (WGS84), enabling precise GIS mapping
- Spatial readiness:
  - Site coordinates (Eastings/Northings, Latitude/Longitude) and elevations allow integration with GIS layers (rivers, catchments, land-use maps)

## Data quality and provenance
- Calibration steps: None specified
- Quality control: None described
- Documentation includes references and data catalogue notes for linking site data with external sources

## How this data can be used in GIS (applications and workflows)
- Map and analyze spatial distribution of reference vs. experimental zones across streams
- Integrate with catchment and land-use layers to explore spatial drivers of cellulose decomposition responses
- Visualize leaf litter treatment timing/extent and correlate with changes in tensile-strength metrics (breaking_strain and %_loss)
- Use replicate and exposure fields to assess spatial and temporal patterns across reaches
- Link site_description metadata to create enriched maps with coordinates, elevation, and survey campaigns
- Facilitate data transformation and cleaning workflows to harmonize data from multiple streams and scales

## References and data sources (context)
- Data catalogue and site description provide linkages between the study data and external references, including geographic coordinates and catchment associations.