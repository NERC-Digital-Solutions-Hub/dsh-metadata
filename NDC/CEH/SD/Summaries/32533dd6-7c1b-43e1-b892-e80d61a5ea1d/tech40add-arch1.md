# CORINE land cover technical guide - Addendum 2000

- Purpose and scope
  - Provides new information not in the 1994 CORINE Land Cover Technical Guide.
  - Describes methodological developments for producing the CORINE Land Cover (CLC) database, notably softcopy interpretation and (semi-) automated conversions.
  - Expands the CLC nomenclature with Central/Eastern Europe relevance, generalisation rules for mapping at 1:100 000, and enhanced landscape-characterisation guidance.
  - Aims to improve data quality, traceability, and usability for monitoring across Europe.

## Part I State-of-play production methods of the CORINE land cover database

### 1. Introduction
- Transition from hardcopy-based inventory to softcopy/digitized approaches.
- Automated spectral procedures are possible but human interpretation remains essential due to CLC’s territorial and functional nuances.
- A variety of analogue–digital integration strategies were used across countries; both approaches remain valid.

### 2. Hardcopy inventory
- Early CORINE method: computer-assisted photo-interpretation using overlays on 1:100 000 hardcopy prints; ancillary data used for verification.
- Pros: established workflow with reasonable accuracy.
- Cons: digitisation errors, border-matching challenges, multiple intermediate hardcopy products.

### 3. Softcopy inventory
- Emergence of on-screen interpretation and digitisation; integrated with GIS.
- 3.1 GIS: need for multi-dataset, multi-format support; raster and vector data handling; emphasis on interoperable exchange formats (geoTIFF, etc.).
- 3.2 Text, images and icon information: linking alphanumeric attributes, images, and icons to geographic objects; editable texts.
- 3.3 System customization: modular software, customizable interfaces, with attention to standards for portability.
- 3.4 Required functionalities: interactive editing, image and data management, various query options, a flexible database structure, robust import/export, georeferencing, and statistical capabilities.
- 3.5 Co-pilot software: JRC’s integrated softcopy tool running on Windows; manages data "at continuum" in a single geodatabase; object-based data model (points, lines, surfaces); ASCII-based, well-documented data structures; distributed to national CLC teams.

### 4. Conversion of (semi-) automated classifications
- Cautions about automatic classification: image quality, ground truth differences between land cover vs. land use, and the gap between pixel-based classifications and holistic human interpretation.
- Conversion may be successful for positional accuracy and generalisation, but relies on complex interactions among feature size, patterns, user objectives, input/output scales.
- Methodological approaches include:
  - Reclassification: hierarchical relabelling to CORINE classes.
  - Aggregation: merging nearby units into a single area.
  - Amalgamation: joining or splitting contiguous features with attribute/spatial rules.
  - Smoothing and simplification: boundary refinement for legibility.
- Acknowledges that automatic generalisation introduces errors; the overall quality is a trade-off between accuracy, generalisation, and interpretive judgment.
- Data-model considerations: polygon vs raster representations; pixel size should be small enough so boundary errors are negligible.

### 4.1 Methodological aspects of a conversion
- Spatial generalisation reduces data complexity but adds errors; map quality reflects required simplicity and legibility.
- Types of spatial generalisation: no contiguity, contiguity-aware, and time-varying attributes.
- UK/ Swedish/ Finnish approaches distilled into steps: reclassification, aggregation, amalgamation, smoothing, simplification; emphasis on human interpretation to maintain CORINE’s semantic coherence.

### 4.2 Specific conversion quality issues
- Land cover is a categorical, nominal map; two data models involved: polygon (homogeneous areas) and raster (dominant class per cell).
- Four main error sources in multispectral classification: spectral confusion, mixed pixels, system errors, conceptual errors.
- Phase-space model used to study accuracy of land cover measures; non-parametric or distribution-free methods preferred due to nominal, spatially differentiated classes.
- Generalisation quality assessment is challenging; imperfections are expected and must be weighed against usability and scale.

### 5. Validation methodology
- Validation assesses identification and delineation against CORINE methodology, not the data model/methodology itself.
- Repeats data collection with the same sources using random sampling; results yield a confusion matrix for omission/commission errors.
- Allows stratification across nomenclature levels and regional divisions; outputs include reliability metrics for whole databases or specific strata.

