# BirdSpecies.csv

## Data overview
- Bird species survey data from 441 sampling points in the Atlantic Forest of Brazil, collected in four replicates per point between December 2015 and February 2017.
- Part of the ECOFOR project (Biodiversity and Ecosystem Functioning in Degraded and Recovering Amazonian and Atlantic Forests), within the NERC HumanModified Tropical Forest programme.

## Sampling design
- 441 sampling points across Vale do Paraíba and Serra do Mar, São Paulo.
- Even distribution across 49 landscapes using a nine-point regular grid with 75 m spacing (where feasible).
- 15 landscapes are controls with a single predominant land-use (native forest, Eucalyptus plantation, pasture) and split evenly among land-use types.
- Remaining 34 landscapes contain native forest fragments embedded within other land-use types.
- Fragmented landscapes include three points in native forest fragment, three at fragment edge, and three in surrounding matrix.
- Two matrix types surveyed: 15 fragments bordering plantation and 19 bordering pasture.
- Fragmented landscapes chosen to represent a range of patch sizes and connectivity.

## Data collection techniques
- Point counts of 15 minutes per survey; all bird species detected within a 25 m radius recorded.
- Four temporal replicates conducted between Dec 2015 and Feb 2017, evenly split between dry and wet seasons.

## Data structure
- Data stored in a single CSV file: BirdSpecies.csv.
- Each row represents an individual sampling point.

## Column headings and contents
- Species columns (267 columns; columns 1–267): Species identity following BirdLife International taxonomy (BirdLife International 2017). Values indicate the number of temporal replicates in which the species was detected.
- LandscapeID: Numeric reference to the landscape containing the sample point.
- HabitatType: I = native forest interior, E = native forest edge, M = matrix. In controls, values indicate transect aggregation for original analysis.
- MatrixType: P = pasture, E = plantation, CF = control forest landscape, CP = control pasture landscape, CE = control plantation landscape.
- X and Y: Coordinates in SAD 1969 UTM 23S; rounded to the nearest kilometre to protect sensitive species locations.

## Taxonomy and references
- Taxonomy aligned with BirdLife International (BirdLife International 2017). Handbook of the Birds of the World and BirdLife International digital checklist (Version 9.1).

## Data governance and stewardship considerations
- Metadata should reflect the BirdLife taxonomy, coordinate reference system (SAD 1969 UTM 23S), temporal coverage (Dec 2015–Feb 2017), and sampling design (9-point grid, 441 points, 4 replicates).
- Clearly document data provenance: field collection methods, QC steps, and any data transformations (e.g., aggregation for control transects).
- Note spatial sensitivity: coordinates are rounded to protect rare/threatened species; consider access controls or data masking for sensitive outputs.
- Include data licensing and sharing terms (not specified in the text) and any embargoes or usage restrictions.
- Provide guidance on updating: potential future replicates or expansions; maintain versioning and provenance tracking.
- Ensure compatibility with data portals/catalogues used by the hosting organization; align metadata fields with standard data governance practices (e.g., data lineage, stewardship contact, last updated date).

## References
- BirdLife International. 2017. Handbook of the Birds of the World and BirdLife International digital checklist of the birds of the world. Version 9.1.