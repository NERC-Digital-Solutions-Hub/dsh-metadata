# Experimental Design/Sampling Regime

- Study aim and scope
  - Document describes earthworm and soil sampling across seven fields to monitor temporal changes around land-use conversions, with baseline in April 2015 and follow-up samples through 2017.
  - Temporal sampling includes winter, summer, and autumn 2015–2016, spanning from pre-conversion baseline to April 2017.
  - Sampling locations were standardized to represent spatial variation relative to hedges and field margins along 70 m transects.

- Study design and locations
  - Fields included: BSSE (Big Substation East), BSSW (Big Substation West), Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field.
  - For each sampling occasion, earthworm and soil samples were collected at 8 locations per transect: under the hedge, field-margin boundary, and within the transect at 2, 4, 8, 16, 32, and 64 m from the hedge boundary.
  - Sampling considered field-use treatments (e.g., CAL, UAL, Ctrl, NTL-A, CTL_A) where applicable, with April 2015 baseline from control land use prior to treatment strip creation.

- Collection methods and field instrumentation
  - Earthworm sampling: soil block (18 x 18 x 15 cm) lifted at each distance; diluted allyl isothiocyanate applied to enhance collection of deeper-dwelling species; 30-minute exposure; hand-sorting used to collect worms.
  - Preservation and identification: earthworms stored in 80% ethanol; adults with clitellum identified using Sims & Gerard keys; juveniles grouped by functional type (epigeic, endogeic, anecic).
  - Biomass: counting of earthworms used to derive biomass from December 2015 onward.
  - Soil measurements: moisture and temperature recorded at 5 and 10 cm depths around each pit (ThetaProbe soil moisture sensor; Checktemp 1 temperature probe); bulk density measured at 5 and 10 cm using density rings; oven-dried to 105°C for 24 hours to compute bulk density.
  - Sampling protocol: earthworm-free soils returned to pits; sample position recorded to prevent re-sampling the same spot later.

- Data recording and structure (general)
  - Data files contain detailed coding to locate samples by field, strip, and distance, plus environmental measurements and earthworm data.
  - A consistent approach is used to document sample position relative to hedges and margins to enable self-contained spatial analysis.

- Specific data files and schemas
  - April2015_earthworm_Soil data.csv
    - 9 columns: Date, Field_name, SBH_code, X, Y, ZZ, Distance, Soil_Temp_10cm, soil_moisture_1, soil_moisture_2, soil_moisture_3, plus any blanks for missing data.
    - SBH_code encodes Field (X), Strip (Y), and Sample location (ZZ) with defined codes; Distance denotes metres from hedge.
    - April 2015 sampling used control land use; pre-designated strip and distances recorded.
  - Dec2015_Earthworm_Soil data.csv
    - 10 columns: Date, SBH_code, X, Y, ZZ, Field_name, Strip, Distance, Soil_temp_5cm_1, Soil_temp_10_cm_1, moisture_5cm_depth_1, moisture_5_cm_depth_2, moisture_5_cm_depth_3, moisture_10_cm_depth_1, moisture_10_cm_depth_2, moisture_10_cm_depth_3, with blanks for missing data.
    - Adds depth- and strip-specific fields; continues to use the Hedge/Margin distance coding.
  - April2016_Earthworm_Soil data.csv; April2017_Earthworm_Soil data.csv; July2016_Earthworm_Soil data.csv; Oct2016_Earthworm_Soil data.csv
    - Each has 15 columns: Date, SBH_code, X (field), Y (strip), ZZ (sample location), Field_name, Strip, Distance, Soil_temp_5cm_1, Soil_temp_10_cm_1, moisture_5_cm_depth_1, moisture_5_cm_depth_2, moisture_5_cm_depth_3, moisture_10_cm_depth_1, moisture_10_cm_depth_2, moisture_10_cm_depth_3, with depth- and location-specific measurements.
  - The following earthworm count files: April2015_EW_count.csv, April2016_EW_count.csv, April2017_EW_count.csv, Dec2015_EW_count.csv, July2016_EW_count.csv, Oct2016_EW_count.csv
    - 31 columns: Date, SBH_code, X (field), Y (strip), ZZ (sample location), Field_name, Strip, Distance, Depth (Mustard or Topsoil), Sample_type (abundance A or biomass B), plus abundance/biomass counts for numerous species.
    - Species columns are coded (e.g., END-Al-chl for endogeic Allolobophora chlorotica; END-Ad-esi for endogeic Allolobophoridella eiseni; ANE-Ap-noc for anecic Aporrectodea caliginosa nocturna; etc.) and grouped by functional categories:
      - Endogeic (e.g., END-...), Epigeic (e.g., EPI-...), Anecic (e.g., ANE-...).
  - Depth and sampling notes
    - Depth field indicates Mustard (P) or Topsoil (S) sampling.
    - Sample_type indicates whether data represent abundance/count (A) or biomass (B).
    - Blank cells indicate missing data.
  - Miscellaneous references
    - Functional groups: Endogeic (soil-living, horizontal burrowing), Epigeic (litter-living), Anecic (soil-living, deep vertical burrows).
    - Taxonomic references: Sims & Gerard (1999); Zaborski (2003); Pelosi et al. (2008).

- Data accuracy and usage notes
  - The dataset is designed for longitudinal analysis of earthworm populations and soil properties across changing land uses, with careful documentation of sampling positions and methods to facilitate reproducibility and re-use.
  - Position-recording and standardized distance measures support spatial analyses within and between fields across sampling occasions.