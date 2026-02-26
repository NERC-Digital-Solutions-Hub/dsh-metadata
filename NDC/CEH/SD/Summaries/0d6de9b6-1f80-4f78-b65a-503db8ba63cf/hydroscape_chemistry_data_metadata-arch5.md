# Data collection/generation methods

## Overview
- Describes sampling of streams and lakes in England’s Lake District and the Norfolk Broads for nutrient and isotope analyses.
- Includes field measurements of basic water quality parameters and laboratory analyses of nutrient species and stable nitrogen/oxygen isotopes in nitrate.

## Sampling and field measurements
- Water from streams/rivers collected via off-bridge samplers from well-mixed flow areas; lake/broad surface samples collected by boat from pelagic zones when possible.
- If boat sampling was not feasible, lakes sampled from the shore about 2–5 m from the shoreline; Norfolk Broads rivers sampled by boat as well.
- In-field measurements taken immediately on unfiltered samples: temperature, pH, and electrical conductivity using handheld probes/meters (WTW 3420 and WTW 340i).

## Sample processing and storage
- Field filtration of NO3, NO2, NH4, and SRP using 0.45 µm cellulose acetate syringe filters.
- NO3 isotope samples filtered in the field to 0.2 µm.
- All samples kept on ice during transport; stored at 4°C in the dark, except NO3 isotope samples which were frozen at -20°C until analysis.

## Laboratory analyses and isotopic measurements
- Nutrient concentrations measured colorimetrically with an AQ2 Discrete Analyser:
  - NO2 via USEPA method 353.2.
  - NO3 reduced to NO2 using copperised cadmium coil; nitrate concentration derived from difference with/without reduction.
  - NH4 via USEPA Method 350.1 (hypochlorite and salicylate method).
  - SRP via USEPA Method 365.1 (molybdate reaction with ascorbic acid reduction).
- NO3 dual isotope analysis (δ15N-NO3 and δ18O-NO3) using the denitrifier method:
  - If NO2 exceeded 0.01 mg NO2-N/L, treated with sulfamic acid to remove interference.
  - Depending on NO3 concentration, 10 or 20 nmol NO3 converted to N2O for isotopic analysis.
  - Isotopic composition measured on Isoprime TraceGas system at NEIF (UKCEH Lancaster, UK).

## Quality control and standards
- Field blanks (MilliQ water) collected at each visit; confirmed no contamination.
- External certified reference standards used to calibrate nutrient analyses.
- 10% of samples reanalyzed to assess precision.
- δ15N-NO3 calibrated with USGS-34 and IAEA-NO-3; δ18O-NO3 calibrated with USGS-34, USGS-35, and IAEA-NO-3 (USGS-35 avoided for δ15N due to 17O interference).
- All international standards run in triplicate, plus an internal NO3 standard; at least one environmental sample analyzed in triplicate.
- Reported precision: ≤0.2‰ for δ15N-NO3 and ≤0.5‰ for δ18O-NO3 in standard runs and sample replicates.

## Data structure and units
- Data headers include: Date_and_time, Sample_ID, N, W, Temperature, pH, EC, NO2, NO3, NH4, SRP, d15N_NO3, d18O_NO3, Latitude, Longitude.
- Units:
  - Temperature: °C
  - pH: unitless
  - EC: µS/cm at 25°C
  - NO2, NO3, NH4: mg N/L
  - SRP: mg P/L
  - d15N_NO3: per mille (‰) relative to AIR-N2
  - d18O_NO3: per mille (‰) relative to VSMOW
- Geographic coordinates provided as decimal degrees.

## Data provenance and storage considerations for Data Stewards
- Document sampling locations, dates, field measurements, filtration steps, storage conditions, and analytical methods (including instrument models and standard methods) to ensure traceability.
- Capture isotopic treatment steps (e.g., sulfamic acid addition) and decision points (e.g., when NO2 is high) for reproducibility.
- Maintain clear versioning and metadata for units, calibration standards, and QA results (blanks, replicates, standards).

## Challenges and considerations for data stewardship
- Incomplete visibility into certain column meanings (e.g., N and W fields) requiring clear metadata definitions.
- Timely data collection across multiple sites and ensuring consistent adherence to sample handling and storage protocols.
- Ensuring interoperability across systems/formats when integrating field and lab data.
- Managing large isotope datasets and maintaining traceability of all calibration and QC steps.