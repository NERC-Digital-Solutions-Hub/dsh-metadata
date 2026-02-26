# Final Report for LCM2007 - the new UK land cover map

- Overview
  - Presents the UK-wide Land Cover Map 2007 (LCM2007), a parcel-based land cover product mapped to UK Broad Habitats, intended as a policy-relevant evidence base for biodiversity, ecosystem services, and landscape planning.
  - Compares LCM2007 with Countryside Survey (CS) 2007 data and discusses alignment, discrepancies, and implications for monitoring frameworks.

- Key comparisons with Countryside Survey 2007
  - Similar area estimates (within CS 95% confidence limits UK): Broadleaved woodland, Acid Grassland, Inland Rock.
  - Dissimilar area estimates (beyond CS 95% confidence limits UK): Arable and Horticulture; Improved Grassland; Neutral Grassland; Dwarf Shrub Heath; Bog; Montane Habitats; coastal habitats.
  - Factors contributing to differences:
    - How “Arable and Horticulture” is defined and classified in each product.
    - Spectral confusion due to diverse crop types and growth stages.
    - Inclusion of Boundary and Linear Features in LCM2007 vs CS mapping approach.
    - Temporal differences and multi-year image requirements affecting land cover categorisation (e.g., temporary grass vs arable).
    - Differences in how Grassland types are represented (e.g., Neutral vs Improved Grassland) and how peat and fen areas are captured.
    - CS patch sizes vs LCM2007 MMU affecting representation of small habitats (e.g., Fen, Marsh and Swamp).

- UK-wide and country-level land cover patterns (4.4 UK Land Cover)
  - More than 50% of the UK is intensive land use (Arable and Horticulture plus Improved Grassland) or Built-up Areas.
  - Woodlands account for about 12% UK-wide (split between Broadleaved and Coniferous).
  - Semi-natural areas constitute a large share, with Scotland hosting the largest proportion of Mountain, Heath, and Bog and substantial semi-natural grassland.
  - Notable cross-country differences in land-cover composition and representation of certain habitats compared with LCM2000.

- Discussion and interpretation (4.5 Summary and discussion)
  - Agreement between LCM2007 and CS varies by Broad Habitat, highlighting sampling, classification, and spatial-structure differences.
  - Grassland classes pose particular challenges due to one-to-many relationships with Broad Habitats, underpinning Broad Habitat Association (BHA) rules to improve interpretability.
  - LCM2007 shows high correspondence with CS for Arable and Horticulture at the 1 km square scale, but broader habitat extents may diverge due to structural differences in spatial frameworks.
  - Fen, Marsh and Swamp exhibits large discrepancies; CS often records smaller patches, while LCM2007 frequently maps as Rough Grassland or Acid Grassland, suggesting potential use of additional KBEs to reallocate some areas.
  - The discussion emphasizes that LCM2007 and CS are complementary: CS provides ground-based habitat detail; LCM2007 provides coast-to-coast coverage and consistent UK-wide frame for policy monitoring.

- Example areas (5.1)
  - Illustrative examples across uplands, calcareous grasslands, urban areas, and arable/fenland landscapes demonstrate LCM2007’s ability to depict mixed habitat mosaics and landscape contexts (e.g., montane, calcareous grassland, urban parks, fen/arrost).

- Vector and raster products (5.2)
  - Vector product: land parcels with attributes including area, source images, Broad Habitat, KBE history, and processing details.
  - 25 m raster: 23 LCM2007 classes with full thematic detail; enhanced metadata linked to each parcel.
  - 1 km raster: two options per pixel:
    - Percentage cover for each LCM2007 class.
    - Dominant class per pixel.
  - Metadata and provenance documented; KBEs are recorded in the parcel attributes to enable traceability and potential reversion if needed.
  - Access: 1 km rasters via CEH Information Gateway; full vector and 25 m rasters available on request under licence.

- Validation, accuracy and quality assurance
  - Ground reference data and validation procedures underpin reported thematic accuracy; the document discusses both Producer’s and User’s accuracies and the influence of KBEs on misclassification.
  - The validation framework acknowledges uncertainties at the class level, particularly for grassland, fen, bog, montane habitats, and coastal categories.
  - The parcel-level metadata enables users to assess the plausibility of classifications in their local context, supporting “fit for purpose” use.

- Change mapping and monitoring
  - Change detection across LCM1990, LCM2000, and LCM2007 is complex due to differing spatial structures and class schemes; robust per-pixel change methods are not fully established.
  - Recommendation to explore aggregated class changes, focus on consistently mapped classes, or apply trajectory-based analytical approaches.

- Governance, metadata, and data access
  - LCM2007 governance emphasizes data provenance, traceability, and data sharing considerations; rich metadata accompanies the vector product.
  - Data access channels and licensing details:
    - 1 km rasters via CEH Information Gateway.
    - Full vector and 25 m rasters available on request under licence; licensing fees may apply.
  - The document advocates for data governance practices that support policy use while balancing openness and licensing constraints.

- Implications for monitoring frameworks (practical takeaways)
  - LCM2007 delivers UK-wide, policy-relevant Broad Habitat land cover with a robust spatial framework suitable for biodiversity monitoring, ecosystem service assessment, and landscape planning.
  - The combination of KBEs and contextual data (terrain, soils, urban context, coastal proximity) demonstrates how ancillary information can reduce spectral confusion but also introduces management and interpretive risks.
  - Validation results highlight the need to consider both producer’s and user’s accuracies when informing policy decisions, especially for grasslands, fen/bog, montane, and coastal habitats.
  - The alignment with CS remains valuable for cross-validation and multi-source evidence; however, differences in spatial structure and MMU necessitate careful interpretation when integrating with field surveys or ground-truth data.
  - The bespoke validation approach and parcel-level metadata provide a transparent basis for monitoring frameworks to assess data quality, reproduce analyses, and apply fit-for-purpose classifications in policy contexts.

- Key methodological and governance notes for monitoring authors
  - Use the UK-wide vector-based framework for policy-relevant habitat networks and connectivity analyses, while leveraging higher-resolution raster data for detailed local assessments.
  - Consider the Broad Habitat Association rules to reconcile grassland-to-habitat mappings across datasets.
  - Recognize change detection challenges across historical CEH land cover products; plan for data harmonisation using a common spatial structure as a long-term objective.
  - Ensure metadata, data provenance, and processing histories are primary outputs to enable auditability and governance in monitoring programs.
  - Leverage accessibility options and licensing arrangements to balance open access with user needs and intellectual property considerations.