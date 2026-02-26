# Land Cover Map of Great Britain (1990)

## Overview for Data Stewards
- Digital land cover dataset for Great Britain with 25 classes at 25 m resolution, derived from Landsat Thematic Mapper data.
- License-based access; available for any area of the country; used by government, business, and researchers.
- Provides the first complete digital national land cover map for GB since the 1960s; first nationwide satellite-based land cover map; accuracy checked against ground surveys.
- Data supports planning, management, and monitoring across sectors (agriculture, ecology, conservation, forestry, environment, water, urban planning, transport, telecommunications, recreation, minerals).

## Dataset contents and classifications
- 25 target classes covering sea/inland waters, bare ground, arable land, pastures/meadows, rough grass/heaths, bracken, scrub, woodlands (deciduous/coniferous), bogs, urban/suburban development, and inland bare ground; includes an UNCLASSIFIED category for small areas not fitting target classes.
- Outputs available in two forms:
  - 25 m resolution: single layer with values 0–25 representing target cover types (0 = unclassified).
  - 1 km resolution: 17 “key” classes with proportion values (0–100) for each 1 km cell, representing the fraction of the cell covered by each key class.
- Data structure supports customized aggregations (e.g., recombining subclasses) to meet user objectives; minimum mapped unit is the practical size of features, often around 1 ha, with smaller components detectable if spectral signatures are strong.

## Methodology and accuracy
- Produced via supervised maximum likelihood classification of Landsat TM data; combined summer and winter imagery improved accuracy to about 88% (vs. single-date analyses with lower accuracy).
- Registration: Landsat raster maps aligned to 1 km field maps; typical positional error ~0.8 pixels (~20 m).
- Accuracy notes:
  - Ground-truth data are scarce and varied in methods; class definitions differ across surveys, affecting comparisons.
  - Overall correspondence between field data and LCMGB estimates around 67% (including boundary pixels); 71%–82% if boundary pixels are excluded and time differences considered.
  - Realistic, broad accuracy is estimated at 80–85% when accounting for definitional differences and temporal changes.
  - The largest error source is mixed boundary pixels; spatial displacement and landscape changes between dates also contribute.
- Users should interpret accuracy as average error rates; local discrepancies are expected due to scale, resolution, and classification rules.

## Spatial details and data quality
- Resolution and mapping: 25 m grid; minimum consistently mappable area approximates 1 ha (spectral signature dependent); features as small as 0.125 ha detectable under favorable conditions.
- Stand-alone data: Area-based data orders possible with area coordinates or shapefiles; data provided at 25 m (labels 0–25) or 1 km (17 key classes with percentages).
- 2% of GB remains unclassified in the 25 m dataset; in 1 km summaries, unclassified proportion is represented by the difference from 100% across the 17 key bands.

## Licensing, access, and data management
- Licensing: Various options, including single-user, corporate multi-user, and flexible licenses; data charges in three bands: commercial, non-commercial, and research; potential further reductions for UK academics under NERC arrangements.
- Access: Stand-alone datasets available; data orders can be customized to specified geographic areas; contact details provided for ordering and licensing.
- Updates and governance: Appendix notes emphasize good practice, metadata, and a Data Assessment Report (DAR) to collect user feedback, issues, and guidance for analysis and application.
- Related resources: Land Cover Map 2000 is now available; sample data (1 km) accessible; download via Countryside Information System; CEH contact provided.

## Classification schema (A–Q) and usage
- The document defines 25 target classes (A–Q) with detailed ecological descriptions and full key names, including:
  - A Sea/Estuary; B Inland Water; C Coastal Bare Ground; D Saltmarsh; E Rough Pasture / Dune Grass / Grass Moor; F Pasture / Meadow / Amenity Grass; G Marsh / Rough Grass; H Grass / Shrub Heath; I Shrub Heath; J Bracken; K Deciduous / Mixed Wood (including Scrub/Orchard); L Coniferous / Evergreen Woodland; M Bog (Herbaceous); N Tilled Land (Arable Crops); O Suburban / Rural Development; P Urban Development; Q Inland Bare Ground; UNCLASSIFIED.
- Each class includes a fuller description and notes on how it appears spectrally and in practice, plus notes on regional variations and potential aggregation (e.g., combining some classes in GIS analyses).
- The 25 m data is the primary standard; 17-key class aggregation is provided for the 1 km data, with bands aligned to the 17 key classes.

## Practical guidance for use and interpretation
- The dataset distinguishes land cover (not always same as land use); interpretations should consider the time of imaging and phenology.
- Users should acknowledge the limitations of class Definitions, boundaries, and potential temporal changes when applying results to local decisions.
- For best practice, refer to the Data Assessment Report (DAR) and accompanying notes on interpretation, accuracy, and analysis approaches.

## Appendices and color mapping
- Appendix 2 provides the color recipe mapping for LCM1990 classes to display colors, aiding visualization consistency across datasets.
- Guidance notes emphasize good practice and potential customization for mapping and analysis needs.

## Availability of updated data
- Land Cover Map 2000 (LCM2000) is now available with further information on its creation, potential applications, sample data, and download options.

## References
- The document cites key methodological and accuracy references (e.g., Congalton 1991; Fuller et al. 1989a, 1989b, 1994a, 1994b; Wyatt et al. 1994) relevant to remote sensing classification, ground-truth comparisons, and map production.

## Contact
- Land Cover Map Sales, CEH Wallingford; email and telephone provided for licensing, queries, and data requests.