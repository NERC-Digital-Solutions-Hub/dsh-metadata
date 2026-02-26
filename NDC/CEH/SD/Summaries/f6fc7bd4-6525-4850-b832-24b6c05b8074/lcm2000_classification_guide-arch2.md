# LCM2000: Calibration and Assessment against CS2000 Field Survey

- Aim
  - Support UK Biodiversity Action Plan implementation and reporting by using Broad Habitats (BHs) to provide a consistent, time-aware view of environmental health and habitat distribution.
  - Deliver standardized outputs (maps, statistics) and enable integration with broader datasets for policy performance monitoring.

- What LCM2000 is
  - A thematic classification of satellite-derived spectral data, designed to map Broad Habitats (BHs) and their Subclasses, with Variants reflecting detailed components.
  - Outputs include both BHs and aggregated 10-class levels used for reporting; map displays use standardized cartographic conventions to highlight patterns at national/regional scales.

- How calibration was done
  - Used CS2000 field survey (FS) data as a calibration dataset to assess map accuracy and to derive BH statistics from LCM2000 coverage.
  - FS data cover 569 one-kilometre squares (GB; 1998 and 1999) with high detail but not a strict ground truth; an independent QA test showed ~88% repeatability for primary FS codes.
  - Calibration focused on inter-comparison (calibration) rather than strict validation due to differences in resolution, timing, and data models.

- GIS operations and tests
  - ARC/Info workflows produced BH-labeled GIS coverage for FS squares and equivalent LCM2000 map sections.
  - Three primary tests to assess correspondence:
    - Per-pixel: direct overlay comparisons, sensitive to resolution and MMU differences.
    - Per-segment: dominant FS class within LCM2000 segments.
    - Per-parcel: FS parcels labeled against LCM2000-derived labels.
  - Correspondences evaluated at multiple levels:
    - BH level (excluding boundaries and rivers/streams)
    - Generalised urban vs non-urban categories
    - Target class level
    - Aggregate class level (where LCM2000/FS align closely)

- Confidence limits for measures of correspondence
  - Bootstrapping used to estimate 95% confidence intervals.
  - Summary results (GB; England & Wales; Scotland):
    - Per-pixel:
      - GB: 54% (95% CI ~53–56%)
      - England & Wales: 60% (CI ~58–62%)
      - Scotland: 44% (CI ~40–47%)
    - Per-segment:
      - GB: 58% (CI ~57–60%)
      - England & Wales: 64% (CI ~62–66%)
      - Scotland: 47% (CI ~43–50%)
    - Per-parcel:
      - GB: 62% (CI ~60–64%)
      - England & Wales: 69% (CI ~67–72%)
      - Scotland: 48% (CI ~44–52%)
    - Target class (weighted):
      - GB: 65%
      - England & Wales: 73%
      - Scotland: 51%
  - LCM2000 segments labelled with FS classes show similar trends; BH-level correspondences generally lower for finer distinctions, with higher agreement at parcel/aggregate levels.

- LCM2000 assessments at class level
  - Summary matrices synthesized for GB, England/Wales, and Scotland by National Land Class, then aggregated to common BH concepts for reporting.
  - Key habitat-specific observations:
    - Broadleaved/mixed and Coniferous woodland: similar total cover reported by LCM2000 and FS, but direct agreement is limited by the 0.5 ha minimum mapping unit (MMU) in LCM2000; many small woods appear as grassland or arable in FS, and vice versa.
    - Arable and horticultural land: LCM2000 ~23.4% (GB) vs FS ~21.5%; some misclassifications between arable and improved grassland due to rotation timing and spectral confusion.
    - Improved grassland vs semi-natural: FS often records improved as distinct; LCM2000 frequently assigns to Neutral/grassland; spectral and management-related distinctions are challenging, with about 20% FS-improved grassland misclassified by LCM2000.
    - Semi-natural grasslands, bracken, fens/marshes, and bogs: significant classification challenges; peat depth and acid/neutral/Calcareous distinctions are difficult spectrally; bogs under LCM2000 are conservative due to peat masks, leading to underestimation relative to FS. Bracken is not a Target BH class and is mapped as a Bracken variant; timing (May imagery) affects detection.
    - Heath, bog, montane, and inland bare ground: notable mismatches due to differing definitions and contextual cues (e.g., peat depth, altitude-based montane criteria, urban vs rural context for bare ground).
    - Coastal BHs: generally small and near resolution limits; intertidal areas subject to tidal state and sampling differences.
    - Built-up areas/gardens and boundary/linear features: LCM2000 excludes many linear features and some urban open spaces; FS captures more of these elements, affecting BH vs non-BH correspondences.
  - Overall, LCM2000 and FS show substantial similarities in broad totals for many major BHs, but many discrepancies arise from resolution, definitions, and management practices that are not fully captured spectrally.

- LCM2000 accuracy
  - The correspondence between LCM2000 and FS should not be interpreted as a direct measure of LCM2000 accuracy.
  - Given FS limitations and different data structures, a realistic target is around 85% accuracy at the Target class level; segment-based similarity suggests LCM2000 achieves roughly 63–72% of the maximum potential depending on the metric and region.
  - Contributing factors to mis-match:
    - 25 m parcel granularity vs FS’s finer details
    - MMU differences (>0.5 ha for LCM2000 vs ~0.04 ha FS)
    - Temporal differences (FS mainly 1998 vs LCM2000 imagery 1998–2001)
    - Inherent classification and data-model differences
  - In practice, LCM2000 is estimated to approach about 87% success at Target class level, implying overall practical accuracy around 85% for that level.

- Change detection
  - Detecting landscape changes with satellite data alone is challenging; differences between LCMGB 1990 and LCM2000 are likely small and often confounded by error.
  - A direct BH-based comparison with 1990 classes is not feasible; a more intelligent approach is needed.
  - Proposed path: leverage FS 1990/1998 data to guide interpretation of differences, and use calibrated change signals that align with known patterns of land-use change.

- Appendix I: Distinguishing features of Broad Habitats (highlights)
  - Provides guidance on how BHs relate to land cover classes and the limitations of remote sensing for fine-scale distinctions.
  - Key points include: difficulties separating hardwood vs coniferous woodlands spectrally, limitations in distinguishing semi-natural vs improved grasslands, peat depth influencing bog vs heath classification, and the challenges of mapping rare or small coastal/HB components at 1 km resolution.
  - Emphasizes the role of supplementary contextual data (soil maps, pH, peat depth, altitude) to refine classifications and improve alignment with field knowledge.

- Implications for environmental analysts
  - LCM2000 provides broad, time-spread habitat mapping with nationwide coverage, suitable for monitoring broad habitat extents and generating BH statistics, but requires cautious interpretation at finer scales due to resolution and classification limitations.
  - To maximize utility for environment monitoring:
    - Use direct calibration against field surveys to generate robust Broad Habitat statistics.
    - Combine LCM2000 outputs with FS-derived data and external datasets to improve validity and utility for policy performance assessment.
    - Employ change-detection approaches that integrate prior knowledge of land-use change patterns and probabilistic classifications to distinguish true change from dataset differences.
    - Plan for ongoing refinement by incorporating Variant-level distinctions (e.g., rough grasslands, peat-associated subsets) as supplementary information to improve future BH mapping.

- Summary takeaway
  - LCM2000 advances standardized, nationwide habitat mapping with clear alignment to BH concepts, but the accuracy and change-detection capabilities rely on careful calibration with detailed field surveys (CS2000) and integration of contextual data to address spectral and definitional challenges across habitat types.