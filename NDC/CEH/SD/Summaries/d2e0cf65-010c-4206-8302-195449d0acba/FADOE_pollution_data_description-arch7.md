# FADOE_pollution.csv

## Overview
- Dataset of ambient pollutant concentrations and wind conditions around a field experiment.
- Measures NOx (sum of NO and NO2), NO, NO2, and Ozone (O3) at the centres of eight 8 m-diameter Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Includes experimental treatments, wind data from multiple directions, and precise temporal information.

## Data content and structure
- Pollutants and columns:
  - NOx (ppb)
  - NO (ppb)
  - NO2 (ppb)
  - O3 (ppb)
  - Each pollutant measured at the centre of the rings.
- Experimental design columns:
  - Treatment (E): diesel exhaust (D), ozone (O3), diesel exhaust + ozone (D+O3), control (CON)
  - Each treatment assigned to two rings (total of eight rings, two rings per treatment)
- Temporal and sampling fields:
  - Year (Column A), Date (Column B), Time (Column C)
  - Sampling cadence: every 60 seconds
- Wind data:
  - Wind speed and direction collected from anemometers located around the field to the south, west, north, and east
  - Directions and positions indicated as ws1/wd1, ws2/wd2, ws3/wd3, ws4/wd4 (columns indicating their values)
- Spatial context:
  - Field located around a wheat field
  - Field coordinates provided for 2018 and 2019:
    - 2018: latitude 51.482853, longitude -0.897749
    - 2019: latitude 51.482374, longitude -0.895855

## Experimental design and collection/Instrumentation
- Rings:
  - Center of eight 8 m-diameter FADOE rings
  - Two rings per treatment (D, O3, D+O3, CON)
- Measurements:
  - NO, NO2, NOx (NO + NO2), and O3 concentrations monitored sequentially every 60 seconds
  - Automated switching system connected to:
    - O3 analyzer: Model 49i (Thermo Scientific, USA)
    - NOx analyzer: Model 42C (Thermo Scientific, USA)

## Spatial context and GIS considerations
- Primary spatial unit: ring centre points (8 centers)
- Ring diameter and arrangement provide a localized study area within the wheat field
- Peripheral wind measurements (four cardinal directions) can be used to analyze dispersion and directionality relative to ring positions
- Spatial geolocation data available at field level; per-ring coordinates are not explicitly listed, so ring-level geolocations may need to be derived from a field plan or approximated from the field centroid and ring layout

## Temporal scope and data cadence
- Data collected across multiple years (2018, 2019) with daily timestamps and sub-minute cadence (60-second intervals)
- Timestamp fields: Year, Date, Time

## Data quality, transformation, and integration considerations
- Data likely require:
  - Verification of per-ring vs. center-point readings and alignment with ring IDs
  - Integration of pollutant data with corresponding wind measurements by time and ring
  - Handling of potential data gaps or sensor interruptions
- Quality assurance, cleaning, and transformation steps recommended:
  - Standardize units (ppb for all pollutants)
  - Verify consistent treatment mapping (two rings per treatment)
  - Derive per-ring spatial attributes (coordinates or geometry) for GIS mapping
  - Synchronize time indices across pollutant and wind data

## GIS-ready uses and suggested visualizations
- Map-based visualization options:
  - Point map of ring centers with pollutant concentrations color-coded per timestamp
  - Time-enabled animations showing spatial and concentration changes across the four treatments
  - Compare D vs. O3 vs. D+O3 vs. CON effects on NOx, NO, NO2, and O3
  - Overlay wind vectors from ws1/wd1, ws2/wd2, ws3/wd3, ws4/wd4 to assess dispersion relative to the rings
- Analytical possibilities:
  - Spatial-temporal analyses of pollutant dispersion under different treatments
  - Calculation of treatment effects by ring and time
  - Integration with field crop reaction data (if available) for impact assessment

## Metadata and preparation notes
- Coordinate reference system (CRS) not specified; GIS preparations should document CRS (likely WGS84 for the provided lat/long)
- Ring-level coordinates may need to be inferred from a field layout plan
- Ensure proper documentation of column mappings (Year, Date, Time, Treatment, pollutant columns, and wind columns) for reproducibility
- Consider deriving hourly and daily aggregates for summary mapping and reporting