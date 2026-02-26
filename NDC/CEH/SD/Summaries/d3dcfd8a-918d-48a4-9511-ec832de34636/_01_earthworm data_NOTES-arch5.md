# Experimental Design/Sampling Regime

- Overview
  - Describes earthworm and soil sampling across seven fields, with transects and multiple distances from the field-margin boundary.
  - Sampling occurred before conversion transects were established (April 2015), then in April 2016 and 2017, plus additional temporal sampling in December 2015, July 2016, and October 2016.
  - At each occasion, 8 sampling locations per field were used: under the hedgerow, at the head margin, and along transects at 2, 4, 8, 16, 32, and 64 m from the hedge.
  - Temporal sequence spans baseline (April 2015) through April 2017 to capture changes across fields.

- Experimental Design and Temporal/Spatial Layout
  - Seven fields include hedgerows, field margins, and transects up to 70 m from the hedge.
  - Temporal sampling spans winter, summer, and autumn (e.g., December 2015, July 2016, October 2016) to track seasonal variation.
  - Treatment context described via field codes and strip classifications (e.g., CAL, UAL, Ctrl, NTL-A, CTL_A) with notes on design progression (April 2015 sampling from control land uses; designation of treatment strips occurred after baseline sampling).

- Collection Methods and Field Instrumentation
  - Earthworm sampling:
    - Soil blocks (18 x 18 x 15 cm) collected at each distance; hand-sorting to extract earthworms.
    - Dilute allyl isothiocyanate used to facilitate collection of deeper-dwelling species; 30-minute monitoring per pit.
    - Specimens stored in 80% ethanol; adults identified using Sims & Gerard keys; juveniles grouped by functional group (epigeic, endogeic, anecic).
    - Biomass recorded from December 2015 onward (counted as individuals).
  - Soil measurements:
    - Soil moisture and temperature recorded around the pit at 5 and 10 cm depth.
    - Soil moisture measured with ML3 ThetaProbe; temperature with Checktemp1.
    - Bulk density determined at 5 and 10 cm depths using steel rings; density calculated from oven-dried samples (105°C for 24 h).
    - Earthworm-free soils returned to pits; position tracked to avoid re-sampling the same spot.

- Nature and Units of Recorded Values
  - Values are described in the data structure details (see below).

- Data Structure and Files
  - April2015_earthworm_Soil data.csv
    - 9 columns: Date, Field_name, SBH_code, X (field code), Y (strip), ZZ (sample location), Distance, Soil_Temp_10cm, soil_moisture_1, soil_moisture_2, soil_moisture_3, etc. (blank cells = no data).
  - Dec2015_Earthworm_Soil data.csv
    - 10 columns: Date, SBH_code, Field_name, Strip, Distance, Hedge/Margin context, Soil_temp_5cm_1, Soil_temp_10_cm_1, moisture_5cm_depth_1, moisture_5_cm_depth_2, moisture_5_cm_depth_3, etc. (blank cells = no data).
  - April2016_Earthworm_Soil data.csv; April2017_Earthworm_Soil data.csv; July2016_Earthworm_Soil data.csv; Oct2016_Earthworm_Soil data.csv
    - Each file has 15 columns: Date, SBH_code, X, Y, ZZ, Field_name, Strip, Distance, Depth, Sample_type, plus multiple soil moisture/temperature measurements and other metadata (blank cells = no data).
  - Remaining earthworm data files: April2015_EW_count.csv; April2016_EW_count.csv; April2017_EW_count.csv; Dec2015_EW_count.csv; July2016_EW_count.csv; Oct2016_EW_count.csv
    - Each file has 31 columns: Date, SBH_code, X, Y, ZZ, Field_name, Strip, Distance, Depth, Sample_type, followed by abundance/biomass counts for 30+ earthworm species.
    - Columns are named to reflect functional groups and species (e.g., END-Al-chl = endogeic Allolobophora chlorotica, EPI-E-fet = epigeic Eisenia fetida, etc.).
  - Miscellaneous
    - Earthworm functional groups defined (Endogeic, Epigeic, Anecic) with examples of representative species.
  - References
    - Key taxonomic and methodological references (Sims & Gerard 1999; Zaborski 2003; Pelosi et al. 2008).

- Coding, Metadata, and Data Quality
  - Coding scheme for sampling locations:
    - SBH_code encodes X (field), Y (strip), and ZZ (sample location) as combinations to identify precise sampling sites.
    - Distance denotes metres from hedge; Hedge (H) and Margin (M) labels indicate sampling contexts.
  - Strip and treatment context:
    - Strip values (CAL, UAL, Ctrl, NTL-A, CTL-A) describe arable/pasture strip treatments; NB note that April 2015 samples were from control land uses as strips were not yet created.
  - Units and measurements:
    - Distances: metres from hedge.
    - Temperature: degrees Celsius.
    - Moisture: millivolts (sensor output).
    - Bulk density: g cm^-3.
  - Data completeness:
    - Blank cells indicate missing data.
    - Position-tracking ensures no duplicate sampling of the same location across surveys.

- Data Stewardship and Governance Considerations (from a Data Steward perspective)
  - Metadata completeness:
    - Ensure codebooks for SBH_code (field/strip/location encodings) are preserved and accessible.
    - Document strip/treatment design history and NB notes (e.g., April 2015 sampling from control land uses).
  - Provenance and lineage:
    - Capture sampling dates, field identifiers, transect geometry, and equipment details to enable traceability.
  - Data quality control:
    - Maintain standards for earthworm identification keys, measurement protocols, and sample storage conditions.
    - Record QA steps and any deviations from protocol.
  - Interoperability and standardization:
    - Harmonize units across files (e.g., ensure moisture and temperature columns are consistently named and scaled).
    - Maintain consistent species naming and functional-group mappings across all EW_count files.
  - Accessibility and reuse:
    - Provide clear data dictionaries and column-level definitions; reference external taxonomic keys where appropriate.
    - Note blank/missing data handling and any imputation assumptions if later used for analyses.
  - Versioning and updates:
    - Track revisions to data files and any corrections to field codes or column mappings.

- References
  - Earthworms by Sims & Gerard (1999); Zaborski (2003); Pelosi et al. (2008).