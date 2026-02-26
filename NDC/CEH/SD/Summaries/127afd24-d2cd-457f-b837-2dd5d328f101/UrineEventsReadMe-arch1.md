# UrineEvents.csv

- Purpose: A large dataset on urination behaviour (squatting duration, frequency, estimated volume) of Welsh Mountain ewes on two contrasting upland pastures, with implications for nitrogen cycling in grazed ecosystems (nitrate leaching and N2O emissions) due to urine patches.

- Study context and campaigns:
  - Four campaigns with 30 ewes each: Spring 2016, Autumn 2016, Spring 2017 (unimproved montane), Autumn 2017 (unimproved montane).
  - Sites:
    - Semi-improved upland field at Henfaes Research Centre (11.5 ha; 240–340 m asl) with U4/MG6 vegetation.
    - Unimproved montane grazing area on the Carneddau, Snowdonia NP (495 ha; 322–943 m asl) with H12 heath and patches of acid grassland.

- Sheep and deployment details:
  - Mean starting weights: semi-improved Spring 33.5 kg; semi-improved Autumn 39.7 kg; unimproved Spring 41.6 kg; unimproved Autumn 38.0 kg.
  - Individual sheep IDs: R1–R30 per campaign; different sets of sheep between the two sites.

- Data collection and measurement:
  - Instruments: Daily Diary (DD) tags (Wildbyte Technologies Ltd., UK) affixed to a shaved hind area.
  - Measurements: urination start time, frequency, and squatting duration detected via a Boolean algorithm.
  - Volume estimation: urine event volume (Vol_Est, ml) derived from squatting duration using a linear relationship established from penned sheep with DD tags (PennedSheepWithTags.csv used as the regression basis).

- Data processing and quality control:
  - Final filtered/cleaned dataset; some tags removed due to early deployment failures (e.g., rubbing off on trees/posts).
  - Frequency data filtered if zero urination events persisted for >2 consecutive days or showed irregular patterns (likely due to sensor attachment issues).
  - Urination events shorter than 1 second filtered as noise; the shortest directly observed squatting duration in penned sheep was 1.9 s.

- Data headers and units:
  - Site: SemiImproved or Unimproved upland pastures.
  - Season: Spring or Autumn.
  - Sheep: ID R1–R30 per campaign; missing values noted; different sheep sets per site.
  - Date, Time, DateTime: event timing in dd/mm/yyyy and hh:mm:ss formats.
  - Duration: squatting duration in seconds (from tri-axial accelerometers and Boolean detection).
  - Vol_Est: estimated urine event volume in ml (derived from Duration via the regression; see PennedSheepWithTags.csv).

- Data structure and references:
  - PennedSheepWithTags.csv contains the regression data used to estimate Vol_Est.
  - UrineEvents.csv represents the final cleaned dataset; includes notes on data limitations and cleaning steps.

- Data usage considerations for analysts:
  - Enables analysis of urination patterns and estimation of urine-derived nitrogen inputs across two grazing systems and four campaigns.
  - Supports modeling of nitrate leaching and N2O emissions from urine patches, with attention to site-specific variability and sensor reliability issues.
  - Data gaps and exclusions (tag failures, unreliable frequency days, and short-duration events) should be accounted for in analyses.

- Citation and reuse:
  - If data are reused, ensure full citation.
  - Project: Uplands-N2O; Grant NE/M015351/1; Authors include Marsden, Lush, Holmberg, Harris, Whelan, Webb, King, Wilson, Jones, Charteris, Cardenas, Chadwick, among others.