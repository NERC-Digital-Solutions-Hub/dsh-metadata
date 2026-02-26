# Experimental Design and Laboratory Incubation Method

- Study context and sampling
  - Sediment collected from 0–10 cm depth in Wood Brook, Staffordshire, UK, June 2015.
  - Two locations: a sandy mid-stream reach and a gravel downstream reach.
  - Five pseudo-replicates per location; samples homogenised, sieved to 2 mm, and stored cold within 36 hours.

- Fluorescein diacetate (FDA) hydrolysis assay
  - Procedure: 1 g airdried sediment in 125 ml flasks with 50 ml 1 M THAM buffer and 0.5 ml FDA substrate; include blanks and a no-substrate control.
  - Incubation: 37 °C for 3 h; stop reaction with acetone; filter and measure absorbance at 490 nm.
  - Output: rate of fluorescein production (mg fluorescein kg−1 h−1).

- Extracellular phenol oxidase activity
  - Procedure: 0.5 g dried sediment in tubes with 3 ml deionised water; add 2 ml 10 mM L-DOPA; shake 30 min at 25 °C; terminate by centrifugation.
  - Measurement: dopachrome colorimetric product at 475 nm.
  - Output: phenol oxidase activity (μmol dopachrome g−1 h−1).

- Denitrification potential assays
  - Setup: 10 g field-moist sediment in 100 ml serum bottles; create dark, anoxic conditions; add 20 ml of appropriate stock solution (control, nitrate, carbon, or nitrate+carbon).
  - Substrates for treatments: nitrate (NO3), carbon (glucose equivalent), or both.
  - Anoxic induction: flush headspace with argon; replace 10% with acetylene to inhibit N2O reduction to N2.
  - Incubation: 22 °C, 400 rpm; headspace gas sampling at 0, 3, and 6 h with subsequent analysis.
  - Output: potential N2O production under each condition (μg N2O-N g−1 h−1).

- Organic matter, moisture, and pH analyses
  - Organic matter: loss on ignition by combusting dried, ground samples at 550 °C for ≥3 h.
  - Moisture: drying field-moist sediment at 105 °C; calculate moisture content from mass loss.
  - pH: slurry of 5 g sediment in 5 ml deionised water; shake and measure slurry pH after settling.

- Laboratory instrumentation
  - Nitrous oxide: Agilent 7890A GC with micro electron capture detector (ECD); splitless 1 ml loop; N2O elutes at ~7 min.
  - Fluorescein and dopachrome: Varian Cary UV-Vis spectrophotometer; readings at 490 nm and 475 nm respectively.
  - pH: HQ40d portable pH probe.

- Calibration and quality control
  - GC-ECD calibration: four-point standards (0, 2, 4, 6 ppm N2O) and periodic pure nitrogen blanks.
  - pH probe: calibration with buffers at pH 4.00 and 7.00.

- Data collected and units
  - Fluorescein production: mg fluorescein kg−1 h−1.
  - Dopachrome production: μmol dopachrome g−1 h−1.
  - Denitrification potential: μg N2O-N g−1 h−1 for control, nitrate-spiked, carbon-spiked, and nitrate–carbon-spiked incubations.
  - Organic matter content: percent.
  - Moisture content: percent.
  - pH: unitless (pH).

- Data structure and dataset details
  - Single CSV file named MicrobialActivityRates.
  - 11 columns: Sediment_Type, Sample_Number, Fluorescein, Dopachrome, N2O_control, N2O_nitrate, N2O_carbon, N2O_mixed, OM_Content, Moisture_Content, pH.
  - Notes: NAs result from missed sampling during the experiment.

- References for methods
  - Toberman et al. 2008 for extracellular phenol oxidase activity.
  - Sgouridis & Ullah 2014 for denitrification potential methodology.