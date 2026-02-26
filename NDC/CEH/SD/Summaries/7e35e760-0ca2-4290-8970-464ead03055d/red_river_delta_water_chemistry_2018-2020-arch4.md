# Water chemistry from the Red River Delta, Vietnam, 2018 to 2020

## Access, licensing and citation
- Dataset available at https://doi.org/10.5285/7e35e760-0ca2-4290-8970-464ead03055d
- Open Government Licence v3
- חובה: cite McGowan, S. & Salgado, J. (2022). Water chemistry from the Red River Delta, Vietnam, 2018 to 2020. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/7e35e760-0ca2-4290-8970-464ead03055d
- Suitable for reuse with attribution under the licencing terms

## Sampling regime
- Area: rivers in the Red River Delta within ~100 km of Hanoi
- Stations: 10 sampling stations on the Red River (H1–H10) and 11 on the Day River (D1–D11)
- Locations recorded with latitude/longitude; GPS coordinates provided in dataset
- Frequency: monthly sampling from February 2018 to January 2020
- Sample handling: surface water collected in Nalgene bottles, stored at 4°C, analyzed within 48 hours
- Seasonal timing: dry season (Nov–Apr) or rainy season (May–Oct)

## Collection/Generation/Transformation methods
- In-field data: temperature, pH, dissolved oxygen, salinity, turbidity measured in situ with Hydrolab Sonde DS5
- Additional measurements: latitude-longitude recorded for each sampling point
- Sample processing: standard filtration (Whatman GF/F, 0.7 µm) for soluble parameters
- Temporal scope: 2018–2020 (monthly sampling)

## Analytical methods
- Nutrients and related parameters:
  - Total dissolved nitrogen (TDN), total dissolved phosphorus (TDP)
  - Nitrate-N (NO3-N), Nitrite-N (NO2-N), Ammonium-N (NH4-N)
  - Soluble reactive phosphorus (SRP as PO4-P), Total soluble phosphorus (TSP as PO4-P), Total phosphorus (Ptot)
  - Silicate as SiO2 (SiO2) and silicate as Si (SiO2 as Si)
  - Alkalinity (mol/L and µmol/L)
  - Other ions: Na, Mg, K, Ca, Cl-, SO4
- Phytoplankton pigments:
  - Chlorophyll a (Chl a) and derivatives (Chl a derivatives), Fucoxanthin, Violaxanthin, Diadinoxanthin, Diatoxanthin, Lutein, Zeaxanthin, Canthaxanthin
- Methods referenced:
  - Standard APHA methods (e.g., for NO3-N, NO2-N, NH4-N, TA, TDN)
  - Cadmium column reduction for NO3-N, Griess reaction for nitrite
  - Kjeldahl digestion for TDN
  - Oxidation of samples for TDP, followed by PO4 determination
  - Turbidity-based sulfate determination via BaSO4 suspension
  - HPLC for pigment separation/quantification
- Pigment quantification:
  - Extraction in acetone:methanol:water, 80:15:5, at -4°C, 12 h
  - Re-dissolution in acetone:methanol:IPR; pigment identification by absorbance spectra and retention times
  - Quantification against commercial standards

## Quality control
- pH and oxygen electrode calibration between campaigns; pH precision/accuracy ±0.01
- Calibration standards run with each colorimetric analysis
- Pigment quantification calibrated with 8-point standards
- Retention time drift checked using grass extract as an internal control for Chl a, Chl b, lutein

## Data structure and units
- Dataset consists of 44 columns with explicit metadata
  - Examples of columns and descriptions:
    - Site name, Site code, Date (text and formatted), Month, Year, Season, Latitude, Longitude, Time
    - Physical parameters: Temperature (°C), Dissolved Oxygen (mg O2/L), Salinity (ppt), pH, Turbidity (NTU), Conductivity (µS/cm), TDS (mg/L)
    - Nutrients: NO3-N, NO2-N, NH4-N, Ntot (all mg N/L), SRP PO4-P, TSP PO4-P, Ptot (mg P/L), SiO2 and SiO2 as Si (mg/L)
    - Alkalinity: mol/L and µmol/L
    - Major ions: Na, Mg, K, Ca, Cl-, SO4 (mg/L)
    - Pigments: Fucoxanthin, Violaxanthin, Diadinoxanthin, Diatoxanthin, Lutein, Zeaxanthin, Canthaxanthin (nmol/L)
    - Chlorophylls: Chl a, Chl a'1, Chl a'2 (nmol/L)
- Data capture across 44 columns supports comprehensive water chemistry profiling and phytoplankton indicators

## References and methodological context
- APHA, Standard methods for the examination of water and wastewater (Vol. 2) as a methodological backbone (1912)
- Chen et al. (2001) referenced for pigment biomarker context in historical hypoxia studies

## Relevance for data leadership and data strategy
- Demonstrates end-to-end data lifecycle: planning, field collection, laboratory analysis, quality control, data structuring, and documentation
- Aligns with data-system thinking: locational data, seasonal sampling, comprehensive parameter set, and explicit metadata to support discoverability and reuse
- Highlights licensing and attribution requirements, underscoring governance for data sharing
- Provides a detailed, standardized dataset schema (44 columns) that supports interoperability, provenance tracking, and analytical reuse
- Addresses common data-system challenges relevant to the archetype: data discovery (locations and methods clearly described), data quality controls, and clear metadata for reuse across networks or communities of practice