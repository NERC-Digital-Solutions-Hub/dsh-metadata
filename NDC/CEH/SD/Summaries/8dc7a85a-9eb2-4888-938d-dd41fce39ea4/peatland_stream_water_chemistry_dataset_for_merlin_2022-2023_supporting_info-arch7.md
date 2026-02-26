# Data Overview

- The MERLIN project aims to upscale and transform freshwater ecosystem restoration across Europe by creating a replicable framework for nature-based solutions. This dataset covers the first two years of water quality data from Hare Moss (peatland in the Forth catchment), implementing a control–intervention approach to characterise baseline conditions before restoration.

## Study area and sampling design

- Monitoring sites (initial setup and changes)
  - Black Burn (AUCH) – control location near restoration area
  - Hare Burn (HARE) – initial Hare Burn site; later discontinued (Aug 2022)
  - Hare Burn Upstream (HARE US) – added May 2022
  - Hare Burn Downstream (HARE DS) – added May 2022
- Spatial details
  - Hare Burn and Black Burn locations are in close proximity to the planned restoration area
  - Grid reference for the sampling locations: NT 21245 56644
  - Table 1 provides site codes, names, and coordinates
- Temporal sampling
  - Fortnightly sampling from December 2021 to May 2022
  - In May 2022, two additional sites were added (Upstream and Downstream)
  - In August 2022 the original Hare Burn site was discontinued; monitoring continued at three sites (HARE US, HARE DS, AUCH)
- Notable site context
  - Hare Burn is influenced by intensive peat extraction upstream, contributing to bank erosion and sand deposition observed during the study

## Data collected and key variables

- In-field physicochemical measurements
  - pH, pH temperature, dissolved oxygen (DO) and DO temperature, DO percentage, conductivity and conductivity temperature
  - Temperature ( Temp_av = average of three probe readings)
  - Additional DOC/TdN-related measurements (see below)
- Laboratory analyses (water chemistry)
  - Dissolved organic carbon (DOC) and total dissolved nitrogen (TdN); carbon-to-nitrogen ratio (C_N); absorbance at 254 nm (Abs_at_254) and SUVA (specific UV absorbance)
  - Particulate organic carbon (POC) via LOI method
  - Total phosphorus (TP) and soluble reactive phosphorus (SRP)
  - Dissolved methane (CH4_C), dissolved carbon dioxide (CO2_C), dissolved nitrous oxide (N2O_N)
- Greenhouse gas concentrations
  - Dissolved GHGs measured using gas chromatography with appropriate detectors; results converted to µg/L using Henry’s law

## Sampling, storage, and analysis methods

- In-field sampling and handling
  - Samples collected mid-stream using rinsed syringes and filtered where required
  - Specific bottle types and filtration steps outlined for TP, SRP, DOC/TdN, and POC
  - Headspace method used for dissolved greenhouse gases; duplicate sampling
  - Field measurements conducted with HACH HQ4300 multimeter and calibrated probes
- Sample storage
  - TP, SRP, and spare filtered samples frozen at -18°C for batch analysis
  - DOC and POC stored at 4°C and analyzed within a week
  - GHG samples stored at room temperature until analysis
- Laboratory analyses
  - DOC/TdN: Shimadzu TOC-LCPH with NPOC/TDN method; quality controls with standards and blanks
  - UV/Vis SUVA: PerkinElmer UV/Vis Lambda 365; absorbance from 230–800 nm; SUVA 254 calculated
  - POC: pre-combusted GF/F filters; LOI-based conversion to POC (0.58)
  - TP/SRP: SEAL AQ2 discrete analyser with acid digestion and colorimetric determination
  - GHGs: GC with μECD (N2O) and FID (CH4/CO2); calibration with mixed standards
- Data structure and units
  - Recorded values span field measurements and laboratory results
  - Columns cover site metadata, date/time, pH, DO, temperature, conductivity, DOC, TdN, C_N, Abs_at_254, SUVA, TP, SRP, CH4_C, CO2_C, N2O_N, POC
  - Units and descriptions are detailed in Table 3 (e.g., Date in dd/mm/yy, Time in hh:mm, pH unitless, DO mg/L, Conductivity µS/cm, etc.)

## Data quality, completeness, and exclusions

- Data completeness
  - Field instrument or laboratory analyzer failures caused missed observations or results
  - Table 4 lists data exclusions with dates, site codes, determinants, and reasons (e.g., below detection limit, not recorded, samples not collected, pH probe malfunction, instrument faults, sample contamination)
- Common issues noted
  - Some measurements unavailable or unreliable due to instrument faults or procedural deviations
  - Specific exclusions include pH/meter issues, timing gaps, sample unavailability, and suspected instrument faults for DOC/TdN and SUVA measurements

## Metadata and data structure for GIS use

- Spatial attributes
  - Four sampling sites with precise coordinates; spatial layout suitable for mapping as point features
  - Grid reference provided for mapping context
- Temporal attributes
  - Fortnightly sampling window with explicit dates; multiple site changes over time (site addition and a site discontinuation)
- Attribute schema guidance
  - Site_name, Site_code; Date, Time; pH, pH_temp, DO, DO_percent, DO_temp, Conductivity, Conductivity_temp, Temp_av
  - DOC, TdN, C_N, Abs_at_254, SUVA, TP, SRP, CH4_C, CO2_C, N2O_N, POC
- Usage considerations for GIS specialists
  - Time-series integration across sites requires handling site discontinuation (HARE) after Aug 2022
  - Data quality flags may be needed to mask or filter excluded observations
  - Unit consistency and calibration notes are important when linking with other hydrological or geospatial datasets
  - Reference to methodological details supports reproducible GIS-based analyses and QA/QC workflows

## Access, provenance, and references

- Acknowledgement
  - MERLIN is a research and innovation action funded under the European Commission’s Horizon 2020 programme (grant agreement No 101036337)
- References for methods and context
  - Dawson et al. (1995); Dinsmore et al. (2013); Pribyl (2010); Weishaar et al. (2003)
- Authors
  - Alanna Grant, Rebecca McKenzie, Amy Pickard, Toby Roberts, Bryan Spears

- This dataset provides a comprehensive, GIS-ready set of water-quality measurements across four peatland monitoring sites, with detailed metadata, measurement protocols, and documented data quality considerations suitable for map-based data visualisations and spatial analyses.