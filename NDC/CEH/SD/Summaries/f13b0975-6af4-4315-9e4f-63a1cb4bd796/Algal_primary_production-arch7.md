# Experimental design/Sampling regime

## Overview
- Study used a before-after-control-impact (BACI) design to compare upstream reference zones with downstream experimental zones within each stream.
- Zones within streams are similar in length, habitat (riffle, glide, pool), slope, flow, substratum, and land use.
- A 20–50 m separation between reference and experimental zones ensures independence.

## Experimental design and timeline
- Before period (T1): 61–65 days from early November 2012 to early January 2013; no manipulation; both zones treated equally.
- After period (T2): 57–62 days from early January to March 2013; experimental zone manipulated with leaf litter addition for entire period.
- January samples considered part of the before period; February–April samples part of the after period.

## Manipulation details
- Leaf litter added using one-tonne bags containing oak, birch, and alder leaves; distributed proportionally by experimental zone area.
- Leaves placed above the experimental zone but below the reference zone; designed to mimic natural senescence and abscission.
- Vegetable nets maintained a minimum wet weight of 1.7 kg m^-2 in the experimental zone.
- Additional leaf litter (630 kg wet weight) added on two dates (12 February 2013 and 5 March 2013) following large storm events.

## Experimental units and sampling design
- Six experimental units (algal tiles) placed randomly within each reach of the experimental sites before and after manipulation.
- Each tile pair includes a treated tile (edges Vaseline-coated to deter grazing) and a control tile to assess grazing pressure.

## Measurements and analytical methods
- Primary metric: chlorophyll a on tiles as a proxy for algal production and herbivory rates.
- Sample processing: algal biofilm scrubbed, filtered, and chlorophyll extracted with acetone; spectrophotometric measurement at 664 nm (chlorophyll-a) and 750 nm (turbidity).
- Calculation: chlorophyll-a concentration per area using the specified equation with constants from the protocol (A, K, V, S, l).
- Supporting analyses and references provided for methodology.

## Data collection and instruments
- Field and laboratory procedures referenced; mass spectrometry mentioned for laboratory instrumentation.

## Calibration and quality control
- Calibration steps and specific values: None provided.
- Quality control: None described.

## Data structure and units
- Data format: flatbed CSV files.
- Main data fields (10 columns) include:
  - site_code: sampling site code
  - region: stream basin
  - date: sampling date
  - time: pre/post manipulation indicator
  - landuse: basin land-use
  - reach: site is experimental or control
  - treatment: indicates Vaseline or no-vaseline condition on tile edges
  - replicate: replicate code (A–F)
  - exposure: number of days exposed
  - chlorophyll: chlorophyll a concentration (μg cm^-2)
- NA indicates missing data.

## Supporting data and documentation
- Supporting file: DURESS_CU_site_description.csv containing site metadata:
  - site_code, name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment
- Provides spatial context (grid references and coordinates) for GIS integration.

## Relevance for GIS specialists
- Design emphasizes spatial separation of reference and experimental zones and fixed sampling units (tiles) suitable for map-based visualization.
- Data include explicit location identifiers, coordinates, and grid references, enabling geospatial mapping and spatial analysis.
- The 10-column chlorophyll dataset and site description support integration into GIS workflows for trend mapping, BACI analysis, and visualization of upstream vs downstream effects.