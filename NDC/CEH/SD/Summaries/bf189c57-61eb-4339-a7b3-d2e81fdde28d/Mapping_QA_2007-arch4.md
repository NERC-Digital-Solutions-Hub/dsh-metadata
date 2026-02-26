# Mapping Quality Assurance Exercise

- Overview
  - Purpose: assess quality of Countryside Survey (CS) 2007 habitat and landscape mapping; deliver high-quality data compatible with national spatial datasets in a geodatabase.
  - Approach: field mapping with Surveyor software (mandatory fields, prompts, visit status); early data checks via an interactive wiki; QA teams conducted in-field and office checks.
  - Outcome: improved data clarity, format, and traceability; QA used to identify issues and guide analysis and interpretation.

- Data Architecture, Tools and Workflow (for Data Leaders)
  - Data stored in a geodatabase; two datasets (CS surveyor data and QA data) compared in common surveyed areas using masks to exclude unsurveyed or refused areas.
  - QA mapping largely conducted in different squares from survey QA to broaden representation; data uploaded to a wiki for early validation.
  - Quality control teams visited survey teams to ensure protocol adherence; 23 1km squares mapped for QA analysis (target scope exceeded previous QA efforts).

- QA Methodologies (and why they matter for data governance)
  - Direct comparison: aggregate areas/lengths/points per square to compare Broad Habitat (BH) allocations.
  - Raster comparison: convert polygons to 10x10 m raster cells to compare absolute BH extents and spatial locations.
  - 100-point grid: assess agreement of BH codes at fixed points within squares.
  - Attribute analysis: compare species-attributes within matched polygons; assess consistency of species recording.
  - Surveyor efficiency: evaluate visit status usage, proportion of land visited, and species recording frequency.
  - Linear features: 100-point approach less suitable; use buffering (5 m) to compare land-use themes between QA and CS linears.
  - Points: buffer point features to compare habitat codes with CS points; check code consistency.

- Key Findings and Metrics (highlights important for data strategy)
  - Habitat-level agreement (6.1):
    - 81% of squares had BH presence recorded by both CS and QA.
    - Mean differences in BH proportions between QA and CS were mostly under 1% for 13 BH types; 1-2% for 5 BH types; under 3.5% for the remaining two.
    - Some habitats showed greater variability (SD > 5%), notably Improved/Neutral Grassland, Dwarf Shrub Heath, Bog, Urban.
    - Notable issues around Blanket Bog definitions and upland mosaics; potential misclassifications between Dwarf Shrub Heath and Blanket Bog in some squares.
  - Raster agreement (6.2):
    - Overall average BH raster agreement across squares ~76%.
    - High-performing squares include 364 (98%), 488 (94%), 434 (66%), while poorer examples include 261 (49%), 773 (23%), 935 (52%).
  - 100-point concordance (6.3):
    - Concordance varies by square; overall good performance with several squares showing strong agreement (364, 359, 355, 694, 695, 1113) and some weak concordance (261, 773).
    - Summary across BH/PH shows substantial agreement, but some mismatches linked to habitat definitions, mosaics, and landscape context.
  - Habitat/Broad Habitat coding inconsistencies (6.3):
    - Common issues involve Neutral vs Improved Grassland; Broadleaf vs Coniferous Woodland; upland mosaic variability; and Urban vs Improved Grassland classifications.
    - Blanket Bog mismatches were a major source of discrepancy, tied to evolving definitions and field-handbook updates in 2007.
  - Species attributes in polygons (6.4):
    - 45% of QA polygons had at least one listed species matching the CS polygon (excluding mosaic BH polygons).
    - Of matched polygons, 77% also had the same BH for the matched species, suggesting decent alignment between species identity and habitat classification but notable variance by habitat type.
    - Species concordance overall around 40% for commonly recorded species; CS tended to record more species than QA.
  - Points and species lists (Tables 6.5):
    - Common species (e.g., Lolium perenne) show varying concordance; overall pattern indicates QA and CS often identify different dominant species in mixed habitats.
  - Change recording (9):
    - Digital recording enabled more detailed change coding (Real change, Error change, No change).
    - High agreement on change codes for many Broad Habitats; some confusion remains, particularly in relation to habitat context (e.g., Blanket Bog).
    - Training and field handbook updates improved consistency but complexity remained.

- Linear Features, Points and Change (7–8)
  - Linear features (7.1–7.2):
    - Aggregate lengths show minor differences between QA and CS across most squares.
    - High consistency in land-use themes for linears (e.g., boundaries, fences, walls, belts of trees), with limited instances where QA detected features CS did not.
  - Points (8.1):
    - Point feature counts show minimal discrepancies; overall alignment between QA and CS in land-use themes and point placements.
    - Some confusion around woodland vs. forest codes; generally strong agreement on habitat codes for points.

- Change Assessment and Data Stewardship (9)
  - The shift to digital change coding allowed more precise historical corrections and updates.
  - Generally strong adherence to change-coding protocols across habitats, with some challenges in complex habitat mosaics.
  - The exercise demonstrates the value of consistent metadata and provenance for tracking changes over time.

- Challenges and Implications for Data Leaders
  - Habitat definitions need ongoing refinement, especially Blanket Bog, Sand Dune/machair, and upland mosaics, to reduce cross-surveyor interpretation variance.
  - High variability in some BH proportions suggests the need for better training, clearer allocation rules, and potential revision of allocation matrices for certain habitats.
  - Mosaic mapping in uplands complicates exact BH matching; consider enhancing methods to represent mosaics and transitions between BHs.
  - Urban classifications require clearer criteria to distinguish between Amenity Grassland and Built/Urban areas.
  - Metadata, versioning, and field handbook updates are essential for ensuring long-term data quality and cross-cycle comparability.
  - The positive takeaway: digital Capture, in-field checks, and wiki-based QC substantially improve data quality, with overall robust agreement between CS and QA in many areas.

- Takeaways for Data Strategy and Next Steps
  - Maintain and expand the digital workflow (Surveyor-based field data capture, wiki QC, geodatabase integration) to preserve data quality gains.
  - Invest in ongoing training and clear, up-to-date habitat definitions; incorporate lessons from Blanket Bog and upland mosaic discrepancies.
  - Enhance metadata standards, change-tracking protocols, and documentation to support reproducibility and governance across surveys.
  - Consider refining rasterization and 100-point methods for mosaicked or transitional habitats; ensure comparability with national datasets.
  - Use QA findings to guide iterative improvements in data collection, classification rules, and data dissemination practices to support policy colleagues and data consumers across networks.