### 5.1 Sampling methodology
- Stratifed random sampling: strata can be land cover items and/or regions.
- Input: digital land cover map and desired number of points per stratum.
- Phase 1: select strata and allocate points; phase 2: draw sampling points within each land cover unit proportionally to area.

### 5.2 Determination of the number of sampling points
- Points per stratum h: nh = [ph(1 - ph)] / (sh^2) with ph = estimated error rate and sh = acceptable absolute standard error.
- Guidance given on balancing precision with practicality (e.g., max 2 points per km^2; densely packing points in small strata may be impractical).

### 5.3 The first and 5.3.2 The second step of random sampling
- Step 1: area-proportional selection of units; step-size derived from stratum area and nh.
- Step 2: determine exact locations of points within units using pure random or systematic/local-random methods; multiple schemes to handle cases with many or few points and variable unit shapes.

### 5.4 Interpretation of the random sampling points
- Interpretation proceeds from higher to lower nomenclature levels; validation circles (1 km radius) interpreted on-screen with a scale not exceeding 1:40,000.
- Final interpretation relies on the same CORINE methodology, with careful attention to minimum mapping size and context.

### 5.4.1 Conduction of the validation
- Validation maps checked for topology; meta-documents and plots accompany interpretations; validation area is cross-checked against original data sources.

### 5.4.2 Verification of the interpretation results
- Documentation includes a plotted validation map, error notes, and plausibility checks; total inner circle area verified against initial estimates.

### 5.5 The raising
- Post-validation overlay of coverages with random points yields a confusion matrix and estimates of correctly classified area per stratum.
- Overall accuracy P is weighted by stratum areas; standard errors computed per stratum and aggregated.
- Aggregation can be performed by regions or by nomenclature levels with area-weighted sums and variances.

### 6. References
- Cited sources include CEC (1994) CORINE Land Cover Technical Guide, DIN norms, and methodological papers on quality, sampling, and validation.

## Part II Addendum to the CORINE land cover nomenclature illustrated guide

### 1. Introduction
- Over ten years of image interpretation experience led to refinements of class definitions without changing core definitions.
- Provides enhanced class definitions, contents, patterns, textures, representative photographs, and country-specific particularities to support uniform interpretation at 1:100 000.

### 2. Methodology used for the compilation of the addendum
- Visual interpretation of Landsat/SPOT imagery remains central.
- Emphasises interpretation elements and landscape-object relationships; aims to tighten guidance for class contents and typical image representations.

### 3. Characteristics of the CORINE land cover classes
- The addendum provides refined/class descriptions with:
  - Dominant objects within each class
  - Typical arrangement patterns and textures
  - Representative photographs
  - Country-specific particularities
- Offers generalisation guidance and explicit thresholds for various classes (e.g., urban, arable, forests, wetlands, waters) to support consistent mapping at 1:100 000.
- Includes examples and figures illustrating texture, patterns, and representative sites.

- Illustrates key classes and general rules, including but not limited to:
  - 1.x Urban fabric (e.g., 111 Continuous urban fabric with high impermeability; 112 Discontinuous urban fabric)
  - 2.x Agricultural lands (e.g., 211 Non-irrigated arable land; 212 Permanently irrigated land; 221 Vineyards; 231 Pastures; 242 Complex cultivation patterns)
  - 3.x Forests (e.g., 311 Broad-leaved forest; 322 Dwarf mountain pine scrub; 324 Forest degradation; 331 Beached dune contexts)
  - 4.x Inland and coastal wetlands (e.g., 411 Treeless fens and transitional bogs; 412 Forested bogs)
  - 5.x Inland and coastal waters (e.g., 511 Water courses and channels; 512 Inland water bodies; 521 Coastal lagoons; 523 Sea water)
- Includes numerous extensions, patterns, and particularities to ensure cohesive interpretation across Phare and non-Phare contexts.

## Overall takeaway for analysts
- The Addendum 2000 framework modernizes CORINE production by documenting softcopy workflows, GIS integration, and standardized validation, while acknowledging limitations of automated classifications.
- Validation employs stratified random sampling to quantify item-level and area-level accuracy, with explicit formulas for sample sizes and error propagation.
- Part II provides refined, example-driven class definitions and interpretation aids to improve cross-country consistency and comprehensibility of landscape features at 1:100 000.