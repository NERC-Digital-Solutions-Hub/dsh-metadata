# Final Report for LCM2007 - the new UK land cover map

- Overview
  - Presents the UK Land Cover Map 2007 (LCM2007), a parcel-based land cover product for the UK, GB, England, Scotland, Wales, and Northern Ireland.
  - Built from multi-temporal satellite imagery and integrated with national cartography; aims to provide a robust, reusable evidence base for biodiversity, habitat monitoring, landscape planning, and change detection.
  - Delivers a UK-wide spatial framework that supports cross-sector collaboration and policy analysis, with detailed metadata and traceability of processing steps.

- Data and product architecture
  - Vector product: land parcels annotated with Broad Habitat (BH) class, Broad Habitat sub-classes (BHSub), processing history, and knowledge-based enhancements (KBEs). Includes 23 LCM2007 classes mapped to Broad Habitats, plus 10 aggregated classes.
  - Raster products: 
    - 25 m resolution raster (23 classes)
    - 1 km resolution rasters: 
      - Percentage cover per 1 km cell for each class
      - Dominant class per 1 km cell
  - Knowledge-based enhancements (KBEs): seven automated rules (e.g., Terrain, Soil, Coastal/Offshore, Urban proximity, etc.) applied after initial classification to resolve spectral confusion and refine class allocation; KBEs modified about 20% of parcels; supports reversibility and auditing.
  - Metadata and provenance: each parcel includes image sources, KBE history, ProbList (top spectral class probabilities), CorePixels, and Construct history; designed to enable validation and reproducibility.
  - Access and licensing:
    - 1 km raster data via CEH Information Gateway
    - Full vector and 25 m raster products available on request (licensing may apply)
  - Validation status: overall Producer/User accuracy around 83% for the 23-class system; accuracy varies by class; spatial framework is designed to improve cross-year comparability.

- Validation against Countryside Survey (CS) 2007
  - Key findings:
    - Broad Habitat (BH) level agreement: about 62%
    - Broad Habitat Association (BHA) level agreement: about 76% (when using BHA links to accommodate one-to-many relationships)
    - Grassland categories show notable discrepancies due to spectral variability and how classes are defined across products
    - Arable and Horticulture tends to be overestimated by LCM2007 relative to CS; differences partly driven by what is included in the Arable and Horticulture class (e.g., boundaries, temporary grass, uncropped land) and the need for multi-year imagery to achieve full UK coverage
    - Fen, Marsh and Swamp (FMS) shows large disparities (CS estimates much higher than LCM2007) due to complex mosaics and small patch sizes; many FMS areas in CS are mapped as Rough Grassland or Acid Grassland in LCM2007
    - Differences in boundary delineation, MMU constraints, and CS’s field-based measurement vs. satellite-derived maps contribute to the discrepancies
  - Implications:
    - Spectral confusion and differing spatial structures across products limit exact year-to-year change detection
    - FMS and certain grassland categories require careful interpretation and potential KBEs or supplementary data to improve alignment

- Implications for Data Leaders (data strategy, governance, and use)
  - Data strategy and governance
    - LCM2007 provides a stable, UK-wide land-cover framework suitable for biodiversity monitoring, habitat assessment, and ecosystem service analysis; its vector framework with rich metadata supports reproducibility, auditability, and governance.
    - Facilitates cross-network collaboration by offering a common land-cover reference, with controlled data access and licensing.
    - Enables traceability of processing history and knowledge-based adjustments, allowing users to understand model assumptions and to reproduce or update analyses.
  - Data quality, interoperability, and standards
    - 83% overall accuracy highlights usefulness as a baseline for many applications, but users should account for class-level variability and known problem areas (e.g., upland, mosaic, grassland types).
    - KBEs and multi-source data integration improve thematic resolution and spatial coherence; however, some KBEs rely on external data and may introduce errors, necessitating manual validation where critical.
    - The spatial framework, derived from MasterMap and other high-resolution cartography, enhances interoperability with other national datasets and supports future change detection.
  - Data sharing and access
    - UK-wide design supports cross-network adoption for policy and planning; licensing arrangements allow broader use while controlling access where necessary.
  - Change detection and longitudinal analyses
    - Comparing LCM2007 with earlier CEH maps (LCM1990, LCM2000) is complex due to evolving class definitions and spatial structures; robust change detection requires sophisticated methods and potentially re-structuring older maps into a common spatial framework.
    - The generalised spatial framework of LCM2007 offers a path toward consistent long-term monitoring but requires careful methodological alignment across years and products.
  - Future directions and improvement opportunities
    - Ongoing alignment with new data sources and cartographic updates to support change detection and long-term monitoring.
    - Potential standardisation of cross-year spatial structures to improve comparability, and the development of additional KBEs to better allocate mosaic or difficult habitats (e.g., Fen, Marsh and Swamp).
    - Integration with other data sources (soil, climate, hydrology, etc.) to refine classification and support more robust ecological analyses.

- Limitations and challenges (for strategic planning)
  - Spectral confusion remains a major issue, particularly for grasslands and complex mosaics; KBEs help but cannot eliminate all misclassifications.
  - Change mapping between generations is challenging because of non-commensurate class definitions, spatial fragmentation, and varying error rates.
  - Data licensing and availability differ by country and data source; some datasets have restrictions or fees.
  - MMU (Minimum Mapping Unit) constraints and boundary delineation can affect detection of small or fragmented habitats, especially in upland and coastal mosaics.
  - Differences between CS field data and satellite-derived maps require careful interpretation; some habitat types are better represented in one source than the other.

- Practical takeaways for Data Leaders
  - Adopt LCM2007 as a baseline UK-wide land-cover reference for monitoring and policy support, while using CS and other data sources for validation and cross-checks.
  - Leverage the parcel-level metadata and KBEs to assess data quality in specific regions and to tailor analyses to local needs.
  - Plan for evolving data frameworks, with attention to cross-year comparability, and consider re-aligning older maps into the LCM2007 spatial structure when feasible.
  - Utilize the open data pathways (CEH Information Gateway) for scalable analyses, and engage with licensing to balance access with stewardship.
  - Anticipate and address class-specific limitations in strategic reporting, particularly for grasslands and fen-like habitats, by integrating supplementary datasets or developing targeted KBEs.

- End note
  - LCM2007 represents a significant advancement in national-scale land cover mapping, offering a transparent, reusable, and governance-friendly framework that supports diverse policy, planning, and scientific needs, while acknowledging the complexities in comparing with field-based surveys and earlier maps.