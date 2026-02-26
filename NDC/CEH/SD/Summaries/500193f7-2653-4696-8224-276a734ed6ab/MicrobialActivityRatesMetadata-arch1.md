# Experimental Design and Laboratory Incubation Method

- Study objective: quantify microbial activity indicators and denitrification potential in streambed sediments to understand biogeochemical processes and potential limiting factors.
- Sampling context: Wood Brook, Staffordshire, UK; collected in June 2015 from 0–10 cm depth at five pseudo-replicates across two locations (sandy mid-stream reach and gravel downstream reach); samples homogenised, sieved to 2 mm, stored cold within 36 hours.

- Assays and measurements
  - FDA hydrolysis (extracellular enzyme activity)
    - Procedure: 1 g airdried sediment in 125 ml flasks with 50 ml 1 M THAM buffer and 0.5 ml FDA substrate; incubated 37 °C for 3 h; stop reaction with acetone; absorbance read at 490 nm.
    - Controls: blank (buffer + substrate, no sediment) and a no-FDA control.
    - Output: fluorescein production (mg fluorescein kg-1 h-1).
  - Extracellular phenol oxidase activity
    - Procedure: 0.5 g dried sediment in four tubes (three replicates + one non-substrate control) with 3 ml water and 2 ml 10 mM L-DOPA; shake 30 min at 25 °C; centrifuge to terminate; measure dopachrome at 475 nm.
    - Output: phenol oxidase activity (µmol dopachrome g-1 h-1).
  - Denitrification potential
    - Setup: 10 g field-moist sediment in 100 ml bottles; dark conditions; substrates added (control, nitrate, carbon, nitrate+carbon) as appropriate; flush headspace with argon for anoxic conditions; replace 10% headspace with argon:acetylene to inhibit N2O reduction to N2.
    - Incubation: 22 °C, shaker at 400 rpm.
    - Sampling: headspace gas at 0, 3, and 6 h; analyze N2O in exetainers.
    - Purpose: determine if denitrification is limited by nitrate, carbon, or both.
    - Output: potential N2O production rates under each condition (µg N2O-N g-1 h-1).
  - Organic matter and moisture content
    - Organic matter: loss on ignition (crushed dried sediment, 550 °C for ≥3 h).
    - Moisture content: drying field-moist sediment at 105 °C and reweighing.
  - pH
    - Method: 5 g sediment in 5 ml deionised water, slurry, settle 40 min; measure pH with a portable probe.

- Instrumentation and calibration
  - Nitrous oxide: Agilent 7890A GC with micro-ECD; splitless entry (1 ml loop), oven 60 °C, ECD 350 °C; argon/methane make-up at 2 ml min-1; 9 min run; N2O elutes at 7 min.
  - Fluorescein and dopachrome: UV-Vis spectrophotometer (490 nm for fluorescein, 475 nm for dopachrome).
  - pH: portable pH probe.
  - Calibration: daily four-point N2O calibration (0, 2, 4, 6 ppm) with nitrogen blanks; pH calibrated with buffers pH 4.00 and 7.00.

- Data structure and reporting
  - Data file: MicrobialActivityRates (CSV) with 11 columns:
    - Sediment_Type, Sample_Number
    - Fluorescein (mg kg-1 h-1)
    - Dopachrome (µmol g-1 h-1)
    - N2O_control (µg N2O-N g-1 h-1)
    - N2O_nitrate (µg N2O-N g-1 h-1)
    - N2O_carbon (µg N2O-N g-1 h-1)
    - N2O_mixed (µg N2O-N g-1 h-1)
    - OM_Content (%)
    - Moisture_Content (%)
    - pH
  - Note: NAs indicate missed sampling events during the experiment.
  - Replication: three replicates per treatment for denitrification with a non-substrate control; multiple sites and horizons included.

- Key references
  - Toberman et al., 2008. Summer drought effects on soil and litter extracellular phenol oxidase and soluble carbon release.
  - Sgouridis & Ullah, 2014. Denitrification potential in UK catchments.

- Data considerations for analysts
  - Multi-parameter dataset linking enzymatic activity (FDA, phenol oxidase), denitrification potential under varied substrates, and basic sediment properties (OM, moisture, pH).
  - Careful handling of missing data (NAs) and alignment of sampling times and treatments across replicates and locations.
  - Potential for cross-dataset analyses to correlate enzyme activities with denitrification potential and organic matter content.