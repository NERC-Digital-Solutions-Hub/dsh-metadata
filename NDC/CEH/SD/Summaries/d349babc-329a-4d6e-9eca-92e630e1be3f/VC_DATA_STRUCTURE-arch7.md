# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Coarse Grain (VC)

- Overview
  - Long-running ECN vegetation dataset intended for GIS visualization and analysis at a coarse grain.
  - Part of the ECN Data Centre ecosystem; data are suitable for map-based analyses of vegetation presence and associated environmental context.
  - Data usage guidance emphasizes citing ECN data and acknowledging provenance in outputs.

- Data structure and GIS-ready components
  - Multi-table, site-focused schema (11 site-specific tables per VC dataset):
    - D1VC_xxx: Plot-level data (site, year, PLOTPID, CELLID, FIELDNAME, VALUE)
    - D2VC_xxx: Site/environmental data (e.g., PEDATE, LANDUSE, SLOPE, ASPECT, SLOPEFORM, NVCCLASS)
    - D3VC_xxx: Cell-level features (SITECODE, SYEAR, PLOTPID, CELLID, FEATURE)
  - Supports GIS workflows such as:
    - Plot polygon creation with site/year/plot attributes
    - Cell-level data for raster-like visualization of species/quality per cell
    - Site-level covariates for contextual mapping
  - Data across sites require harmonization of resolutions and time frames for cross-site analyses.

- Taxonomic and quality coding
  - Species codes:
    - A comprehensive mapping of numeric species codes to Latin botanical names (and related identifiers), including equivalents and synonyms (e.g., 2741, Salix aurita (s) = Salix caprea (c); extensive pairings across codes and taxa).
    - Codes are used to annotate species presence/absence within cells and plots.
  - Quality codes:
    - Standard ECN quality codes (e.g., 100–507, etc.) indicating data quality factors (no information, sample issues, loss, contamination, etc.).
    - 999 denotes an unusual event; accompanying text in quality metadata provides details.
    - Site managers assign applicable codes to reflect field conditions, sampling issues, or environmental disturbances.

- Spatial and temporal coverage
  - Spatial scope: 12 ECN sites with main sites listed in the VC dataset; data primarily non-spatial grid attributes (plots and cells) plus site environmental variables.
  - Temporal scope: sampling years span mid-1990s to around 2012, varying by site.
  - Woodland protocol data exist as a separate dataset or tables and may require joining additional datasets for complete GIS analyses.

- Data standards, metadata, and governance
  - Rich metadata and reference tables underpin field definitions and code mappings; consult core metadata for precise field meanings.
  - Data standards emphasize cross-site harmonization when integrating different sites or time periods.
  - Provenance and citation are required for outputs derived from ECN VC data.

- Access, usage, and credits
  - ECN Data Centre contact: ecn@ceh.ac.uk
  - Protocol references and documentation links are available within dataset metadata.

- Practical GIS notes for the VC dataset
  - Expect a large, multi-table schema with extensive coding (land use, slope, features, species, and quality codes).
  - Key workflows:
    - Map plotting data (D1VC_xxx) to create site-wide plots with attributes.
    - Map cell-level data (CELLID, FIELDNAME, VALUE) to generate grid-based vegetation representations.
    - Integrate site environmental variables (D2VC_xxx) for contextual maps.
    - Use D3VC_xxx when cell-level features are relevant to analysis.
  - When aggregating across sites:
    - Harmonize resolutions and years.
    - Handle missing plots/cells with metadata guidance.
  - Data cleaning and standardization are recommended before GIS integration; always reference the metadata for field definitions.
  - Acknowledge ECN provenance in outputs and publications; follow reprint requests as specified.