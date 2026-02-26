# Data collection and analysis methods for nutrients and NO3 isotopes in English Lake District and Norfolk Broads

## Overview
- Describes sampling, laboratory analyses, isotopic measurements, quality control, and data structure for nutrients (NO2, NO3, NH4, SRP) and nitrate isotopes (d15N-NO3, d18O-NO3) in rivers and lakes.
- Study areas include streams and lakes in the English Lake District and the Norfolk Broads, with specific sampling approaches per habitat.

## Sampling methods
- Rivers in the English Lake District: sampled from road bridges, foot bridges, or riverbanks using a custom off-bridge sampler to collect water from well-mixed areas.
- Lakes/Broad surface waters: sampled by boat from pelagic areas in the upper 10–30 cm of the water column; if boats were not feasible, shoreside sampling from the shoreline 2–5 m offshore using the same off-bridge sampler.
- Rivers in the Norfolk Broads: all samples collected by boat from well-mixed areas of the flow.
- In-field measurements: water temperature, pH, and electrical conductivity (EC) measured on unfiltered samples immediately after collection using handheld meters.

## Sample processing and storage
- Filtration: samples for NO2, NO3, NH4, and SRP filtered in the field using 0.45 µm cellulose acetate syringe filters; NO3 isotope analysis filtered to 0.2 µm.
- Storage: all water samples kept on ice and returned to the laboratory; stored at 4°C in the dark, except NO3 isotope samples which are frozen at -20°C until analysis.
- Isotope sample prep: where NO2 exceeded 0.01 mg NO2-N/L, samples treated with sulfamic acid to remove interference prior to NO3 isotope analysis.

## Analytical methods
- Nutrients (NO2, NO3, NH4, SRP): analysed colorimetrically on an AQ2 Discrete Analyser (SEAL Analytical).
  - NO2: USEPA Method 353.2 (0.01–0.1 mg NO2-N/L).
  - NO3: reduction to NO2 with a copperized cadmium coil; range 0.012–2.0 mg NO3-N/L; NO3 concentration calculated as the difference between reduced and unreduced NO2 measurements.
  - NH4: USEPA Method 350.1 (0.02–1.0 mg NH4-N/L).
  - SRP: USEPA Method 365.1 (0.005–1.0 mg PO4-P/L).
- NO3 stable isotopes: denitrifier method (Sigman et al. 2001; Casciotti et al. 2002); isotopic composition measured at NEIF (UKCEH Lancaster) with Isoprime TraceGas preconcentrator and IRMS.
  - Interference management: if NO2 > 0.01 mg NO2-N/L, treated with sulfamic acid prior to analysis.
  - Nitrogen to N2O conversion: 10 or 20 nmol NO3 converted to N2O depending on concentration.

## Isotope analyses and QA
- Instruments and facilities: Isoprime TraceGas connected to an autosampler; isotope ratios measured at NEIF (UKCEH Lancaster, UK).
- Standards and calibration: calibrated against international standards (USGS-34, USGS-35, IAEA-NO-3).
- Replicates and precision: triplicate runs for standards, internal NO3 standard, and at least one environmental sample run in triplicate.
- Performance criteria: standard deviations of replicates 0.2‰ or better for d15N-NO3 and 0.5‰ or better for d18O-NO3.

## Data structure and units
- Parameters and units:
  - Temperature: degrees Celsius
  - pH: unitless
  - EC: micro siemens per centimeter (µS/cm) at 25°C
  - NO2, NO3, NH4: mg nitrogen per liter (mg N/L)
  - SRP: mg phosphorus per liter (mg PO4-P/L)
  - d15N_NO3: per mille (‰) relative to AIR-N2
  - d18O_NO3: per mille (‰) relative to VSMOW
- Data headers (13 columns):
  - Date_and_time
  - Sample_ID
  - Temperature
  - pH
  - EC
  - NO2
  - NO3
  - NH4
  - SRP
  - d15N_NO3
  - d18O_NO3
  - Latitude
  - Longitude

## Quality control and data management
- Field blanks included in each sampling visit to check for contamination.
- Calibrations against externally-certified reference standards.
- 10% of samples repeatedly analysed to assess precision.
- Datasets stored and uploaded to the appropriate data portals for dissemination and reuse.

## Particular challenges and opportunities for analysts
- Challenge: increasing the value of monitoring datasets by combining nutrient and isotope data with other relevant datasets to enable broader environmental insights.
- Challenge: enabling access to underlying data used to create final outputs, supporting transparency and reproducibility of monitoring and policy assessments.