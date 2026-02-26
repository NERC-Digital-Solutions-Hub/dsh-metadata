# Dataset documentation

- LCM2015 provides a UK parcel-based land cover map classified into 21 classes, using satellite data (Landsat-8 at 30 m, supplemented by AWIFS at 60 m) and two-date composites.
- The product suite includes a core vector dataset, a 25 m raster, and 1 km raster products (dominant and percentage cover) for both 21 classes and 10 aggregate classes.
- Vector polygons carry rich metadata and uncertainty information; per-polygon label (gid) ensures unambiguous communication between users.
- The data are designed to support diverse GIS applications, from policy to public information, with formats suitable for both detailed analysis (vector) and scalable mapping (raster).

- The dataset is intended as stable, archived data with a Digital Object Identifier (DOI) for each product; users should cite the DOIs in publications.

- Note: LCM2015 should not be used for change mapping in its current state; differences between maps reflect real changes, classification choices, and varying data inputs over time.

- Availability and access: 
  - 1 km raster products accessible via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector and 25 m raster products available on request under licence from CEH (licensing may apply).

- Coverage and resolution:
  - GB and Northern Ireland included separately with appropriate projections.
  - 25 m raster: two bands (band 1 = dominant class; band 2 = mean per-polygon probability).
  - 1 km rasters: aggregate percentage and dominant class products derived from the 25 m data.

- Classification and methodology (LCM2015 vs earlier maps):
  - New classifier: Random Forest (replacing Maximum Likelihood).
  - Ancillary data (e.g., slope, distance to rivers) are integrated into the input data rather than applied post-classification.
  - Training areas are more broadly defined and enhanced for coastal and poorly-mapped classes.
  - Per-pixel classification; polygon labels are derived from modal class at the polygon level.
  - No spectral sub-classes; removal of image segmentation in the spatial framework to improve consistency for change mapping.
  - Stable training areas update built upon 2000 and 2007 classifications, with coastal and challenging areas supplemented manually.

- Output data and structure:
  - Core vector dataset: ~6.7 million GB polygons in Great Britain and ~0.9 million in Northern Ireland.
  - Vector attributes include dominant land cover (BHAB), per-class pixel counts (Pix_dist), uncertainty (unc), standard deviation (unc_stdev), number of pixels (npix), modal class (Modal_class), and proportion of dominant class (Modal_prop), plus Composite meaning.
  - 25 m raster: two bands as described; raster data aligned to per-polygon classification.
  - 1 km rasters: 
    - 1 km dominant class for both 21-class and 10-aggregate datasets.
    - 1 km percentage cover for each class (21 bands or 10 aggregate bands).
  - Spatial resolutions and extents differ between Great Britain and Northern Ireland; data are provided in respective national grid projections.

- Class structure and mapping:
  - LCM2015 maps 21 Broad Habitat-based classes (based on JNCC Broad Habitats, Jackson 2000).
  - Some classes are further divided in certain products (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
  - Appendix materials provide detailed definitions for each Broad Habitat and the translation to LCM2015 target class numbers.

- Data quality and uncertainty:
  - Random Forest provides per-pixel probability; uncertainty is reported per polygon and in the 25 m raster’s band 2.
  - The documentation emphasizes caution when interpreting change using LCM2015 due to potential classification errors and differences in input data across years.

- Data provenance and DOIs:
  - Each LCM2015 product (GB vector, GB 25 m raster, GB 1 km percentage and dominant classes, NI vector, NI 25 m raster, NI 1 km percentage and dominant classes) has a DOI for citation (details in the document’s citation section).

- Projections and geographic references:
  - Great Britain data in British National Grid (OSGB 27700); Northern Ireland data in TM75 Irish Grid (29903).
  - The 25 m and 1 km rasters are designed to support various analyses, from detailed local assessment to national-scale modelling.

- Practical notes for users:
  - Retain the gid attribute in the vector dataset for unambiguous communication and potential re-joining of polygon-level metadata.
  - The 25 m raster’s band 2 value provides the mean probability of the dominant class, while the 1 km products present aggregated information suitable for large-scale modelling.
  - When using DOIs in publications, follow the recommended citation format and include author names and year.

- Example usage scenarios:
  - Map-based appraisal of Broad Habitat distributions across Great Britain and Northern Ireland.
  - Integration with other spatial datasets (e.g., meteorological, species distribution) using the 1 km dominant and percentage cover rasters.
  - Detailed spatial analysis with the vector dataset and its rich polygon-level metadata, including uncertainty information.

- Appendices and supporting information:
  - Appendix 1–3 (class definitions, color mapping, and composite image metadata) provide detailed guidance for class interpretation and visualisation.
  - Appendix 4 lists composite images used in LCM2015 to aid reproduction and understanding of the classification input data.

- Key references:
  - Jackson (2000) on Broad Habitat definitions.
  - Morton et al. (2011) Final Report for LCM2007.

- Contact and further information:
  - Queries: spatialdata@ceh.ac.uk
  - More information: ceh.ac.uk and eip.ceh.ac.uk/lcm

- Cited product overview:
  - LCM2015 vector (GB and NI), GB 25 m raster, GB 1 km percentage and dominant classes, GB 1 km aggregate classes, NI vector, NI 25 m raster, NI 1 km percentage and dominant classes, NI 1 km aggregate classes.