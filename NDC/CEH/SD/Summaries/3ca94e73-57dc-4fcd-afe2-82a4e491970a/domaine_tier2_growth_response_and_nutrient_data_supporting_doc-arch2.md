# DOMAINE_Tier2_growthresponse_nutrients.csv

## Overview
- Purpose: Use bioassay experiments to assess how river phytoplankton growth responds to inorganic and organic nutrient additions, and how these responses relate to in situ nutrient concentrations.
- Main outputs: Calculated growth responses to various nutrient additions (inorganic and organic) expressed as natural log response ratios; comparisons to background nutrient data collected concurrently.

## Data content and structure
- Growth response variables (example names):
  - RP: Growth response to sodium phosphate
  - RN: Growth response to ammonium nitrate
  - RNP: Growth response to sodium phosphate and ammonium nitrate
  - RON1–RON4: Growth responses to four organic N additions (urea, glycine, glutamic acid, etc.)
  - ROP1–ROP4: Growth responses to four organic P additions (glucose-6-phosphate, phytic acid, etc.)
  - TON..mg.N.l.1., Ammonia..mg.N.l.1., TN..mg.N.l.1., SRP..mg.P.l.1., TP..mg.P.l.1., DOC..mg.C.l.1., etc.: Corresponding water chemistry measurements
  - DONTNratio, DOPTPratio: Ratios of dissolved organic N/P to total N/P
  - RONav, ROPav: Average growth responses for all dissolved organic N and P compounds
- Units: Natural log response ratio for growth metrics; nutrient concentrations in mg N L-1 or mg P L-1; ratios are 0–1 for specific metrics.
- Data file: DOMAINE_Tier2_growthresponse_nutrients.csv

## Spatial coverage
- Sites include: Ashop, Black Burn, Brocky Burn, Coln, Cottage Hill, Deepford Brook, Dickler, Dove, East Dart, Enbourne, Frome, Goredale Beck, Lambourne, N. Teign, Newby Beck, Piddle, Pow Beck, Sherbourne, Tarn Beck, Taw, Tippets Brook, Upper Chew, Windrush, Yeo
- Location details: Each site with northings/eastings and OS grid references (OSGB 1936)

## Temporal coverage
- Sampling period: 01 September 2017 to 31 October 2017
- Frequency: One sampling date per site

## Collection, transformation, and measurement methods
- Bioassay design (based on Mackay et al. and Maberly et al.):
  - Raw water collected at each site, stored at 4°C in the dark, transported within 48 hours
  - Acclimation in a constant-temperature room at 20°C
  - 12 nutrient treatments in triplicate: control (no additions), inorganic N only, inorganic P only, inorganic N and P, four organic N additions, four organic P additions
  - Incubation: 14 days, 20°C, light cycle 18 h light / 6 h dark with 80–120 µmol m-2 s-1
  - Growth response measured as chlorophyll a change, assessed via filtering, extraction, and spectrophotometric measurement
  - Growth response quantified as natural log response ratio relative to the appropriate control
- Water chemistry measurements:
  - Instrument: Skalar ++ autoanalyzer
  - Analytes: TN, TP, TDN, TDP (unfiltered and filtered samples after persulphate digestion), DIN (including NH3/NH4), SRP, DON, DOP, and DOC
  - Calculations: DON = TDN − DIN; DOP = TDP − SRP
- Data management:
  - Missing values denoted as NA
  - File naming and variable documentation align with DOMAINE project conventions

## Data quality and provenance
- Data are linked to established coastal/river nutrient methodologies and chlorophyll-based growth indicators
- References for methods and analyses provided (Elser et al. 2007; Maberly et al. 2002; Mackay et al. 2020; Ritchie 2008; Talling 1974; Yates et al. 2019, 2022)

## Relevance for environmental monitoring and policy
- Enables assessment of how dissolved organic and inorganic nutrients drive phytoplankton growth in rivers
- Supports understanding of nutrient limitation and uptake dynamics, informing nutrient management and water quality assessments
- Data can be combined with other monitoring datasets to enhance interpretation of environmental health and ecosystem responses to nutrient regimes

## Accessibility and data value
- Data are provided in a machine-readable CSV format with clearly described variables and units
- Potential for linkage with underlying water chemistry and site metadata to enable cross-dataset analyses
- Aligns with the archetype’s aim to store, standardize, and present monitoring outputs for scrutiny over time