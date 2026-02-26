# Experimental Design/Sampling Regime

- Study scope and timeline
  - Seven fields were sampled before conversion transects were established in April 2015, with follow-up sampling in April 2016 and April 2017.
  - Additional temporal sampling occurred in December 2015 (winter), July 2016 (summer), and October 2016 (autumn), creating a temporal window from April 2015 baseline to April 2017.
  - Data indicate annual changes in these fields were representative of changes in the other study fields.

- Sampling design and locations
  - At each sampling occasion, earthworm and soil samples were collected from 8 locations per field: under the hedge, the margin at the head of each 70 m transect, and within the transect at 2, 4, 8, 16, 32, and 64 m from the field-margin boundary.
  - Distance is measured in metres from the hedge; hedge and margin are specific sampling positions.
  - Fields: BSSE (Big Substation East), BSSW (Big Substation West), Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field.
  - Presence of treatment strips across fields includes CAL (connected arable ley strip), UAL (unconnected arable strip with earthworm barrier), Ctrl (control land use), NTL-A (no till), CTL-A (conventional till).

- Temporal and baseline considerations
  - April 2015 sampling occurred before treatment strips were created; samples were taken from pre-designated strips and distances.
  - The study assumes that changes observed in arable and pasture fields reflect broader field responses over time.

- Field and measurement details
  - Earthworm sampling: a soil block (18 × 18 × 15 cm) was hand-sorted to collect worms; allyl isothiocyanate was used to aid collection of deeper-dwelling species; observation period lasted 30 minutes.
  - Identification and categorization: adults with a clitellum identified to species; juveniles classified into functional groups (epigeic, endogeic, anecic).
  - Biomass: earthworm biomass was recorded as the number of individuals from December 2015 onward.
  - Soil measurements: soil moisture (ThetaProbe) and soil temperature measured at specified depths (5 cm and 10 cm, depending on the sampling file); bulk density measured at 5 cm and 10 cm with standard rings.

- Data structure and file overview
  - Multiple CSV files capture different aspects of the data (earthworm counts/biomass, soil properties, and site metadata) across time points.
  - Location coding: SBH_code encodes field, strip, and distance in a consistent XYZZ format; X maps to field, Y to strip, ZZ to distance location (hedge, margin, 2 m, 4 m, 8 m, 16 m, 32 m, 64 m).
  - Field names: abbreviations for Big Substation East/West fields (BSSE, BSSW) and full field names elsewhere.
  - Treatment strip descriptions and the evolution of strips are documented (CAL, UAL, Ctrl, NTL-A, CTL_A).

- Detailed data files and schemas
  - April2015_earthworm_Soil data.csv: 9 columns (Date, Field_name, SBH_code, Distance, soil properties, and related measurements); includes 70 m transect context and sampling positions (Hedge, Margin, 2, 4, 8, 16, 32, 64 m).
  - Dec2015_Earthworm_Soil data.csv: 10 columns; adds Field_name, Strip, and distance-context details; includes 5 cm and 10 cm soil measurements.
  - April2016_Earthworm_Soil data.csv, April2017_Earthworm_Soil data.csv, July2016_Earthworm_Soil data.csv, Oct2016_Earthworm_Soil data.csv: 15 columns; expanded soil measurements (moisture and temperature at 5 cm and 10 cm) and bulk density at 5 cm and 15 cm; retains SBH_code and distance-positioning.
  - Earthworm counts files: April2015_EW_count.csv, April2016_EW_count.csv, April2017_EW_count.csv, Dec2015_EW_count.csv, July2016_EW_count.csv, Oct2016_EW_count.csv: 31 columns; include Date, SBH_code, field/strip location, distance, Depth (Mustard P or Topsoil S), Sample_type (abundance A or biomass B), and a comprehensive set of species-level columns with functional-group mappings.
  - Species and functional groups
    - Endogeic, Epigeic, and Anecic groupings with numerous species names (e.g., Allolobophora chlorotica, Aporrectodea caliginosa, Lumbricus spp., Eisenia fetida, etc.).
    - Column codes reflect functional group and species name (e.g., END-Al-chl for endogeic Allolobophora chlorotica; EPI-E-fet for epigeic Eisenia fetida; ANE-L-ter for anecic Lumbricus terrestris; and many others covering a broad taxonomic scope).

- Data quality notes and usage considerations
  - Blank cells denote missing data.
  - Data span pre-conversion baselines and multiple post-conversion timepoints, enabling temporal trend analyses.
  - Codes and tables document mapping between field codes, strip positions, sampling locations, and treatments, which is essential for data harmonization and cross-field comparisons.
  - Data support analysis of earthworm community composition, functional group dynamics, and soil property associations across spatial scales (hedge to 64 m) and temporal scales (2015–2017).

- Miscellaneous and references
  - Earthworm functional groups: Endogeic (soil-living, horizontal burrowing), Epigeic (litter-living), Anecic (soil-living, deep vertical burrows).
  - References cited for methods: Sims & Gerard (1999); Zaborski (2003); Pelosi et al. (2008).