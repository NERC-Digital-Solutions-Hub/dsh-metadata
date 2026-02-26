# Dataset documentation

## Overview

- LCM2015 (Land Cover Map 2015) is a parcel-based UK land cover map produced to support diverse user needs, using 21 land cover classes based on UK Broad Habitat definitions.
- Data products cover multiple formats and resolutions: core vector, 25m raster, and 1km aggregated products (dominant and percentage covers).
- Primary data sources: Landsat-8 (30 m) with AWIFS (60 m) as needed; designed to reflect real-world boundaries and be interoperable with other geospatial datasets.
- Data are archived with DOIs for citation; GB and Northern Ireland datasets have separate data products and DOIs; access and licensing are managed by CEH.

## Data products and formats

- Vector data (core product)
  - 6.7 million polygons (Great Britain) and 0.9 million polygons (Northern Ireland).
  - Attributes include: gid (unique parcel id), BHAB (dominant Broad Habitat class), Pix_dist (per-class pixel counts), unc (mean per-polygon RF probability), unc_stdev, npix, Modal_class (LCM2015 target class), Modal_prop, Composite (composite image used).
- 25m raster
  - 2-band raster: band 1 = dominant LCM2015 class; band 2 = mean per-polygon RF probability.
- 1km raster (aggregates)
  - Dominant class at 1km (21-target classes or 10 aggregate classes).
  - Percentage cover at 1km for both 21 target classes and 10 aggregates (rounded integers; sum may deviate slightly from 100 due to rounding and coastal extents).
- Data scope and mapping
  - GB and NI data provided separately due to projection differences; GB uses British National Grid, NI uses TM75 Irish Grid.
  - Minimum mappable area: >0.5 ha; parcels smaller than 0.5 ha and linear features under 20 m are dissolved into surrounding landscape.
- Labelling and metadata
  - Each parcel has a unique gid; rich polygon metadata and per-class pixel breakdown (Pix_dist) are provided.
  - Color mapping and class documentation are detailed in appendices; DOIs exist for all products.

## Data lineage, methodology, and structure

- Classification methodology
  - Uses Random Forest (RF) classifier (instead of Maximum Likelihood) to handle multi-modal training data and avoid spectral sub-class grouping.
  - Training data built from a stable core: areas consistently classified the same in 2000 and 2007, supplemented with coastal areas and historically challenging classes.
  - Ancillary data (e.g., slope, distance to water) are integrated as input features rather than applied post-classification, improving objectivity of knowledge-based enhancements.
- Spatial framework and segmentation
  - No segmentation-based polygons in LCM2015; per-pixel classification with per-polygon aggregation.
  - Removal of segmentation in the spatial framework improves change-mapping readiness and avoids misalignment between segmentation and final classifications.
- Differences from LCM2007 (output, methodology)
  - Montane class removed; replaced by Inland Rock or upland habitat based on spectral data.
  - Rough grassland class removed; grassland types now align with JNCC Broad Habitats without soil data.
  - 25m raster now two-band; probability data moved to band 2.
  - RF classifier replaces Maximum Likelihood; stable training areas used, with expanded coastal and poorly mapped classes.
  - No spectral sub-classes used; per-pixel classification summarized to polygon labels.
  - Spatial framework segmentation removed; improved consistency for change mapping.
- Data products and uncertainty
  - RF provides per-pixel probability; summarized as mean polygon probability (vector) and band 2 in 25m raster.
  - Uncertainty data available and documented; per-polygon probabilities aid assessment of classification confidence.
- Land cover versus land use
  - LCM2015 maps land cover; users should be cautious in equating with land use.

## Data governance, access, and citation

- Access channels
  - 1km raster: available via CEH Environmental Information Platform (EIP).
  - Full vector and 25m raster: available on request under licence from CEH; licensing may apply.
  - Applications and licensing processes are described on CEH’s information products page; contact spatialdata@ceh.ac.uk.
- Licensing and rights
  - Licences may apply; some data are restricted; fees may apply for certain users/applications.
- Data citation and DOIs
  - Each LCM2015 product has its own DOI (GB vector, GB 25m, GB 1km percentage, GB 1km dominant, GB 1km aggregates; NI equivalents provided).
  - Publication citations should include author, date, and DOI (e.g., Rowland et al., 2017) following CEH/EIDC guidance.
- Projections and data access details
  - Projections: GB vector/raster in British National Grid; NI data in Irish Grid (TM75).
  - Access details and data product descriptions are provided in the CEH pages and the LCM2015 data paper (in preparation).

## Metadata, quality, and usage considerations

- Metadata richness
  - Each polygon carries dominant class, per-class pixel breakdown, mean probability, and other quality indicators; extensive metadata enhances traceability and reproducibility.
- Uncertainty handling
  - RF-derived probability is included; users can assess confidence per polygon and per class, aiding risk-aware analyses.
- Change mapping cautions
  - LCM2015 is not recommended for current-state change mapping without careful consideration; changes reflect both real change and classification differences across time, plus methodological updates.
- Class definitions and habitat mapping
  - 21 target classes aligned with UK Broad Habitats; Appendix 1–3 provide detailed class interpretations and color mapping.
  - Some habitat distinctions (e.g., Montane, specific grassland subtypes) are handled spectrally rather than by field-verified thresholds; consult appendices for caveats.
- Data standards and reuse
  - Clear DOIs and per-product documentation support reproducibility and data provenance in scientific work and governance.

## Appendices (governance-relevant details)

- Appendix 1 and 2
  - Summaries of Broad Habitat definitions mapped by LCM2015; guidance on how spectral data map to habitat classes.
- Appendix 3
  - Standard LCM2015 colour mapping for visualization.
- Appendix 4
  - Composite image metadata used in LCM2015 production.

## Practical takeaways for Data Stewards

- Ensure licensing compliance and provide clear DOIs for all LCM2015 products in any data-sharing or publication workflow.
- Maintain rich metadata (gid, Pix_dist, unc, npix, Modal_class, Modal_prop, Composite) to enable traceability and uncertainty assessment.
- Monitor method updates and ensure users are aware of differences from LCM2007, especially regarding class definitions, probability reporting, and the removal of segmentation.
- Leverage RF-based uncertainty metrics to communicate data quality and support risk-aware decision-making.
- Facilitate access through CEH platforms, with clear guidance on which products are openly accessible vs. licensing-restricted, and provide contact points for licensing questions.
- Be mindful of the 0.5 ha minimum mapping threshold and the dissolution of small or linear features when integrating LCM2015 into broader datasets or analyses.