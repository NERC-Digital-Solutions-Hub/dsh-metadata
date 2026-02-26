# RAINFOR Field Manual for Plot Establishment and Remeasurement

- Goal: Use long-term permanent plots to monitor Amazon forest biomass, dynamics, and their links to soil/climate, enabling regional insights and basin-scale carbon dynamics modelling. Emphasizes standardised methods to enable cross-site comparisons and discussions of methodological issues.

- Objectives of RAINFOR:
  - Quantify long-term changes in biomass and turnover
  - Relate forest structure, ecophysiology, biomass, and dynamics to climate and soils
  - Understand productivity–mortality–biomass relationships
  - Use these relationships to inform basin-scale carbon dynamics
  - Examine biodiversity variability and its relation to soils/climate
  - Promote standardisation of inventory protocols and methodological discussion

- Data governance and management (for Data Leaders):
  - Central data hub: ForestPlots.net; standardized data upload and QC procedures
  - One plot = one Excel file with three worksheets (trees, lianas, site), ensuring consistent structure and metadata
  - Emphasis on documenting methodology, data provenance, and any corrections or interpolations
  - Clear logging of corrections, assumptions, and measurement changes; maintain original values alongside edits

- Plot design and sampling strategy:
  - Pan-Amazon strategy: maintain plots across edaphic and climatic variation; new plots randomly located within local geomorphological strata
  - Selection criteria for new plots: homogeneous soil parent material, adequate access, long-term security, institutional support, minimal anthropogenic disturbance (unless explicit study of human impacts)
  - Randomization: plots within strata assigned randomly; avoid bias toward “good” forest
  - Scale and layout: 1-hectare (1 ha) plots; subdivided into 20 m x 20 m subplots; boundaries defined in 20 m segments
  - Shape considerations: choice between square and rectangular plots; aim for minimal edge effects and logistical practicality
  - Topography: consider slope corrections when projecting 1 ha; use d = 20 / cos(theta) for distance along slope; slope corrections for cross-site comparability

- Timing, orientation, and logistics:
  - Measurements should occur over full-year intervals; time surveys to minimize soil-water variation (prefer wet season timing in El Niño-impacted areas)
  - Plot orientation (N/S or E/W) is convenient; document bearings, latitude, longitude, elevation
  - Relocation markers: durable but unobtrusive markers; optional additional edge stakes for long-term monitoring

- Field procedures: stringing, tagging, and measurement
  - Stringing: four-person team (compass, line cutter, distance measurer, line follower)
  - Tree tagging and measurement: tag all trees >50% root area inside plot; tag height typically 1.60 m (or 30 cm below POM if tagging at 1.6 m)
  - POM (Point of Measurement): standard height 1.3 m; record alternative POM if deformities or buttresses prevent 1.3 m measurement
  - Buttresses and deformities: adjust POM location when buttresses or deformities alter measurement baseline; record changes and apply consistent rules (e.g., measure 50 cm above buttress if needed)
  - Large buttress trees: often require two-person, dedicated measurement sessions; use ladders; photos as backup method if needed
  - Height measurement: measure tree height where possible; if not, record method (laser hypsometer, trigonometry, manual), and sample across size classes where feasible

- Measurement points and protocols
  - Trees:
    - Measure diameter at breast height (DBH) where possible at 1.3 m; use POM if 1.3 m is impractical
    - Record multiple stems (>10 cm DBH) in separate rows
    - Mark POM with paint; record bearing, distance, and all measurement details
    - Follow detailed rules for special cases (slopes, buttresses, resprouts, lianas, single/multi-stemmed trees)
  - Lianas:
    - Include if any part of the stem is within 2.5 m of ground and >10 cm diameter
    - Measure lianas at three points to enable long-term growth and recruitment analyses:
      1) d1.3length (130 cm from rooting point)
      2) d1.3height (130 cm above ground)
      3) dmax (widest point within 2.5 m of ground)
    - Tag lianas and record host tree interactions; define apparent genet if stems join underground
  - Subplot and plot metadata:
    - Record subplot coordinates, slope, soil texture, drainage
    - Plot-level metadata: latitude/longitude, elevation, boundary bearings, local landmarks
  - Tree height estimation and sampling:
    - When full height measurement is impractical, sample representative trees across size classes (10 trees per class in predefined DBH ranges) and measure height with laser hypsometer or trig methods; document method
  - Wood density (for biomass estimation):
    - Collect branch samples (10 cm long, ≥1.5 cm diameter); measure fresh and dry mass to compute density
  - Botanical collection:
    - Collect morphospecies that cannot be confidently identified in the field; press, label, and send to herbarium
    - Record collector initials and collection numbers; link to voucher specimens

- Data capture, formats, and processing
  - Data entry: structured Excel file per plot with three worksheets (trees, lianas, site) and separate sheets for Relaskop/digital camera observations
  - Coordinates and measurements: capture exact X/Y coordinates, tag IDs, species, diameters, POM, measurement method, bole form, and notes
  - Data upload and QC: upload to ForestPlots.net; apply standard quality-control procedures; document issues such as unlikely recruits, missing census data, or abnormal growth
  - Corrections and audit trail: retain original measurements; record presumed error and correction; ForestPlots.net supports tracking data manipulations
  - Optical-diameter correction: optical diameter measurements underestimate true diameter; apply a correction factor using a defined equation to adjust diameter estimates

- Mortality, recruitment, and liana interactions
  - Trees: record alive/dead status with coded alive-status flags and detailed mortality mode
  - Mortality codes: use a multi-category system (physical mechanism, number of trees affected in event, killer process)
  - Recruitment: tag and track new recruits; clearly mark unknown recruits for later collection
  - Lianas: record liana alive/dead status, mode of death, host interactions (which tree hosts the liana, and how the liana affects host mortality)

- Post-field data management and revisions
  - Post-field data management flags and codes: document retrospective modifications, extrapolations, interpolations, or corrections
  - POM changes for buttressed or irregular stems: apply documented field-change protocols with explicit field-notes
  - Recensus procedures: defined timelines and staffing for relocating plots, tagging recruits, and remeasuring
  - Data quality control: cross-checks for missing trees, remeasurements, and alignment with historical data; follow a consistent spatial sequence when recensuing

- Timing and staffing for field operations
  - New 1-ha plot: approximately 48 person-days (location, stringing, tagging, topography, botanical collection)
  - Remeasurement: approximately 13 person-days for a 1-ha plot
  - Additional time considerations: rain delays, rest breaks, and unforeseen circumstances

- Appendices and references
  - Appendices provide detailed field codes for alive status, mode of death, measurement techniques, and post-field data management
  - Reference materials encompass foundational works on tropical forest plot methods, structure–biomass relationships, and methodological corrections (e.g., optical diameter correction)

- Practical takeaways for Data Leaders
  - Prioritize standardization across plots and sites to enable robust cross-site comparisons and meta-analyses
  - Implement rigorous data governance: metadata, provenance, QC, and a transparent audit trail for all data manipulations
  - Leverage ForestPlots.net for centralized data storage, sharing, and quality control
  - Design data schemas and pipelines that accommodate complex measurement schemes (trees and lianas), POM changes, and diverse measurement techniques
  - Ensure documentation of measurement context, sampling timing, and site-specific logistical constraints to support reproducibility and future re-enumeration efforts