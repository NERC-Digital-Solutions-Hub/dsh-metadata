# Experimental Design/Sampling Regime

- Study aims and design
  - Seven fields were sampled before establishing conversion transects in April 2015, with follow-up sampling in April 2016 and April 2017.
  - Temporal sampling occurred in one arable field (BSSE) and one pasture field (SP); additional temporal sampling in December 2015 (winter), July 2016 (summer), and October 2016 (autumn) provides a window from the April 2015 baseline through April 2017.
  - At each sampling, earthworm and soil samples were taken from 8 locations: under the hedgerow and the field-margin at the head of each 70 m transect, plus within the transects at 2, 4, 8, 16, 32, and 64 m from the field-margin boundary.

- Spatial and sampling layout
  - Fields included: BSSE (Big Substation East), BSSW (Big Substation West), Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field.
  - Sampling positions are coded by hedge (H) and distance from hedge along transects, with margins (M) and distances 2–64 m.

- Collection methods and field instrumentation
  - Earthworms: soil block (18 cm × 18 cm × 15 cm) removed at each distance; concrete method uses dilute allyl isothiocyanate to flush deeper worm species; 30-minute observation window; adults identified with Sims & Gerard (1999) keys; juveniles grouped by functional groups (epigeic, endogeic, anecic); biomass recorded from December 2015 onward.
  - Soil measurements: moisture and temperature recorded at 5 cm and 10 cm depths around pits; moisture with ML3 ThetaProbe, temperature with Checktemp; bulk density at 5 cm and 10 cm depths using 118 cm3 rings, calculated from oven-dried weight (105°C, 24 h).
  - Sampling protocol includes returning earthworm-free soils to pits and recording sample position to avoid resampling the same location.

- Data structure and file suite
  - Earthworm soil data files (appearance, sampling conditions, and measurements)
    - April2015_earthworm_Soil data.csv: 9 columns (Date, Field_name, SBH_code, X, Y, ZZ, Distance, Field identifiers and strip codes, soil temp and moisture measurements).
      - Field_name codes include BSSE, BSSW, Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field.
      - ZZ codes map to Hedge, Margin, 2 m, 4 m, 8 m, 16 m, 32 m, 64 m positions.
      - Distances are metres from hedge; Hedge and Margin markers indicate sampling zones.
      - Temperature and soil moisture recorded at 10 cm depth and 1–3 moisture channels.
      - April 2015 samples come from control land use; strips were pre-designated (no treatment strips yet).
    - Dec2015_Earthworm_Soil data.csv: 10 columns (Date, SBH_code, X, Y, Field_name, Strip, Distance, and later additional fields for location and soil properties).
      - Includes Strip type (CAL, UAL, Ctrl, NTL-A, CTL_A).
      - Distance and Hedge/Margin indicators as above.
      - Additional soil variables: soil_temp_5cm_1, soil_temp_10_cm_1, moisture_5cm_depth_1, moisture_5_cm_depth_2, moisture_5_cm_depth_3.
    - April2016_Earthworm_Soil data.csv; April2017_Earthworm_Soil data.csv; July2016_Earthworm_Soil data.csv; Oct2016_Earthworm_Soil data.csv: 15 columns.
      - In addition to date and location (SBH_code), include Field_name, Strip, Distance, Hedge/Margin indicators, and depth-related measurements.
      - Depth indicators: Mustard (P) or Topsoil (S).
      - Temperature at 5 cm and 10 cm, moisture at 5 cm and 10 cm (three channels each), and bulk density measurements at defined depths.
      - Extensive soil and microhabitat variables accompany earthworm measurements.
  - Earthworm count data files
    - April2015_EW_count.csv; April2016_EW_count.csv; April2017_EW_count.csv; Dec2015_EW_count.csv; July2016_EW_count.csv; Oct2016_EW_count.csv: 31 columns.
      - Core identifiers: Date, SBH_code, X (field), Y (strip), ZZ (sample location), Field_name, Strip, Distance.
      - Field layouts and Strip definitions as above; includes species- or functional-group specific counts (e.g., END, EPI, ANE with numerous species such as Allolobophora chlorotica, Aporrectodea caliginosa, Lumbricus terrestris, Eisenia fetida, etc.).
      - Columns capture abundance counts per species and functional group assignments (Endogeic, Epigeic, Anecic).
  - Miscellaneous
    - Earthworm functional groups and species mappings are provided (Endogeic, Epigeic, Anecic; with corresponding species names).
    - Blank cells denote missing data.
  - References for methods
    - Sims & Gerard (1999); Zaborski (2003); Pelosi et al. (2008).

- Data interpretation and GIS relevance
  - Data are spatially anchored to transects with fixed positions (hedge, margin, and fixed distances from hedge), enabling spatial analyses along field boundaries and hedgerows.
  - The SBH_code encoding allows reconstruction of field, strip, and sampling location, facilitating georeferencing to field polygons and transect lines in GIS.
  - Temporal coverage across multiple years and seasons supports assessment of spatial-temporal dynamics in earthworm communities and soil properties.
  - The dataset combines species-level abundance/biomass with soil microhabitat measurements (temperature, moisture, bulk density), enabling correlation analyses and map-based visualization of habitat suitability and organism distributions.

- Notes and caveats
  - April 2015 sampling occurred in control land uses; treatment strips were not yet established.
  - Missing data are represented by blanks in the datasets.
  - Units: temperatures in degrees Celsius; soil moisture in millivolts (sensor outputs); bulk density in g/cm3; distances in metres.

- References
  - Sims & Gerard (1999); Zaborski (2003); Pelosi et al. (2008)