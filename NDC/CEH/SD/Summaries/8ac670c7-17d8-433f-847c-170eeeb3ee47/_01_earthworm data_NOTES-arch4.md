# Experimental Design/Sampling Regime

- Longitudinal field study across seven fields with baseline established in April 2015, prior to land-use conversions, and follow-up sampling in April 2016 and April 2017.
- Additional temporal sampling at winter (December 2015), summer (July 2016), and autumn (October 2016) to cover seasonal variation, yielding a temporal window from April 2015 to April 2017.
- Sampling framework: 8 locations per occasion (under hedgerow and field-margin at the head of each 70 m transect, plus sampling along the transect at 2, 4, 8, 16, 32, and 64 m from the field-margin boundary).

## Study design and scope

- Fields include arable and pasture types; two fields (BSSE and SP) provided temporal data but all fields contributed to spatial variation analysis.
- Aimed to capture spatial gradients relative to hedgerows and field margins, plus changes due to land-use treatment strips implemented after April 2015.
- April 2015 samples were from control land uses; subsequent years include designated treatment strips (e.g., CAL, UAL, Ctrl, NTL-A, CTL_A).

## Data collection methods

- Earthworm sampling: soil blocks (18 x 18 x 15 cm) drilled and hand-sorted, with allyl isothiocyanate used to access deeper-dwelling species; monitoring over 30 minutes.
- Specimen handling: adults (with clitellum) identified to species; juveniles grouped into functional groups (epigeic, endogeic, anecic); biomass recorded from December 2015 onward.
- Soil measurements: soil moisture (via ThetaProbe) and soil temperature (Checktemp) at 5 and 10 cm depths; bulk density measured at 5 and 10 cm depths.
- Sample labeling and tracking: positions recorded to prevent re-sampling; samples returned to pits after processing.

## Data structure and files

- Earthworm and soil data files (temporal series):
  - April2015_earthworm_Soil data.csv (9 columns; baseline data with location codes and distances)
  - Dec2015_Earthworm_Soil data.csv (10 columns; includes Field_name, Strip, and depth-related measurements)
  - April2016_Earthworm_Soil data.csv
  - April2017_Earthworm_Soil data.csv
  - July2016_Earthworm_Soil data.csv
  - Oct2016_Earthworm_Soil data.csv
- Each file includes: Date, SBH_code (field/strip/location encoding), field name, sample location ( Hedge, Margin, and distances), field/strip metadata, and environmental measurements (soil temp and moisture) with blanks indicating missing data; some files include bulk density.
- Earthworm counts/biomass files (31 columns):
  - April2015_EW_count.csv
  - April2016_EW_count.csv
  - April2017_EW_count.csv
  - Dec2015_EW_count.csv
  - July2016_EW_count.csv
  - Oct2016_EW_count.csv
- Each EW_count file contains: Date, SBH_code, Field, Strip, Distance, Field_name, and abundance or biomass per species (e.g., END-Al-chl Allolobophora chlorotica, ANE-Ap-noc Aporrectodea caliginosa nocturna, etc.), plus functional group and species mappings.

## Variables and measurements

- Spatial designations:
  - Field codes: BSSE (Big Substation East), BSSW (Big Substation West), Hillside, Copse, Sub Paddock, Warren Paddock, Valley Field.
  - Strips: CAL (connected arable ley strip), UAL (unconnected arable strip with earthworm barrier), Ctrl (control land use), NTL-A (no-till strip in pasture), CTL-A (conventional tillage strip in pasture).
  - Distances from hedge: Hedge, Margin, 2 m, 4 m, 8 m, 16 m, 32 m, 64 m.
- Environmental measurements:
  - Soils: moisture readings (in millivolts) and temperature (°C) at specified depths (5 cm, 10 cm).
  - Bulk density: g/cm3 at 5 cm and at 15 cm (where available).
- Biological measurements:
  - Earthworm counts and/or biomass per sample (adult vs juvenile separation; juvenile assigned to functional groups).
  - Species list includes multiple endogeic, epigeic, and anecic taxa (e.g., Allolobophora chlorotica, Aporrectodea caliginosa, Lumbricus terrestris, Eisenia fetida, etc.).

## Earthworm taxonomy and functional groups

- Functional groups:
  - Endogeic, Epigeic, Anecic with corresponding species mappings (e.g., END-Al-chl = Allolobophora chlorotica; EPI-L-rub = Lumbricus rubellus; ANE-L-ter = Lumbricus terrestris; etc.).
- Species-level data accompanied by functional-group classification for ecological interpretation of soil health and structure.

## Data quality, notes, and caveats

- Blank cells denote missing data.
- April 2015 samples were all from control land uses; treatment strips were introduced subsequently.
- Data are organized across multiple files with consistent coding schemes, but cross-file harmonization may be needed for integrated analyses.
- Depth designation included in later files (e.g., mustard/topsoil in earlier datasets; explicit depth columns in later datasets).

## Data governance and stewardship implications for Data Leaders

- Data assets are rich, multi-temporal, and spatially explicit; define a centralized metadata schema to ensure discoverability and consistency across files.
- Maintain a data dictionary mapping SBH_code codes to field names, strip types, and distances to improve interoperability.
- Harmonize variable naming (e.g., depth indicators, moisture units) across files to support seamless integration and longitudinal analyses.
- Ensure provenance, versioning, and lineage are documented for each file, given updates across years and multiple sampling campaigns.
- Facilitate access and reuse by clearly documenting experimental design, sampling regime, and species-level taxonomy with authoritative references.

## Practical implications for data strategy

- This dataset illustrates the value of comprehensiveMetadata and standardized coding for multi-temporal, multi-site ecological data.
- Potential data products include time-series analyses of earthworm communities, associations with field treatments, hedgerow proximity effects, and soil health indicators.
- Encourages establishing shared ontologies for agricultural soil biodiversity data and promoting data-sharing practices within the wider research community.

## References

- Sims & Gerard (1999)
- Zaborski (2003)
- Pelosi et al. (2008)