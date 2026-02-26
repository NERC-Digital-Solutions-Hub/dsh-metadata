# Water chemistry from the Red River Delta, Vietnam, 2018 to 2020

- Data accessible at: https://doi.org/10.5285/7e35e760-0ca2-4290-8970-464ead03055d
- Licence: Open Government Licence v3
- Citation: McGowan, S. & Salgado, J. (2022). Water chemistry from the Red River Delta, Vietnam, 2018 to 2020. NERC EDS Environmental Information Data Centre. Dataset. https://doi.org/10.5285/7e35e760-0ca2-4290-8970-464ead03055d

## Overview and scope

- Geographic focus: rivers in the Red River Delta, within ~100 km of Hanoi, Vietnam.
- Sampling period: February 2018 to January 2020; monthly sampling at each station.
- Stations:
  - Red River: Yen Bai (H1), Vu Quang (H2), Hoa Binh (H3), Son Tay (H4), Ha Noi (H5), Gian Khau (H6), Quyet Chien (H7), Nam Dinh (H8), Truc Phuong (H9), Ba Lat (H10) — total 10 stations.
  - Day River: Phung Dam (D1), Mai Linh Bridge (D2), Ba Tha (D3), Te Tieu Bridge (D4), Que Bridge (D5), Do Bridge (D6), Doan Vy Bridge (D7), Non Nuoc Bridge (D8), Do Thong (D9), Do Muoi (D10), Nhu Tan (D11) — total 11 stations.
- Sample type: surface water; Brought into 4°C storage and analysed within 48 hours.
- In situ measurements: temperature, pH, dissolved oxygen, salinity, turbidity (via Hydrolab Sonde DS5).
- Geolocation: GPS coordinates recorded for each sampling point.

## Sampling regime

- Frequency: once per month at each station.
- Seasonal designation: dry season (Nov–Apr) and rainy season (May–Oct).
- Data recorded about timing: date, month, year, and season for each sample.
- Location data: latitude and longitude provided for each site; time of sampling recorded.

## Analytical methods and parameters

- In vitro chemical analyses (filtration prior to some measurements):
  - Total dissolved nitrogen (TDN), total dissolved phosphorus (TDP)
  - Nitrate-N (NO3-N), Nitrite-N (NO2-N), Ammonium-N (NH4-N)
  - Sulfate (SO4^2-), Total alkalinity (TA)
  - Total phosphorus forms: soluble reactive P (SRP - PO4-P), total soluble P (TSP - PO4-P), total P (Ptot)
  - Silicate species: SiO2 (as SiO2 and as Si)
  - Chloride (Cl-), major cations (Na, Mg, K, Ca) and sulfate (SO4)
- Nutrient determination: APHA standard methods (1912), colorimetric and digestion-based approaches (e.g., Kjeldahl for TDN, cadmium-reduction for NO3-N, Griess reaction for nitrite).
- Pigment analysis: chlorophyll and carotenoids
  - Extraction and HPLC-based quantification (Chl a, Chl a derivatives, fucoxanthin, violaxanthin, diadinoxanthin, diatoxanthin, lutein, zeaxanthin, canthaxanthin)
  - Pigment concentrations reported as nanomoles per liter (nmol/L)
- Quality control details:
  - pH and oxygen probes calibrated between campaigns with precision/accuracy around ±0.01 pH units
  - Colorimetric methods calibrated with standards; pigment identifications aided by retention times and drift checks using grass extract

## Data structure and units

- Dataset comprises 44 columns with consolidated metadata and measurements:
  - Site name, site code, date (text) and date (formatted), Month, Year, Season, Latitude, Longitude, Time
  - In situ: Temperature (°C), Dissolved Oxygen (mg/L), Salinity (ppt), pH, Turbidity (NTU), Conductivity (µS/cm), TDS (mg/L)
  - Nutrients and major ions: NO3-N (mgN/L), NO2-N (mgN/L), NH4-N (mgN/L), Ntot (mgN/L), SRP-PO4-P (mgP/L), TSP-PO4-P (mgP/L), Ptot (mgP/L), SiO2 (mgSiO2/L), SiO2 (mgSi/L), Alkalinity (mol/L and µmol/L), Na (mg/L), Mg (mg/L), K (mg/L), Ca (mg/L), Cl- (mg/L), SO4 (mg/L)
  - Pigments: Fucoxanthin, Violaxanthin, Diadinoxanthin, Diatoxanthin, Lutein, Zeaxanthin, Canthaxanthin (all nmol/L)
  - Chlorophyll: Chl a, Chl a′1, Chl a′2 (nmol/L)
- All measurements anchored to the same temporal framework (monthly samples across 21 stations total)

## Data quality and provenance

- Source and method documentation provide clear provenance for sampling, handling, and analytical steps.
- Methods align with established APHA standard methods; quality control steps described to support reproducibility.

## Access, reuse, and citation details

- Data license permits reuse under Open Government Licence v3
- Required citation and attribution per dataset metadata (McGowan & Salgado, 2022) when using the data
- Data and metadata are structured to support discoverability and potential data portal upload with accompanying metadata

## Potential uses for Analysts

- Explore spatial patterns across Red River and Day River stations (temporal and seasonal variations in nutrients, major ions, and pigments)
- Build correlations and predictive models linking nutrient status (NO3-N, NH4-N, PO4-P) with dissolved oxygen, pH, salinity, and turbidity
- Examine pigment profiles as indicators of phytoplankton community structure and potential primary productivity shifts
- Assess data at appropriate scales for local or regional decision-making, considering the monthly cadence and 2018–2020 time window
- Combine with additional datasets (e.g., land-use, hydrology) to contextualize nutrient inputs and water quality dynamics