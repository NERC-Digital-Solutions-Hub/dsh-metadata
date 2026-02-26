# Abstract

- Overview: A dataset of stable isotopic information (delta 13C and delta 15N) from two tissues (whole blood and mantle feathers) of 16 adult individuals across 8 procellariiform species collected at Bird Island, South Georgia, during austral summer 2001-2002. Used to examine interspecific competition across breeding and non-breeding periods.
- Spatial and temporal context:
  - Location: Bird Island, South Georgia (54°00´ S, 38°03´ W).
  - Timeframe: Austral summer 2001-2002; sampling aligned with breeding cycles (surface-nesting species sampled after hatching; burrow-nesting species in chick-rearing).
  - Subjects: 16 adults (8 males, 8 females) across 8 species; sex determined by morphology or genetic markers.
- Data collected and columns:
  - Core fields: Species (common name), sp_code (numeric species type), d13C, d15N, TissueType (feather or whole blood), Sex (male/female; NA for some diving petrels).
  - Tissue samples: Blood (0.2–1.0 ml per individual) and mantle feathers (8–10 feathers per individual).
- Sampling and preparation details:
  - Blood: Centrifuged 1–3 h post-collection; plasma/cells separated; stored at -20°C; lipids not removed.
  - Feathers: Dried, ground to fine powder in liquid nitrogen temperature.
- Isotopic analysis and quality control:
  - Instrumentation: Continuous-flow isotope ratio mass spectrometry using EA linked to Finnigan Tracer Mat and Costech EA with Thermo Finnigan Delta Plus XP.
  - Standards and precision: Three internal standards per ten unknowns; precision ≤ 0.2‰ for both d13C and d15N; internal standards calibrated monthly against IAEA and NIST reference materials.
- Data schema and relevance for GIS:
  - Attributes include species identifier, isotopic values for two tissues, and tissue type, enabling cross-tissue comparisons by species.
  - Location is fixed to Bird Island; per-sample geographic coordinates are not provided, so analyses map isotopic patterns at site-level and by species/tissue rather than per-point locations.
  - Suitable for GIS workflows that join isotopic data to species layer, breeding/season metadata, or environmental layers to explore spatial isotopic ecology and interspecific interactions.