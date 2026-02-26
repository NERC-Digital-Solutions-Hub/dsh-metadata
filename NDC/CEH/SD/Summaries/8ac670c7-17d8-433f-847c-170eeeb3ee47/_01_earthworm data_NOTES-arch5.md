# Experimental Design/Sampling Regime

- Seven fields were sampled prior to conversion transects being established in April 2015, with follow-up sampling in April 2016 and April 2017. Temporal sampling also occurred in December 2015 (winter), July 2016 (summer) and October 2016 (autumn), providing a sampling window from the April 2015 baseline through to April 2017.
- At all sampling occasions, earthworm and soil samples were taken from 8 locations per transect: under the hedgerow and the field-margin boundary at the head of each 70 m transect, plus within the transects at 2, 4, 8, 16, 32 and 64 m from the hedge.
- One arable field (BSSE) and one pasture field (SP) were included for temporal sampling, with these fields under continuous arable or permanent pasture since the 1970s.
- April 2015 sampling occurred before treatment strips were fully established; later sampling locations reflect pre-designated strips and distances.

## Collection methods / fieldwork instrumentation

- Earthworm sampling used a soil block (18 x 18 x 15 cm) collected at each distance, with dilute allyl isothiocyanate poured into each pit to aid recovery of deeper-dwelling species; earthworms were hand-sorted, observed for 30 minutes, stored in 80% ethanol, and adults were identified using Sims & Gerard (1999) keys. Juveniles were grouped into functional groups (epigeic, endogeic, anecic). Biomass was recorded from December 2015 onwards.
- Soil moisture and temperature were measured around the excavated pit at 5 cm and 10 cm depths using a ThetaProbe soil moisture sensor and a Checktemp thermometer.
- Soil bulk density was measured at 5 cm and 10 cm depths using 118 cm³ rings; bulk density was calculated from oven-dried weights (105°C, 24 h).
- Earthworm-free soils were returned to their pits and sample positions were recorded to avoid resampling the same location later.

## Nature and units of recorded values

- Values include: date, field, location code (SBH_code) combining field, strip and distance codes, sample position (hedge, margin, or distance from hedge), field name, strip/treatment designation, and environmental measurements (soil temperature and moisture at specified depths, bulk density at specified depths).
- Measurements are recorded with explicit depth references (5 cm, 10 cm), and moisture readings in millivolts (for three positions) and temperature in degrees Celsius.
- Blank cells indicate missing data.

## Details of data structure and key files

- April2015_earthworm_Soil data.csv
  - 9 columns: Date, Field_name, SBH_code, X, Y, ZZ, Distance, Soil_Temp_10cm, soil_moisture_1-3 (and related fields for year-specific structure).
  - Codes map fields to: BSSE, BSSW, Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field; strips and sample locations (Hedge, Margin, 2m, 4m, 8m, 16m, 32m, 64m).
- Dec2015_Earthworm_Soil data.csv
  - 10 columns: Date, SBH_code, Field_name, Strip, Distance, Hedge/Margin, Soil_temp_5cm_1, Soil_temp_10_cm_1, moisture_5cm_depth_1-3, etc.
  - Includes Strip designations (CAL, UAL, Ctrl, NTL-A, CTL-A) and notes on sampling context.
- April2016_Earthworm_Soil data.csv; April2017_Earthworm_Soil data.csv; July2016_Earthworm_Soil data.csv; Oct2016_Earthworm_Soil data.csv
  - Each includes 15 columns: Date, SBH_code, Field_name, Strip, Distance, Hedge/Margin, Field-specific identifiers, Field_name, and depth-related measurements (moisture_5cm_depth_1-3, moisture_10_cm_depth_1-3, Soil_temp_5cm_1, Soil_temp_10_cm_1, Bulk_density_5cm, Bulk_density_15cm).
  - Similar coding for field, strip, distance, and sample positions as above.
- The files: April2015_EW_count.csv; April2016_EW_count.csv; April2017_EW_count.csv; Dec2015_EW_count.csv; July2016_EW_count.csv; Oct2016_EW_count.csv
  - 31 columns: Date, SBH_code, Field_name, Strip, Distance, Depth (Mustard or Topsoil), Sample_type (abundance A or biomass B), plus a set of columns for earthworm taxa.
  - Columns enumerate the abundance or biomass per species, with functional group and species names encoded (e.g., END-Al-chl Allolobophora chlorotica; END-Ad-esi Allolobophoridella eiseni; ANE-Ap-noc Aporrectodea caliginosa nocturna; and many others across Endogeic, Epigeic, and Anecic groups).
  - The dataset supports species-level counts/biomass and functional-group summaries across the sampling events.
- Earthworm functional groups and species coverage
  - Endogeic, Epigeic, and Anecic groups are recorded with species-level detail for a broad range of earthworms (e.g., Allolobophora chlorotica, Aporrectodea caliginosa, Lumbricus terrestris, Eisenia fetida, Dendrodrilus rubidus, etc.).
  - Miscellaneous notes provide the functional group definitions (habitat and burrowing behavior).

## Treatments, field context and temporal coverage

- Treatments/strips include:
  - CAL: connected arable ley strip in an arable field
  - UAL: unconnected arable strip in an arable field (earthworm barrier to bedrock at field-margin boundary)
  - Ctrl: control land use (arable in arable field or pasture in pasture field)
  - NTL-A: "no till" tillage strip in a pasture field
  - CTL_A: conventional tillage strip in a pasture field
- NB: April 2015 sampling used control land use, as treatment strips had not yet been created; samples were taken from pre-designated strips and distances.
- Spatial design includes hedgerows, margins, and transects extending up to 64 m from field margins, with data collected across multiple fields: BSSE (Big Substation East), BSSW (Big Substation West), Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field.
- Temporal coverage spans:
  - Baseline: April 2015
  - Follow-ups: April 2016, April 2017
  - Additional temporal snapshots: December 2015, July 2016, October 2016

## Data governance, provenance and usage notes

- Data are structured for cross-field, cross-year comparability with explicit coding for fields, strips, locations, and sampling positions.
- Documentation includes explicit definitions of field codes, strip types, and sampling positions ( Hedge vs Margin; distances from hedge).
- Blank cells denote missing data; explicit notes clarify treatment contexts and sampling conditions (e.g., April 2015 sampling from control land use; timing of strip establishment).
- References cited for earthworm taxonomy and methodology: Sims & Gerard (1999); Zaborski (2003); Pelosi et al. (2008).

## References

- Sims, S. & Gerard, B. (1999). Earthworms.
- Zaborski, 2003.
- Pelosi et al., 2008.