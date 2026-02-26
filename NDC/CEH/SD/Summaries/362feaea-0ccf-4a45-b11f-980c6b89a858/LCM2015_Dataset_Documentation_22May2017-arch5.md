# Dataset documentation

- The Land Cover Map 2015 (LCM2015) is a UK-wide parcel-based land cover dataset produced from two-date Landsat-8 (30 m) and AWIFS (60 m) composites, classifying into 21 Broad Habitat-based classes. Outputs include a rich vector dataset (parcels with attributes), a 25 m raster, and 1 km aggregated products, designed to support diverse user needs while enabling change mapping over time.

- The dataset is distributed in multiple formats and spatial resolutions:
  - Core vector dataset: polygons with extensive metadata per parcel.
  - 25 m raster: per-polygon dominant class with a second band representing mean per-polygon probability.
  - 1 km rasters: dominant cover and percentage cover products for both 21 target classes and 10 aggregated classes.
  - Separate data for Great Britain and Northern Ireland, using British National Grid and TM75 Irish Grid respectively.

- Provenance, citation, and versioning:
  - LCM2015 is a stable, archived dataset with DOIs for each product (GB and NI) and guidance to cite these DOIs in publications.
  - Version 1.2 (May 22, 2017) includes minor updates (e.g., composite metadata) and 1.1/1.0 history documented within the dataset docs.
  - Data access: 1 km rasters via CEH Environmental Information Platform; full vector and 25 m products on request (licensing may apply).

- Data governance, metadata, and uncertainty:
  - Rich metadata at polygon level (dominant class, breakdown of pixels by class, mean probability, etc.) and per-polygon uncertainty (probability) captured in vector attributes and 25 m raster band 2.
  - Each parcel has a unique geometry identifier (gid) to ensure unambiguous communication; retaining gid is recommended for data provenance and downstream processing.
  - Class definitions link to UK Broad Habitat classifications (JNCC) with detailed appendices defining the 21 classes and how they map to Broad Habitats.

- Classification methodology and changes since earlier maps:
  - New Random Forest classifier (versus previous Maximum Likelihood) to handle multi-modal training data and simplify training data preparation.
  - Ancillary data (e.g., slope, proximity to rivers) are integrated into the input rather than applied post-classification.
  - Training areas are derived from a stable set (areas classified consistently in 2000 and 2007) and supplemented for coastal areas and challenging classes.
  - Spatial framework no longer includes segmentation; per-pixel classification with polygons summarised to polygons for vector outputs.
  - Several output and class adjustments compared to older maps (e.g., Montane class removed, Rough grassland removed, updated handling of mixed woodland, and changes to probability information representation).

- Data products and content details:
  - 21 LCM2015 target classes aligned with Broad Habitat concepts; some classes are subdivided within the 21 (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
  - Vector product: ~6.7 million GB parcels and ~0.9 million NI parcels; nine primary attributes per polygon (including dominant class and pixel breakdown).
  - 25 m raster: two-band dataset (band 1 = dominant class; band 2 = mean probability for the polygon’s dominant class).
  - 1 km rasters: dominant cover and percentage cover for both 21 target classes and 10 aggregate classes; note rounding may cause sums to differ slightly from 100%.
  - Minimum mapping unit: polygons larger than 0.5 ha; polygons smaller than 0.5 ha and linear features under 20 m are dissolved into surrounding landscape.

- Data access and licensing considerations:
  - GB vector and 25 m raster: available on request under license from CEH; online application process and potential licensing fees.
  - GB 1 km products: available via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - NI products: also provided under license on request; DOIs available for each product and region.
  - Projections: GB products use British National Grid; NI products use TM75 Irish Grid.

- Usage notes and caveats:
  - LCM2015 maps land cover, not land use; interpretation of land use may require additional information.
  - Changes across LCM series reflect methodological and data-source evolution; users should review differences when migrating scripts from LCM2007 to LCM2015 and when mapping change.
  - The dataset emphasizes per-polygon class labels and associated uncertainties to support informed usage and quality assessment.

- Appendix-oriented guidance (high-level):
  - Definitions and mappings to JNCC Broad Habitat categories; guidance on class interpretation (e.g., Broadleaved vs Coniferous Woodland, various grassland types, coastal and aquatic habitats).
  - Colour mapping rules and composite image usage to reproduce standard displays.

- Contact and further information:
  - CEH Spatial Data contact: spatialdata@ceh.ac.uk; and project pages for LCM2015 with access and citation details.

- Key governance takeaways for data stewardship:
  - Maintain clear lineage with DOIs and version history; document changes between versions and their implications for analyses.
  - Ensure robust metadata and provenance (gid, pixel distributions, probabilities, and uncertainty) to enable reproducibility.
  - Manage licensing and access controls, balancing open research needs with licensing requirements.
  - Preserve data model consistency (GB vs NI, vector vs raster outputs) and support users with guidance on use cases (land cover vs land use) and caveats for change mapping.