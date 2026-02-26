# README for dataset: 'Home range size and habitat availability data for 39 individual European nightjars on the Humberhead Peatlands NNR from 2015 - 2018' From submitted manuscript: 'High inter-individual variability in habitat selection and functional habitat relationships in European nightjars over a period of habitat change' Authors: Mitchell, Lucy J.; Kohler, Tim; White, Piran C .L.; Arnold, Kathryn E.

- What the dataset contains
  - Main data file includes:
    - Home range sizes at the 95% use level (hectares, ha)
    - Habitat availability within the 95% home range (percentage by habitat category)
    - Habitat selection ratios (Manly's Selection Ratios)
    - 95% home ranges derived from an accompanying GPS metadata file
    - Habitat availability derived from an independent habitat map
  - Interpretation of selection ratios:
    - Values > 1 indicate positive selection for a habitat type
    - Values < 1 indicate avoidance of a habitat type
  - Habitat types included in availability and selection ratios cover woodland, scrub, dry open (bracken/heather), cleared, wetland, water, and various named habitat categories (e.g., bare peat, cottongrass, bracken, heather, scrub, grass, buildings, off-site)

- Data structure and files
  - Two CSV data files:
    - Home Range and Habitat Availability
      - Columns include: Individual, Size_HR, Year, Av_woodland, Av_Scrub, Av_Dry, Av_cleared, Av_wetland, Av_water, SR_Water, SR_Bare_peat, SR_Woodland, SR_Wetland, SR_Cottongrass, SR_Bracken, SR_Heather, SR_Scrub, SR_Cleared+1, SR_Cleared+2, SR_Cleared, SR_Grass, SR_Building, SR_Off_Site
    - GPS Tracking Data
      - Columns include: ID, Date, Year, Time, Lat, Long
  - Study site and data collected from:
    - Thorne and Hatfield Moors, Humberhead Peatlands NNR, South Yorkshire
  - Timeframe and sample
    - June–August, 2015–2018
    - 39 individual European nightjars

- Methods (data collection)
  - Nightjars captured by mist nets between 21:00 and 01:00
  - Tagged with nanoFix mini GPS units (Pathtrack, Otley, UK)
  - Tracking schedule: 3- or 5-minute intervals (year-dependent)
  - Tags were archival (not transmitting) and birds were recaptured after 7–16 days
  - GPS data used to construct foraging tracks, estimate home range sizes, and assess habitat selection

- Data quality and processing
  - Data quality checks:
    - Manual checking for missing points
    - Exclusion of points with <3 satellites (considered poor GPS fix)
    - Visual QC in ArcMap to identify points outside plausible foraging ranges
  - GPS fixes are in WGS84 coordinates
  - Reported GPS fix accuracy estimates ranged from 5 to 25 meters depending on habitat

- Spatial and temporal context
  - GPS fixes at 3- or 5-minute intervals
  - Yearly fixed effects included as a factor in analyses
  - Location-specific sampling at Thorne and Hatfield Moors, Humberhead Peatlands NNR

- Use cases and applications
  - Constructing foraging tracks and estimating 95% home ranges
  - Quantifying habitat availability within home ranges
  - Assessing habitat selection patterns (Manly's Ratios) and their variation among individuals
  - Monitoring behavioural responses to landscape change over time
  - Supporting analyses of inter-individual variability in habitat relationships

- Metadata, provenance, and notes for data governance
  - Data derive from an independent habitat map and GPS-derived home ranges
  - Clear documentation of variable definitions and units in both CSV files
  - Values and categories aligned with habitat types observed on-site
  - Data support publication in a manuscript addressing high inter-individual variability in habitat selection under habitat change

- Considerations for data leaders and data management
  - Demonstrates end-to-end data lifecycle: collection, QC, geospatial processing, and explicit metadata
  - Includes structured metadata for both habitat availability and GPS tracking data
  - Useful for practices around data discoverability, format consistency, and provenance
  - Highlights the importance of documenting sampling schedules, GPS error estimates, and data filtering criteria for reproducibility and cross-study reuse