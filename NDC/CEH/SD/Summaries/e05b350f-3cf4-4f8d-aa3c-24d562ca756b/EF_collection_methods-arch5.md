# Vegetation work and Greenhouse gas flux

- Objective of data collection: quantify vegetation structure and diversity, biomass, and greenhouse gas fluxes (CO2, CH4, N2O) to support ecosystem function analyses.

- Data scope
  - Vegetation metrics: species cover, species richness, grass/forb cover, biomass, and overall diversity (Shannon's index).
  - Greenhouse gas metrics: net ecosystem CO2 exchange, CO2 influx/efflux, photosynthesis, respiration; CH4, CO2, and N2O concentrations.

- Data collection methods
  - Vegetation
    - Four 50 cm x 50 cm quadrats placed randomly at the site.
    - Visual estimation of percentage cover for each species.
    - Species richness and percentage cover of grasses/forbs summed across quadrats.
    - Biomass collected by clipping at ground level from each quadrat, dried at 80°C for 24 hours, weighed; sums calculated per site (g biomass per m^2).
    - Shannon's Diversity index calculated (Shannon & Weaver, 1963).
  - Greenhouse gas flux
    - Net ecosystem CO2 exchange, photosynthesis, and respiration measured using four plastic collars (25 cm diameter) with transparent chambers attached to an IRGA (EGM-4 IRGA).
    - CO2 influx measured over two minutes; a reflective cover placed over the chamber to obtain CO2 efflux in the dark.
    - Concurrent measurements: soil moisture and temperature (WET sensor), and PAR (photons) in triplicate.
    - Gas concentration measurements converted from 27 CO2 readings (ppm) over two minutes to CO2 flux (mg CO2 m^-2 h^-1).
    - Methane (CH4), CO2, and N2O
      - Chambers with reflective cover used; 9 mL air sampled at 0, 10, 20, and 30 minutes.
      - Gas analysis performed with a Gas Chromatograph (Agilent 7890B).
      - Final gas flux values calculated using the same approach as for IRGA-derived CO2 flux.

- Data processing and calculations
  - CO2 flux derived from chamber measurements, accounting for chamber volume, area, and time.
  - CO2 flux expressed as mg CO2 m^-2 h^-1.
  - For CH4, CO2, and N2O, concentration changes over the sampling interval used to calculate fluxes following the IRGA method.

- Metadata and references
  - Reference for diversity metric: Shannon, C.E. and Weaver, W. (1963) The Mathematical Theory of Communication.
  - Specific formulas and parameter definitions (e.g., time variables, atomic masses, gas constants) are provided for CO2 flux calculations.

- Data management and governance considerations for data stewards
  - Standardization of data formats: clearly labeled fields for quadrat IDs, site coordinates, date/time, species codes, cover percentages, biomass, and derived flux values.
  - Metadata requirements: instrument models (IRGA, PAR sensor, moisture/temperature sensors, GC), sampling cadence (timing of measurements), calibration notes, and any data transformations.
  - Units and scaling: ensure consistency (e.g., percent cover, g biomass m^-2, mg CO2 m^-2 h^-1, ppm for gas concentrations).
  - Provenance and reproducibility: store raw measurements (ppm, time stamps) separately from processed flux values; include data processing scripts or parameter settings (e.g., formulas used, Excel forecast steps).
  - Data quality considerations: triplicate measurements for moisture and PAR, documentation of any data exclusions or anomalies, handling of incomplete measurements (e.g., partial time series).
  - Data sharing and interoperability: describe data lineage and context so datasets can be discovered and reused by others; plan for linking vegetation data with gas flux measurements where relevant.
  - Access controls and embargoes: note any restricted data arising from site sensitivity or collaboration agreements.

- Practical notes
  - Instruments and setup details (collar design, chamber dimensions, IRGA model) to support replication.
  - Timing and environmental covariates collected concurrently to support interpretation of flux data.