# CORINE land cover technical guide - Addendum 2000

## Overview and aim
- Technical guide addendum to the CORINE Land Cover (CLC) Technical Guide (CEC, 1994) to support land cover monitoring by the EEA.
- Provides additional information not in the 1994 guide, describes methodological developments for softcopy interpretation, (semi-) automated classifications, and extended nomenclature guidance.
- Extends class descriptions and generalisation rules for mapping at 1:100 000, and improves understanding of landscape contents for varied audiences.

## Production methods and workflow

### Hardcopy inventory
- Original approach: computer-aided photo-interpretation using hardcopy satellite image prints with transparencies and ancillary data.
- Strengths: well-established, transparent, simple in mid-1980s context.
- Limitations: prone to digitisation errors, border matching issues, border/region alignment challenges, multiple intermediate hardcopy products.

### Softcopy inventory
- Modern shift to interpret and digitise in a single pass on-screen.
- Integration with GIS for real-time data handling and visualization; supports multiple data types and flexible workflows.
- Emphasis on human interpretation to complement (semi-) automated results, given the complexity of CORINE classes.

### GIS and data management considerations
- Integrated GIS environments expected to manage raster and vector data, support multiple datasets, and offer broad import/export capabilities (raster: BSQ, BIL, BIP, TIFF/geoTIFF; vector: DXF, Arc/Info formats).
- Text, images, and icons linked to geographic objects; editable attribute data and supporting documentation in metadata.

### Co-pilot software (JRC)
- A dedicated softcopy tool for CORINE data production, maintenance, and updating.
- Runs on MS Windows; data are managed in a continuum across times/maps; object-based data model (points, lines, surfaces) with Catalogue, Typelook, and GraphicSet structures.
- ASCII-based main data structures; provided by JRC to national CLC teams.

## Conversion of (semi-) automated classifications
- Acknowledges limitations of automatic classifications due to image quality variability, ground truth differences between land cover vs. land use, and the holistic nature of human interpretation.
- Automated conversions can yield solid positional accuracy but may struggle with attribute accuracy and thematic coherence.
- Generalisation techniques (manual or automated) include:
  - Reclassification: regrouping to CORINE classes, often hierarchical.
  - Aggregation: merging nearby features into a single area.
  - Amalgamation: joining or dividing features based on semantic proximity and spatial relations.
  - Smoothing: boundary relocation to reduce raster step effects.
  - Simplification: reducing boundary complexity.
- Quality considerations emphasize the trade-off between simplification and accuracy; per-pixel classification quality, generalisation method quality, and visual interpretation all influence outcomes.

## Validation and quality assessment

### Validation methodology
- Validation repeats data collection using the same sources as the original, via random (stratified) sampling.
- Produces confusion matrices to assess omission/commission errors and item-level validity.
- Enables reliability estimates at different nomenclature levels and across regions; supports stratified aggregation.

### Sampling methodology (5.1)
- Stratified random sampling: strata can be land cover items and/or geographic regions.
- Process: select strata and determine points per stratum; draw sampling points proportionally to stratum area; interpret points to derive error rates.
- Objective: minimize standard error; tailor sample size per stratum to expected variation; cap suggested density (e.g., 2 points per km² for practicality).

### Determination of the number of sampling points (5.2)
- Uses a binomial-based formula to compute points per stratum: nh = (ph(1-ph)) / (sh^2), where nh is points, ph estimated error rate, sh accepted absolute standard error.
- Guidance on density adjustments for small strata and practical limits; higher density acceptable with methods that interpret multiple points per unit.

### Random sampling steps (5.3)
- First step: area-weighted selection of land cover units within a stratum; determine step-size and allocate points to units.
- Second step: place points within units using local random/systematic methods; three cases based on desired number of points (1, several, many).
- Grid-based approach used for higher point counts to ensure even spatial distribution.

### Interpretation of random points (5.4)
- Interpretation proceeds from larger to smaller units, ensuring adherence to minimum mapping size.
- Validation is performed on-screen with digital imagery at fixed scales (not exceeding 1:40 000) to maintain consistency with original data.
- Validation maps are documented and checked for topology; meta-data and field survey documentation are crucial for interpretation.

### The raising (5.5)
- Overlay validated data with random points to construct a confusion matrix.
- Estimation of correctly classified area per stratum and overall accuracy using weighted sums by area.
- Provides standard errors for accuracy estimates; supports aggregation across strata and nomenclature levels.

## Part II: Addendum to the CORINE land cover nomenclature illustrated guide

### Introduction and purpose
- Over a decade of experience with Landsat and SPOT interpretation; refinements to class definitions without changing core content.
- Adds clarifications to class definitions, contents, typical patterns, textures, representative photographs, and country-specific particularities to aid image analysis.

### Methodology
- Visual interpretation remains the core method; emphasis on interpretation elements and landscape objects that drive image manifestations.
- Provides graphic/text presentation of class characteristics at scale 1:100 000 to assist interpreters.

### Selected content highlights (class-focused guidance)
- Urban fabric (Class 1.x) and related densities:
  - 111 Continuous urban fabric: >80% impermeable surfaces; complex fabric, roads, and urban greenery considered.
  - 112 Discontinuous urban fabric: 30–80% impermeable surfaces; density of housing as a key criterion; various sub-situations addressed (e.g., housing estates, road-adjacent built-up areas).
  - Extends to sub-classes and particularities (e.g., 121 Industrial/commercial units; 122 Road and rail networks; 124 Airport areas) with detailed texture and pattern guidance.
- Agricultural and land-use classes (2.x and 3.x families):
  - 211 Non-irrigated arable land, 212 Permanently irrigated land, 221 Vineyards, 222 Fruit trees and berry plantations, 231 Pastures, 231/241 nuances for meadow and abandoned land, 241 Olive trees, etc.
  - Forest classes (3.x): 311 Broad-leaved forests, 312 Coniferous forests, 313 Mixed forests, plus textures and generalisation notes, including dwarf pine scrubs and sclerophylous vegetation (classes 322–324).
- Wetlands and coastal/marine classes (4.x, 5.x):
  - Inland wetlands (411), Coastal wetlands (412), Salt marshes (421), Salines (422), Water bodies (512) and related coastal lagoons (521) and estuaries (522), with texture guidance and mapping nuances.
- Generalisation and extension notes across classes to support mapping at 1:100 000, including typical patterns, textures, and representative photographs.

## References
- Core references include the CORINE Land Cover Technical Guide (CEC, 1994), standards and related methodological works cited in the addendum, and supporting regional studies.

## Implications for GIS Specialists
- The addendum provides a comprehensive framework for modernizing CORINE data production with softcopy GIS workflows, ensuring data interoperability, and documenting validation procedures.
- Emphasizes the importance of rigorous validation (stratified random sampling, confusion matrices, area-weighted accuracy) and transparent metadata.
- Offers detailed guidance for class interpretation and generalisation, aiding consistent map production and cross-country comparability at 1:100 000.
- Recommends using Co-pilot or equivalent GIS-centric tools for integrated data management, update cycles, and cross-map data continuity.