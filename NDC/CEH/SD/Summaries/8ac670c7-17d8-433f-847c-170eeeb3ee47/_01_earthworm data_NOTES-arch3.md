# Experimental Design/Sampling Regime

- Study design
  - Seven fields were sampled before conversion transects were established in April 2015, with follow-up sampling in April 2016 and April 2017.
  - Temporal sampling occurred in December 2015 (winter), July 2016 (summer), and October 2016 (autumn), creating a continuous temporal series from the April 2015 baseline to April 2017.
  - At all times, earthworm and soil samples were collected from 8 locations per transect: under the hedgerow and at the field-margin head, plus sampling within transects at 2, 4, 8, 16, 32, and 64 m from the hedge boundary.

- Experimental context
  - Fields include Big Substation East (BSSE), Big Substation West (BSSW), Hillside, Copse, Sub Paddock, Warren Paddock, and Valley Field.
  - Distinct strip treatments were used (CAL, UAL, Ctrl, NTL-A, CTL_A) with April 2015 sampling from control land uses since treatment strips were not yet created.

- Spatial and sampling layout
  - Distances from hedge are recorded in metres, with sample locations coded as Hedge, Margin, 2m, 4m, 8m, 16m, 32m, and 64m.
  - Distinguishing features include hedge proximity and strip treatment type, enabling analysis of hedgerow effects and management practices on soil biota.

- Measurements and depth coverage
  - Soil moisture and soil temperature measured around each excavated pit at depths of 5 cm and 10 cm.
  - Bulk density collected at 5 cm and 10 cm depths.

- Data collection and sample handling
  - Earthworms were collected from soil blocks (18 x 18 x 15 cm) using hand-sorting, with allyl isothiocyanate applied to promote deeper-dweller extraction.
  - Specimens were preserved in 80% ethanol; adults with a clitellum were identified to species, while juveniles were grouped into functional groups: epigeic, endogeic, or anecic.
  - Biomass (as counts of individuals) was recorded from December 2015 onward.

- Data quality and sampling integrity
  - Sampling positions were recorded to avoid resampling the same site in subsequent surveys.
  - All sampling notes indicate blank cells denote missing data; datasets include dates, field codes, strip codes, and precise location codes.

- Types of data collected
  - Earthworm abundance and biomass by species and functional group (count-based and biomass measurements).
  - Soil temperature and soil moisture at multiple depths and locations.
  - Bulk density at two depths.
  - Metadata describing field, strip, distance, and sampling occasion.

- Nature of data files and schemas
  - Earthworm and soil datasets are distributed across multiple CSV files, each corresponding to specific sampling periods:
    - April2015_Earthworm_Soil data.csv (9 columns; baseline with field/location codes and initial measurements)
    - Dec2015_Earthworm_Soil data.csv (10 columns; added fields)
    - April2016_Earthworm_Soil data.csv
    - April2017_Earthworm_Soil data.csv
    - July2016_Earthworm_Soil data.csv
    - Oct2016_Earthworm_Soil data.csv
  - Each file uses a standardized coding scheme for Field (BSSE, BSSW, Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field), Strip (CAL, UAL, Ctrl, NTL-A, CTL_A), and Distance/Location (Hedge, Margin, 2m, 4m, 8m, 16m, 32m, 64m).

- Detailed data structure highlights
  - April2015_earthworm_Soil data.csv: 9 columns including Date, Field_name, SBH_code, X/Y/Z Z code, Distance, Soil_Temp_10cm, soil_moisture_1-3.
  - Dec2015_Earthworm_Soil data.csv: 10 columns with added Field_name, Strip, and additional moisture/temperature fields.
  - April2016/2017 and July2016/Oct2016_Earthworm_Soil data.csv: 15 columns, expanding to include multiple moisture/temperature measurements, density data, and depth-specific metrics.
  - The remaining columns across EW_count datasets total 31 columns, capturing Date, SBH_code, Field, Strip, Depth, and species-specific abundance/biomass counts.

- Earthworm data specifics
  - 31-species/functional-group columns (e.g., END-Al-chl Allolobophora chlorotica; END-Ad-esi Allolobophoridella eiseni; ANE-Ap-noc Aporrectodea caliginosa nocturna; EPI-Ds-rub Dendrodrilus rubidus; etc.).
  - Functional groups used: Endogeic, Epigeic, Anecic; explicit species names provided for detailed biodiversity assessments.

- Miscellaneous notes
  - The dataset includes explicit functional-group mappings and species-level identifiers aligned with Sims & Gerard (1999), Zaborski (2003), and Pelosi et al. (2008).
  - Blank cells indicate missing data; April 2015 sampling was from control land use.

- Implications for monitoring and policy evaluation
  - Provides longitudinal, spatially-resolved data on soil biota (earthworm communities) and soil properties under different management strips and hedgerow contexts.
  - Enables assessment of how arable strips, no-till, conventional tillage, and hedgerow proximity influence soil health indicators.
  - The structured metadata and standardized data schemas support data sharing, meta-analyses, and policy evaluation of soil biodiversity and soil quality in agricultural landscapes.