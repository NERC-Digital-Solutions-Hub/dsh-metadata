# LCM2000: A Broad Habitats classification of Great Britain and its calibration with the CS2000 field survey

## Background and objectives
- UK Biodiversity Action Plan framework uses Broad Habitats (BHs) to cover the range of UK habitats.
- LCM2000 provides a spectral data–based, thematic classification intended to map widespread examples of terrestrial, freshwater, and coastal BHs, with Subclasses, Variants, and Aggregate classes to support diverse user needs.
- The mapping aims to align BH concepts with Landsat-type spectral classes, while accommodating practical data use and reporting needs.

## LCM2000 and Broad Habitats: nomenclature and mapping approach
- BHs: Broad Habitats defined by ecological characteristics; used for national reporting and planning.
- LCM2000 classes: spectral-target classes that can be combined into BHs; Subclasses, Variants, and Aggregate classes provide finer or broader grouping.
- Read-across: where exact BH-to-LCM2000 matches aren’t possible, best-fit Target classes and Subclasses are used; Rare BHs may be aggregated for display purposes.
- Map displays balance reliability with pattern visibility; some rare or very small BHs are aggregated to broader categories for national/regional plots.
- Some specific BH distinctions (e.g., Neutral/Calcareous/Acid grasslands, Bracken, Fen/Marsh/Swamp) are challenging to separate spectrally; contextual data and peat-depth masks are used to improve distinctions in some cases.

## Data sources and calibration approach
- CS2000 field survey (CSLCM): used to assess LCM2000 accuracy and calibrate BH statistics.
- Coverage: 569 one-kilometre squares surveyed in GB (549 in 1998, remainder in 1999); Northern Ireland data available but not yet digital for testing.
- CS2000 data are not “ground truth” due to differences in resolution, timing, and classification; 88% repeatability for primary codes (BH labels) noted in an independent QA study.
- Calibration approach emphasized: calibration against CS2000 rather than validation; inter-calibration between datasets with differing resolutions.

## Methodology of calibration and accuracy assessment
- GIS workflow: ARC/Info used to generate BH-labeled map sections for all CS2000 squares; 569 correspondence matrices created (one per 1 km square).
- Three main tests to compare CS2000 and LCM2000:
  - Per-pixel: direct overlay; sensitive to resolution, timing, and class definitions.
  - Per-segment: segment-dominant FS class compared to LCM2000 segment labels.
  - Per-parcel: FS parcels versus LCM2000-derived parcel labels to test transfer to vector maps.
- Correspondences assessed at multiple levels:
  - BH level (excluding boundaries and some linear features).
  - BH level with urban areas generalized to match FS results.
  - Target class level.
  - Aggregate class level.
- Confidence limits: bootstrapping to estimate 95% confidence intervals around correspondence measures.

## Overall accuracy and key results by level
- Per-pixel (GB): 54% correspondence (95% CI 53–56%); England & Wales: 60% (58–62%); Scotland: 44% (40–47%).
- Per-segment (GB): 58% (57–60%); England & Wales: 64% (62–66%); Scotland: 47% (43–50%).
- Per-parcel (GB): 62% (60–64%); England & Wales: 69% (67–72%); Scotland: 48% (44–52%).
- Target class level (parcel-based): GB 65%; England & Wales 73%; Scotland 51% (higher than BH-level due to differences in classification and aggregations).
- Overall interpretation: differences arise from resolution mismatches (CS2000 vs LCM2000 MMU), timing differences, and class-definition nuances; dimly, parcel- and target-level matching is higher than raw BH-level matching.

## Class-level findings and challenges
- Woodland (Broadleaved/mixed and Coniferous): overall UK cover similar between LCM2000 and CS2000, but direct agreement is moderate (≈44%), largely because many small woodlands (<0.5 ha) fall below LCM2000’s minimum mappable unit, leading to discrepancies where FS shows woodland as grassland or arable and vice versa.
- Coniferous woodland: higher correspondence (≈70%) due to larger, contiguous blocks.
- Arable and horticultural land: LCM2000 ~23.4% vs FS ~21.5%; misclassifications often occur between grass and arable and between arable and built-up areas.
- Improved vs semi-natural grasslands: LCM2000 distinguishes improved grassland well, but around 20% of FS “improved” grassland is recorded as semi-natural by LCM2000; the distinction between neutral, calcareous, and acid grasslands is problematic spectrally.
- Neutral, Calcareous, and Acid grasslands: weak spectral separation; peat-depth-based rules used to classify bog vs heath in some cases, but results remain uncertain.
- Bracken, Dwarf shrub heath, Bogs, Fen/Marsh/Swamp: notable differences between LCM2000 and CS2000; field indicators and peat-depth masks influence outcomes; bogs depend on peat depth (>0.5 m) and peat maps for context.
- Montane habitats and Inland bare ground: coverage estimates differ; montane habitats are rarely sampled in the field; inland bare ground often misclassified as urban context due to context interpretation.
- Coastal (Supralittoral/Littoral) habitats: generally small and near resolution limits; aggregated for reporting; differences largely due to tidal timing and coastal masking.
- Boundary and linear features: not targeted by LCM2000; FS mapping includes them; this contributes to mismatches in calibration.

## Change detection and future work
- Measuring landscape changes between 1990 and 2000 is difficult with satellite data alone due to resolution, timing, and classification differences; only partial detection is feasible.
- Intelligent change-detection approaches are proposed, leveraging FS data on directions and rates of change (Haines-Young et al. 2000) to distinguish real changes from errors.
- Calibration results identify under- and over-estimates to inform change analyses; integration with field data (CS2000) to generate Broad Habitat statistics for broader, accurate use is planned.
- Future work includes deeper integration of LCM2000 with CS2000 and external datasets to refine BH mapping and statistics, and potential re-examination of bogs and heaths.

## Practical implications for analysts
- LCM2000 provides broad, survey-ready habitat statistics with comprehensive national coverage, suitable for reporting and trend analyses when combined with field calibration.
- Users should account for planned data integration (CS2000) and known limitations at finer scales (especially for small patches, peat-related features, and semi-natural vs improved grasslands).
- Aggregate reporting (10-class level) can help align maps with user needs while acknowledging spectral and contextual uncertainties.
- Change-detection work will rely on intelligent, pattern-based approaches that integrate historical field data with satellite-derived classifications.