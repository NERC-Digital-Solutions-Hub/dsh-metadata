# Mapping Quality Assurance Exercise

- Purpose and context
  - Assess quality assurance (QA) of the Countryside Survey 2007 mapping effort.
  - Move to digital mapping (Surveyor software) to reduce interpretation errors and enable rapid analysis in a geodatabase.
  - QA involved comparing surveyors’ data (CS) with QA data across multiple dimensions (areas, lines, points, attributes), using several analytical approaches.
  - Used an interactive wiki for early data checks; QA teams visited survey squares to ensure protocol adherence.

- Scope and extent
  - QA mapping covered 23 one-kilometre squares, representing diverse land classes; some areas were inaccessible or refused access.
  - QA and survey data were aligned by masking unsurveyed or refused areas to ensure comparability.
  - The study examined both spatial extents (areas, lines, points) and associated attributes (habitat codes, species).

- Methodology and workflow
  - Fieldwork and QA conducted close in time to minimise temporal vegetation changes.
  - Data collected on tablets and uploaded to a single geodatabase; differences in visit coverage and access were accounted for.
  - Several analytical methods used:
    - Direct comparison of aggregate areas/lengths/points per square.
    - Raster-based comparisons by converting polygons to 10x10 m cells within each 1 km square.
    - A 100-point grid overlay to assess concordance of Broad/Priority Habitats at equivalent resolution.
    - Attribute-level comparisons for areas, lines, and points (reference IDs for polygon matches).
    - Assessment of surveyor efficiency and data completeness (e.g., visit status layers, species recording).

- Key analysis methods (highlights)
  - 4.1 Direct aggregate comparison for areas, lengths, and points.
  - 4.2 Raster data analysis (dominant Broad Habitat per 10x10 m cell; sampled with a resolution grid).
  - 4.3 100-point grid analysis to gauge commonality of Broad Habitats at a consistent density.
  - 4.4 Polygon-level analysis of species attributes within spatially matched polygons.
  - 5 Surveyor efficiency metrics (visit coverage, data completeness, species recorded per area).
  - 6.1–6.3 Habitat-area concordance across squares; 6.2 raster agreement by square; 6.3 100-point concordance by square.
  - 6.4 Species attributes within polygons; concordance between QA and CS on listed species and their habitat associations.
  - 7 Linear features: consistency of land-use themes and alignment of linear features between QA and CS datasets.
  - 8 Point features: habitat codes for features like scattered trees, woodland, etc., and cross-checks between QA and CS.
  - 9 Change recording: analysis of how change codes (Real Change, Error Change, No Change) were assigned, including agreement between QA and CS.

- Main findings (overall quality and areas needing attention)
  - Broad Habitat (BH) agreements between CS and QA
    - Direct-area concordance: 81% of squares record the same BH by CS and QA; overall differences in mean BH extents are typically small (mostly <3.5% for most BH types).
    - Notable discrepancies: Improved grassland, Neutral grassland, Dwarf Shrub Heath, Bog, Urban areas, and some upland/mosaic areas; Blanket Bog issues linked to definitional revisions and habitat classification debates.
    - Some squares with higher disagreement identified (e.g., certain upland squares with mosaics or local habitat peculiarities like machair in Scotland).
  - Raster data agreement (per square)
    - Overall average agreement across squares: 76%.
    - High agreement squares: 364 (98%), 488 (94%).
    - Low agreement squares: 261 (49%), 773 (23%), 935 (52%).
    - Discrepancies often tied to habitat definitions, mosaics, or local landscape specifics.
  - 100-point concordance (per square)
    - Overall concordance: around 77% (varied widely by square).
    - Notable outliers: square 773 (19% concordance), square 261 (41% concordance); some squares showed strong agreement (355, 364, 359, 694, 694, etc.).
    - Differences attributed to habitat boundary delineations, mosaic representations, and local habitat idiosyncrasies (e.g., Blanket Bog vs Dwarf Shrub Heath, machair).
  - Polygon-level species attributes
    - 45% of QA polygons had at least one listed species present in the matched CS polygon.
    - Species concordance varied by habitat type; woodland and Improved Grassland showed higher concordance; broader plant groupings often yielded lower species-level agreement.
    - Among polygons with matching species, 77% also had a matching habitat code, indicating habitat and species assignments were generally coherent but not always aligned.
  - Point and linear feature codes
    - Point features: habitat codes for co-located QA and CS points were largely consistent; minor confusion between some woodland classifications persisted.
    - Linear features: strong consistency in land-use theme coding between QA and CS; very few cases where QA recorded a feature and CS did not.
  - Change recording
    - Change coding largely aligned with QA protocols; the digital system enabled more precise change documentation (Real, Error, No Change).
    - Some surveyors initially struggled with change coding; overall, QA indicated broad agreement, though some habitat-related change coding remained challenging.
  - Data and definitions issues
    - Woodland definitions and Broad Habitat distinctions (e.g., Coniferous vs Broadleaved woodland) revealed some misapplications or ambiguity in field guidance.
    - Upland mosaics and complex boundary areas highlighted limitations of fine-scale correspondence between habitat types in some squares.
    - Blanket Bog remained a challenging habitat to classify consistently, due in part to evolving definitions and field-handbook revisions.

- Implications for data quality and future work
  - The digital approach substantially improved data quality and in-field verification compared with prior methods, but some habitat-definition ambiguities and mosaic mapping challenges persist.
  - Training and clearer, updated field guidance are important to reduce misclassification in sensitive or newly redefined habitats (e.g., Blanket Bog, conifer/broadleaved woodland distinctions).
  - Mosaics and fine-scale boundaries in upland and machair-type landscapes require careful handling or acknowledgment of inherent mapping uncertainty.
  - Continued refinement of habitat dictionaries and QA procedures can further improve alignment between CS surveyors and QA assessors in future surveys.
  - The QA exercise demonstrates that, while not perfect, the combination of multiple analytic approaches provides robust multi-scale validation of habitat mapping and associated species data.

- Notable sections and their contributions to the dataset quality
  - 6.1 Direct BD-area comparison: showed general alignment with small mean differences across many habitats, spotlighting specific habitats with larger discrepancies.
  - 6.2 Raster and 6.3 100-point analyses: gauge spatial concordance at multiple resolutions, identifying which squares reliably agree and which require review.
  - 6.4 Polygon species analysis: links habitat accuracy to species occurrence, illustrating how habitat-coded polygons align with species lists.
  - 7 Linear and 8 Point analyses: confirmed consistency in land-use and habitat coding for linears and points, with some cautions about classification boundaries.
  - 9 Change assessment: validated the change-recording workflow under digital survey conditions, highlighting strong overall adherence to protocols.

- Bottom-line
  - The 2007 Mapping Quality Assurance Exercise demonstrates a high level of overall agreement between CS surveyors and QA assessments across multiple data dimensions, with some habitat-specific and square-specific exceptions.
  - The shift to digital data collection markedly improved QA capabilities, though continued attention to habitat definitions, mosaics, and localized landscapes will further enhance reliability in future surveys.