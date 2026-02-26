# CORINE land cover technical guide - Addendum 2000

## Purpose and scope
- Addendum to the CORINE Land Cover Technical Guide (1994) to support ongoing land cover monitoring by the European Environment Agency.
- Provides extra information not in the 1994 guide, including new softcopy methods, semi-automated classifications, and extension of nomenclature for Central/Eastern Europe.
- Extends generalisation rules and enhances understanding of landscape contents at scale 1:100,000.
- Aims to improve data collection, update processes, and cross-country comparability.

## Production methods for CORINE Land Cover
- Hardcopy inventory: computer-assisted photo-interpretation from 1/100,000 scale prints with transparencies; reliance on ancillary data; prone to digitisation errors and border mismatches but historically valuable.
- Softcopy inventory: full interpretation and digitisation on screen; increased efficiency and potential cost reductions; supports integration with GIS and multiple data types.
- Mixed approaches: jurisdictions used various analogue/digital mixes; both approaches and conversion methods remain valid.
- Softcopy/desktop GIS emphasis: visualization, integration of raster and vector data, and flexible data handling.

## Data management and tooling
- GIS integration: need for systems that can handle multiple data sets in parallel, with robust import/export (raster: geoTIFF, BSQ/BIL/BIP; vector formats: Arc/Info, DXF, etc.).
- Text, images, and icons: linkage of alphanumeric attributes with images and non-georeferenced assets; support for editable textual data.
- System customization: modular, flexible software architectures enabling customized interfaces and extensions; preference for standards to ease porting across OSs.
- Required functionalities: interactive editing of geometry/attributes, image management, various query types, customizable geospatial indexing, data import/export, georeferencing, and basic statistics.
- Co-pilot software: JRC-developed integrated GIS for continuous data management across time; main unit is geographic object (points/lines/surfaces) with Catalogue, Typelook, and GraphicSet structures; distributed by JRC for national CLC teams.

## Conversion of (semi-)automated classifications
- Caution on automated conversion: limitations due to variable image quality, differences between land cover vs. land use, and the gap between pixel-based classification and human interpretation.
- Conversion process: can achieve good positional accuracy and support generalisation, but relies on careful handling of scale, features, and context.
- Generalisation methods: reclassification, aggregation, amalgamation (attribute/spatial), smoothing, and simplification; quality depends on per-pixel classification quality and human interpretation.
- Data models: polygon (homogeneous areas) vs. raster (dominant class per cell); both are viable when pixel size is small relative to mapping unit.

## Validation methodology
- Validation aims to assess reliability of the CORINE inventory, not to re-evaluate data collection methods.
- Reinterpretation using random sampling to produce a confusion matrix, allowing error analysis by land cover item and nomenclature level.
- Validation can be stratified by land cover item or geographic region to tailor accuracy assessments.

## Sampling methodology
- Stratified random sampling: strata can be defined by land cover items and/or regions; aim to minimize standard error and tailor sample sizes per stratum.
- Determining the number of sampling points: n_h = p_h(1 - p_h) / sigma_h^2; estimates error rate p_h from repeat interpretations; practical considerations may cap points per square kilometer (e.g., 2 points/km^2).
- Phase 1: select strata and allocate points; phase 2: draw sampling points within strata with area-proportional allocation.
- Location within units: proportional, systematic, and local random sampling to ensure even spatial distribution and valid point placements.

## Random sampling and interpretation
- Three cases for drawing points within units:
  - One point per unit: random point within the unit’s bounding rectangle, ensuring the point lies inside.
  - More than one point: combine systematic and local random sampling.
  - Large numbers of points: use a grid approach with carefully chosen cell size to distribute points evenly.
- Point interpretation: after points are located, land cover at the sampling points is interpreted following the CORINE methodology, with attention to minimum mapping sizes and outer boundary delineation.

## Validation conduction and verification
- Validation on-screen using digital imagery at fixed scales (not exceeding 1/40,000) to preserve context.
- Interpretations documented on plots; meta-data and field survey documentation are essential for interpretation fidelity.
- Topology and mapping checks performed via GIS; total area checks and plausibility reviews ensure consistency across the national dataset.

## The raising (accuracy estimation)
- Build a confusion matrix from validation results to estimate correctly classified area per stratum and overall accuracy.
- Accuracy estimates can be aggregated across strata or across levels of the nomenclature, weighted by stratum areas.
- Standard errors calculated via binomial formulations; area weighting considered for aggregation.
- The approach allows reporting accuracy at different nomenclature levels and regions.

## Part II Addendum to nomenclature illustrated guide
- Introduction: over ten years of CORINE interpretation experience led to refinements of class definitions without altering core content; addendum provides clarifications to improve image interpretation and reduce ambiguities.
- Methodology: emphasis on visual interpretation, interpretation elements, and landscape-object relationships; presentation includes patterns, textures, representative photographs, and particularities for Phare countries.
- Class descriptions: extensive refinements and generalisations for major classes (urban fabrics, agricultural classes, roads/rail networks, water, wetlands, forests, etc.) with:
  - Generalisation rules (e.g., urban fabric density thresholds, 80% impermeable surfaces for continuous urban fabric).
  - Specific peculiarities and examples illustrating typical patterns and textures.
  - Thresholds and exclusions to resolve common confusions.
  - Notes on extensions and cross-country particularities (including Phare countries).
- Scale and coverage: Class definitions and generalisation rules aligned with mapping at 1:100,000; aim to harmonise interpretations across diverse European landscapes.

## Class descriptions overview (highlights)
- Urban fabric (1.x): density-based distinctions between continuous and discontinuous urban fabric; several specific rules for aggregation and buffering.
- Industrial/transport and related areas (1.3–1.4, 121, 122, etc.): distinctions based on built-up surfaces, infrastructure, and associated lands; emphasis on buffer zones around runways, ports, and roads.
- Agricultural classes (2.x): division into arable land, permanent crops, pastures, and heterogeneous areas; special notes on abandoned/fallow land and irrigation.
- Forests and natural areas (3.x): subdivided into broad categories (forests, shrubs, open spaces, moorlands, sclerophyllous vegetation, coniferous forests, mixed forests); detailed textures and extension rules; many country-specific particulars.
- Wetlands and coastal zones (4.x): inland wetlands vs coastal wetlands with specific vegetation and hydrology criteria.
- Inland and marine waters (5.x): distinctions among inland waters, coastal/marine waters, lagoons, channels, and associated hydrological features; guidance on linking/disconnecting water bodies for mapping logic.

## Implications for data leaders
- Emphasize robust data governance: standardized production workflows (hardcopy to softcopy to GIS), consistent validation, and transparent accuracy reporting.
- Prioritise data interoperability: support for multiple formats, shared nomenclature, and cross-border comparability through the addendum’s refinements.
- Invest in metadata and documentation: detailed methodological notes, validation procedures, and class definitions to enable reuse and auditability.
- Plan for updates and continuity: Co-pilot-like systems illustrate the benefits of a continuous, time-consistent data base across revisions.
- Leverage stratified validation: stratified random sampling enables targeted accuracy assessments by region or class, improving confidence in aggregated results.

## References
- Core sources include CEC CORINE Land Cover Technical Guide (1994), DIN standards, and various methodological and quality management references cited in the addendum.