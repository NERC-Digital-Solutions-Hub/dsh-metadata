# Final Report for LCM2007 - the new UK land cover map

## Overview
- First continuous parcel-based land cover map for the UK, produced for Countryside Survey 2007.
- 23 LCM2007 classes mapped at a national scale, aggregated to 17 Broad Habitats; supports 25 m raster and 1 km raster products; UK-wide continuous vector coverage.
- Approximately 10 million land parcels (8.6 million GB, 0.9 million NI); 91% imagery from composites, 9% from single-date imagery; minimal manual filling.
- Data provenance and governance embedded in the products; 1 km rasters openly accessible; full vector and 25 m rasters available under licence.

## Data assets and products
- Vector: land parcels with attributes including area, source images, Broad Habitat (BH), KBE history, and processing details.
- Broad Habitat sub-classes (BHSub) and FieldCode metadata included; CorePixels and ProbList provide spectral-class likelihoods.
- 25 m raster: 23 LCM2007 classes.
- 1 km raster: two modes per location (A) percentage cover per class, (B) dominant class.
- Access: CEH Information Gateway for 1 km rasters; full vector and 25 m raster under licence on request.

## Data sources and spatial framework
- Satellite imagery: Landsat-5 TM, Landsat-7 ETM+, SPOT-4/5, IRS AWIFS; 34 composites (summer + winter) plus single-date images; cloud/cloud-shadow masked.
- Ground reference: CEH field campaigns (2006–2008); Countryside Survey 2007 for comparisons.
- External datasets: OS MasterMap (GB), LPS NI, agricultural boundaries, urban datasets, DEMs, soils, coastal context.
- Spatial framework: GB uses refined OS MasterMap boundaries with agricultural boundaries and image segments; NI uses LPS + OS-based framework; MMU of 0.5 ha; segmentation combines image segments with cartographic parcels for spectral coherence.

## Image processing and segmentation
- Pre-processing: cloud masking, atmospheric correction (FLAASH), image georegistration (target RMSE < 0.3 pixel), topographic correction (Minnaert with NEXTMap DEM).
- Image segmentation: 60 composites segmented using winter NIR, summer red, and summer MIR to form a segment-based vector framework; limited manual edits and hole-filling as needed.
- MMU and segment handling: segments retained if ≥ 9 pixels; smaller areas dissolved into the most spectrally similar adjacent segment.

## Classification and knowledge-based enhancements (KBE)
- Classification: parcel-based supervised maximum likelihood classification using ground-reference data; iterative refinement.
- Knowledge-based enhancements: seven automated rules (KBEs) to reduce spectral confusion and add contextual information (urban, coastal, terrain, water, etc.).
- KBEs affect about 20% of parcels; designed to be progressive and traceable with manual checks to minimize misclassification.

## Knowledge base, parameters and integration
- Contextual data: urban boundaries, coastal outlines, terrain (altitude, slope, aspect), soils, and other ancillary datasets.
- Soil and terrain integration informs upland and coastal classifications; sequence of algorithms converges to the most plausible class per parcel.

## UK-wide coverage and data assembly
- Designed as a continuous UK vector product with boundary continuity challenges addressed via a nine-chunk production strategy.
- Northern Ireland required special handling; integration with OSMM and agricultural data improved outputs.
- Aims to enable robust change detection through a common, reusable spatial framework.

## Quality assurance and accuracy
- Ground reference validation: 9127 CEH points; overall accuracy ≈ 83% across LCM2007 classes.
- Class-level accuracy varied due to spectral ambiguity and KBEs limitations; some classes performed better (e.g., bog, montane habitats) than others (e.g., neutral/calcareous grasslands).
- Validation methods include producer’s accuracy and user’s accuracy; detailed class-specific accuracy tables discuss implications for users.
- Change mapping challenges noted due to differences in class definitions across historical maps and inherent classification errors.

## Change mapping and Countryside Survey (CS) comparison
- Change mapping is difficult due to redefined classes and ~20% image-classification error rates; robust national-change methods were not established.
- CS 2007 comparison shows varying correspondence depending on thematic level; grassland mosaics cause significant discrepancies.
- Broad Habitat Association (BHA) rules improve correspondence by allowing cross-habitat links (e.g., bog with montane/other habitats).
- Fen, Marsh and Swamp areas are particularly challenging due to mosaics; many CS Fen polygons map to Rough Grassland or Acid Grassland in LCM2007.

## UK Land Cover summary and interannual context
- UK distribution: over 50% of land in intensive agriculture (Arable and Horticulture + Improved Grassland) or built-up areas; approx. 12% Broadleaved/Mixed/Yew Woodland; remainder semi-natural and coastal/montane.
- Country-level variation: England shows highest intensive-use share; Scotland has substantial coniferous woodland and upland semi-natural areas; NI and Wales show different distributions.
- LCM2007 vs LCM2000: differences in arable, semi-natural grassland, conifer cover, and urban proportions; spatial framework changes contribute to some differences.

## Access, usage and governance
- 1 km raster data accessible via CEH gateway; full vector and 25 m raster available under licence (fees may apply).
- Provenance and processing steps are well-documented; KBEs provide traceable history of classifications.
- The data are intended to support policy, biodiversity monitoring, land-use planning, and cross-sector applications with explicit metadata and versioning.

## Key figures and highlights
- 23 LCM2007 classes; 17 Broad Habitats; continuous UK vector coverage; nine production chunks; nine-chunk strategy for overlap management.
- Nearly 10 million parcels; 83% overall accuracy; 25 m and 1 km raster products available; strong metadata and change-tracking capabilities via KBEs.

## Implications for data leadership
- Demonstrates end-to-end data product lifecycle: data sourcing, spatial framework design, segmentation, classifier optimization, KBEs, QA, validation, and cross-dataset comparison.
- Emphasizes transparent processing, traceable metadata, and governance to support policy needs and multi-sector applications.
- Highlights balancing global coverage with local accuracy, managing multi-resolution outputs, and enabling data reuse through clear licensing and interfaces.
- Provides concrete lessons for leading national-scale data initiatives: integrate diverse data sources (cartography, soils, elevation) with imagery; create a reusable spatial framework; adopt knowledge-based enhancements to improve thematic resolution; and align validation with user needs and policy objectives.