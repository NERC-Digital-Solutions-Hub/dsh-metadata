# Macroinvertebrate composition of Welsh upland rivers in response to organic matter addition

- Study design
  - Before-after-control-impact (BACI) setup with each stream split into an upstream reference zone and a downstream experimental zone.
  - Approximately 20–50 m between zones to ensure independence.
  - Time periods:
    - Before period (T1): 61–65 days, from early November 2012 to early January 2013; no manipulation; both zones treated equally.
    - After period (T2): 57–62 days, from early January 2013 to March 2013; experimental zone receives leaf litter addition for the entire period.
  - Leaf litter manipulation: one-tonne bags of deciduous leaves (oak, birch, alder) added proportionally to experimental zone area; additional 630 kg (wet weight) added on 12 February 2013 and 5 March 2013 following storm events to maintain leaf litter availability.
  - Sampling months during the study: January, February, March, April, and May 2013.
  - Temporal framing: January samples considered within the before period; February–April samples within the after period.

- Manipulation details
  - Leaf litter addition simulated natural senescence/abscission in wooded catchments.
  - Vegetable net bags used to maintain minimum wet weight (1.7 kg/m2) in the experimental zone.
  - Leaves degraded gradually to maintain loose leaf litter throughout the stretch.

- Collection methods
  - Six random macroinvertebrate samples per reach per time point using Surber net (0.1 m2 area, 330 µm mesh, 10 cm depth).
  - Sampling occurs across all reaches in five occasions: January, February, March, April, May 2013.
  - On-site preservation in 70% IMS; laboratory processing includes rinsing, sorting macroinvertebrates from debris, and preservation in 70% IMS.

- Field and laboratory instrumentation
  - Surber net sampler (0.1 m2, 330 µm mesh, 10 cm depth).
  - Laboratory stereo microscope for identification and measurements.

- Calibration
  - None reported.

- Analytical methods
  - Taxonomic identification to the lowest possible level using standard keys.
  - Body size measurements (millimeters) for each individual (Size1 and Size2), with Size1/Size2 indicating body part measured (e.g., head width vs. body length).

- Data structure and content
  - Data stored as flatbed CSV files.
  - Surber data schema (11 columns):
    - site_code: code of the sampling site
    - region: stream basin
    - month: collection month
    - time: before or after manipulation
    - landuse: basin land-use
    - reach: Experimental or Control site
    - replicate: replicate code
    - taxon_name: taxon name (as specific as possible)
    - Size1: body measurement 1 in mm
    - Size2: body measurement 2 in mm
    - Measurement: description of which size corresponds to which body part (e.g., head width vs. body length)
    - Comment: notes on body part associated with Size1/Size2
  - Additional site description file: DURESS_CU_site_description.csv with 10 columns, including site_code, name, coordinates (Eastings/Northings, Latitude/Longitude), elevation, survey campaign, catchment, etc.

- Supporting documents
  - DURESS_CU_site_description.csv provides site-specific metadata (locations, coordinates, elevation, survey campaign, catchment).