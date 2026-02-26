# Experimental Design and Laboratory Incubation Method

- Purpose and scope
  - Describes sediment collection, preparation, and incubation protocols to measure microbial activity, enzyme activity, denitrification potential, and basic sediment properties in Wood Brook, Staffordshire, UK.

- Study design and sampling
  - Sediment collected from 0–10 cm depth in June 2015 using a 5 cm AMS slide hammer.
  - Two locations: a sandy mid-stream reach and a gravel downstream reach.
  - Five pseudo-replicates per location; samples homogenised, sieved to 2 mm, stored cold within 36 hours.

- Assays and measurements
  - FDA hydrolysis (extracellular hydrolase activity)
    - Procedure: 1 g airdried sediment in flasks with 50 ml 1 M THAM buffer and FDA substrate; incubated at 37 °C for 3 h; stop with acetone; measure absorbance at 490 nm.
    - Output: rate of mg fluorescein kg-1 h-1.
  - Extracellular phenol oxidase activity
    - Procedure: 0.5 g dried sediment in water; add 2 ml 10 mM L-DOPA; shake, incubate 25 °C; terminate with centrifugation; measure dopachrome at 475 nm.
    - Output: rate in μmol dopachrome g-1 h-1.
  - Denitrification potential
    - Procedure: 10 g field-moist sediment in serum bottles; create anoxic conditions; apply substrates (control, nitrate, carbon, nitrate+carbon); flush headspace with argon; add acetylene to inhibit N2O reduction; incubate at 22 °C with shaking; sample headspace at 0, 3, 6 h.
    - Output: N2O production rates under each condition (μg N2O-N g-1 h-1).
  - Organic matter and moisture
    - Organic matter: loss on ignition at 550 °C for ≥3 h.
    - Moisture content: dry sediment at 105 °C and weigh loss.
  - pH
    - Slurry of 5 g sediment with 5 ml deionised water; shake and settle; measure pH after settling.

- Instrumentation and calibration
  - Nitrous oxide: GC with micro electron capture detector (Agilent 7890A), splitless 1 ml loop, 60 °C oven, 350 °C ECD; 9 min run; N2O elutes at 7 min.
  - Fluorescein and dopachrome: UV-Vis spectrophotometer (Varian Cary).
  - pH: portable HQ40d pH probe.
  - Calibration: N2O GC calibrated daily with zero and 2, 4, 6 ppm standards; pH probe calibrated with pH 4.00 and 7.00 buffers; occasional nitrogen blank runs.

- Data structure and units
  - File: MicrobialActivityRates.csv
  - Columns:
    - Sediment_Type
    - Sample_Number
    - Fluorescein (mg fluorescein kg-1 h-1)
    - Dopachrome (μmol dopachrome g-1 h-1)
    - N2O_control (μg N2O-N g-1 h-1)
    - N2O_nitrate (μg N2O-N g-1 h-1)
    - N2O_carbon (μg N2O-N g-1 h-1)
    - N2O_mixed (μg N2O-N g-1 h-1)
    - OM_Content (%)
    - Moisture_Content (%)
    - pH
  - Note: NAs reflect missed sampling events.

- Analytical methods (summary)
  - N2O concentrations via GC-ECD; fluorescein and dopachrome via UV-Vis; pH via standard probe.
  - Specific parameters and run conditions provided for reproducibility.

- Context and references
  - Related methods cited: Toberman et al. 2008 (extracellular phenol oxidase/soil processes) and Sgouridis & Ullah 2014 (denitrification potential in UK catchments).

- Relevance to environmental monitoring
  - Provides standardized, reproducible measurements of microbial enzyme activity, denitrification potential, and basic sediment properties to support evaluation of environmental health and policy performance over time. Data are structured for integration into monitoring datasets and cross-site analyses, with explicit quality controls (calibration, blanks, replicates).