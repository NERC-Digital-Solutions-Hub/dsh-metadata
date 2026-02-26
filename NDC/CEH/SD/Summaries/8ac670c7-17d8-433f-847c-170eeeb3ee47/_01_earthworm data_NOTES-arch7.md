# Experimental Design/Sampling Regime

- Purpose: Describe how earthworm and soil samples were collected across seven fields to assess spatial and temporal changes before and after land-use conversions, with representative annual changes observed across fields.

- Study design and timing:
  - Seven fields were sampled before conversion transects were established in April 2015, and again in April 2016 and April 2017.
  - Additional temporal sampling occurred in December 2015 (winter), July 2016 (summer), and October 2016 (autumn).
  - Sampling period spans from the April 2015 baseline to April 2017, intended to capture year-to-year changes and field-wide patterns.

- Spatial sampling scheme:
  - Sampling locations per occasion: 8 locations per field/ transect.
  - Locations include: under the hedgerow and at the middle of the field-margin at the head of each 70 m transect; within transects at distances of 2, 4, 8, 16, 32, and 64 m from the field-margin boundary.
  - Distances and positions are labeled to indicate hedge (H) or margin (M) contexts.

- Target variables and methods:
  - Earthworm sampling: soil blocks (18 x 18 x 15 cm) extracted; earthworms collected by hand-sorting; a dilute allyl isothiocyanate applied to enhance retrieval of deeper species; 30-minute observation per pit; adults identified with keys; juveniles grouped by functional group (epigeic, endogeic, anecic).
  - Soil measurements: soil moisture (ML3 ThetaProbe) and soil temperature (Checktemp) at 5 cm and 10 cm depths; bulk density measured at 5 cm and 10 cm depths using density rings; samples replaced to pits with position tracked to avoid re-sampling.
  - Biomass/abundance: recorded for earthworms; biomass expressed as number of individuals (and later, biomass for certain samples).

- Data collection and file structure (geospatially oriented data):
  - Multiple CSV files with standardized coding to locate samples within fields and transects.
  - Core coding scheme:
    - SBH_code: field and distance code in the format XYZZ, where X indicates the field (e.g., BSSE, BSSW, Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field) and Y indicates the strip (Strip, Central strip) and ZZ indicates the sample location (Hedge, Margin, 2m, 4m, 8m, 16m, 32m, 64m).
    - Field_name: full or abbreviated field names (e.g., BSSE = Big Substation East; BSSW = Big Substation West).
    - Strip: treatment type (CAL, UAL, Ctrl, NTL-A, CTL_A) with descriptions such as connected arable ley strip, unconnected arable strip (earthworm barrier), control land use, no-till arc, conventional tillage.
    - Distance: distance from hedge in meters; Hedge (H) or Margin (M) contexts noted.
  - Data files and key variables:
    - April2015_Earthworm_Soil data.csv: 9 columns (Date, Field_name, SBH_code, X/Y/Z components, Distance, Soil_Temp_10cm, soil_moisture_1/2/3, etc.).
    - Dec2015_Earthworm_Soil data.csv: 10 columns; includes Field_name, Strip, Depth (Mustard P or Topsoil S), Sample_type (A or B), and location codes; extensive species- and biomass-related columns.
    - April2016_Earthworm_Soil data.csv; April2017_Earthworm_Soil data.csv; July2016_Earthworm_Soil data.csv; Oct2016_Earthworm_Soil data.csv: 15 columns, including SBH_code, Field_name, Strip, Distance, Field context, and moisture/temperature measurements at multiple depths.
    - April2015_EW_count.csv, April2016_EW_count.csv, April2017_EW_count.csv, Dec2015_EW_count.csv, July2016_EW_count.csv, Oct2016_EW_count.csv: 31 columns; record counts/biomass by earthworm species across functional groups (e.g., END-, EPI-, ANE-), with species names and functional group annotations.
  - Units and metadata:
    - Soil temperature: degrees Celsius; soil moisture: millivolts; bulk density: g/cm3.
    - Distances: meters from hedge; transect length: 70 m.
    - Blank cells indicate missing data.

- Earthworm taxonomy and functional groups (reference for data interpretation):
  - Endogeic: soil-living, horizontal burrowing.
  - Epigeic: litter-living.
  - Anecic: soil-living, deep vertical burrows.
  - Examples of species and associated functional groups provided (e.g., Allolobophora chlorotica; Aporrectodea caliginosa; Lumbricus terrestris; Eisenia fetida; and others).

- Important notes:
  - April 2015 sampling used control land use since treatment strips had not yet been created.
  - Samples were taken from pre-designated strips and distances.
  - The datasets include extensive site- and species-specific columns, enabling spatial-temporal analyses of earthworm communities and soil properties.

- References:
  - Earthworms by Sims & Gerard (1999); Zaborski (2003); Pelosi et al. (2008) for sampling methods and taxonomic guidance.