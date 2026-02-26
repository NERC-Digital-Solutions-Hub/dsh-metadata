# Final Report for LCM2007 - the new UK land cover map

- Overview
  - LCM2007 provides UK-wide, parcel-based land cover mapping with 23 Broad Habitat classes, plus 25 m raster and 1 km raster derivatives.
  - GB and NI are mapped within a unified UK framework but maintained as separate spatial databases.
  - Vector parcels carry rich metadata (training data, processing history, KBE steps, provenance) to enable traceability and validation.

- Key data assets and structure
  - Vector product: land parcels with attributes including area, source images, Broad Habitat (BH) class, Broad Habitat sub-classes, processing history (Construct, KBE history), ProbList (top spectral class probabilities), and CorePixels.
  - Raster products: 25 m resolution with 23 LCM2007 classes; 1 km resolution rasters (percentage cover per class and dominant class per pixel).
  - Spatial framework: integration of OS MasterMap and large-scale vector data; minimum mappable unit ~0.5 ha; minimum feature width ~20 m; segmentation tied to cartographic parcels and image segments.
  - Knowledge-based enhancements (KBE): seven automated rules using context such as terrain, soils, urban/coastal proximity to improve classifications; traceable provenance captured in KBE logs.
  - Data sources: multi-temporal satellite imagery (Landsat TM, ETM+, SPOT-4/5, AWIFS), ground truth (Countryside Survey Broad Habitat data, field points), national cartography (OS MasterMap GB, OSNI LPS), soils and DEM layers, etc.
  - Accessibility: 1 km rasters publicly via CEH Information Gateway; full vector and 25 m rasters available on license.

- Processing and methodology
  - Image preparation and segmentation: cloud masking, atmospheric correction, geo-registration; segmentation across ~37 composites and single-date images; integration with cartographic parcels and agricultural boundaries.
  - Classification: parcel-based supervised maximum likelihood classification using training areas from ground data; multiple dates used to capture phenology; top spectral classes recorded per parcel.
  - Knowledge-based enhancements: sequential application of KBEs to resolve spectral confusion (urban, soils, coast, terrain) and improve thematic resolution; ~20% of parcels reclassified due to KBEs.
  - Edits and change mapping: targeted manual edits for rare classes and winter-image issues; cross-epoch change detection acknowledged as challenging due to differing class definitions and temporal misalignment.
  - Quality assurance: ground validation with 9,127 points; overall accuracy ~83% for LCM2007 classes; class-level challenges noted for grassland types, Montane and coastal habitats, Fen/Marsh/Swamp (often below MMU or spectrally ambiguous).
  - Change interpretation: differences in spatial framework and class definitions between epochs complicate distinguishing real habitat change from classification error.

- Knowledge-based enhancements and data integration
  - KBEs leverage urban context, coastal proximity, terrain, and soils to improve classification where spectral data alone is ambiguous.
  - Terrain-soil interactions are especially important for distinguishing grassland types and upland habitats (e.g., Montane Habitats, Calcareous/Acid Grasslands, Fen).
  - Five-step KBE sequence; terrain/soil adjustments typically applied after initial pass; provenance stored for traceability.

- Comparison with Countryside Survey (CS) 2007
  - Similar area estimates: Broadleaved woodland and Acid Grassland and Inland Rock show similarity within CS 95% limits.
  - Dissimilar area estimates: Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane, and coastal habitats show differences beyond CS 95% limits.
  - Key drivers for differences:
    - Classification scope and definitions (e.g., how Arable/Horticulture and Boundary/Linear Features are treated).
    - Spectral confusion and spectral variability (notably in Arable and Horticulture).
    - Boundary and linear features often below MMU in CS, thus merged into surrounding polygons in LCM2007, inflating some area totals.
    - Grassland classifications: disparate handling of Neutral vs Improved Grassland; spectral indistinctness; soil context limitations.
    - Fen, Marsh and Swamp: CS captures mosaic patches; LCM2007 tends to reclassify small components as Rough Grassland or Acid Grassland.
  - CS vs LCM2007 methodology differences (field survey vs satellite-based mapping) contribute to non-trivial differences in UK-wide estimates and country-level patterns.

- UK Land Cover distribution and temporal context
  - LCM2007 indicates the UK profile: over 50% of land in intensive use (Arable and Horticulture plus Improved Grassland) or Built-up Areas; around 12% Broadleaved/Conifer Woodland; remainder semi-natural (coastal, semi-natural grasslands, mountain habitats, etc.).
  - England shows the highest share of intensive land use; Scotland has substantial semi-natural and montane components; NI and Wales show mixed patterns.
  - LCM2000 vs LCM2007 differences reflect reworked spatial framework and updated classification, with some persistent shifts in major classes (e.g., Arable share, conifer woodland).

- Access, licensing, and governance implications
  - 1 km raster data are publicly accessible via the CEH gateway.
  - Full vector and 25 m raster data require licensing and formal requests to CEH.
  - Rich provenance and metadata enable users to assess data fitness for purpose and apply user-specific validation approaches.
  - The document emphasizes the need for careful interpretation when using grassland and boundary-related classes due to MMU effects and cross-product differences.

- Implications for Data Leaders
  - LCM2007 provides a robust, policy-relevant UK land-cover asset with transparent lineage, enabling multi-scale monitoring and cross-sector analyses (biodiversity, ecosystems, land planning, water, climate, etc.).
  - The KBEs demonstrate the value of context data (terrain, soils, urban/coastal context) in improving thematic resolution beyond spectral signals alone.
  - Data governance considerations include clear provenance, comprehensive metadata on processing steps, and licensing pathways for access across public and research partners.
  - Validation highlights class-specific quality variability; suggests focusing on aggregated grassland analyses and applying bespoke validation for target use cases.
  - For change detection, users should account for structural differences between LCM2007 and earlier CEH maps and consider reorganizing to a common spatial framework for robust temporal analysis.
  - Recommendations for future work include leveraging KBEs to better allocate mosaic habitats (e.g., Fen, Marsh and Swamp), refining grassland classifications, and aligning with field survey data to improve cross-product comparability.

- Bottom-line takeaways for policy and practice
  - LCM2007 is a landmark UK-wide land cover resource with detailed attribution and a reusable spatial framework, suitable for nationwide habitat monitoring, policy support, and cross-sector planning.
  - Its strength lies in the integration of cartographic structure with multi-temporal imagery and knowledge-based enhancements, enabling robust analyses of land cover distribution and change while acknowledging inherent classification and boundary challenges.
  - Stakeholders should use the dataset with attention to class-level caveats (grasslands, Fen, Montane, coastal mosaics) and employ bespoke validation strategies, leveraging parcel-level metadata and KBEs to inform interpretation.