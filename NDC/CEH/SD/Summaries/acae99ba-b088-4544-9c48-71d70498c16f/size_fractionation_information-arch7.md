# The eight stage non-viable Andersen sampler was used for the size fractionation of endotoxin

- Purpose and setup:
  - An eight-stage non-viable Andersen sampler was used to fractionate endotoxin by particle size.
  - Each stage uses a glass fibre filter; two samplers run together for 1 hour per sample (except at source sites like compost and farms, where 1 sampler runs for 15 minutes per sample).

- Stage-by-stage size fractions (µm):
  - Preseparator: >10.0
  - Stage 0: 9–10
  - Stage 1: 5.8–9
  - Stage 2: 4.7–5.8
  - Stage 3: 3.3–4.7
  - Stage 4: 2.1–3.3
  - Stage 5: 1.1–2.1
  - Stage 6: 0.65–1.1
  - Stage 7: 0.43–0.65
  - Backup filter: <0.43

- Analysis grouping (to reduce sample count):
  - 0–1 fraction: 5.8–10 µm
  - 2–4 fraction: 2.1–5.8 µm
  - 5–7 fraction: 0.43–2.1 µm
  - B/UP: <0.43 µm
  - CTL (Control Filter): N/A for analysis (taken in the field and extracted as usual)
  - LNE (Loaded Not Exposed): N/A (loaded onto the Andersen without air flow, then extracted)

- Sampling and labeling:
  - Each set of filters is assigned a letter; typically A and B run together for the first hour, C and D for the second hour, and E and F for the third hour.
  - Sampling files contain site-specific details on this arrangement.

- Implications for GIS data capture:
  - Enables spatial mapping of endotoxin fractions by size at multiple sites (e.g., compost and farm locations).
  - Data will include site coordinates, sampling times, and fraction-specific results, linked to filter letters (A–F) and their corresponding size fractions.
  - Data standardization needed across samples (consistent fraction groupings) and handling of differing sampling durations (1 h vs 15 min at source sites).
  - CTL and LNE are not directly used in analysis but may be referenced for provenance and quality control.