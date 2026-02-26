# Soil sampling

- Purpose and context
  - Document describes a soil/root/fungal study conducted on 1 April 2015 with climate treatments (warming, drought, control) and an approach to minimize destructive sampling by limiting soil cores to a single 8 cm diameter per plot (0-8 cm depth), yielding 3 replicates per treatment.
  - Cores were collected near Calluna vulgaris shrubs, kept moist, and stored at 4°C until processing.

- Root extraction and species verification
  - C. vulgaris roots were isolated from soil cores by sectioning, washing, and careful cleaning.
  - Criteria used to identify C. vulgaris roots included morphological characteristics (larger roots >1 mm: dark, woody, kinked; fine roots reddish and non-woody) and tracing to larger identifiable roots to confirm origin.
  - Necrotic/rotten roots were discarded, and cleaned roots were stored in deionised water at 4°C for measurements.

- Root measurements
  - Measurements focused on fine roots (≤ 1 mm) using WinRHIZO 3.2 on scanned root images; parameters included total length, surface area, average diameter, and root volume.
  - Dry weight was obtained for root fractions (≤2 mm and >2 mm) following oven drying at 70°C for 24 hours.
  - Additional root metrics included number of root tips and length per volume.

- Fungal colonisation assessments
  - Ericoid mycorrhizal (ErM) colonisation was determined in fine root fragments via microscopy after chemical pre-treatment (10% KOH, then vinegar-ink staining) and heating.
  - Hyphal coils were used to confirm ErM presence; assessments were semi-quantitative, evaluating colonisation levels across root cells.
  - Categories included ErM and Dark Septate Endophytes (DSE), with root segments analyzed in multiple passes along each root.

- Quality control
  - Method comparison for root bleaching (10% vs. 2.5% KOH; 10, 20, and 30 minutes) showed no discernible differences, supporting method robustness.
  - Preliminary testing and standard photography were used to prevent measurement drift; data were checked for outliers and improbable values.

- Data structure and dataset details
  - The dataset comprises 53 columns and 72 rows, with a detailed schema for each variable.
  - Key structure elements:
    - Plot and Depth identifiers (Plot, Depth in cm)
    - Treatment status (Treatment: warming, control, drought)
    - Image analysis metrics (AnalysedRegionArea_cm2, Length_cm2, SurfArea_cm2, AvgDiam_mm, LenPerVol_cm_m3, RootVol_cm3)
    - Root morphology data (Tips; DryWeightAll_g; DryWeight2mm_g; Length_Root1..Length_Root5)
    - Size-specific dry weights (for different diameter thresholds)
    - Fine-root colonisation data (ErM_ and DSE-related counts across Root1–Root5, with further breakdowns by colonisation percentage ranges 0–1%, 1–10%, 10–50%, 50–90%, 90–100%)
  - Descriptive descriptions accompany each column to aid interpretation (e.g., plot number, depth, treatment, area/length measurements, rooting parameters, and microbial colonisation indicators).

- Implications for monitoring frameworks
  - Provides a multi-dimensional data package linking environmental treatments (warming, drought) to root morphology and mycorrhizal associations, useful for evaluating ecosystem responses in policy monitoring.
  - Includes a comprehensive data dictionary and explicit processing steps, aiding transparency, reproducibility, and governance of environmental health data.
  - Highlights the need for specialized equipment and expertise (WinRHIZO analysis, microscopy) and the importance of standardized protocols and quality control to ensure data reliability in monitoring frameworks.
  - Demonstrates how complex biological measurements can be structured into a dataset with metadata-rich columns, supporting sharing and reuse while clarifying data provenance and transformation steps.