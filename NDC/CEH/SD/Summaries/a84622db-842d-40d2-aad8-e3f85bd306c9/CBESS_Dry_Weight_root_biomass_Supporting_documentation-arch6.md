# Dry weight root biomass from three soil depths on salt marsh sites at Morecambe Bay and Essex.

- Purpose and scope
  - Dataset documenting root biomass (dry weight) in three soil depth intervals (0–10 cm, 10–20 cm, 20–30 cm) for saltmarsh sites in Essex and Morecambe Bay.
  - Seasonal coverage: Winter and Summer 2013, with additional Essex winter sampling (2–6 March 2013); no repeated sampling planned.
  - Intended for analysis of below-ground biomass across depth, site types, and grazing contexts, enabling cross-site comparisons and data-driven insights into marsh stability.

- Location and site context
  - Essex sites (clay soils): Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay sites (sandy soils): Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
  - Site descriptions reflect contrasting soil types, inundation patterns, creek structure, and vegetation.
  - Grazing regimes differ: Essex areas heavily grazed by brent geese; Morecambe Bay sites grazed by sheep with occasional geese.

- Data collection and methods
  - Sampling unit: 1 x 1 m quadrats; 22 quadrats per site.
  - Core method: one large sediment core (16 cm diameter, 30 cm depth) per quadrat, including soil, roots, and vegetation.
  - Processing: cores exposed to water erosion in a recirculating flume; roots separated into depth intervals; roots dried at 60°C for 72 hours; weighed to determine dry weight.
  - Conversion: results converted to kilograms dry weight per square meter (kg DW m^-2).

- Sampling design and spatial structure
  - Site-scale area: rectangular marsh areas ranging from 400 x 500 m to 1000 x 1000 m, spanning low, mid, and high marsh zones.
  - Quadrat allocation and spatial scales (via R): A = 1 quadrat; B = 3 quadrats 1–10 m apart; C = 6 quadrats at broader spacing; D = additional random allocation (details reflect site-specific design).
  - Random allocation used to reduce sampling bias.

- Variables and data structure
  - Primary variables: RB_0-10 (root biomass 0–10 cm), RB_10-20 (root biomass 10–20 cm), RB_0-30 (total root biomass 0–30 cm).
  - Units: kg DW m^-2.
  - Dataset fields include: season (Winter or Summer), location (Morecambe or Essex), site code (CS, WS, WP; AH, FW, TM), habitat (Saltmarsh or Mudflat), Quadrat Number (1–22), Scale (A–D), alongside data quality and format descriptors.
  - Total root biomass at 0–30 cm is the sum across depth layers.
  - File format: CSV.
  - Data quality notes: data checks performed by entering scale readings into spreadsheets; outliers checked; some missing data due to sample loss (blank cells).

- Data quality, calibration, and documentation
  - Calibration: scales calibrated according to laboratory protocols where applicable.
  - Quality control: standard checks, including transcription checks and outlier review.
  - Documentation: includes comprehensive location coordinates, site descriptions, and sampling procedures to support reproducibility.

- Accessibility and metadata
  - Dataset staff: Hilary Ford.
  - Precise site coordinates provided for Essex and Morecambe Bay locations.
  - Metadata captures sampling window specifics, site grazing context, and data processing steps to enable re-use and interpretation.