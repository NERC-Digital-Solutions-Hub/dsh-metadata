# Physical and chemical properties of wildfire ash collected from different ecosystems and burn severities across the globe, 2003-2021

## What this dataset is
- Global dataset characterising chemical and physical properties of wildfire ash across multiple ecosystems and burn severities.
- Two data files: ash_chemical_properties.csv (chemical characteristics) and ash_physical_properties.csv (physical characteristics).

## Sampling scope and provenance
- Timeframe: ash samples collected 2003–2021; laboratory analyses conducted 2003–2022.
- Locations: sampling sites include Madre del Agua (Tenerife, Spain), Thompson reservoir (Victoria, Australia), Higher Swineshaw reservoir (Manchester, UK), Mesa Fire (Idaho, USA); country field identifies sampling locations.
- Lead researchers/institution: Swansea University, Swansea (UK); contributors include Dr Jonay Neris Tome, Dr Carmen Sánchez-García, Dr Cristina Santín, and Prof. Stefan Doerr.

## What is included in the data

### Chemical characteristics (ash_chemical_properties.csv)
- Key fields: Country, site name, year, burn severity, material type, sample name; δ13C (‰); total concentrations of C, CO3, N; total mg/kg for P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb, Cr, Co, Br, Sr; total µg/kg for Hg, As, Cd; pH; electrical conductivity (EC; µS cm-1); UV 250 (%T); dissolved concentrations (mg/kg) of organic C (DOC), NH4+, NO3-, Cl-, SO4-, F-, P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb, B; dissolved Hg, As, Cd (µg/kg).
- Completeness: Chemical characteristics dataset is not complete for every parameter on every sample (some parameters not analysed for certain ash samples).

### Physical characteristics (ash_physical_properties.csv)
- Key fields: Country, site name, year, burn severity, sample name; WR_33kPa (water retention at 33 kPa); WR_1500kPa (water retention at 1500 kPa); particle density (g cm-3); WDPT (water drop penetration time) class across 10 categories (WDPT_1 to WDPT_10).

## How the data were collected and analyzed (Methods)

### General approach
- Laboratory analyses were performed on wildfire ash samples to characterize chemical and physical properties, following standardized protocols described in detail below.

### Chemical analyses: general workflow
- Digestion for total analysis (As, Ca, Br, Mg, Al, Cd, Co, Cr, Cu, Fe, Mn, Ni, Pb, Sr, Zn, Na, etc.) following EPA 3051 (alternative): 0.25 g ash, 8 mL HNO3, 1 mL HCl; 200°C for 45 minutes; diluted to 50 mL.
- Leachate experiments: 4.0 g sample in 100 mL DI water; shake 5 minutes, stand 10 minutes; filter (0.45 µm) and analyze sub-samples for specific parameters; some sub-samples acidified for AA analysis.
- Carbonates (CO3): Bernard Calcimeter with ISO 10693:1995 calibration using CaCO3 standards.
- UV index: Measured as UV transmittance at 254 nm (%T) via spectrophotometry.
- DOC: Colorimetric method (Hue & Liu 1995) with digestion using K2Cr2O7/H2SO4 and reading at 590 nm.
- P & PO4: Ascorbic acid method with mixed reagent and reducing solution; measured at ~880 nm.
- Anions and cations: Cl-, NO3-, SO4-, F-, Na, etc., via Liquid Ion Chromatography or related methods.
- %C and %N: Elemental analysis (combustion) using LECO TruSpec CHN.
- Individual trace elements (As, Ca, Br, Mg, Al, Cd, Co, Cr, Cu, Fe, Mn, Ni, Pb, Sr, Zn, Na): via leachate and total digestion followed by Atomic Absorption Spectrometry (AAS) or equivalent (PerkinElmer PinAAcle 500) for specific elements; Hg via EPA 7473 Thermal Decomposition, Amalgamation and AAS (DMA-80).

### Physical analyses: general workflow
- Bulk density: oven-dried core sample (105°C) by weight for a core with known volume.
- Water retention capacity: field capacity (33 kPa) and permanent wilting point (1500 kPa) using Richards pressure plates.
- Particle density: pycnometer with deionized water at several time steps to monitor density changes.
- WDPT (water repellency): standard WDPT test with 5 water drops to determine infiltration time, categorized into WDPT classes.

## Replication, completeness, and quality notes
- Replication: chemical characteristics typically include 2–20 replicates per site and treatment; physical characteristics include 4 replicates per site and treatment.
- Completeness caveat: chemical parameters may be missing for some samples; physical dataset is complete for the measured variables.
- Observations: 296 wildfire ash chemical samples; 36 wildfire ash physical samples.

## Data provenance and usage considerations
- Authorship and analytical provenance are documented, with standard references for methods used (e.g., Klute, Doerr, Blake & Hartge, EPA guidelines).
- The dataset enables cross-ecosystem comparisons of ash chemistry and physical properties, supports understanding of ash behavior post-fire, and can feed into modeling or data products for end users to explore self-serve.
- Users should account for missing data in certain chemical parameters and the varying number of replicates across sites.

## Practical applications and outputs
- Potential outputs include dashboards, pivot tables, or reports enabling exploration of ash composition and physical behavior by country, site, burn severity, or time.
- Outputs can inform environmental risk assessments, soil and water interactions after wildfires, and policy or management decisions related to wildfire impacts.