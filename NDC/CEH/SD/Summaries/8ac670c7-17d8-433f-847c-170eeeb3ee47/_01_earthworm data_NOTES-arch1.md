# Experimental Design/Sampling Regime

- Seven fields were sampled before conversion transects were established in April 2015, with follow-up sampling in April 2016 and April 2017.
- Temporal sampling occurred in one arable field (BSSE) and one pasture field (SP): December 2015 (winter), July 2016 (summer), and October 2016 (autumn), providing a temporal span from April 2015 baseline to April 2017.
- At every sampling, earthworm and soil measurements were taken from 8 locations per field along a 70 m transect: under the hedgerow, at the margin, and at 2, 4, 8, 16, 32, and 64 m from the field-margin boundary.

- Collection methods:
  - Earthworm sampling used an 18 x 18 x 15 cm soil block; earthworms were hand-sorted from each pit.
  - Dilute allyl isothiocyanate (1.5 L; 0.1 g L-1) was poured into pits to aid collection of deeper-dwelling species.
  - Earthworms were observed for 30 minutes, stored in 80% ethanol, and adults (with clitellum) identified via Sims & Gerard (1999) keys; juveniles were grouped into functional groups (epigeic, endogeic, anecic).
  - Earthworm biomass was recorded for samples from December 2015 onwards.

- Measurements and field instrumentation:
  - Soil moisture (ML3 ThetaProbe) and soil temperature (Checktemp) at 5 cm and 10 cm depths.
  - Soil bulk density at 5 cm and 10 cm depths using steel rings; bulk density calculated from oven-dry weights (105°C for 24 h).
  - Samples re-buried at original positions to avoid re-sampling.

- Data structure and detailing:
  - Multiple CSV data files record earthworm and soil data across time points and treatments.
  - April 2015 earthworm/soil data file contains 9 columns (Date, Field_name, SBH_code, Y, ZZ, Distance, soil/moisture/temperature variables, etc.).
  - December 2015 earthworm/soil data file contains 10 columns, adding Field_name, Strip, and related metadata.
  - April 2016, April 2017, July 2016, and Oct 2016 files (earthworm/soil) contain 15 columns, consistent with Field_name, Strip, Distance, and depth-related measurements.
  - April 2015 and subsequent months include a standardized coding scheme for SBH_code (field), Y (strip), and ZZ (sample location), with Hedge (H) and Margin (M) as sample contexts.
  - The remaining EW_count files (April 2015, 2016, 2017; Dec 2015; July 2016; Oct 2016) contain 31 columns, including date and the SBH_code, field, strip, distance, depth/type (Mustard or Topsoil), sample type (abundance A or biomass B), and species/functional-group columns.

- Field and treatment context:
  - Fields include: BSSE (Big Substation East), BSSW (Big Substation West), Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field.
  - Treatments across strips include connected arable ley strip (CAL), unconnected arable strip with earthworm barrier (UAL), control land use (Ctrl), no-till strip in pasture (NTL-A), and conventional tillage strip in pasture (CTL-A).
  - Note: April 2015 sampling was from control land use because treatment strips were not yet established; sampling followed pre-designated strips and distances.

- Notable data details:
  - Blank cells indicate no data available.
  - The dataset includes explicit coding for field, strip, distance, and sample position (Hedge, Margin, 2 m, 4 m, 8 m, 16 m, 32 m, 64 m).
  - Earthworm functional groups and species are enumerated (e.g., Endogeic, Epigeic, Anecic; species names like Allolobophora chlorotica, Aporrectodea caliginosa, Lumbricus terrestris, etc.).
  - Miscellaneous: the dataset provides a mapping of functional groups to ecological roles (e.g., Endogeic—soil-living, horizontal burrowing; Epigeic—litter-living; Anecic—deep vertical burrows).

- Data use and accessibility:
  - The data are organized for analysis of spatial and temporal patterns in earthworm communities and soil properties across different land-use strips and hedgerow contexts.
  - Analysts can examine correlations between earthworm abundance/biomass (by species and functional group) and field treatments, distances from hedges, and seasonal timing.
  - Datasets are accompanied by metadata (coding schemes and measurement units) to support reproducibility and discoverability.