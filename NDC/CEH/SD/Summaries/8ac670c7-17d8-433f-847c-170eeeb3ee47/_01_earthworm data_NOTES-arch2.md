# Experimental Design/Sampling Regime

- Objective: Document a long-term, standardized dataset to monitor soil health and earthworm communities across multiple fields and land-use treatments, enabling assessment of environmental health and policy performance over time.

- Study scope: Seven fields sampled before conversion transects were established (April 2015), with follow-up sampling in April 2016 and April 2017. Temporal sampling also occurred in December 2015 (winter), July 2016 (summer), and October 2016 (autumn). Baseline measurements started prior to treatment strips being created in 2015.

- Sampling framework:
  - For earthworms and soil, samples collected from 8 locations per transect: under hedgerow and field-margin head, plus 2, 4, 8, 16, 32, and 64 m from the field-margin boundary along the transect.
  - In each sampling occasion, transects ran through 70 m field boundaries.

- Field locations and treatments:
  - Fields include BSSE (Big Substation East), BSSW (Big Substation West), Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field.
  - Treatments include CAL (connected arable ley strip), UAL (unconnected arable strip with bedrock-depth earthworm barrier), Ctrl (control land use), NTL-A ("no till" strip), CTL_A (conventional tillage strip).
  - Note: April 2015 sampling came from control land use as strips were not yet created; pre-designated strip locations and distances were used.

- Data collected:
  - Earthworm sampling: hand-sorted from a soil block (18 x 18 x 15 cm); using dilute allyl isothiocyanate to mobilize deeper species; identification of adults to species (Sims & Gerard 1999) with juveniles grouped into functional groups (epigeic, endogeic, anecic); biomass recorded from December 2015 onward.
  - Soil measurements: moisture (ML3 ThetaProbe) and temperature (Checktemp) at 5 cm and 10 cm depths; bulk density at 5 cm and 10 cm depths using standard rings; soils returned to original pits with position tracked to avoid re-sampling.

- Sampling targets and outputs:
  - Temporal continuity across years to assess changes over time and under different treatments.
  - Outputs include earthworm abundance and biomass, species composition (functional groups and species names), soil moisture, soil temperature, and bulk density.

- Data management and quality:
  - Data are structured and stored in multiple CSV files with explicit field codes and location identifiers to standardize cross-year comparisons.
  - Sampling position and depth data are maintained to support reproducibility and spatial analyses.
  - Earthworm identification follows established taxonomic keys; juvenile data aggregated by functional group.

- Data availability and structure overview:
  - Earthworm/soil data files (sampled across years):
    - April2015_earthworm_Soil data.csv (9 columns): Date, Field_name, SBH_code, X, Y, ZZ, Distance, Soil_Temp_10cm, soil_moisture_1-3.
    - Dec2015_Earthworm_Soil data.csv (10 columns): Date, SBH_code, X, Y, ZZ, Field_name, Strip, Distance, Soil_temp_5cm_1, Soil_temp_10_cm_1, moisture_5cm_depth_1 (plus related fields).
    - April2016_Earthworm_Soil data.csv, April2017_Earthworm_Soil data.csv, July2016_Earthworm_Soil data.csv, Oct2016_Earthworm_Soil data.csv (each with 15 columns): Date, SBH_code, X, Field_name, Y, Strip, ZZ, Distance, Depth indicators (P/S), Soil_temp/moisture at 5 cm and/or 10 cm, bulk_density at specified depths, etc.
  - Earthworm count data files (31 columns):
    - April2015_EW_count.csv, April2016_EW_count.csv, April2017_EW_count.csv, Dec2015_EW_count.csv, July2016_EW_count.csv, Oct2016_EW_count.csv.
    - Each includes Date, SBH_code, X, Y, ZZ, Field_name, Strip, Distance, Depth, Sample_type, and species- or group-specific abundance or biomass values (e.g., END-Al-chl Allolobophora chlorotica; EPI-L-rub Lumbricus rubellus; ANE-L-ter Lumbricus terrestris; etc.).
  - Miscellaneous: definitions of earthworm functional groups (Endogeic, Epigeic, Anecic) and references (Sims & Gerard 1999; Zaborski 2003; Pelosi et al. 2008).

- Data applicability for analysts:
  - The dataset supports standardized environmental monitoring across multiple years, fields, and treatments.
  - Outputs suitable for reports, maps, and charts to evaluate environmental health and policy performance over time.
  - Datasets are prepared for storage in appropriate data portals, with explicit data structure facilitating integration with other relevant environmental data.