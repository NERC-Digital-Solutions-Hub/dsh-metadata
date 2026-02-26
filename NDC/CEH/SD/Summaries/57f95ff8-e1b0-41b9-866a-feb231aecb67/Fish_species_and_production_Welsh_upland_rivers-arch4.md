# Fish species and production of Welsh upland rivers

## Objective and scope
- Investigates fish populations and variations in biomass across upland Welsh rivers during a stable base-flow period.
- Data collected in 2012 (June–September) and 2013 (July and September) across upland Wales.

## Sampling design
- Representative 30 m reaches per site, enclosed with stop nets (mesh size 10 mm^2).
- Three-pass depletion electrofishing (Pulsed DC) to maximize catch and represent total abundance.
- Site-specific conductivity used to adjust applied voltage.
- Field measurements prioritize representative sampling for multiple species.

## Collection methods and measurements
- Identification to species, measurement of fork length (mm) and weight (g) for each fish.
- Mass estimation for some individuals using a length-mass regression when direct measurement was not possible.
- Length-mass model described as WM = b3 FL + b1 FL + intercept (nonlinear gain with length; cubic term noted in text; coefficients available in a separate file).
- References provided for methodology and equipment, including Beaumont (2011) and Kruse et al. (1998); Maitland (1972) for species IDs.

## Data structure and content
- Primary data file: flatbed CSV with eight columns:
  - site_code, season, date, fish (number and species), run, species, length (mm), weight (g).
- Supporting site metadata: DURESS_CU_site_description.csv with ten columns:
  - site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment (and related descriptors).
- Units: length in millimetres; weight in grams.

## Data quality, provenance, and governance
- Quality control: None explicitly documented.
- Data provenance includes field methods and equipment details; references to external methodological sources.
- Links to some references are provided but may not be permanently maintained.

## Potential uses and considerations for data leaders
- Useful for analyzing spatial variation in fish biomass and species composition across upland rivers.
- Enables linking fish data with precise site metadata (geolocation, elevation, catchment) for broader ecological analyses.
- Considerations:
  - Some biomass estimates rely on length-mass regression rather than direct measurement, introducing estimation uncertainty.
  - No formal quality control documented; users may need to apply their own validation.
  - Data coverage is limited to specific base-flow periods and sites in upland Wales; integration with other datasets may require harmonization of methods and metadata.