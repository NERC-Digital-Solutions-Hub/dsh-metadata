# Stable isotope values for 108 water samples collected in the Gandak River Basin, in Bihar, India are presented, with accompanying values for SEC (specific electrical conductivity) for most of these samples.

- Overview
  - 108 water samples collected in the Gandak River Basin, Bihar, India, between February 2017 and February 2019.
  - Sample types include surface water, groundwater, and rainfall.
  - Stable isotopes measured: d18O and dD relative to VSMOW; SEC measured at source in the field.
  - Analyses conducted by British Geological Survey laboratories (UK) as part of the CHANSE project.
  - Data designed to enable exploration of water sources, mixing, and hydrogeochemical relationships; data are accompanied by extensive metadata.

- What is included in the dataset
  - Isotopic and chemical measurements
    - d18O VSMOW2 (‰)
    - dD VSMOW2 (‰)
    - SEC (uS/cm)
  - Metadata fields for each sample
    - sample_date
    - BGS LIMS or Lab Code
    - sample identifier (often presented as a code such as 13965-0001, NIGL_001, etc.)
    - source_type (e.g., River Gandak, Tube well, Hand pump, Canal, Rainfall, etc.)
    - source_water_type (Groundwater, River Gandak, Canal, Rainwater)
    - lat, long (decimal degrees)
    - surface_elevation_mOD (meters above datum)
    - source_depth_m (depth in meters; may be blank)
    - Source_use (usage context if specified)
    - Notes (detailed sampling context, conditions, equipment, timing, etc.)
  - Data formatting
    - Missing values recorded as blank
    - Dates formatted day/month/year (dd/mm/yyyy) in the sample_date field
    - Units: d18O and dD in per mil relative to VSMOW; SEC in microSiemens per centimeter

- Variable descriptions (highlights)
  - sample_date: date the sample was taken
  - d18O VSMOW2 (‰): Oxygen-18 concentration relative to VSMOW
  - dD VSMOW2 (‰): Deuterium concentration relative to VSMOW
  - SEC uS/cm: Specific electrical conductivity
  - BGS Sample identifier or Lab Code: reference to the sample in the BGS LIMS
  - lat/long: geographic coordinates of the sampling point
  - surface_elevation_mOD: elevation above mean datum
  - source_depth_m: depth of the source well or sampling point (if applicable)
  - Source_use: reported usage context (e.g., domestic, irrigation)
  - Notes: qualitative context for the sampling point (e.g., pumping performed before sampling, canal conditions, presence of bubbles, sampling method)

- Site locations and sampling context
  - The dataset includes a wide range of sampling sites across the Gandak basin, including:
    - River Gandak sampling points
    - Tube wells and hand pumps (groundwater)
    - Canals and canal-related sampling
    - Rainfall collectors
  - Coordinates (lat/long) and context notes accompany each site, with dates from late February 2017 through March 2019
  - Notes provide detailed sampling context (e.g., times pumping occurred before sampling, proximity to canals, well depths, and sampling procedures)

- Data collection, processing, and provenance
  - Sampling: unfiltered samples bottled at the source in Nalgene containers, filled to brim to minimize air exposure
  - Field measurements: SEC measured in the field at the source
  - Isotope analysis: performed by British Geological Survey laboratories (UK)
  - Data provenance: CHANSE (Coupled Human And Natural Systems Environment) project
  - Quality and structure considerations:
    - Data include a combination of quantitative measurements and rich qualitative notes describing sampling conditions
    - Some entries have missing depth or elevation data; others include extensive Notes with sampling context
    - Date formats and field naming follow the dataset’s schema; user should verify consistency when merging with other datasets

- Potential uses for data support
  - Isotope hydrology analyses to investigate groundwater-surface water interactions and mixing
  - Spatial mapping of isotopic signatures and SEC across the Gandak basin
  - Data-driven dashboards or self-serve analyses combining d18O, dD, SEC with location and depth information
  - Quality assurance, data cleaning, and integration with broader CHANSE data products
  - Temporal trend assessment across 2017–2019 and cross-referencing with rainfall events and pumping practices

- Practical considerations for use
  - Be mindful of formatting variations (e.g., date representations and occasional long Notes fields)
  - Some samples have incomplete metadata (e.g., source_depth_m or surface_elevation_mOD blank)
  - Pumping context and sampling timing documented in Notes can influence isotopic or conductivity readings
  - Ensure consistent unit interpretation (‰ for isotopes, uS/cm for SEC)

- Summary takeaway
  - The dataset provides a comprehensive set of stable isotope values and conductivity measurements for 108 water samples across a diverse set of water sources in the Gandak River Basin, with rich site- and context-specific metadata to support robust, self-serve data analysis and visualization efforts in hydrogeochemical research.