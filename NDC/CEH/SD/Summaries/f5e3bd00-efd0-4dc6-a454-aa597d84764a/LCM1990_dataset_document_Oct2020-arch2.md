# Dataset documentation

- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover dataset produced from Landsat-5 30 m imagery, classified into 21 Broad Habitat-based classes, and engineered to be compatible with newer LCM products (LCM2007/LCM2015) to enable long-term change analyses.
- It provides a range of data products (vector and raster) to support diverse user needs and applications, with each product having a Digital Object Identifier (DOI) for stable citation.

## Data products and formats

- Vector data set
  - Approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Eight key attributes per polygon, including:
    - gid: unique geometry identifier
    - hist: list of classes present with pixel counts
    - mode: recommended LCM1990 target class (1–21)
    - purity: percentage of the polygon covered by the modal class
    - conf: mean per-polygon classification confidence (0–100)
    - n: number of pixels in the polygon
    - cmp: composite image source
- Raster data sets
  - 25 m raster (GB and NI): 3-band product
    - Band 1: dominant LCM1990 class per polygon
    - Band 2: mean per-polygon confidence
    - Band 3: percentage of polygon area covered by modal class
  - 1 km raster (GB and NI): aggregates from 25 m rasters
    - Dominant cover (1-band, target and aggregate classes)
    - Percentage cover (21 bands for target, 10 bands for aggregate)
- Spatial framework and comparability
  - Core 25 m raster and vector products are aligned with the LCM2015 framework for cross-version comparability.
  - Minimum mappable area > 0.5 ha; polygons smaller than 0.5 ha or lines < 20 m dissolved into surrounding landscape.

## Class structure and labeling

- LCM1990 maps 21 classes based on UK Broad Habitat definitions.
- Some classes are split to improve thematic detail:
  - Built-up Areas and Gardens into Urban and Suburban
  - Dwarf Shrub Heath into Heather and Heather grassland
  - Littoral Sediment into Littoral sediment and Saltmarsh
- Unique object labeling
  - Each polygon carries a gid for unambiguous communication between users.
- Rich metadata and uncertainty
  - Per-polygon mean classification probability (uncertainty) is included in vector attributes and 25 m raster Band 2.

## Data access, licensing, and citation

- Access
  - 25 m and 1 km raster data are available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - The full vector product is available on request under licence from CEH (fees may apply).
- Citation and DOIs
  - All LCM1990 products have DOIs; formal citation is encouraged in publications.
  - DOIs are provided separately for Great Britain and Northern Ireland vectors and raster products (GB/NI, vector, 25 m raster, 1 km dominant/percentage/aggregate products).
  - Example citation guidance provided (author, date, title, DOI).
- Projections
  - Great Britain vector/raster: British National Grid.
  - Northern Ireland vector/raster: Irish Grid (TM75).

## Quality assurance, validation, and limitations

- QA process
  - Defined methods and code with trained staff; multiple checks for projection accuracy, spatial completeness, polygon modal class consistency (vector), value ranges (0–100 for rasters), and pixel size accuracy.
  - Full validation exercise comparing LCM1990 with other datasets (e.g., Countryside Survey) planned for publication.
- Uncertainty and interpretation
  - Random Forest per-pixel probabilities are provided, enabling assessment of classification confidence.
  - Some habitat classes are spectrally challenging (e.g., Fen/Marsh/Swamp, Saline/coastal interfaces) and may require ancillary data or field validation for final interpretation.
- Data scope and use notes
  - LCM1990 maps land cover rather than direct land use; some land-use inferences may be ambiguous from remote sensing alone.
  - Parcels < 0.5 ha or narrow linear features < 20 m are dissolved into the surrounding landscape during production.

## Implementation and further information

- Data formats
  - Core vector product; 25 m and 1 km raster products; documentation includes detailed metadata and Appendix mappings.
- Documentation and references
  - Detailed appendices cover class definitions, Broad Habitat mappings, standard color mapping, and composite imagery used in production.
- Contact
  - Further information and access requests handled via CEH channels (spatialdata@ceh.ac.uk) and CEH’s LCM1990 pages.

## Endnotes and acknowledgments

- Data and methodology support acknowledge NERC and the UK-SCAPE programme.
- The LCM1990 dataset serves as a foundational product for long-term land cover change analyses, linked to subsequent LCM datasets (2000, 2007, 2015) for enabling multi-decadal environmental monitoring.