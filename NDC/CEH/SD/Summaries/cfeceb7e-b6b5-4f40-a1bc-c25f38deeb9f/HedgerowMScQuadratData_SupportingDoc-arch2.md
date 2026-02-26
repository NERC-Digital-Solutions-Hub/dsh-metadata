# Plant community basal data from a hedgerow cutting experiment in England, 2016

- Aim
  - Document plant abundance data to assess how hedgerow cutting regimes affect species richness of basal flora, contributing to monitoring environmental health and the effectiveness of agri-environment schemes.
  - Data underpin analyses such as biodiversity outputs and Ellenberg indicator profiles in related research.

- Data scope and usage
  - Contains vegetation abundance data from an MSc project using long-running hedgerow experiments.
  - Data linked to a publication on hedgerow management, biodiversity, and restoration relevant to agri-environment schemes (Stanbury et al., 2020, Biodiversity and Conservation).

- Experimental design
  - Randomised block experiment (Experiment 2) evaluating hedgerow management treatments on basal flora species richness.
  - Full factorial design: 2 (Time of cutting: Autumn vs Late winter) × 2 (Intensity: Standard vs Incremental) × 3 (Frequency: Annual, Once every two years, Once every three years) = 12 treatment codes, plus a control with no cutting (13 total).
  - Three replicates per treatment per site, with contiguous hedgerow sections of 15–20 m.
  - Study period: September 2010 to January/February 2016.
  - Four field sites:
    - Woburn, Buckinghamshire (WO) – hawthorn-dominated
    - Waddesdon Estate, Oxfordshire (WB) – blackthorn-dominated
    - Waddesdon Estate, Oxfordshire (WC) – mixed species
    - Yarcombe, Devon (YC) – traditional mixed hedge
  - Note: Winter cutting treatments not applied at WB due to hedgerow scarcity.

- Data collection and measurement
  - Two quadrats per side of each hedgerow plot (1 m × 10 m each), inner and outer quadrats to capture plants under and beside the hedge.
  - Height sampling up to 80 cm; vegetation cover assigned to nearest 5% (5–100%) or 1% (1–4%), with 0.1% for <1% occurrences.
  - Quadrats placed roughly 5 m from plot start to avoid edge effects.
  - Species list includes vascular plants, bare ground, and litter; some sites had access limitations (Waddesdon locations).

- Quality control
  - Standard protocol followed.
  - Field data collected by experienced surveyors; expert-checked lists; data screened for anomalous values.

- File structure and dataset content
  - HedgerowMScQuadratData.csv
  - Key columns:
    - EXPERIMENT (Experiment number), SITE (site code: WO, WB, WC, YC), BLOCK_NO, PLOT_NO, TREATMENT (1–13, see experiment design), VISIT_DATE, VISIT_YEAR (2016 for this dataset), QUADRAT (inner/outer), SPECIES_NAME (scientific name; includes bare ground/litter), COVER (percentage cover)
  - Data describe vegetation abundance in the basal area of hedgerow plots, collected across multiple visits.

- References
  - Mechanisms and baseline context: Carey et al. 2008 Countryside Survey UK Results.
  - Related methodology and experimental framework: Defra BD2114 project report (Staley et al., 2018) and the Defra-supported hedgerow biodiversity work.

- Funding and support
  - Long-running hedgerow experiments funded by Defra (BD2114), managed by the UK Centre for Ecology & Hydrology (UKCEH).
  - MSc student supported by University of Reading; fieldwork support provided by UKCEH staff.

- Relevance for environmental monitoring and data stewardship
  - Provides standardized, QA-checked plant abundance data suitable for tracking hedgerow biodiversity responses to management regimes over time.
  - Data can be integrated with other environmental datasets to enhance monitoring value and facilitate broader policy performance assessments.
  - Clear documentation of methods and data structure supports reproducibility and data sharing, with explicit notes on site access limitations.