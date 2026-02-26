# Physical, chemical and biological data from peatland ponds, Pennines, UK, 2012-2014

- A dataset accompanying Beadle et al. (in press) that documents biological, physical, and chemical data from peatland ponds in the Pennine hills of northern England, collected 2012–2014.
- Biological data: invertebrate abundances (macroinvertebrates) per pond.
- Physical data: geography, pond morphology, and vegetation cover.
- Chemical data: concentrations of dissolved ions, nutrients, and related solutes.

## What was recorded and data format

- Recorded data types:
  - Biological: invertebrate taxa abundances (species-level where possible; Chironomidae may be sub-sampled when abundant).
  - Physical: location, altitude, aspect, pond dimensions (long/short axis, perimeter), estimated volume, pond age, habitat metrics.
  - Chemical: dissolved oxygen, water temperature, pH (with one sensor failure later corrected), total nitrogen (TN), total phosphorus (TP), dissolved organic carbon (DOC), aluminum (Al), iron (Fe), silica (Si), and vegcover.
- Data are stored in four CSV files with consistent pond identifiers and cross-file linkage.

## Study location and sampling design

- Study area: peatland ponds in the Pennine hills, northern England.
- Study sites (six): Moor House, Tennant Gill, Cold Fell, Yad Moss, Halton Lea, Oughtershaw Beck. Several ponds are natural (denoted with an 'n') or part of chronosequences; restoration years and pond ages are provided where applicable.
- Sampling regime:
  - Chronosequence sampling across six peatlands: two monthly visits per year for 2013–2014 (April/2013 to June/2014; ages 4–18 months); one month affected by snow (month 14).
  - On each visit, five ditches per site were sampled and one pond per ditch selected at random.
  - Ponds were small (≤3 m²) and disturbed during sampling; independent ponds were sampled on each visit and marked.
  - 20 naturally-formed ponds across four peatlands were studied in 07/2012 (non-random due to landowner access).
- Total ponds sampled: 105.

## Data collection methods

- Biological sampling:
  - Two-minute macroinvertebrate samples across mesohabitats (open water, floating vegetation, littoral vegetation, bottom sediments) plus one minute additional surface search.
  - Samples preserved in 70% methylated spirits and identified to species level where possible.
  - Chironomidae subsampling (n ≈ 50) when total Chironomidae > 50 for finer taxonomic resolution.
- Physical measurements:
  - Altitude and location recorded with a Garmin GPS; aspect derived from coordinates.
  - Pond dimensions measured on-site; depth measurements (minimum, maximum, mean) taken with a tape; approximate volume estimated from area × mean depth.
  - Vegetation cover estimated visually on-site.
- Chemical measurements:
  - On-site: dissolved oxygen, water temperature, and pH using a portable meter (HACH HQ30d).
  - Lab analyses (on a 50 mL filtered sample): TN, TP, DOC, Al, Fe, Si using standardized instruments (Analytikjena multi N/C 2100, San++ AF Analyzer, ICP-OES).
- Data completeness and correction:
  - pH sensor failure in month 12; missing pH values imputed using the relationship pH ~ [Mg] across other samples (r = 0.81).

## Data structure and file contents

- Four CSV files:
  - Chron_nat_inverts.csv (82 columns): pond code plus abundances for all invertebrate taxa; pond codes include site prefixes and ‘n’ denotes natural ponds.
  - MH_inverts.csv (45 columns): pond code plus taxa abundances for chronosequence ponds.
  - Chron_natural_physical_chemical.csv (26 columns):
    - A: pond code; B: location; C: sampling date; D: pond age (years); E-G: coordinates; H: aspect; I: elevation; J-O: pond dimensions; P: pond volume (m³); Q: water temperature (°C); R: DO (mg/L); S: pH; T-Y: dissolved solutes (mg/L).
  - MH_physical_chemical.csv (26 columns):
    - pool/site mapping; date; pond age (years); OS Grid Ref and coordinates (easting/northing); habitat metrics (aspect, vegcover); depth metrics (mindepth, maxdepth, meandepth); pond dimensions (longaxis, shortaxis, perimeter, volume); chemical measurements (temp, do, ph, tn, tp, doc, al, fe, si); vegcover (visual %).
- Cross-file linkage:
  - The pond code in Chron_nat_inverts.csv and MH_inverts.csv matches the pond code in the corresponding physical–chemical files (Chron_natural_… and MH_…).
- Data standards:
  - Units and methodology summarized in the 26-column files; OS Grid references used for location; pond age and restoration year recorded where applicable.

## Data quality and governance

- Quality controls:
  - Macroinvertebrate identifications independently verified by experts.
  - Field sensor calibrations (DO, temperature, pH) conducted before each visit.
  - Laboratory instruments calibrated with standards covering and extending the sample range.
- Completeness:
  - Overall dataset is complete, with five pH values estimated post hoc due to sensor failure.
- Provenance and documentation:
  - Full methodological details described in Beadle et al. (in press); metadata include sampling dates, pond age, site restoration year, and exact coordinates.
  - Data include both chronosequence and naturally formed ponds, with clear site-specific context (e.g., elevations, restoration years, pond ages).

## Usage and considerations for data management

- Suitability for analyses linking aquatic invertebrate communities to physico-chemical context across a peatland restoration chronosequence.
- Rich, structured linkage between biological and environmental data enabling alpha/beta diversity analyses and community–environment associations.
- Important considerations:
  - Some ponds are natural or NA for restoration age; treat accordingly in analyses.
  - pH data gaps addressed via imputation; consider uncertainty in models incorporating pH.
  - Data are site-specific to Pennine peatlands; if generalizing, account for local environmental conditions.
- Access and citation:
  - Data linked to the Beadle et al. study; use the Beadle et al. reference for context and methods when reusing these data.