# UK estuary greenhouse gas and nutrients data set

- Scope and aim
  - Data from seven UK estuaries: Clyde, Forth, Tay (central Scotland); Conwy, Clwyd (northern Wales); Dart, Tamar (southwest England).
  - Four sampling campaigns: July and October 2017; January and April 2018.
  - Measurements include greenhouse gases (CH4, CO2, N2O) and water chemistry (DOC, total dissolved carbon, nutrients) along the estuarine salinity gradient.
  - Geolocated sampling with explicit spatial design to span salinity intervals.

- Spatial and sampling design
  - Six sampling positions per estuary (Position 1 to 6): Position 1 is furthest upstream (freshwater); Position 6 is furthest downstream (saline).
  - Sampling locations chosen to cover the salinity range; exact points varied by survey to achieve target salinities (1, 2, 5, 10, 15, >25 ppt).
  - In situ measurements at each location: surface water temperature and salinity measured ~10 cm below surface; lat/long recorded for each point.
  - Data attributes include Estuary, Position, Lat, Long, Day, Month, Year, Salinity, Temperature.

- Sampling methods and greenhouse gas analyses
  - Clyde, Clywd, Conwy, Forth, Tay:
    - Headspace method with 40 mL estuary water equilibrated with 20 mL ambient headspace in a syringe; vigorous underwater shaking; samples collected in 12 mL Labco vials.
    - Ambient air sample collected at each site.
  - Tamar and Dart:
    - Gas samples collected in 500 mL borosilicate bottles, overfilled thrice, poisoned with mercuric chloride.
  - Gas analyses:
    - Gas chromatography: CH4 and CO2 measured with flame ionisation detector (FID); N2O with micro electron capture detector (μECD) for Clyde/Clywd/Conwy/Forth/Tay.
    - Tamar/Dart analyses used single-phase equilibration GC with CH4 (FID) and N2O (ECD) detectors at ~25°C.
  - Solubility and calibration:
    - CH4, CO2, N2O concentrations calculated with Henry’s law and Bunsen solubility corrections; CH4 solubility references Weiss & Price (1980).
    - Calibration against certified standards traceable to NOAA/WMO; specific standards and LODs documented per method.

- Water chemistry analyses
  - Dissolved organic carbon (DOC) and total dissolved carbon (TDC) analyzed at UKCEH using TOC-L with combustion/IR detection.
  - Freshwater nutrients (Position 1; some sites with multiple freshwater positions) analyzed at UKCEH:
    - Nitrate/Nitrite (NO3- + NO2-), Ammonium (NH4+), Total Nitrogen (TN), Total Phosphorus (TP), Dissolved Phosphate (PO4-P) and related analyses; various QC steps and LODs specified.
  - Saline nutrients (Positions 2–6) analyzed at Plymouth Marine Laboratory using SEAL Analytical systems; methods per GO-SHIP protocols with established LODs.
  - Units and conversions follow standard marine chemistry conventions; detailed table (Table 1) provides column headers and unit details.

- Data structure, units, and quality notes
  - Data reported to two decimal places; missing values marked with an asterisk.
  - Saline vs freshwater samples are analyzed at different laboratories, leading to many missing values in certain columns (and potential relevance in others).
  - Column descriptions include estuary name, position (1–6), coordinates, date (day, month, year), salinity (ppt), temperature (°C), and various gas and nutrient concentrations and saturations (units in µM/L or mg/L as specified).
  - Table 1 provides explicit units for all measured variables, including N2O, CH4, CO2, DOC, TDC, TN, TP, NO3-N, NO2-N, NH4-N, PO4-P, Si, and gas saturations.

- Temporal coverage
  - Campaigns conducted in July 2017, October 2017, January 2018, and April 2018.

- Practical GIS considerations
  - Rich geolocated dataset suitable for mapping spatial patterns of estuarine GHGs and nutrient dynamics.
  - Integrates with other GIS layers (estuaries, coastlines, salinity isopleths) for visual exploration and policy-relevant spatial analyses.
  - Be mindful of cross-laboratory differences and missing values when combining freshwater and saline datasets.

- References and methodological basis
  - Core analytical methods and references for gas analyses, nutrient determinations, and solubility data (e.g., Becker et al., 2020; Upstill-Goddard et al., 1996; Weiss & Price, 1980; GO-SHIP protocols).