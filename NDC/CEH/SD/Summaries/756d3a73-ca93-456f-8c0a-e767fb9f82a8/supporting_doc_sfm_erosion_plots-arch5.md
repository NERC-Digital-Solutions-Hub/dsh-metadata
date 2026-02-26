# Collection, generation methods and quality control

- Purpose and scope: Establish seven erosion plots on Iron Tongue Hill to capture burnt moorland conditions and monitor erosion and vegetation recovery through Structure-from-Motion photogrammetry.
- Study dates and coverage: Surveys conducted from 26/07/2018 to 22/11/2019, totaling ten survey events (S1–S10), including the initial survey date.

## Study site and data collection

- Plot locations: Seven plots with precise OS Grid References provided (plots 1–7).
- Field data collection: Each survey collected 40–60 photographs in the field to build SfM models.
- Survey schedule: S1 (26/07/2018), S2 (02/08/2018), S3 (12/09/2018), S4 (04/10/2018), S5 (13/11/2018), S6 (13/12/2018), S7 (08/01/2018), S8 (16/05/2019), S9 (29/07/2019), S10 (22/11/2019).

## Data processing and outputs

- Processing workflow: Structure-from-Motion photogrammetry performed to generate models; dense SfM point clouds created in Agisoft Photoscan (Metashape).
- Georeferencing and scaling: Ground Control Point coordinates used to scale and georeference point clouds based on differential GPS data collected in the field.
- Quality metrics: Registration errors reported around 20 mm.
- Data products: Cleaned dense DEM point cloud and 1 mm/pixel resolution orthomosaic (exported as .tif files) for later analysis.

## Data organization and naming conventions

- File structure: For each plot and survey, two .tif files exist:
  - P1_S1_DEM.tif (DEM dense point cloud)
  - P1_S1_ortho.tif (orthophoto)
- Naming convention: Pn = Plot number (1–7), Sn = Survey number (S1–S10); two file types per plot per survey, totaling 140 files (7 plots × 10 surveys × 2 file types).

## Provenance, metadata, and reproducibility

- Provenance: Data derived from SfM photogrammetry using 40–60 field photographs per survey; georeferenced with differential GPS and Ground Control Points.
- Software: Agisoft Photoscan (Metashape) used for dense point cloud generation.
- Metadata scope implied: survey identifiers, plot IDs, dates, and file naming scheme; georeferencing method and accuracy details provided.

## Relevance for data governance (Data Stewards perspective)

- Standards and interoperability: Uses widely recognized raster formats (.tif) with explicit naming conventions to facilitate discovery and reuse.
- Metadata and documentation needs: Clear mapping of plot IDs, survey IDs, dates, coordinate system references (via GPS and GCPs), and processing workflow to support traceability and reproducibility.
- Data quality and stewardship: Quantified accuracy (~20 mm registration error) and 1 mm/pixel resolution orthomosaics provide defined quality attributes for data consumers.
- Data lifecycle considerations: A complete dataset spanning multiple surveys over time, with explicit file organization supporting updates and expansion; attention needed for long-term storage, versioning, and potential scale-up to additional plots or future surveys.
- Practical data management: 140 total TIFF files represent a substantial but manageable data package; consistent directory structure and naming aid discoverability and reuse.