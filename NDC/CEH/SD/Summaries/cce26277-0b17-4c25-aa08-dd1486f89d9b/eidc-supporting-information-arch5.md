# Hydraulic mobility of aquatic insect (Trichoptera) bioconstructions and incorporated sediments

- Overview
  - A hydraulic flume study investigating how caddisfly case construction affects sediment transport in rivers.
  - Species studied: two tubular-case builders (Potamophylax latipennis; Sericostoma personatum) and one domed-case builder (Agapetus fuscipes).
  - Approach: compare bed shear stress required to move empty cases versus disaggregated sediment; 11 discharge steps in the flume; sediment erosion quantified from photographs.
  - Field/experimental timeline: caddisflies collected 17–18 June 2019 and 18 August 2019; flume experiments conducted 20 August–20 September 2019.
  - Lead: R. Mason, with co-authors assisting in data collection and interpretation.

- Data contents and structure
  - S1_Velocimetry_data
    - Post-processed acoustic Doppler velocimetry (ADV) outputs for each discharge step.
    - Key variables include mean velocities (U, V, W) and their raw and adjusted values, correlations, signal-to-noise ratios, turbulent kinetic energy (TKE), and bed shear stress (Tb).
    - Time-stamped by Date and Discharge_step (1–11).
  - S2_Case-grain-size-distribution_data
    - Grain size distributions for each caddisfly case derived from sieving.
    - Variables include Sample_ID (G/S/L with individual number), mass before/after sieving, mass lost, loss percentage, sieve size references (mm).
  - S3_Entrainment_data
    - Entrainment percentages during each flow stage, measured via photography of sediment on the measurement platform.
    - Variables include Sample_ID, State (Case or loose sediment), Discharge_step (1–11), and cumulative % area transported.
  - S4_Case-and-entrainment-threshold_data
    - Case characteristics (mass, axes a, b, c) and bed shear stress thresholds for entrainment (E_10) and general movement (E_90).
    - Variables cover Case/Sediment ID, State, Mass, a (long axis), b50 (intermediate axis / D50 for loose sediment), c (short axis), E_10, E_90, plus explanatory notes on units.

- Data collection, processing, and provenance
  - Experimental design: cases and sediments placed centrally in the flume; hydraulic force increased through 11 discharge steps; sediment loss and movement tracked via photographs.
  - Post-processing and quality indicators: S1 includes data quality metrics (SNR, correlation) alongside velocity and turbulence calculations.
  - Documentation: each dataset file includes variable-by-variable descriptions and units; S4 provides definitions and units for case dimensions and thresholds.

- Data quality and usability considerations
  - Standardized data structure across four related files facilitates reuse, cross-dataset linking (e.g., linking velocimetry with entrainment and grain-size data).
  - Clear variable definitions and units support comparability with other hydrodynamics and sediment-transport datasets.
  - Potential limitations to note: study-specific biological materials (three caddisfly taxa) and controlled flume conditions may affect generalizability to other systems; data capture relies on photographic estimates of movement and derived metrics (e.g., bed shear stress) that require careful interpretation.

- Governance, stewardship, and reuse considerations
  - Metadata richness supports discoverability and reuse (explicit variable names, units, and data provenance).
  - Alignment with data governance practices: standardized data formats, clear documentation of methods, and explicit thresholds and measurements aid data sharing and interoperability.
  - Considerations for data updates or extensions: potential to expand with additional species, different flow regimes, or in-field validation; ensure versioning and provenance tracking when integrating with broader river-ecology data holdings.
  - Anticipated challenges for data stewards: matching user needs to available data, integrating with diverse datasets and formats, and maintaining up-to-date metadata as methods or standards evolve.