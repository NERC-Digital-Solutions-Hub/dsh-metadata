# Water chemistry from the Red River Delta, Vietnam, 2018 to 2020

## Overview
- Data access: https://doi.org/10.5285/7e35e760-0ca2-4290-8970-464ead03055d
- License: Open Government Licence v3
- Citation requirement: McGowan, S. & Salgado, J. (2022). Water chemistry from the Red River Delta, Vietnam, 2018 to 2020. NERC EDS Environmental Information Data Centre. Dataset. https://doi.org/10.5285/7e35e760-0ca2-4290-8970-464ead03055d
- Repository: NERC Environmental Information Data Centre (EDS)

## Sampling regime and scope
- Study area: Rivers of the Red River Delta within ~100 km of Hanoi (coordinates provided for sampling sites)
- Stations:
  - Red River: Yên Bài (H1) to Ba Lat (H10) – 10 stations
  - Day River: Phung Dam (D1) to Nhu Tan (D11) – 11 stations
- Data structure: Geographic coordinates for each site included in the dataset
- Sampling frequency and period: Once per month from February 2018 to January 2020
- Sample handling: Surface water collected in Nalgene bottles, stored at 4°C, analyzed within 48 hours
- Field measurements: Temperature, pH, dissolved oxygen, salinity, and turbidity measured in situ with a Hydrolab DS5
- Seasonal timing: Sampling aligned with wet/dry seasons (dry: Nov–Apr; wet: May–Oct)

## Analytical methods
- Nutrients and inorganic chemistry:
  - Total dissolved nitrogen (TDN), total dissolved phosphorus (TDP)
  - Nitrate-N (NO3-N), Nitrite-N (NO2-N), Ammonium-N (NH4-N)
  - Sulfate (SO4 2-), Total alkalinity (TA)
  - TA determined by single-point titration (methyl orange and phenolphthalein indicators)
  - NO3-N determined by cadmium-reduction and Griess reaction
  - NO2-N method follows NO3-N without reduction
  - TDN by Kjeldahl digestion
  - TDP post-oxidation to phosphate for PO4 determination
  - SO4 2- by turbidity method via BaSO4
  - Soluble phosphorus and total phosphorus reported as PO4-P and Ptot
- Chlorophyll and pigments:
  - Pigments extracted from filters (acetone:methanol:water) and quantified by HPLC (Agilent 1200) with an ODS column and PDA detector
  - Pigments measured: fucoxanthin, violaxanthin, diadinoxanthin, diatoxanthin, lutein, zeaxanthin, canthaxanthin
  - Chlorophyll a and derivative concentrations provided as nmol/L
- Quality control:
  - pH and oxygen electrode calibration before sampling campaigns; pH accuracy ±0.01
  - Calibration standards run with colorimetric analyses
  - Pigment identifications aided by retention time drift controls (grass extract)

## Data structure and units
- Data columns: 44 total, covering:
  - Site information: Site name, Site code
  - Date details: Date (text), Date (formatted), Month, Year, Season
  - Location: Latitude, Longitude
  - Time: Time of sampling
  - In-situ measurements: Temperature (°C), DO (mg/L), Salinity (ppt), pH, Turbidity (NTU), Conductivity (µS/cm), TDS (mg/L)
  - Nutrients and ions: NO3-N, NO2-N, NH4-N, Ntot, SRP-PO4-P, TSP-PO4-P, Ptot, SiO2 (SiO2 and Si as Si), Alkalinity (mol/L and μmol/L), Na, Mg, K, Ca, Cl-, SO4
  - Pigments and chlorophyll: Fucoxanthin, Violaxanthin, Diadinoxanthin, Diatoxanthin, Lutein, Zeaxanthin, Canthaxanthin, Chl a, Chl a'1, Chl a'2
- Units are specified per column descriptions (e.g., NO3-N mg/L, pH units, Chl a nmol/L, etc.)

## Licensing, attribution, and governance
- Data is released under Open Government Licence v3
- Clear citation requirement to facilitate discoverability and reuse
- Dataset hosted with accompanying metadata and 44-column data schema for interoperability
- Guidance to ensure updates and embargo considerations are respected; documentation of data processing steps advisable

## Usage notes for data stewardship
- Ensure dataset discovery through the provided DOI and repository
- Verify license compliance and proper citation in any reuse
- Maintain metadata fidelity (site, date, season, and units) to support data integration with other datasets
- Monitor for updates or versioning and document any transformations or QC steps applied
- Consider documenting any data gaps, availability constraints, or potential embargo conditions that could affect reuse
- Facilitate user needs by maintaining standardized data formats and clear parameter definitions aligned with APHA references and HPLC methodologies prior to sharing

## References
- APHA, Standard methods for the examination of water and wastewater (Vol. 2). American Public Health Association (1912)
- Chen, N., Bianchi, T. S., McKee, B. A., & Bland, J. M. (2001). Historical trends of hypoxia on the Louisiana shelf: application of pigments as biomarkers. Organic Geochemistry, 32(4), 543-561