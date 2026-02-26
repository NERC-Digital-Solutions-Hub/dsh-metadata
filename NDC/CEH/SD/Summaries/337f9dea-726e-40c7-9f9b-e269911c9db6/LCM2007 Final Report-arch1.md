# Final Report for LCM2007 - the new UK land cover map

- The report compares LCM2007 with Countryside Survey (CS) 2007, discusses data products, validation, and implications for policy and research.
- It documents areas of strong and weak agreement between LCM2007 and CS across Broad Habitats, explains sources of discrepancy, and outlines data access and usage.

## Key comparative findings with Countryside Survey 2007

- Very similar area estimates (within CS 95% confidence limits) for:
  - Coniferous Woodland
  - Freshwater
  - Built-up Areas and Gardens
  - Calcareous Grassland
- Similar area estimates (within UK CS 95% confidence limits) for:
  - Broadleaved woodland
  - Acid Grassland
  - Inland Rock
- Dissimilar area estimates (beyond CS 95% confidence limits) for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Key factors driving differences:
  - Differences in what is classified under Arable and Horticulture between CS and LCM2007
  - Spectral confusion and temporal differences across multi-year imagery
  - Inclusion or fragmentation of Boundary and Linear Features in LCM2007 vs CS
  - How grassland types (Improved/Neutral/Calcareous/Acid) are mapped spectrally and through KBEs
  - Mismatch in spatial structure and parcel sizes between CS field squares and LCM2007 polygons
  - Fen, Marsh and Swamp area is particularly challenging due to mosaic/patch size and spectral complexity
- CS patch size and the MMU (minimum mappable unit) influence how CS estimates map to LCM2007 polygons, affecting comparisons for certain habitats.

## UK-wide land cover patterns and country differences (LCM2007 vs CS2007)

- Overall UK distribution: majority of land under intensive use (Arable/Horticulture and Improved Grassland) with significant semi-natural and woodland components.
- Country-level patterns:
  - England shows the highest proportion of intensive land use
  - Scotland has the largest proportion of Coniferous Woodland and the greatest share of Montane/Highland habitats
  - Northern Ireland and Wales show different balances of Improved Grassland, Arable areas, and woodland
- Comparisons to LCM2000 indicate notable shifts in Arable/Horticulture and grassland proportions, with some uncertainty linked to spatial framework changes and data processing.

## Discussion and interpretation (4.5)

- Agreement between LCM2007 and CS 2007 varies widely by Broad Habitat; grassland categories are particularly difficult due to a one-to-many relationship with Broad Habitat types and the need for Broad Habitat Association rules.
- LCM2007 shows high correspondence with CS 2007 in the area mapped as Arable and Horticulture in 1 km CS squares, but estimates at the Broad Habitat level can differ due to classification and boundary treatment.
- Fen, Marsh and Swamp estimates vary by an order of magnitude between CS and LCM2007 due to mosaic landscapes and classification challenges.
- The report highlights that changing spectral signatures, multi-year image ranges, and differences in spatial structure complicate direct change detection across LCM versions.
- The authors suggest methodological approaches to improve interpretation, such as using KBEs and integrating additional datasets to better allocate grassland mosaics to Fen, Marsh and Swamp.
- The value of integrating in-situ Countryside Survey data with satellite-derived LCM2007 data is emphasized for a more complete understanding of land surface dynamics.

## Example areas (5.1)

- A set of area examples demonstrates LCM2007 performance across diverse landscapes:
  - North Wales montane areas with Montane Habitats and associated grasslands
  - Salisbury Plain calcareous grassland with surrounding broadleaved woodland and arable land
  - Suburban/urban areas of London showing built-up and parkland patterns
  - East Anglia fenland interspersed with arable and improved grassland
  - Grampian Mountains illustrating Montane Habitats and upland mosaics
- Each example includes corresponding OS map context to illustrate the fidelity of parcel-level mapping.

## Data products and access (5.2)

- Vector product
  - Parcel-based land cover with attributes: area, source images, Broad Habitat (BH), processing history, and KBEs
  - Includes Broad Habitat sub-classes (BHSub) and FieldCode metadata for detailed interpretation
- Raster products
  - 25 m raster: 23 LCM2007 classes
  - 1 km raster: UK-wide summaries in two formats
    - Percentage cover per class per 1 km pixel
    - Dominant class per 1 km pixel
- Data availability
  - 1 km raster datasets available via the CEH Information Gateway
  - Full vector and 25 m raster products available on request under license (fees may apply)
- Data richness and QA
  - Vector includes extensive metadata and a knowledge-based enhancement (KBE) history
  - Guidance on QA and validation provided, with a recommendation to perform user-specific validation on Broad Habitat sub-classes

## Change detection and future directions (Chapter 6)

- LCM2007 provides a robust, parcel-based nationwide framework that supports change detection, but cross-product changes require careful methodological alignment due to differing spatial structures among LCM generations.
- A suggested path is to reorganize earlier CEH maps into a common spatial framework based on real-world land-use units to improve comparability and change detection.
- The generalised spatial framework from LCM2007 is designed to facilitate future national land cover monitoring and more reliable change detection.

## Validation approach (Appendix: Bespoke validation)

- Emphasizes "fit for purpose" validation rather than absolute truth, given geography’s inherent variability.
- Parcel-level metadata (KBE history and probability listings) enables users to assess consistency with imagery and perform location-specific validation.
- Proposes a two-part validation approach: assess high-probability target classes and moderate-probability cases, potentially using fuzzy categorizations to bound accuracy.
- A Python-based toolset has been developed to support this validation methodology.

## Broader context and availability

- LCM2007 supports policy-relevant, ecosystem-based analysis and is linked to European-scale efforts (e.g., Corine Land Cover) and pan-European datasets (IMAGE2020 family).
- The project builds on prior CEH maps and Countryside Surveys, enabling integrated evidence for habitat monitoring, biodiversity, climate, water, and land-use planning.

## Access and contact

- CEH Information Gateway provides 1 km raster data
- Full vector and 25 m raster data are license-based and available on request via CEH
- Contact: spatialdata@ceh.ac.uk (licensing and data access inquiries)