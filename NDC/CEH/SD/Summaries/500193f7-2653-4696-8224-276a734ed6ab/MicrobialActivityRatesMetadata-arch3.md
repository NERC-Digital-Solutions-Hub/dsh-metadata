# Experimental Design and Laboratory Incubation Method

## Overview
- Describes sediment collection, incubation experiments, and analytical procedures to assess microbial activity and denitrification potential in Wood Brook, Staffordshire, UK (June 2015).

## Sampling Design and Sediment Preparation
- Depth: 0–10 cm within the streambed.
- Locations: two reaches (sandy mid-stream; gravel downstream).
- Replicates: five pseudo-replicates at each location.
- Handling: homogenised, sieved to 2 mm, stored cold within 36 hours of collection.

## Assays and Measurements

- Fluorescein diacetate (FDA) hydrolysis
  - Procedure: 1 g airdried sediment, 50 ml 1 M THAM, 0.5 ml FDA substrate; incubated 37 °C for 3 hours; acetone added to stop hydrolysis; filtered; absorbance read at 490 nm.
  - Output: rate of fluorescein production (mg fluorescein kg^-1 h^-1).

- Extracellular phenol oxidase activity
  - Procedure: 0.5 g dried sediment in 15 ml tubes with 3 ml deionised water; add 2 ml 10 mM L-DOPA; shake 30 minutes at 25 °C; centrifuge to terminate; filter; measure dopachrome at 475 nm.
  - Output: phenol oxidase activity (μmol dopachrome g^-1 h^-1).

- Denitrification potential
  - Setup: 10 g field-moist sediment in 100 ml bottles; dark/incubation conditions; substrates added (control, NO3, carbon, NO3+carbon).
  - Anoxic induction: bottles flushed with oxygen-free argon for 30 minutes; 10% headspace replaced with argon:acetylene (to inhibit N2 to N2O reduction).
  - Incubation: 22 °C with shaking; headspace gas sampled at 0, 3, 6 hours; analyzed for N2O.
  - Output: rate of potential denitrification (μg N2O-N g^-1 h^-1) for each treatment (control, nitrate, carbon, nitrate+carbon).

- Organic matter content
  - Method: loss on ignition (LOI) after drying; approximately 10 g dried sediment combusted at 550 °C for ≥3 hours.
  - Output: organic matter percentage.

- Moisture content
  - Method: field-moist sediment dried at 105 °C overnight; weight loss determined.
  - Output: moisture percentage.

- pH
  - Method: 5 g sediment with 5 ml deionised water, shaken 30 minutes, slurries allowed to settle; pH measured.

## Instrumentation and Calibration

- Instruments
  - Nitrous oxide: Agilent 7890A gas chromatograph with micro electron capture detector (μECD).
  - Fluorescein and dopachrome: Varian Cary UV-Vis spectrophotometer.
  - pH: HQ40d portable pH probe.

- Calibration
  - N2O GC-ECD: daily four-point calibration (0, 2, 4, 6 ppm N2O); occasional nitrogen blanks.
  - pH: standard buffers of pH 4.00 and 7.00.

## Data Structure and Units

- Recorded variables (dataset: MicrobialActivityRates)
  - Sediment_Type: sediment type used in incubations.
  - Sample_Number: replicate identifier.
  - Fluorescein: fluorescein production, mg kg^-1 h^-1.
  - Dopachrome: dopachrome production, μmol g^-1 h^-1.
  - N2O_control: N2O production in control, μg N2O-N g^-1 h^-1.
  - N2O_nitrate: N2O production in nitrate-spiked, μg N2O-N g^-1 h^-1.
  - N2O_carbon: N2O production in carbon-spiked, μg N2O-N g^-1 h^-1.
  - N2O_mixed: N2O production in nitrate+carbon-spiked, μg N2O-N g^-1 h^-1.
  - OM_Content: organic matter content, percent.
  - Moisture_Content: moisture content, percent.
  - pH: sediment pH.

- Notes
  - NAs indicate missed sampling events.

## Data Structure Details
- File: MicrobialActivityRates (CSV)
  - 11 columns as listed above.

## References
- Toberman, H. et al. 2008. Summer drought effects on soil and litter extracellular phenol oxidase activity. Soil Biology and Biochemistry. 40:1519-1532.
- Sgouridis, F. and Ullah, S. 2014. Denitrification potential in UK catchments. Environmental Science: Processes and Impacts. 16:1551-1562.