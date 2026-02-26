# Water chemistry from the Red River Delta, Vietnam, 2018 to 2020

## Data access and citation
- Data available at https://doi.org/10.5285/7e35e760-0ca2-4290-8970-464ead03055d
- License: Open Government Licence v3
- Citation: McGowan, S. & Salgado, J. (2022). Water chemistry from the Red River Delta, Vietnam, 2018 to 2020. NERC EDS Environmental Information Data Centre. Dataset. https://doi.org/10.5285/7e35e760-0ca2-4290-8970-464ead03055d

## Sampling regime
- Area: Rivers of the Red River Delta within ~100 km of Hanoi; sampling sites with precise coordinates provided.
- Red River: 10 stations (H1–H10) including Yen Bai, Vu Quang, Hoa Binh, Son Tay, Ha Noi, Gian Khau, Quyet Chien, Nam Dinh, Truc Phuong, Ba Lat.
- Day River: 11 stations (D1–D11) including Phung Dam, Mai Linh Bridge, Ba Tha, Te Tieu Bridge, Que Bridge, Do Bridge, Doan Vy Bridge, Non Nuoc Bridge, Do Thong, Do Muoi, Nhu Tan.
- Sampling frequency: Monthly from February 2018 to January 2020.
- Sample handling: Surface water collected into Nalgene bottles and stored at 4°C; analyzed within 48 hours.
- Seasonal timing: Sampling designated by dry season (Nov–Apr) or rainy season (May–Oct).
- Positioning: GPS recorded coordinates for each sampling point.

## Collection/Generation/Transformation Methods
- In situ measurements: Temperature, pH, dissolved oxygen, salinity, turbidity measured with Hydrolab Sonde DS5.
- Geographical data: Latitude/longitude recorded for each site.
- Data coverage: Monthly samples across all stations during the study period.

## Analytical methods
- Chemical parameters (surface water): Temperature, pH, DO, salinity, turbidity, conductivity, TDS, NO3-N, NO2-N, NH4-N, Ntot, SRP-PO4-P, TSP-PO4-P, Ptot, SiO2, SiO2 as Si, alkalinity (mol/L and µmol/L), Na, Mg, K, Ca, Cl-, SO4, etc.
- Methods: Standard methods (APHA, 1912) with filtration for soluble parameters; specific procedures include:
  - NO3-N: cadmium column reduction to NO2-N, Griess reaction (540 nm)
  - NO2-N: as NO3-N protocol without reduction
  - NH4-N: phenol hypochlorite method (640 nm)
  - TDN (total organic nitrogen): Kjeldahl digestion
  - TDP: oxidation with (NH4)2S2O8 in H2SO4 to convert to PO4 before phosphate determination
  - SO4^2-: turbidity method via BaSO4 suspension, compared to standards
  - TA: single-point titration using methyl orange and phenolphthalein
- Pigments: Chlorophyll and carotenoids extracted from filters, quantified by HPLC (Agilent 1200) with specific column and detection; pigments quantified against commercial standards and identified by absorbance spectra and retention times.
  - Pigments reported as nanomoles per litre (nmol/L)
  - Included pigments: fucoxanthin, violaxanthin, diadinoxanthin, diatoxanthin, lutein, zeaxanthin, canthaxanthin, chlorophyll a and derivatives
- Quality control: Regular calibration of pH and DO sensors (±0.01 accuracy); calibration standards alongside each analysis; pigment identifications aided by grass extract to monitor retention time drift.

## Quality control and data handling
- Ensures data integrity through routine instrument calibration, use of standards, and drift checks for pigment analyses.
- Data designed for consistent, cross-site monitoring of environmental chemistry and pigment status over time.

## Data structure and units
- Dataset contains 44 columns with fields including:
  - Site name, site code, date (text and formatted), month, year, season, latitude, longitude, time
  - Physical-chemical parameters: Temperature (°C), DO (mg/L), Salinity (ppt), pH, Turbidity (NTU), Conductivity (µS/cm), TDS (mg/L)
  - Nutrients and ions: NO3-N (mg/L), NO2-N (mg/L), NH4-N (mg/L), Ntot (mg/L), SRP-PO4-P (mg/L), TSP-PO4-P (mg/L), Ptot (mg/L), SiO2 (mg/L as SiO2 and as Si), Alkalinity (mol/L and µmol/L), Na, Mg, K, Ca, Cl-, SO4
  - Pigments: Fucoxanthin, Violaxanthin, Diadinoxanthin, Diatoxanthin, Lutein, Zeaxanthin, Canthaxanthin, Chl a, Chl a derivatives (nmol/L)
- Units are specified per parameter (e.g., NO3-N in mg/L, conductance in µS/cm, pigments in nmol/L).

## References
- APHA, Standard methods for the examination of water and wastewater (Vol. 2). American Public Health Association (1912).
- Chen, N., Bianchi, T. S., McKee, B. A., & Bland, J. M. (2001). Historical trends of hypoxia on the Louisiana shelf: application of pigments as biomarkers. Organic Geochemistry, 32(4), 543-561.