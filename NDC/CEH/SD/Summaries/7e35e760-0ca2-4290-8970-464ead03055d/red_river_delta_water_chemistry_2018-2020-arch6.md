# Water chemistry from the Red River Delta, Vietnam, 2018 to 2020

- Overview
  - A dataset detailing water chemistry in rivers of the Red River Delta near Hanoi, collected from February 2018 to January 2020.
  - Monthly sampling at two river systems: Red River (10 stations H1–H10) and Day River (11 stations D1–D11), covering about 100 km from Hanoi.
  - Includes a wide range of physicochemical, nutrient, major ion, and pigment measurements, suitable for data exploration and product development.

- Data access and licensing
  - Data available at https://doi.org/10.5285/7e35e760-0ca2-4290-8970-464ead03055d
  - Open Government Licence v3; must cite McGowan, S. & Salgado, J. (2022).

- Study area and sampling regime
  - Location: Red River Delta rivers within ~100 km of Hanoi (approximate center: 20° 57' 56.52" N, 105° 48' 16.78" E).
  - Stations:
    - Red River: Yen Bai (H1), Vu Quang (H2), Hoa Binh (H3), Son Tay (H4), Ha Noi (H5), Gian Khau (H6), Quyet Chien (H7), Nam Dinh (H8), Truc Phuong (H9), Ba Lat (H10).
    - Day River: Phung Dam (D1), Mai Linh Bridge (D2), Ba Tha (D3), Te Tieu Bridge (D4), Que Bridge (D5), Do Bridge (D6), Doan Vy Bridge (D7), Non Nuoc Bridge (D8), Do Thong (D9), Do Muoi (D10), Nhu Tan (D11).
  - Sampling cadence: once per month at each station from Feb 2018 to Jan 2020.
  - Sample handling: surface water collected into Nalgene bottles and stored at 4°C; analyses performed within 48 hours.
  - In situ measurements: temperature, pH, dissolved oxygen, salinity, and turbidity measured in the field with a Hydrolab Sonde DS5.

- Methods and measurements
  - In situ parameters (plus related fields in dataset): temperature (°C), pH, dissolved oxygen (mg/L), salinity (ppt), turbidity (NTU), conductivity (µS/cm), total dissolved solids (mg/L).
  - Nutrients and major ions:
    - Nitrogen species: NO3-N, NO2-N, NH4-N (mgN/L), total nitrogen (Ntot, mgN/L).
    - Phosphorus: soluble reactive phosphorus (SRP - PO4-P, mgP/L), total soluble phosphorus (TSP - PO4-P, mgP/L), total phosphorus (Ptot, mgP/L).
    - Silicates: SiO2 (mgSiO2/L) and SiO2 as Si (mg/L).
    - Alkalinity: mol/L and µmol/L.
    - Major cations/anions: Na, Mg, K, Ca (mg/L); Cl- (mg/L); SO4 (mg/L).
  - Analytical approaches (APHA standards):
    - Filtration of samples for soluble parameters (Whatman GF/F, 0.7 µm).
    - TA determined by single-point titration with methyl orange/phenolphthalein indicators.
    - NO3-N determined by reduction to NO2-N on a cadmium column and Griess reaction.
    - NO2-N by Griess reaction (without reduction step).
    - NH4-N via phenol hypochlorite method (colorimetric at 640 nm).
    - TDN by Kjeldahl digestion.
    - TDP oxidation with ammonium persulfate to convert phosphate for PO4 determination.
    - SO4 by turbidity method via BaSO4 suspension (colorimetric).
  - Pigments:
    - Chlorophyll and carotenoids extracted from filters in acetone:methanol:water, separated and quantified by HPLC (ODS Hypersil column) with an ion-pairing reagent.
    - Pigments quantified using commercial standards; concentrations reported as nmol/L.
  - Quality control (QA/QC):
    - pH electrode calibration with precision ±0.01.
    - Calibration standards run with colorimetric analyses.
    - Pigment quantification calibrated with 8-point standard curves; retention time drift checked using grass extract for Chl a, Chl b, and lutein.

- Data structure and units
  - Dataset contains 44 columns capturing:
    - Site name, site code, date (text and formatted), month, year, season (WET/DRY).
    - Geography: latitude (decimal degrees N), longitude (decimal degrees E), time of sampling (hhmm).
    - In situ and lab measurements: Temperature (°C), DO (mg/L), Salinity (ppt), pH, Turbidity (NTU), Conductivity (µS/cm), TDS (mg/L).
    - Nutrients and solutes: NO3-N, NO2-N, NH4-N, Ntot, SRP-PO4-P, TSP-PO4-P, Ptot, SiO2, SiO2 as Si, Alkalinity (mol/L and µmol/L), Na, Mg, K, Ca, Cl-, SO4.
    - Pigments and chlorophyll: Fucoxanthin, Violaxanthin, Diadinoxanthin, Diatoxanthin, Lutein, Zeaxanthin, Canthaxanthin, Chl a, Chl a derivatives.
  - Timeframe: data span February 2018 to January 2020, with monthly observations across 21 stations.

- How to use this data (data support perspective)
  - Build time-series dashboards to monitor seasonal and inter-annual water chemistry trends across the Red and Day Rivers.
  - Compare nutrient dynamics (N and P species) with pigment data to infer phytoplankton responses.
  - Spatial analysis across 21 stations to identify hotspots of nutrient enrichment or alkalinity changes.
  - Data merging opportunities with other hydrological or ecological datasets (e.g., flow, sediment, or public health indicators).
  - Create self-serve reports or pivot-table based summaries for policy or public communication.
  - Use the documented QA/QC procedures to assess data reliability and harmonize with other datasets.

- References
  - APHA, Standard methods for the examination of water and wastewater (Vol. 2).
  - Chen, N., Bianchi, T. S., McKee, B. A., & Bland, J. M. (2001/2002) on pigment biomarkers and historical trends.