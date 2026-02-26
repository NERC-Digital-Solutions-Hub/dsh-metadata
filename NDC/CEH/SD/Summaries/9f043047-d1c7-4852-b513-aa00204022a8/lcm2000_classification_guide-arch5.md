CSLCM/Final

## Overview and purpose
- This report documents the calibration and assessment of the LCM2000 land cover map against the CS2000 field survey data to support the UK Biodiversity Action Plan (BAP) Broad Habitats (BH) framework.
- LCM2000 provides a spectral-based thematic classification; CS2000 field surveys provide detailed habitat information. The aim is to align broad habitat classifications and enable generation of BH statistics from comprehensive LCM2000 coverage.
- Important caveat: CS2000 data are not “ground truth”; differences arise from resolution, timing, and classification approaches. Calibration focuses on creating reliable correspondences (per-pixel, per-segment, per-parcel) and understanding limitations.

## Data and classifications
- LCM2000: thematic classification of satellite imagery; maps Broad Habitats (BHs) and Target classes with Subclasses and Variants; includes aggregate classes for reporting.
- CS2000 field survey (FS): detailed, higher-resolution field data used to assess and calibrate LCM2000; provides ground-truth-like references but with its own uncertainties.
- Key mapping concepts:
  - BHs: major habitat types (e.g., Broad-leaved woodland, Coniferous woodland, Arable land, Improved grassland, Neutral/Calcareous/Acid grasslands, Bracken, Fen/Marsh/Swamp, Bogs, Montane, Inland bare ground, Built-up areas, Coastal BHs).
  - Target classes and Variants: spectral/class-based representations used for calibration against FS.
  - Aggregate classes: simplified 10-class level used for reporting where FS and LCM2000 align well.

## Methodology and testing
- Data processing: ARC/Info GIS workflows with correspondence matrices created for 569 CS2000 squares, aligned to LCM2000 map sections.
- Tests conducted:
  - Per-pixel comparisons: overlay of FS vs LCM2000 to assess raw spatial agreement.
  - Per-segment comparisons: LCM2000 segments labeled against FS dominant class.
  - Per-parcel comparisons: FS parcels labeled against LCM2000-derived labels.
- Comparison levels (hierarchy):
  - BH level (excluding some features)
  - Target class level
  - Aggregate class level
- Confidence estimation: bootstrapping to derive 95% confidence limits for correspondence measures across GB, England/Wales, and Scotland.
- Summary of outputs: correspondence matrices by country and by class level, with performance metrics for BH, Target, and Aggregate classes.

## Key findings (overall concordance)
- Per-pixel correspondence (GB): 54% (95%CI 53–56%); England/Wales: 60% (CI 58–62%); Scotland: 44% (CI 40–47%).
- Per-segment correspondence (GB): 58% (CI 57–60%); England/Wales: 64% (CI 62–66%); Scotland: 47% (CI 43–50%).
- Per-parcel correspondence (GB): 62% (CI 60–64%); England/Wales: 69% (CI 67–72%); Scotland: 48% (CI 44–52%).
- Target class level (parcels): GB 65% (England/Wales ~73%; Scotland ~51%); generally higher than BH-level due to aggregation and generalisation.
- Practical takeaway: differences are expected due to resolution gaps, time lags, and classification differences; PB (field survey repeatability) and spatial resolution constraints limit perfect matches.

## Causes of discrepancies and limitations
- Resolution and MMU differences:
  - FS parcels down to ~0.04 ha; LCM2000 minimum mapping unit >0.5 ha.
  This leads to under-recording of small features (e.g., small woodlands, ponds) in LCM2000 and mislabeling in FS.
- Timing differences:
  - FS surveys mainly 1998; LCM2000 imagery from 1998–2001. Changes over time contribute to mismatches.
- Class-definition differences:
  - Complex, continuous vegetation management practices (e.g., improved vs semi-natural grasslands) cause cross-class confusion.
  - Neutral/Calcareous/Acid grasslands not consistently separable spectrally; peat depth influences bog vs heath distinctions.
  - Bracken and Montane/Heath classifications show notable inconsistencies.
- Structural differences in data products:
  - LCM2000 avoids some BHs (e.g., Boundary/linear features) that FS captures; this affects calibration.
  - Coastal and intertidal BHs are small and often below resolution; tidal state further complicates matching.
- Other factors:
  - Urban/governmental data handling leads to differences in how built-up areas and open spaces are classified between FS and LCM2000.
  - Land-cover nuances (e.g., wetlands, rush pastures) can be interpreted differently between FS field notes and spectral data.

## Change detection considerations
- Detecting landscape changes between 1990 and 2000 is challenging with satellite data alone; precision is typically dominated by methodological differences and error.
- An intelligent, pattern-based approach is recommended, leveraging FS change directions and known change patterns to distinguish real changes from artefacts.
- Calibration results indicate under- and over-estimates in 2000; these should be incorporated into change-detection analyses.

## Implications for data governance and stewardship
- Data interoperability:
  - Differences between classification schemes (BH, Target classes, aggregates) require careful crosswalks and metadata.
  - When integrating LCM2000 with FS or other datasets, document the MMU, timing, and class-definition decisions.
- Metadata and provenance:
  - Clearly record the date ranges, spatial resolution, processing steps, and calibration methods used to generate BH and Target class statistics.
- Update and maintenance:
  - Plan for follow-up work to integrate LCM2000 with FS and external data (e.g., peatland maps, soil acidity maps) to improve accuracy for complex habitats (bogs, neutral/calcareous/acid grasslands).
- Data quality expectations:
  - Recognize that LCM2000 provides broad, repeatable large-area coverage with known limitations for small features; use aggregated class results for national/regional reporting where appropriate.
- Change-aware data practices:
  - Develop change-detection workflows that incorporate calibration uncertainties and known biases (e.g., underestimation of bogs, misclassification of rough grasslands).

## Practical guidance for use and governance
- Use BH-to-LCM2000 crosswalks and Appendix I mappings to interpret classifications, with awareness of known mismatches in key habitat types (arable vs grassland, improved vs semi-natural grasslands, bogs, bracken, montane).
- Prefer Target class or Aggregate class analyses for reporting where misclassification risk is high at BH level.
- When combining LCM2000 with FS or other field datasets, document the specific class definitions, peat-depth considerations, and management context used in calibration.
- For future data products, consider enhanced integration (e.g., peatland/peat depth layers, urban-rural gradients) to reduce spectral-context ambiguities in problematic BHs.

## Appendix and technical notes (highlights)
- Appendix I provides a brief review of Broad Habitats with distinguishing features and notes on mapping challenges (e.g., difficulty distinguishing semi-natural vs improved grasslands; peat depth as a key criterion for bog vs heath; limitations in distinguishing neutral vs calcareous vs acid grasslands).
- Table-like mappings indicate how LCM2000 Variants map to BHs, including color-coding conventions and alpha-numeric codes for different habitat components.