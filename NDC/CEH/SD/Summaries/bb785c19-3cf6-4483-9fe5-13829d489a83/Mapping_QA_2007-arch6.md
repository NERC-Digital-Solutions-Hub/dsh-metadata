# Mapping Quality Assurance Exercise

- A 2007 Countryside Survey initiative to map habitats and landscape features digitally in the field, leveraging Surveyor software to reduce interpretation error and enable rapid QA in a geodatabase.
- Data collected included areas, lines, and points with mandatory attributes; outputs uploaded to an interactive wiki for early data checks; QA teams visited survey teams to verify protocols.
- The exercise assesses data quality by comparing field (surveyors) data with QA assessments, and by analysing spatial concordance, attribute consistency, and change coding.

## Data and Methods

- Data architecture and workflow
  - Field data: polygons (areas), lines (linear features), and points (point features) with Broad Habitat (BH) codes and species attributes.
  - Central QA: digital QA datasets aligned to the field data in a single geodatabase; both datasets excluded unsurveyed or refused areas for comparability.
- QA extent and sampling
  - QA covered 23 one-kilometre squares across Great Britain; aimed to be representative of land classes; some areas were inaccessible; focus was on common areas between QA and survey data.
- Analysis approaches
  - Direct comparison of aggregate areas/lengths/points per square (CSV/SAS analyses).
  - Raster analysis: each square divided into 10,000 cells (10x10 m); dominant BH per polygon assigned; raster-level agreement examined.
  - 100-point grid: overlaid on each square to compare BH occurrence at equivalent locations; concordance and discrepancy tallied.
  - Attribute comparisons: reference ID layers enabled comparison of species attributes across matched features.
  - Linear and point features: separate analyses with dedicated matching (buffering or closest matching) to compare land-use themes and habitat codes.
  - Surveyor efficiency: assessment of visit status usage and data completeness (e.g., dominant species recording, coverage of visited areas).

## QA Extent and Coverage

- Squares and scope
  - QA mapped and evaluated data for 23 1km squares; effort exceeded prior QA exercises and encompassed a range of land classes.
  - Data exclusions: unsurveyed areas and areas with refused access were excluded before comparisons.

## Key Findings

- Direct comparison of aggregate data (BHs, areas, lengths)
  - Across BHs, mean differences between CS (surveyors) and QA typically under 1–3.5%, indicating generally good agreement; some BHs showed larger deviations (e.g., Improved grassland, Dwarf Shrub Heath, Bog, Urban).
  - Overall, most BHs exhibited minor discrepancies, though several squares displayed higher variance, flagging potential definitional or boundary issues.
- Raster data comparisons
  - Average raster agreement across squares was 76%, with notable variability by square (high in 364, 488; lower in 261, 773).
  - Agreement by BH per square highlighted specific mismatches (e.g., Neutral vs Improved Grassland, Urban vs other BHs; some squares showed near-perfect alignment, others substantial misalignment).
- 100-point concordance
  - Most squares showed good concordance between QA and CS at 100-point level, but some outliers exhibited low concordance (e.g., square 773 at 19%, square 261 at 41%).
  - A BH/PH matrix (Table 6.3b) indicated generally strong matches for many habitats, but notable mis-matches for certain upland and dune habitats, and for areas where machair or sand-dune-specific habitats were present.
- Polygon species attributes
  - 45% of QA polygons had at least one listed species present in the matched CS polygon (excluding mosaics).
  - 77% of matched polygons had a matching BH between QA and CS when species matched; conversely, 23% had no BH match despite species presence.
  - Species concordance across commonly recorded species was around 40%; Lolium perenne and Calluna vulgaris showed relatively higher agreement, while many grasses and shrubs varied due to dominance and identification differences.
- Linear features and point features
  - Lengths of linear features per square were broadly similar between QA and CS; few mismatches (e.g., distinctions between fences vs walls, or belts of trees vs generic woodland belts).
  - Point feature habitat codes were largely consistent between QA and CS; some confusion between woodland/forest codes observed, likely due to legacy coding in prior surveys.
- Change recording
  - The 2007 digital change field (real change, error change, no change) generally aligned with QA codes; some surveyors struggled with the new change-field workflow early in the survey.
  - Overall, change coding adhered to protocols, though habitat-related change assessment remained challenging.

## Notable Issues and Explanations

- Blanket Bog and upland definitions
  - Discrepancies centered on Blanket Bog vs Dwarf Shrub Heath, exacerbated in squares with complex upland mosaics; the CS field handbook and 2007 key revisions influenced classifications.
- Grassland classifications
  - Neutral vs Improved Grassland often overlapped in species composition; no systematic bias detected between CS and QA, but misclassifications occurred when boundaries were unclear.
- Upland mosaics
  - Mosaic mapping of upland habitats caused mismatches when mosaics were disaggregated into constituent BHs; this highlighted difficulty in mapping a habitat continuum with sharp boundaries.
- Sand dune and machair
  - Scottish machair on dunes presented local nuance; in some squares, machair was allocated to Neutral or Improved Grassland rather than a dune-specific habitat, indicating locality-driven complexities.
- Urban vs grassland
  - Some urban areas were inconsistently coded as Improved Grassland, reflecting ambiguity in field recording guidelines for amenity grassland versus urban land use.

## Data Products and Outputs

- Data products and outputs
  - Geodatabase and raster representations of BHs across squares; 10x10 m raster grid products enabling spatial comparisons.
  - 100-point BH/PH concordance matrices and 100-point habitat agreement tables.
  - Point- and line-based habitat code comparisons, with reference layers for cross-dataset evaluation.
  - Change-coding results and methodology documentation to support data updating and future surveys.
  - QA integration via wiki for early data checks and field guidance.

## Conclusions and Recommendations

- Overall data quality
  - Digital field mapping and in-field QA significantly improved data quality and consistency relative to past paper-based workflows.
- Habitat definitions and training
  - Some key habitat definitions (e.g., Blanket Bog, Coniferous vs Broadleaved Woodland, Neutral vs Improved Grassland) require ongoing refinement and clearer guidance; targeted training could reduce cross-team misclassifications.
- Handling mosaics and upland variability
  - Continue to develop methods for disaggregating mosaics and for interpreting continuums of habitat types in upland areas; consider more nuanced categories or probabilistic approaches in borderline cases.
- Local habitat specificity
  - Account for local habitat nuances (e.g., machair, dune systems) in field manuals and QA protocols to improve cross-square consistency.
- Change recording
  - Maintain the digital change field and refine guidance to help surveyors apply change coding consistently, especially in complex habitat contexts.
- Data use and dissemination
  - The QA framework demonstrates a robust approach for validating data products and supports transparent reporting of uncertainties; continued emphasis on data provenance, metadata, and clear definitions will aid reuse by policymakers and practitioners.

## Relevance to Data Support Archetype

- Demonstrates end-to-end data workflow: from field data capture (Surveyor) to centralized QA, to multi-faceted analyses (direct, raster, 100-point, and polygon/species analyses).
- Highlights data integration challenges when combining heterogeneous data sources and formats (areas, lines, points; BH codes; species lists) within a geodatabase.
- Provides practical QA metrics and benchmarks (per-square agreement, BH-level concordance, and species-level alignment) to inform data quality assurance in broader, non-specialist contexts.
- Illustrates how data products (maps, rasters, grids, and change records) can be produced to enable self-service analysis and decision-making by end users.