# Final Report for LCM2007 - the new UK land cover map

- A comprehensive UK-wide land cover map produced in 2007, delivering a continuous vector framework and derived raster products at 25 m and 1 km resolutions.
- Built on a generalised national cartography spatial framework (OS MasterMap and LPS Large-scale Vector) with image data and knowledge-based enhancements (KBEs) to improve thematic detail and consistency.
- Aimed to support habitat monitoring, policy, landscape planning, and ecosystem service assessments across the UK.

## Data governance, provenance, and accessibility

- Provenance: derived from satellite imagery, national cartography, elevation and soils data, and extensive ground reference data.
- Metadata and traceability: rich metadata accompany vector polygons to enable traceability of processing steps and KBEs; a Knowledge-Based Enhancements (KBE) history is recorded per parcel.
- Licensing and access:
  - 1 km raster data openly accessible via the CEH Information Gateway.
  - Full 25 m vector and raster data available on licence (online application; fees may apply for some users/applications).
- Reproducibility and transparency: comprehensive methodological documentation supports auditability; KBEs can be inspected or disabled to examine original spectral classifications.

## Data sources

- Satellite imagery: Landsat-5 TM/ETM+, SPOT-4/SPOT-5, AWIFS; multi-date composites with occasional back-up imagery; 91% of the UK mapped from composites.
- Ground truth and validation: Countryside Survey (CS) Broad Habitats for external validation; 9,127 ground reference polygons used for validation.
- External auxiliary data: Ordnance Survey MasterMap (GB framework); NI boundaries; soils; DEMs; coastal and terrain layers; urban datasets; and other ancillary layers for KBEs.
- Ground truth and CS data used for training, validation, and cross-comparison.

## Spatial framework and data integration

- GB spatial framework: based on OS MasterMap, generalised to MMU 0.5 ha and minimum feature width 20 m; over 100 million polygons in GB.
- Northern Ireland framework: derived from LPS Large-scale Vector lines, generalised and integrated with image segmentation.
- Integration strategy: agricultural boundaries and image segmentation used to enhance spectral coherence and delineation of land cover objects; aim for consistent, reusable spatial units for change detection and UK-wide mapping continuity.

## Image processing and segmentation

- Pre-processing chain: data import, cloud/mask handling, atmospheric correction (FLAASH), georeferencing, topographic correction (Minneart with NEXTMap DEM).
- Cloud masking: multi-criteria approach plus manual digitization; cloud-shadow modeled from illumination geometry.
- Topographic correction: mitigates slope/aspect effects to reduce spectral variability due to shading.
- Image segmentation: 60 composite images segmented into homogeneous patches; segments merged with generalised cartography and agricultural boundaries; NI segments supplement composite-derived segments.
- Hole-filling: limited manual classification using Landsat ETM+ to avoid cross-dataset hole-filling.

## Classification and knowledge-based enhancements (KBE)

- Classification approach: parcel-based supervised maximum likelihood classification across 37 composite and 21 single-date images.
- Training data: derived from ground reference points; supplemented with OS maps and web maps as needed.
- KBEs (seven automated algorithms) applied sequentially to resolve spectral confusion and increase thematic resolution:
  - Terrain (altitude/slope) to assign montane or other elevations.
  - Soil (soil type with context) to separate grassland types.
  - Terrestrial zone (coastal vs inland) to constrain coastal habitats.
  - Offshore (flag inland parcels misclassified as offshore).
  - Within urban boundary (resolve urban spectral confusions near boundaries).
  - Outside urban boundary (prevent urban-adjacent misclassifications).
  - Water (refine water classes and coastal vs inland distinctions).
- Impact: KBEs reassign portions of parcels to more plausible classes; manual checks minimize false positives; approximately 20% of parcels are modified by KBEs.
- Grassland nuance: spectral signatures alone struggle to distinguish all semi-natural grassland types; KBEs plus soil and altitude corrections improve mapping fidelity.

## Data products and metadata

- Vector product: parcel-based land cover with 10 attributes (e.g., Construct, ProbList, KBE history); includes Broad Habitat sub-classes (BHSub) and field codes (FieldCode); extensive provenance and processing history.
- Raster product: 25 m resolution with 23 LCM2007 classes.
- Aggregated products: 1 km raster products (two formats):
  - Percentage cover per 1 km cell for each LCM2007 class.
  - Dominant class per 1 km cell.
- Minimum mapping unit: 0.5 ha; LCM2007 maps land cover (not land use); 23 classes mapped to UK Broad Habitats with notes on 1-to-many relationships and some grassland ambiguity.
- Documentation: detailed QA, processing history, and KBEs enable reproducibility and reuse.

