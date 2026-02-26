LCM2000: Calibration of Broad Habitat Mapping in Great Britain against CS2000 Field Survey

## Overview and purpose
- Develop a thematic classification (LCM2000) from satellite imagery to map Broad Habitats (BHs) across the UK for biodiversity reporting and policy support.
- Align BH concept with the UK Biodiversity Action Plan framework and JNCC definitions; use LCM2000 to provide broad habitat maps with consistent cross-country coverage.
- Calibrate and compare LCM2000 outputs with CS2000 field survey data to assess map accuracy and enable generation of BH statistics from full-coverage satellite data.

## Key concepts and classification structure
- Broad Habitats (BHs): high-level habitat categories defined for national reporting.
- Target classes, Subclasses, and Variants: hierarchical components used to describe BHs in the spectral-to-thematic classification (Target classes are primary spectral-to-BH mappings; Subclasses add detail; Variants refine components like crop types).
- Aggregate classes: 10-class level aggregations designed to match broad BH patterns for reporting.
- Map display conventions: standardized colors and display rules to balance reliability and pattern visibility; some small or rare BHs are aggregated for national/regional plots.

## Data sources and methodology
- CS2000 field survey: 569 one-km squares across Great Britain (GB) used to assess LCM2000 map accuracy and calibrate BH statistics.
- LCM2000: thematic classification derived from LANDSAT-like spectral data plus external contextual datasets; mapped to BHs with consistency across the UK, acknowledging differences in target classes and subclasses.
- Calibration approach: inter-comparison (calibration) rather than strict validation due to differences in spatial resolution, timing, and class definitions between CS2000 and LCM2000.
- Three main correspondence tests:
  - Per-pixel (direct overlay)
  - Per-segment (dominant FS class within LCM2000 segments)
  - Per-parcel (FS parcels vs. LCM2000 labels)

## Confidence and accuracy measures
- Overall correspondence varies by geography and thematic level:
  - Per-pixel: GB 54%; England & Wales 60%; Scotland 44%.
  - Per-segment: GB 58%; England & Wales 64%; Scotland 47%.
  - Per-parcel: GB 62%; England & Wales 69%; Scotland 48%.
- At the BH level, correspondence is lower than at higher aggregation levels due to resolution and edge effects; at the Target class level, correspondence improves:
  - Target class level (parcel-based): GB 65%; England & Wales 73%; Scotland 51%.
- Interpretative note: CS2000 is not ground truth; differences arise from resolution (LCM2000 MMU ≈ 0.5 ha vs CS2000 parcel mapping down to 0.04 ha), timing differences, and intrinsic class-definition discrepancies.
- Realistic accuracy expectation: around 85% at the Target class level for parcel-based correspondence; overall, LCM2000 performance is about 72% of its maximum potential when accounting for differences with CS2000 repeatability (88%).

## Key findings by habitat categories and mapping issues
- Broadleaved/mixed woodland and Coniferous woodland: similar total cover but lower direct agreement due to small woodlands and boundary delineation; larger blocks map more reliably.
- Arable and horticultural land: LCM2000 tends to overestimate relative to CS2000 in some areas due to small features; confusion with improved grassland can occur.
- Improved vs. semi-natural grasslands: challenging to distinguish spectrally; roughly 20% of CS2000 improved grassland appears as semi-natural in LCM2000.
- Neutral, Calcareous, and Acid grasslands: spectral separation is difficult; Bogs vs. dwarf shrub heath and peat depth criteria complicate distinctions.
- Bracken, fen/marsh/swamp, dwarf shrub heath, bogs, montane habitats: significant classification challenges; peat depth and context (e.g., peatland mapping) strongly influences outcomes.
- Inland bare ground, water bodies, urban/built-up areas, and coastal BHs: varying degrees of accuracy; coastal BHs are small and often below resolving scale; boundary/linear features often excluded in LCM2000 calibration.
- Montane and inland rock concepts: altitude-based and context-based distinctions can lead to mismatches with field data.

## Change detection and future work
- Changes between LCMGB 1990 and LCM2000 are likely small and often eclipsed by survey and mapping errors; satellite-only change detection has limitations.
- An intelligent, multi-source approach is recommended to identify plausible habitat changes by combining CS2000 field data (1990, 1998) with LCM2000 outputs and other external data.
- Ongoing and planned work includes improved calibration, direct Broad Habitat statistics generation from LCM2000 via field-data calibration, and integration with external datasets for more robust change assessments.

## Implications for environmental monitoring
- LCM2000 provides comprehensive UK-wide habitat mapping with standardized BH frameworks, suitable for monitoring policy performance and environmental health over time.
- The calibration against CS2000 highlights strengths (broad coverage, consistent classification structure) and limitations (coarse 25 m resolution, MMU differences, spectral ambiguities in complex habitats).
- For analysts: use LCM2000 as a standardized, repeatable source to assess broad habitat extent and trends, while leveraging field data and supplementary datasets to refine interpretations in key habitat types.

## Appendix I: Distinguishing features and mapping challenges for BHs
- Outlines the practical limitations of remote sensing for fine-scale habitat distinctions (e.g., woodland openness, set-aside, semi-natural vs. improved grassland).
- Provides guidance on spectral vs. contextual cues, soil pH as a correction factor, peat depth for bog vs. heath distinctions, and how to handle mixed or transitional habitats.
- Emphasizes the need for knowledge-based corrections and region-specific considerations when integrating field and satellite data.

## Data handling and outputs
- Outputs include BH maps, Subclass and Variant level details, and aggregate 10-class representations that align with BH reporting.
- Calibration results and method details are described, with full technical specifics and table-based statistics to be provided in the Final Report.