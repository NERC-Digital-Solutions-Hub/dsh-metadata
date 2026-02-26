# Dataset documentation

## Overview for Data Stewards
- Land Cover Map 1990 (LCM1990): UK parcel-based land cover map with 21 classes, created from Landsat-5 two-date composites at 30 m resolution; designed for compatibility with later LCM products (e.g., LCM2015) to support long-term change analysis.
- Purpose and scope: Provide diverse data products for the LCM user community; a stable, archived dataset with persistent identifiers (DOIs) to enable reproducibility and proper citation.

## Data products and formats
- Core vector product: polygons with rich attributes (dominant class, source image, per-polygon pixel breakdown, uncertainty, gid).
- Raster products:
  - 25 m raster: three bands (dominant class, per-polygon mean confidence, percentage cover of modal class).
  - 1 km raster products: dominant class (1-band) and percentage cover for target (21) and aggregate (10) classes.
- Aggregate classes: defined to reduce complexity for some applications; 25 m details underpin 1 km summaries.
- Spatial coverage and resolution:
  - Great Britain and Northern Ireland provided separately with respective projections.
  - Minimum mapping unit (MMU): >0.5 ha; polygons smaller than 0.5 ha dissolved into surrounding landscape.
- Data volumes: vector comprises approximately 6.7 million polygons (GB) and 0.9 million polygons (NI); rasters distributed as uncompressed GeoTIFFs.

## Metadata and uncertainty
- Rich polygon metadata: dominant class, class breakdown (_hist), display code (_mode), maximum per-polygon confidence (_conf), standard deviation (_stdev), and pixel count (_n); composite image source (cmp).
- Uncertainty: per-pixel probability from Random Forest classifier included as mean per-polygon value (vector) and in the 25 m raster.
- This supports governance needs for provenance, traceability, and quality assessment.

## Data access, licensing, and reuse
- Access point: CEH Environmental Information Platform (eip.ceh.ac.uk) for 25 m and 1 km rasters; full vector product available on request under license.
- Licensing: some users/applications may incur license fees; check access terms via CEH pages or contact spatialdata@ceh.ac.uk.
- DOIs: every LCM1990 product has an associated DOI to enable transparent citation and method traceability.

## Citing and provenance
- DOIs provide a persistent citation mechanism (e.g., vector GB, 25 m raster GB, various 1 km products for GB/NI).
- Publications should cite both authors and dates alongside the DOI (e.g., Rowland et al., 2020) and include full DOI references in the bibliography.
- Example citations and DOIs are provided to ensure repeatable methods and usage tracking.

## Quality assurance and validation
- QA regime ensures projections, spatial completeness, polygon modal class, documentation headings, value ranges (0–100 for rasters), and pixel sizes are correct.
- Validation against external datasets (e.g., Countryside Survey, National Forest Inventory) conducted; results to be published separately.
- Data lineage is traceable from the general parcel framework (based on 2007 OS MasterMap) with documented processing steps.

## Projections, coordinate systems, and data structure
- Projections:
  - Great Britain: British National Grid.
  - Northern Ireland: Irish TM75 grid.
- Data structure:
  - Vector: attributes including gid (unique parcel identifier) and a detailed _hist and _mode for interpretation.
  - Raster: 25 m and 1 km products with explicit metadata in accompanying tables (e.g., Table 4 in the documentation).

## Usage notes and caveats
- LCM1990 maps land cover rather than precise land use; some land cover classes may not directly reveal land use (e.g., recreation grass vs. grazing).
- Class distinctions (especially for grasslands, wetlands, and mixed habitats) can be spectrally challenging; users may need to consult metadata (_hist) for possible misclassifications or consider aggregating classes for specific analyses.
- Small patches (<0.5 ha) are dissolved, which may affect fine-scale assessments near MMU boundaries.

## Accessing more information and contacts
- Primary information hub: CEH Environmental Information Platform (https://eip.ceh.ac.uk/lcm/lcmdata).
- Licensing queries and access: spatialdata@ceh.ac.uk.
- Journal article and further methodological details are in preparation; acknowledgement to NERC and UK-SCAPE program.

## Summary of governance and stewardship implications
- Dozens of DOIs and a robust metadata framework support reproducibility, attribution, and data provenance.
- Clear MMU, class definitions, and documentation facilitate consistent data interpretation across organizations.
- Data are delivered in multiple formats and resolutions to suit a range of governance, reporting, and modeling needs, with explicit licensing terms and access controls.
- Ongoing quality assurance and planned publications ensure transparency about data accuracy and validation status.