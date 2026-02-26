# Final Report for LCM2007 - the new UK land cover map

- This section summarizes comparisons between LCM2007 and Countryside Survey (CS) 2007, highlighting similarities, dissimilarities, and implications for data governance, interoperability, and usage.

## Similar and dissimilar area estimates (4.3.2)

- Similar area estimates (within UK CS 95% confidence limits) occur for:
  - Broadleaved woodland
  - Acid Grassland
  - Inland Rock
- Dissimilar area estimates (outside UK CS 95% confidence limits) occur for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Key noted differences and potential causes:
  - Differing definitions of “Arable and Horticulture” between CS and LCM2007
  - Spectral confusion and multi-year image composition
  - Inclusion of boundary and linear features in LCM2007 vs CS
  - Grassland classifications: neutral vs improved; spectral signatures and soil data limitations
  - Boundary/linear features mapping differences; field vs polygon representations
  - Patch size and minimum mapping units affecting comparisons, especially for fen and small habitat patches
  - Temporal range of images influencing spectral variability and class allocation

## Discussion (4.3.3)

- CS estimates are derived from field-based extrapolation and differ conceptually from the satellite-based LCM2007; scaling and method differences affect UK-wide estimates.
- Sensitivity analyses indicate changes in ITE Land Classes can impact comparability; when CS2000 data were scaled to UK estimates, results aligned more closely with CS than when using LCM2000 areas.
- Practical issues for data stewardship:
  - Differences in spatial structure and class definitions complicate change detection and trend analysis.
  - The need for a common spatial framework to improve comparability across products.

## UK Land Cover distribution (4.4)

- UK-wide distribution: over half of the UK is intensive use (Arable + Improved Grassland) or built-up areas; remaining areas are semi-natural or natural habitats.
- Country-level patterns:
  - England shows the highest intensive land use; Scotland has the largest proportion of Coniferous Woodland and montane habitats.
  - Scotland has the largest share of semi-natural habitats (mountain and moorland) and montane grasslands; Wales and NI show varying patterns.
- Comparison with LCM2000 indicates shifts in arable and semi-natural grassland extents and minor changes in woodland classes, but inter-product differences remain.
- Governance note: cross-country comparability benefits from a consistent spatial framework and standardized class mappings.

## Summary and discussion (4.5)

- Main findings:
  - Agreement between LCM2007 and CS varies widely by Broad Habitat class.
  - Grassland categories are especially problematic due to one-to-many relationships between observed land cover and Broad Habitats; Broad Habitat Association (BHA) rules were developed to address this.
  - LCM2007 aligns well with CS 2007 on Arable and Horticulture in 1 km squares, but estimates for Arable and Horticulture at the Broad Habitat level are higher in LCM2007.
  - Fen, Marsh and Swamp estimates differ by an order of magnitude; many Fen areas are recorded as Rough Grassland or Acid Grassland in LCM2007, reflecting complexity and small patch sizes.
- Implications for data stewardship:
  - Consider using KBEs to allocate certain grassland/mosaic areas more accurately (e.g., dedicating more effort to Fen, Marsh and Swamp).
  - Recognize and document the limitations of spectral classification for complex habitats; ensure metadata captures confidence and context.
- Validation and quality:
  - Parcel-level metadata (KBE history, ProbList) enables targeted validation and assessment of relevant classes; supports fit-for-purpose evaluation.
  - Bespoke validation approaches advocate using high-resolution imagery to assess consistency with LCM2007 and to generate uncertainty ranges.

## Access, licensing and usage (data delivery context)

- Data products:
  - 1 km raster data available via the CEH Information Gateway.
  - Full vector product and 25 m raster data available on request from CEH; licences may apply.
- Licensing and rights:
  - CEH Data Licensing and IPR team manages rights; fees may apply for some users or applications.
- Metadata and provenance:
  - Rich metadata and accompanying documentation support traceability, reproducibility, and auditability, including KBE history and segmentation details.

## Governance considerations for Data Stewards

- Provenance and lineage:
  - LCM2007 provides detailed processing history, KBEs, and spectral likelihood information at the parcel level, aiding auditability and reproducibility.
- Interoperability and standards:
  - Cross-walking with CS and BH/BHA schemes is essential for comparability; interpretable mappings and explicit notes on where spectral data are insufficient are necessary.
- Data quality, uncertainty, and validation:
  - Substantial class-level variability; user guidance should emphasize confidence intervals and potential misclassification risks, particularly for grassland, fen, and montane categories.
  - Parcel-based metadata enables user-driven validation and uncertainty quantification; encourage users to apply their own validation approaches.
- Access rights and licensing:
  - Clear licensing pathways and IPR controls are crucial for enabling data sharing while protecting rights; consider providing more accessible licensing for non-commercial or academic use.
- Update and governance of spatial frameworks:
  - The use of a generalised OS MasterMap-based spatial framework supports reuse and change detection but requires ongoing maintenance of compatibility with future updates.

## Applications and impact (aligning with Data Stewards' aims)

- Supports biodiversity assessment, ecosystem services evaluation, habitat connectivity analyses, and landscape planning at national and country levels.
- Provides a nationally consistent base for multi-source environmental policy and planning, enabling cross-sector decision-making and monitoring across the UK.
- The combination of vector (parcel-based) and raster products enables diverse implementation, modelling, and change-detection activities while emphasising provenance and processing transparency.