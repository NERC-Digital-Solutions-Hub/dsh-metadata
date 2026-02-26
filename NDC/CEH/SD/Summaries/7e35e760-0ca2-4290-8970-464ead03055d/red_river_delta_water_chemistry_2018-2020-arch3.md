# Water chemistry from the Red River Delta, Vietnam, 2018 to 2020

## Overview
- A dataset describing surface water chemistry from the Red River Delta near Hanoi, collected from February 2018 to January 2020.
- Aimed at providing environmental health measures to assess and inform policy, with data suitable for monitoring frameworks and decision-making.

## Study area and sampling regime
- Location: rivers within around 100 km of Hanoi, Vietnam.
- Red River sampling: 10 stations (Yen Bai, Vu Quang, Hoa Binh, Son Tay, Ha Noi, Gian Khau, Quyet Chien, Nam Dinh, Truc Phuong, Ba Lat).
- Day River sampling: 11 stations (Phung Dam, Mai Linh Bridge, Ba Tha, Te Tieu Bridge, Que Bridge, Do Bridge, Doan Vy Bridge, Non Nuoc Bridge, Do Thong, Do Muoi, Nhu Tan).
- Sampling frequency: monthly at each station.
- Seasonal timing: dry season (Nov–Apr) and rainy season (May–Oct).
- Data include precise GPS coordinates for each site.

## Data collection, handling, and in-situ measurements
- Sample collection: surface water in Nalgene bottles, stored at 4°C, analyzed within 48 hours.
- In-situ measurements: temperature, pH, dissolved oxygen, salinity, turbidity, using Hydrolab Sonde DS5.
- Geolocation: latitude and longitude recorded for each sampling point.

## Analytical methods and constituents
- Chemical analyses (APHA methods, mostly 1912 standards) including:
  - Total nitrogen (TDN) and total dissolved nitrogen (TDN by Kjeldahl; TDN) and total dissolved phosphorus (TDP) after oxidation.
  - Nitrogen species: NO3-N, NO2-N, NH4-N (via colorimetry and cadmium reduction methods).
  - Sulfate (SO4 2-), alkalinity (mol/L and µmol/L).
  - Phosphorus: soluble reactive phosphorus (SRP PO4-P), total soluble phosphorus (TSP PO4-P), total phosphorus (Ptot).
  - Silicate: SiO2 (as SiO2 and as Si).
- Pigments and productivity indicators:
  - Chlorophyll and carotenoids extracted and quantified by HPLC; pigments reported as nmol/L.
  - Specific pigments measured include fucoxanthin, violaxanthin, diadinoxanthin, diatoxanthin, lutein, zeaxanthin, canthaxanthin, and Chl a derivatives.
- General water quality parameters: temperature, pH, dissolved oxygen, salinity, turbidity, conductivity, total dissolved solids (TDS), alkalinity, major cations (Na, Mg, K, Ca), and major anions (Cl-, SO4 2-).

## Data quality control and validation
- Instrument calibration:
  - pH calibration before sampling campaigns with precision/accuracy to ±0.01 pH.
  - Colorimetric analyses calibrated with standards alongside each run.
- Pigment quality:
  - Calibration with 8-point standards; retention time drift checked using grass extract to verify Chl a, Chl b, and lutein.
- Documentation of methods and adherence to standard protocols to ensure data quality, traceability, and comparability.

## Data structure, units, and accessibility
- Data comprise 44 columns with standardized naming and units, including:
  - Site information (name, code), date (text and formatted), year, month, season, GPS coordinates.
  - In-situ water chemistry: Temperature (°C), DO (mg/L), Salinity (ppt), pH, Turbidity (NTU), Conductivity (µS/cm), TDS (mg/L).
  - Nutrients: NO3-N, NO2-N, NH4-N, Ntot (mg/L), SRP-PO4-P, TSP-PO4-P, Ptot.
  - Anions/cations: Na, Mg, K, Ca, Cl-, SO4 (mg/L).
  - Alkalinity (mol/L and µmol/L).
  - Silicates: SiO2 (mg/L, as Si), and various pigment concentrations (nmol/L) including Fucoxanthin, Violaxanthin, Diadinoxanthin, Diatoxanthin, Lutein, Zeaxanthin, Canthaxanthin, and Chlorophyll a and derivatives.
- Comprehensive metadata and a defined data structure support integration into monitoring dashboards, reports, or governance reviews.

## Licensing, data sharing, and citation
- Data available under Open Government Licence v3.
- Citation requirement for reuse: McGowan, S. & Salgado, J. (2022). Water chemistry from the Red River Delta, Vietnam, 2018 to 2020. NERC EDS Environmental Information Data Centre. Dataset. https://doi.org/10.5285/7e35e760-0ca2-4290-8970-464ead03055d

## Relevance for monitoring frameworks
- Provides a broad suite of environmental health indicators (nutrients, major ions, pigments, basic physicochemical parameters) suitable for evaluating river water quality and ecosystem status.
- Data governance aspects emphasized: openness, traceability, data sharing, and clear data provenance.
- Metadata-rich dataset supports transparency and comparability across time and space, addressing common monitoring framework challenges such as data gaps, standardization, and the need for clear communication of complex findings.