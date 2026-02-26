# CORINE land cover technical guide - Addendum 2000

- Purpose: This addendum to the CORINE Land Cover Technical Guide (1994) provides additional information for data collection and updating, describes new methodological developments (softcopy interpretation and semi-automated conversions), extends nomenclature for Central and Eastern Europe, adds generalisation rules for mapping at 1:100 000, and improves understanding of landscape contents. It supports land cover monitoring by the European Environment Agency and related national teams, and enhances data quality, openness, and update processes.

## Part I: State-of-play and production methods

- Overall aim for monitoring: Deliver comparable, policy-relevant environmental health measures to scrutinise and inform decisions; guide future monitoring approaches.
- Production approaches:
  - Hardcopy inventory: Original CORINE workflow using computer-assisted photo-interpretation on 1/100,000 hardcopy image prints with overlays of ancillary data; valuable but prone to digitisation errors and border-matching issues.
  - Softcopy inventory: Modern approach using on-screen interpretation (softcopy) with integrated GIS; supports more efficient workflows and direct digital outputs.
  - Softcopy tools and integration: Emphasises GIS capability, multi-dataset viewing, and flexible data types; discusses data formats (geoTIFF, GIS vector formats) and interoperability.
  - Co-pilot software: JRC-developed integrated GIS for CORINE data production, maintenance, and updating; data are managed contiguously across time (no breaks) and stored in ASCII-based structures for easy editing.
- Data management and visualization:
  - Requires linking of alphanumeric attributes, icons, and images to geographic objects; supports on-screen display, editing, and cross-referencing with ancillary data.
  - System customization: Encourages modular design, user interfaces, and standards compatibility to facilitate porting across platforms.
  - Required functionalities: Interactive display/editing, image/raster-vector integration, database customization, import/export, geo-referencing, statistical tools, and comprehensive documentation of data structure.
- Methodological developments for conversion:
  - Acknowledges the limitations of (semi-)automated classifications due to image quality, terrain effects, and the gap between pixel-based classifications and human holistic interpretation.
  - Conversion/Generalisation workflow (three broad types): no contiguity consideration, contiguity-aware generalisation, and time-varying attributes.
  - Common conversion operations: reclassification (hierarchical relabelling within the 44-class hierarchy), aggregation (merging nearby small features), amalgamation (joining or splitting features with consideration of neighboring classes), smoothing (boundary adjustment), and simplification (reducing boundary complexity).
  - Relationship between automated per-pixel accuracy and generalisation: generalisation adds simplification errors; overall quality deteriorates with simplification but improves legibility.
- Specific conversion quality issues:
  - Data models: polygon (homogeneous areas with vector boundaries) vs raster (dominant class per cell); both approaches can be valid if pixel size is well below the minimum mapping unit.
  - Primary error types in multispectral classification: spectral confusion, mixed pixels, system errors, and conceptual misalignments with CORINE class definitions.
  - Statistical properties: phase-space model describes the link between taxonomy definitions and map accuracy; traditional formal statistics are often unsuitable for nominal, spatially differentiated land-cover classes.
  - Generalisation properties: recognition that performance measures should reflect both real classification error and the additional errors introduced by simplification and aggregation.
- Validation methodology:
  - Purpose: quantify reliability of CORINE inventories, not to validate the data model itself.
  - Approach: repeat data collection for comparison using random sampling; produce confusion matrices to identify omissions/commissions; enable aggregation to higher nomenclature levels or regions; supports stratification.
- Part II (nomenclature addendum) addresses:
  - Refinements to class definitions, clarifications of contents, and general patterns to aid interpretation.
  - Enhanced guidance on interpretation elements (texture, pattern) and typical photographs for European landscape types.

## Part II: Addendum to the CORINE land cover nomenclature illustrated guide

- Purpose: Improve consistency and accuracy of image interpretation by refining definitions, listing inclusions/exclusions, and presenting generalised patterns, representative photographs, and class particularities.
- Coverage: Detailed refinements across major classes (e.g., urban fabric, industrial units, transport networks, arable land, permanent crops, pastures, forests, wetlands, inland/marine waters, and coastal features).
- Practical guidance for interpreters:
  - Provides texture, pattern, and representative examples to distinguish classes at 1:100 000 scale.
  - Specifies threshold guidelines and generalisation rules (for example, 80% impermeable surfaces for continuous urban fabric, 25 ha minimums, and spacing/aggregation rules for subdivided parcels).
  - Notes class particularities (e.g., housing estates, hop plantations, vineyards, and complex cultivation patterns) and how to handle mixed or transitional areas.
- Outcome: A richer, more actionable set of class criteria and interpretation aids to improve cross-country comparability and update consistency.

## Implications for monitoring frameworks

- Standardization and comparability:
  - The addendum strengthens standardized methods for data collection, interpretation, and updating, enabling consistent comparisons over time and across regions.
- Data quality and governance:
  - Emphasises data provenance, metadata, and open sharing of underlying data where feasible; discusses data management standards at source and governance considerations for data updates.
- Methodological clarity:
  - Provides clear guidance on when to use hardcopy versus softcopy workflows, how to implement semi-automated classifications, and how to validate and quantify accuracy.
- Resource planning and risks:
  - Highlights challenges such as data gaps, organizational silos, and barriers to sharing data; offers validated sampling frameworks and quality-control approaches to mitigate these risks.
- Practical guidance for policy-relevant monitoring:
  - The framework supports monitoring of landscape change, urbanization, agriculture, ecosystems, and land-use pressures with a transparent, auditable methodology and explicit confidence measures.

## Key takeaways for authors of monitoring frameworks

- Adopt a dual production approach where appropriate:
  - Maintain hardcopy/photo-interpretation foundations where necessary, but progressively implement softcopy/GIS-based workflows to improve efficiency, repeatability, and data sharing.
- Use robust validation designs:
  - Implement stratified random sampling for validation, with clear rules for sample size, point placement, interpretation blinding, and scale-consistent interpretation.
  - Report confusion matrices and standard errors at multiple nomenclature levels and strata to quantify reliability.
- Embrace explicit generalisation and data quality concepts:
  - Acknowledge the trade-offs between data generalisation (simplicity and legibility) and accuracy; document how reclassification, aggregation, amalgamation, smoothing, and simplification affect results.
- Ensure data interoperability and openness:
  - Prepare for a range of formats (raster and vector) and encourage open, well-documented data standards and interfaces to facilitate reuse and cross-project coordination.
- Leverage Part II refinements for interpretation consistency:
  - Apply refined class definitions, interpretation patterns, textures, and representative examples to reduce misclassification and improve cross-country comparability, especially when updating the inventory in Central and Eastern Europe.