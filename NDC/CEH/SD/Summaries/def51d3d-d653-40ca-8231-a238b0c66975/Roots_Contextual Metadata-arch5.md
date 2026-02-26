# Root production in human-modified forests of Eastern Amazonia

## Overview
- Dataset Roots.csv contains measurements of fine root production across 20 plots (250 x 10 m each) in the Brazilian Amazon, spanning a disturbance gradient: undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests.
- Data collection period: October 2014 to May 2018.
- Purpose: quantify fine root production in relation to forest disturbance, using a standardized in-growth core approach.

## Sampling design and data collection
- Experimental design: four in-growth cores per plot (12 cm diameter, 40 cm deep), placed 50 m apart; cores inserted 30 cm deep with 10 cm aboveground.
- Measurement timeline per core:
  - First stock measurement: 24 intervals of five minutes each (5-minute breaks between intervals).
  - Second measurement: after 3 months, 12 intervals of five minutes each.
  - Third measurement: 3 months after the second.
  - After one year: a new core ~30 cm from the first; sampling restarts with 24 intervals.
- Field data collected alongside sampling: soil temperature and humidity inside and outside the core; field notes recorded.
- Laboratory processing: roots washed (2 mm sieve), oven-dried at 60°C for 72 hours, and weighed.
- Classification of forest disturbance: based on canopy disturbance from satellite imagery (1988–2010 chronosequence) and field assessments (fire scars, charcoal, logging debris).
- Fire status: Fire_ElNino indicator (1 = plot burned during the 2015–2016 El Niño; 0 = no burn).

## Data structure and variables
- File: Roots.csv (comma-separated values).
- Key columns (with purpose):
  - Date: date of data collection.
  - Catchment: microcatchment (~5,000 ha) containing the plot.
  - Transect: plot number within each catchment.
  - Plot: unique plot code (combination of catchment and transect).
  - Forest: disturbance class before the 2015–16 El Niño.
  - Fire_ElNino: binary burn status during El Niño.
  - Core number: identifier for the in-growth core.
  - Interval: five-minute interval number for sampling.
  - Stock: indicator for the first measurement of each core (1 = stock, 0 = not stock).
  - Weight (g): sample weight.
  - Lab_notes: notes from laboratory processing.
  - Temperature (inside the core) and Temperature (outside the core): in °C.
  - Humidity (inside the core) and Humidity (outside the core): in %.
  - Field notes: notes from field processing.
- Units: Weight in grams; Temperature in °C; Humidity in %.
- Plot-level coordinates: a set of 20 latitude/longitude pairs provided for plot locations.

## Spatial and temporal scope
- Spatial: 20 plots across Eastern Amazonia with explicit coordinates provided.
- Temporal: sampling occurred from 2014 to 2018, with multiple measurements per core over time to capture changes in root production.

## Access, format, and documentation
- Data file: Roots.csv attached with explicit column headers and variable descriptions as described above.
- Structure supports reuse and cross-study integration due to standardized sampling protocol and clear metadata fields.

## Data governance and stewardship considerations
- Metadata alignment: ensure consistent documentation of forest disturbance classification, fire status, sampling timeline, and core identifiers for discoverability.
- Provenance: maintain records of sampling and lab processing procedures to support reproducibility.
- Versioning: track any additions of plots, extended time series, or updated coordinates; preserve original data alongside new versions.
- Interoperability: CSV format facilitates broad reuse; consider providing a machine-readable metadata descriptor to enhance discovery and interoperability.