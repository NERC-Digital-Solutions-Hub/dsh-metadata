# West Halladale wildfire burn severity assessment and peat core analysis in the Flow Country peatlands

- Aim
  - Use standardized, time-consistent data to demonstrate environmental condition and support scrutiny of environmental health and policy performance.
  - Produce outputs suitable for monitoring and comparison over time, including categorization of environmental properties against standards.

- Site context and fire event
  - Location: Flow Country peatlands in northern Scotland (Caithness and Sutherland).
  - Event: Dry, warm spring 2019 followed by wildfire that burned ~60 km2 of wet heath and blanket bog within a ~4000 km2 area.
  - Study footprint: West Halladale wildfire, affecting SSSI and nearby NNR areas (Forsinard Flows).
  - Severity mapping: Areas classified as low, medium, or high severity using NatureScot imagery; high severity mainly in drained peatland; no high severity in near-natural southern portion.
  - Sampling frame: Plots allocated by severity and drainage status (High/Medium/Low x Drained/Near-natural/Undrained), with plot codes combining severity letter (H/M/L), drainage, and an index (1–15). Sampling spread across northern, mid-west, and southern parts of the footprint.

- Sampling design and field execution
  - Plots visited: Six plots per severity–drainage combination where feasible, plus two extra plots in Drained High severity areas, totaling 34 cores.
  - Core depth target: 40–50 cm; actual suitability affected by slope, peat depth, or access restrictions.
  - Field visits: Five field sessions between late February and mid-March 2020 (dates: 20/02, 21/02, 05/03, 15/03, 16/03/20).
  - Core collection: Russian corer; samples stored in PVC half-pipes; codename assigned to each core; top and bottom identified on the container.
  - Field data: GPS coordinates, plot severity, depth, coordinates, elevation, vegetation notes, and photos recorded in field notes and transcribed to an Excel dataset.

- Sample handling, storage, and metadata
  - In-field recording: Field notes (observer, burn severity, codename, depth, coordinates, elevation) plus photos.
  - Data management: Raw data transcribed to a dataset stored on the ERI server; quality checks performed.
  - Storage: Cores returned to cold storage to prevent deterioration until laboratory analysis.

- Instruments and measurements
  - Field equipment: GPS device, maps, Russian corer, PVC half-pipes, saran wrap, measuring tape, camera.
  - Laboratory equipment: Measuring balances (five- and three-decimal accuracy), 100 mL measuring cylinder (water displacement for volume), oven (105°C), muffle furnace (550°C), desiccator, crucibles, Milli-Q water system.
  - Calibration: Balances calibrated with standard weights per manufacturer instructions.

- Data collection and units
  - Metadata per core (Peat_core_coordinate.csv):
    - COREID, Depth (cm, 40–50 cm), Lat_OSGB, Long_OSGB, Grid_Reference, Alt_masl, Exposure, Vegetation.
  - Core-sub-section properties (Peat_core_data.csv), 5 cm intervals:
    - COREID, SEVERITY (LOW/MEDIUM/HIGH), TYPE (DRAINED/UNDRAINED), DEPTH (cm), VOL (volume in cm3, via water displacement, 3–10 cm3), WET_PEAT (g), DRY_PEAT (g), BD (g cm-3), MOIST% (0–100%), vonPOST (scale 1–10), WET_PEAT10 (g), DRY_PEAT10 (g), ASHg (g), OM% (0–100%), ASH% (0–100%), OC% (0–50%).
  - Notes: Values include valid ranges; some sub-samples with weighing errors were removed from final dataset to prevent erroneous calculations.

- Analytical methods and processing
  - Bulk density (BD) and moisture (MC):
    - Wet weight measured from a subsample; volume via water displacement; dry weight after 105°C drying; BD = dry weight / volume; MC calculated from wet and dry weights.
  - Organic matter and carbon:
    - LOI at 550°C for 4 hours to determine OM (from dry weight before and after ashing), and ash content (ASH) calculated from 550°C vs 105°C dry weights.
    - OC content estimated as OM% × 0.5 (assuming 50% organic carbon in organic matter).
  - Von Post humification:
    - Qualitative scale (H1–H10) based on a hand-squeezing protocol describing peat decomposition state; used as a rapid decomposition indicator.
  - Quality control:
    - All sub-sections analyzed; samples with inconsistencies (e.g., dry weight > wet weight) removed to avoid erroneous values.
  - Documentation and sequencing:
    - Core sections cut at 0–5 cm intervals, photographed, and processed; samples handled and weighed with careful lab protocol and cross-checks.

- Data products and accessibility
  - Core datasets:
    - Peat_core_coordinate.csv: core identifiers, depth, coordinates, grid references, elevation, exposure, and vegetation context.
    - Peat_core_data.csv: 5 cm interval measurements per core (severity, drainage type, depth, volume, bulk density, moisture, LOI/OM/ASH/OC, von Post).
  - Data management and sharing:
    - Data stored on ERI server; plans to upload to appropriate portals and enable access for broader use and reuse by stakeholders.

- Quality assurance and challenges
  - Data quality: Standardized collection and lab methods, calibration of equipment, and explicit removal of problematic sub-samples to ensure robust derived properties.
  - Challenges highlighted by the project aim:
    - Increasing value of datasets by integrating with other environmental data (e.g., cross-dataset analyses) to avoid single-use limitations.
    - Providing access to underlying data to support transparency and broader reuse.

- References
  - Beilman et al. (2009); Chambers et al. (2011); Ekono (1981); Heiri et al. (2001); Melling et al. (2006); Ratcliffe et al. (2018a, 2018b).