## Change mapping and temporal considerations

- Change mapping across LCM1990, LCM2000, and LCM2007 is challenging due to differing class definitions and spatial structures; robust separation of real change from mapping artifacts is not fully established.
- Approach emphasizes up-to-date land cover mapping, with recognition that cross-product comparability requires sophisticated, structure-aware methods.
- Summary: LCM2007 provides a consistent spatial framework to support change detection, but direct change detection across all three maps requires careful methodological alignment.

## Validation, accuracy, and comparisons with Countryside Survey (CS)

- Overall validation: 9,127 ground reference polygons; overall accuracy around 83% for LCM2007 classes.
- Class-level performance varies:
  - Strong: Coniferous woodland, Arable and Horticulture, Littoral Rock, etc.
  - Weaker: Semi-natural upland habitats such as Neutral Grassland, Bog, Montane Habitats.
- CS 2007 comparison highlights:
  - Similar area estimates for some classes (e.g., Broadleaved Woodland; Inland Rock) but dissimilar for others (notably Arable and Horticulture, Improved Grassland, Neutral Grassland, Bog, Montane Habitats, Fen/SW).
  - Differences attributed to:
    - Class definition differences and spectral confusion (especially Arable and Horticulture).
    - Boundary and linear feature mapping differences (CS maps field boundaries differently; LCM MMU influences how features are represented).
    - Grassland ambiguity (one-to-many relationships between grassland and Broad Habitats; development of Broad Habitat Association rules).
    - Fen, Marsh and Swamp mapping complexity due to mosaic/nature of fen and small patch sizes, and different spatial representations between CS and LCM2007.
- UK-wide and country-level patterns:
  - LCM2007 tends to overestimate Arable and Horticulture relative to CS upper limits due to classification scope and inclusion of boundaries.
  - Montane and coastal habitats are poorly represented in CS, complicating cross-survey comparisons.
- Broad Habitat Association (BHA) framework used to improve correspondences across habitats.

## Key findings for Data Stewards

- LCM2007 provides a robust, repeatable UK-wide land cover product with rich metadata, suitable for habitat monitoring and policy support.
- The combination of a Cartography-derived spatial framework and image segmentation improves spatial coherence and change-detection potential.
- KBEs significantly improve thematic resolution, particularly in complex landscapes; grassland classifications remain challenging.
- Validation indicates strong performance for many key classes but weaker performance for several semi-natural upland habitats.
- When using LCM2007 for policy or planning, consider aggregating grassland classes or utilizing BHAs to improve correspondence with field-based data and CS outputs.
- Data governance implications: licensing, traceability, and the ability to inspect/disable KBEs support responsible data stewardship and user trust.

## Practical access and usage notes for Data Stewards

- Access points:
  - 1 km raster data available via CEH Information Gateway.
  - Full vector and 25 m data available on licence via online application; fees may apply.
- Use cases: habitat monitoring, landscape planning, ecosystem services, biodiversity policy, catchment management, and cross-country policy analysis.
- Maintenance and updates: LCM2007 is a foundational product for ongoing UK-wide land surface mapping; KBEs and external datasets can be adjusted for regional needs and future updates.
- Documentation and transparency: extensive methodological documentation, including algorithms, KBEs, and spatial framework generalisation, to support auditability and reuse.

## Data stewardship considerations and challenges

- Incomplete user needs and priorities (challenge for aligning outputs with diverse stakeholder requirements).
- Timeliness of data delivery from data creators and data providers.
- Ensuring data creators meet metadata and standardization requirements; interoperability across systems.
- Managing multiple systems, formats, and evolving data structures; large dataset sizes complicate transfer and processing.
- Handling outdated or patchy reference datasets; reliance on multiple data sources with varying spatial resolution and quality.

## Conclusion

- LCM2007 delivers a comprehensive, reference-quality UK land cover product with a robust data governance framework, enabling reproducibility and wide reuse.
- The project demonstrates the importance of integrated spatial frameworks, segmentation-based classification, and knowledge-based enhancements to achieve high thematic resolution at national scale.
- While offering strong alignment with field-based survey data in many classes, it also highlights ongoing challenges in grassland and fen-related habitats, underscoring the value of cautious interpretation and potential aggregation for policy applications.
- For Data Stewards, LCM2007 provides a transparent, well-documented dataset with clear licensing paths, enabling responsible data sharing, provenance tracking, and informed decision-making for land cover monitoring and policy support.