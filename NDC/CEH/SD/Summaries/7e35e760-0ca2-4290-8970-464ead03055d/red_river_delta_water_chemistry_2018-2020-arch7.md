# Water chemistry from the Red River Delta, Vietnam, 2018 to 2020

## Access and licensing
- Data accessible at: https://doi.org/10.5285/7e35e760-0ca2-4290-8970-464ead03055d
- License: Open Government Licence v3
- Citation to use: McGowan, S. & Salgado, J. (2022). Water chemistry from the Red River Delta, Vietnam, 2018 to 2020. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/7e35e760-0ca2-4290-8970-464ead03055d

## Sampling regime and study area
- Geography: Rivers in the Red River Delta within ~100 km of Hanoi; sampling sites include 10 Red River stations (Yen Bai H1, Vu Quang H2, Hoa Binh H3, Son Tay H4, Ha Noi H5, Gian Khau H6, Quyet Chien H7, Nam Dinh H8, Truc Phuong H9, Ba Lat H10) and 11 Day River stations (Phung Dam D1 to Nhu Tan D11). Site coordinates are provided in the dataset.
- Temporal coverage: Monthly sampling from February 2018 to January 2020.
- Sample collection: Surface water collected into Nalgene bottles and stored at 4°C; analysis within 48 hours; GPS coordinates recorded for each sampling point.
- Seasonal timing: Dry season (Nov–Apr) and rainy season (May–Oct) designation.

## Field collection and data generation
- In situ measurements: Temperature (T-C), dissolved oxygen (DO mg/L), salinity (ppt), pH, turbidity (NTU), and conductivity (µS/cm) recorded at the time of sampling.
- Sample handling: In-field collection with standard protocols; filtration and preservation steps described for various analyses.

## Analytical methods
- General water chemistry parameters: TDN, TDP, NO3-N, NO2-N, NH4-N, SO4 2-, total alkalinity; TA measured by single-point titration; nitrate and nitrite analyzed with colorimetric/Griess methods; phosphorus forms quantified after oxidation steps; standards follow APHA (1912) methods.
- Chlorophyll and pigments: Extraction from filters, separation and quantification by HPLC (Agilent 1200) with ODS column; pigments quantified using commercial standards; results reported as nmol/L.
- Quality control: Regular calibration of pH and oxygen electrodes; colorimetric standards run with each analysis; pigment identifications aided by retention time drift checks using grass extract.

## Data structure and units
- Dataset contains 44 columns with the following key fields:
  - Site name, Site code, Date (text), Date (formatted), Month, Year, Season (WET/DRY)
  - Latitude, Longitude
  - Time of sampling (hhmm)
  - In situ physico-chemical parameters: Temperature (°C), DO (mgO2/L), Salinity (ppt), pH, Turbidity (NTU), Conductivity (µS/cm), TDS (mg/L)
  - Nutrients and related ions: NO3-N (mgN/L), NO2-N (mgN/L), NH4-N (mgN/L), Ntot (mgN/L), SRP (PO4-P, mgP/L), TSP (PO4-P, mgP/L), Ptot (mgP/L), SiO2 (mgSiO2/L), SiO2 as Si (mg/L)
  - Alkalinity (mol/L and µmol/L)
  - Cations/anions: Na (mg/L), Mg (mg/L), K (mg/L), Ca (mg/L), Cl- (mg/L), SO4 (mg/L)
  - Pigments: Fucoxanthin, Violaxanthin, Diadinoxanthin, Diatoxanthin, Lutein, Zeaxanthin, Canthaxanthin (nmol/L)
  - Chlorophyll metrics: Chl a and derivatives (nmol/L)
- The 44 columns provide spatial (lat/long), temporal (date, month, year, season, time), and a broad suite of chemical, optical, and pigment measurements suitable for GIS-based mapping and temporal analysis.

## GIS relevance and data use
- Spatial data: Precise site coordinates enable map-based visualization of water chemistry across the Red and Day Rivers.
- Temporal data: Monthly sampling over two years supports trend analysis and seasonal comparisons in map dashboards.
- Data integration: Standardized parameter definitions and units (aligned with APHA methodologies) facilitate integration with other hydrological or environmental GIS layers.
- Recommended uses: Create choropleth or point-based maps of nutrients, alkalinity, ions, and pigment concentrations; overlay with basin features, land use, water quality thresholds, or water management datasets.

## Limitations and considerations
- Data collected over a defined two-year window; may require supplementary data for longer-term analyses.
- Analyses follow APHA (1912) methods; ensure compatibility with any updated protocols when integrating with other datasets.
- Spatial resolution limited to 21 sampling sites; consider clustering or aggregation for regional analyses.

## References
- APHA, Standard methods for the examination of water and wastewater (Vol. 2). American Public Health Association (1912).
- Chen, N., Bianchi, T. S., McKee, B. A., & Bland, J. M. (2001). Historical trends of hypoxia on the Louisiana shelf: application of pigments as biomarkers. Organic Geochemistry, 32(4), 543-561.
- Chen, N., et al. (2002). [Pigment-based methodology details referenced in dataset].
- McGowan, S. & Salgado, J. (2022). Water chemistry from the Red River Delta, Vietnam, 2018 to 2020. NERC EDS Environmental Information Data Centre. Dataset. https://doi.org/10.5285/7e35e760-0ca2-4290-8970-464ead03055d