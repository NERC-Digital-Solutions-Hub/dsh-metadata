# Fieldwork Protocol

- Purpose: Document the multidisciplinary methods used to collect and analyze water and porewater samples to monitor environmental health and biogeochemical processes in stream reaches.

## Field Sampling and Sample Handling

- Sample types and locations:
  - Surface water and multilevel piezometers at 10 cm and 20 cm depths.
  - DET (diffusive equilibrium in thin-film) gels deployed alongside the piezometers in upstream and mid-stream sandy reaches, placed at least 72 hours prior to sampling.
- Immediate measurements in the field:
  - Dissolved oxygen (DO) and temperature measured on site using YSI ProODO or EcoSense ODO200 instruments.
- Sample processing:
  - Water samples filtered sequentially (0.45 μm then 0.22 μm) and frozen.
  - DET gels sliced in situ into 2.5 cm intervals within 25 minutes; gels stored cold until lab equilibration.
  - Porewater gas samples produced via headspace equilibrium by injecting 7 mL water and 14 mL helium into a syringe, shaking, and capturing headspace into pre-evacuated exetainers.
- Isotope and gas sampling:
  - Isotopic analysis of δ15NNO3+NO2 and δ18ONOO3+NO2 performed using denitrifier method followed by IRMS.
  - δ13CCO2 analysis performed with preconcentration and isotope ratio mass spectrometry.

## Laboratory Instrumentation and Analyses

- Nutrients and carbon:
  - Continuous flow analyser (Skalar San++) for NH4+, NO3−, and NO2−.
  - Shimadzu TOC-L CPH with autosampler for DOC.
- Greenhouse gases:
  - GC with micro-ECD for N2O, FID for CH4, TCD for CO2.
  - Headspace concentrations converted to porewater using Henry’s constant.
- Isotopes:
  - GEO 20:20 GC-IRMS for δ15NNO3+NO2− and δ18ONO3+NO2−.
  - IRMS (Isoprime, Elementar UK) for δ13CCO2.
- DET gel analyses:
  - 5 mL ultrapure water used to elute solutes from gel slices; eluates analyzed for nutrients and isotopes as above.

## Calibration, Standards, and Quality Control

- GC-ECD and GC-FID/TCD calibrations:
  - Daily multi-point calibrations with zero and standard gases; periodic checks to correct for drift.
  - Reported accuracies and limits of detection (e.g., N2O: accuracy ~0.1–0.2 ppm, LOD ~5.6e-3 ppm; CH4: accuracy ~35 ppm, LOD ~0.5 μg/L).
- Skalar San++ (nutrients) calibration:
  - Ten standards (0.02–5 mg N/L) used; external references for NH4+, NO3−, NO2− to assess performance; typical accuracies and precisions in the 0.02–0.05 mg L−1 range.
- TOC calibration:
  - Daily curves for low, medium, high methods; accuracy ~0.16 mg L−1, precision ~±0.45 mg L−1 at a 15 mg L−1 standard; LOD ~0.5 mg L−1.
- Isotope analysis calibration:
  - GEO 20:20 calibrated with USGS 34/35 and IAEA NO3−; in-house reference standards for long-term precision (±0.3 to ±0.4 ‰ depending on isotope).
  - CO2 isotope standard calibrated against NIST standard (precision ≥ ±0.12 ‰).
- Instrumentation calibration notes:
  - DO and temperature calibrated with factory settings and 100% air saturation in moist air.

## Data Structure and Recorded Values

- Two CSV datasets:
  - In-situ_carbon_and_nitrogen_data (27 columns): includes Piezo_ID, Depth, Sediment_Type, Season, Reach, Dissolved_Oxygen, Temperature, CO2, CH4, N2O, NH4, NO3, NO2, DOC, d15N_NO3+NO2, d18O_NO3+NO2, d13CCO2, and associated error terms.
  - In-situ_DET_gel_data (11 columns): includes Gel_ID, Depth, Season, NH4, NO3, d15N_NO3+NO2, d18O_NO3+NO2, d13C_NO3+NO2, with corresponding errors.
- Data notes:
  - Not all samples contained enough nitrate for isotope analysis; missing values marked NA.
  - Negative pressure scenarios during piezometer sampling could prevent gas collection, yielding missing gas data.
- Units of recorded values:
  - Temperature: degrees Celsius; DO: mg L−1; NH4/NO3/NO2: mg N L−1; DOC: mg C L−1; CO2/CH4/N2O: mg L−1 or μg L−1 as specified; isotopes (d15N, d18O, d13C): per mil (‰).

## Practical Considerations for Analysis

- Data outputs likely used to assess environmental health by integrating water chemistry, greenhouse gas fluxes, and stable isotope signatures.
- Headspace to porewater conversion via Henry’s constant enables comparison across sample types.
- The standardized workflow supports comparability over time and across monitoring sites, aligning with environmental monitoring aims.

## References and Methodological Foundations

- Key methodological references for isotopic analysis and denitrifier method:
  - Antweiler et al. 1996; Casciotti et al. 2002; Kaiser et al. 2007; Sigman et al. 2001; Wilhelm et al. 1977.
- Calibration and analytical technique references underpin QA/QC and data reliability.