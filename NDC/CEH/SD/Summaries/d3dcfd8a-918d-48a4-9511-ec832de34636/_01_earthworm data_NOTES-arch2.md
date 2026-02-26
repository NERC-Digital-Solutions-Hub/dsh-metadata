# Experimental Design/Sampling Regime

- Study design across seven fields with sampling before and after land-use conversions: baseline in April 2015, follow-up in April 2016 and April 2017, with additional temporal sampling in winter 2015, summer 2016, and autumn 2016. This creates a temporal window from the April 2015 baseline through April 2017 to represent changes across the study fields.
- Spatial framework: within each sampling occasion, earthworm and soil samples collected from 8 locations per field: under the hedgerow, at the field-margin boundary, and at 2, 4, 8, 16, 32, and 64 m from the field-margin along 70 m transects.
- Temporal and field-specific replication: one arable field (BSSE) and one pasture field (SP) received additional temporal sampling; these fields have long-standing arable or permanent pasture history since the 1970s.
- Data structure focus: multiple CSV data files track earthworm counts and biomass, soil properties, and spatial-temporal metadata to support standardized monitoring and trend analysis.

## Sampling locations and temporal coverage

- Locations per sampling occasion: hedge, margin, and distances of 2, 4, 8, 16, 32, and 64 m from hedge along transects.
- Transect design: 70 m length; samples collected to represent field-margin boundary conditions and interior transects.
- Seasonal and date range: baseline April 2015; follow-ups April 2016 and April 2017; plus December 2015 (winter), July 2016 (summer), October 2016 (autumn) to extend temporal coverage.

## Earthworm and soil collection methods

- Earthworm sampling: remove soil blocks (18 × 18 × 15 cm) at each distance; use dilute allyl isothiocyanate to stimulate emergence and collect deeper-dwelling species; monitor earthworm appearance for 30 minutes.
- Specimen handling: store in 80% ethanol; identify adults with clitellum using Sims & Gerard (1999) keys; juveniles assigned to functional groups (epigeic, endogeic, anecic); biomass recorded from December 2015 onward.
- Soil measurements at each pit: soil moisture (via ML3 ThetaProbe) and temperature (Checktemp1) at 5 cm and 10 cm depths; bulk density measured at 5 cm and 10 cm using bulk density rings with oven-dried weight data (105°C for 24 h).
- Sampling integrity: earthworm-free soils returned to original pits; sample positions tracked to avoid re-sampling same location.

## Measurements and instruments

- Soil temperature: measured at 5 cm and 10 cm depths; temperature probes specified.
- Soil moisture: measured at 5 cm and 10 cm depths; moisture reported in millivolts per sensor readings.
- Bulk density: measured at 5 cm and 10 cm depths; calculated from oven-dried mass.
- Earthworm processing: hand-sort within soil blocks; adult species identified; functional grouping for juveniles.

## Data captured and structure

- April2015_earthworm_Soil data.csv: 9 columns (Date, Field_name, SBH_code, X, Y, ZZ, Distance, and soil/temperature/moisture fields); notes on treatment strips not yet created; blanks indicate no data.
- Dec2015_Earthworm_Soil data.csv: 10 columns; includes Field_name, Strip (treatment type), Distance, Hedge/Margin, Soil_temp_5cm/10cm, moisture readings (5 cm and 10 cm), etc.
- April2016_Earthworm_Soil data.csv; April2017_Earthworm_Soil data.csv; July2016_Earthworm_Soil data.csv; Oct2016_Earthworm_Soil data.csv: 15 columns; expanded with more detailed field, strip, distance, and soil measurements.
- Data files for earthworm counts: April2015_EW_count.csv; April2016_EW_count.csv; April2017_EW_count.csv; Dec2015_EW_count.csv; July2016_EW_count.csv; Oct2016_EW_count.csv: 31 columns; counts/biomass per species across sites, strips, distances, and dates.
- Field identifiers: SBH_code encodes field (BSSE, BSSW, Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field) and strip positions (Left, Central, Right); ZZ encodes sample location (Hedge, Margin, 2m, 4m, 8m, 16m, 32m, 64m).
- Species and functional groups: records for Endogeic, Epigeic, and Anecic earthworms with detailed species names (e.g., Allolobophora chlorotica, Aporrectodea caliginosa, Lumbricus terrestris, Eisenia fetida, etc.) and corresponding functional group codes (END-, EPI-, ANE-).

## Field treatment context

- Strip classifications: CAL (connected arable ley strip in an arable field), UAL (unconnected arable strip with earthworm barrier to bedrock), Ctrl (control land use: arable or pasture), NTL-A (no-till strip in pasture), CTL_A (conventional tillage strip in pasture).
- Design note: April 2015 sampling was from control land use as treatment strips had not yet been created; samples were taken from pre-designated strips and distances.

## Notable notes

- Data standardization focus: alignment with pre-defined sampling positions (hedge, margin, distances) to ensure comparability across fields and years.
- Data accessibility and reuse considerations: dataset structure and explicit field/strip coding facilitate integration with external datasets and support cross-site analyses.

## Earthworm functional groups and taxa (miscellaneous)

- Functional groups defined: Endogeic (soil-living, horizontal burrows), Epigeic (litter-living), Anecic (soil-living, deep vertical burrows).
- Referenced taxonomic keys and literature: Sims & Gerard (1999); Zaborski (2003); Pelosi et al. (2008).

## References

- Sims, S. & Gerard, B. 1999
- Zaborski, A. 2003
- Pelosi, L. et al. 2008