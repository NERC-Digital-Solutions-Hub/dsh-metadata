# This document provides information relating to the raw data sets on the behaviour and distribution of Lepidoptera (butterflies and day flying moths) at the Stonehenge Landscape in 2012

## Overview
- Presents raw datasets on Lepidoptera behavior and distribution collected in 2012 at the Stonehenge Landscape.
- Data cover Lepidoptera flight paths, species, start/end locations, and associated environmental and botanical context.
- Data quality assurance performed to identify outliers/anomalies using species occurrence expectations and exploratory analysis.

## Study site and context
- Location: National Trust Stonehenge Landscape within the Stonehenge World Heritage Site, Wiltshire, SW UK.
- Setting: Landscape-scale grassland restoration with a mosaic of chalk grassland fragments, restoration fields, semi-improved pasture, arable land, and woodland.
- Restoration background: Chalk grassland re-creation initiated around 2000 using seed from Salisbury Plain to protect archaeology and ecological value.

## Experimental design
- Field: Seven Barrows grassland re-creation site; sown in 2000 with chalk grassland seed.
- Boundaries: Eight survey boundaries (20 m long each) within two 40 m x 50 m grassland areas; boundaries numbered 1–8.
- Treatments and controls: Four boundaries adjacent to a mown area (treatment) and four corresponding dummy boundary controls in unmown grass.
- Blocks: Two blocks defined as ‘sheltered’ (un-mown side west) and ‘exposed’ (un-mown side east).
- Spatial arrangement: Boundaries within the same block separated by 5 m; treatment and control boundaries separated by 25 m; field area limited to 400 m² mown grass with an experimental fenced area not exceeding 100 m.
- Survey window: Boundaries surveyed from 24 July to 23 August 2012; several logistical constraints noted (edge effects, proximity to fences, etc.).

## Lepidoptera surveys
- Survey method: Observer traces flight paths of Lepidoptera within a 10 m zone on either side of each boundary.
- Observation unit: Each Lepidoptera flight path observed for 3 minutes; individual recorded until stationary >3 minutes or moved >20 m from survey area.
- Survey effort: 20 minutes per boundary per survey period, with three survey periods over five weeks.
- Boundaries: Boundaries 1–8 surveyed per period; random sequence to minimize bias; efforts balanced across sides of boundary.
- Data captured per individual: species, start and finish location (relative to mown/unmown sides and boundary type), flight path, and exit behavior categorized as crossing, following, avoiding, or staying (if not exiting or path indeterminate).

## Environmental variables
- Vegetation: Eight 0.5 m x 0.5 m quadrats per survey area (four on unmown side and four on mown side, plus corresponding control sides) to record vegetation height/density (drop-disc method) and nectar flower availability.
- Nectar resources: Number of flowering units by family (Asteraceae, Fabaceae, Dipsacaceae); flowering surveys conducted on 19 July, 10 August, and 23/24 August.
- Weather proxies: Temperature, wind speed, wind direction, cloud cover (estimated by eye) and wind data sourced from the nearest meteorological station (Boscombe Down) by hour.

## Data structure and nomenclature
- Data sources include:
  - 7_Barrows_Lepidoptera_2012: Key for Lepidoptera observation data columns (DATE, TEMPERATURE, WIND SPEED/DIRECTION, etc.; boundary-specific fields; species, behaviour, habitat start/end, nectar on/off, etc.).
  - 7_Barrows_Resources_2012: Key for plant resource data columns (habitat type, side, quadrat, drop disc, bare ground, dead vegetation, flowering species and coverage data).
- Taxonomy references: Lepidoptera and plant names follow standard UK references (Stace 2010 for plants; Langmaid et al. 1989; Heath & Emmet 1985 for Lepidoptera; supported by field guides).
- Tables included:
  - Lepidoptera species list with common names and codes (e.g., Maniola jurtina – Meadow Brown; Zygaena filipendulae – 6-spot Burnet Moth; etc.).
  - Flowering plant species list with scientific names and abbreviated codes (e.g., Achillea millefolium – Yarrow; Lotus corniculatus – Birdsfoot Trefoil; etc.).
- Scope: Data are raw; intended for GIS-ready integration and further analysis.

## Data quality and limitations
- QA processes included checking for outliers/anomalies using species-expected occurrence patterns and pivot/exploratory analyses.
- Potential confounding factors acknowledged: proximity to mown edges and fences; edge effects from boundary layout; limited survey window focusing on peak adult butterfly/moth occurrence.
- Weather and field conditions were monitored to ensure acceptable survey conditions per Butterflies Monitoring Scheme guidelines.

## How GIS specialists can use this dataset
- Spatial features:
  - Boundaries as polygons with boundary IDs (1–8) and block classifications (sheltered/exposed); mown vs unmown sides.
  - Survey areas represented as 20 m x 20 m grids centered on boundaries; flight path points and trajectories within these grids.
  - Habitat typing and edge effects can be mapped by linking Lepidoptera observations to start/end habitat types (Chalk, Arable, Restoration) and boundary edge status.
- Attributes to map and analyze:
  - Species occurrences and flight path behaviors (Cross, Follow, Avoid, Stay) linked to boundary ID, boundary edge, and block type.
  - Environmental context: vegetation density/height, nectar resources, flowering unit counts, wind/temperature, cloud cover.
  - Temporal dimension: three survey periods within a five-week window; potential for temporal trend analyses.
- Data integration:
  - Join Lepidoptera observations with plant resource data via shared boundaries and quadrats.
  - Cross-reference with taxonomy tables to standardize species codes and enable harmonized queries.
- Potential outputs:
  - Spatial distribution maps of Lepidoptera species and flight behaviors by boundary and habitat type.
  - Edge effect analyses comparing treated (mown edge) versus control boundaries.
  - Environmental correlation maps showing associations between nectar availability, vegetation structure, and Lepidoptera activity.

## References and data provenance
- Campbell (2009); Pemberton (2011); Pollard & Yates (1993); Ries & Debinski (2001); Rodwell (1992); Stace (2010); Heath & Emmet (1985); Langmaid et al. (1989); Stewart et al. (2001); Young et al. (2009).
- Data context: Adapted from Grace Twiston-Davies’ PhD thesis (2014), with data collection methodologies aligned to site-specific restoration aims.