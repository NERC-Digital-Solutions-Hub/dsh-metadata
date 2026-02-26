# Overview of the data

- Mesocosm experiments conducted in three west Greenland lakes (Kangerlussuaq area) to assess the effects of dust addition on water chemistry and phototrophs in water, sediments, and on artificial substrates.
- Data collected by Suzanne McGowan and Amanda Burson.
- Trial setup: six enclosures per lake (60 cm diameter, ~1 m depth) with alternating dust-treated (0.196 g/L; ~25–35 g per enclosure) and control mesocosms; dust sourced from spring snowbank, filtered and freeze-dried.
- In situ measurements: conductivity, temperature, and dissolved oxygen using a YSI multiprobe in the upper 20 cm of water.
- Sampling: water and phytoplankton at start and end (or end only for destructive sampling); surface sediments sampled at start and end; terracotta pots placed at the bottom as artificial substrate for phytobenthos; pot scrapes analyzed at the end.
- Experimental timing: setups with day 0 sampling and final-day sampling; three lakes (SS17b, SS1590, SS906) with sampling dates in July 2018 and a 14-day duration.

## Experimental design and sampling regime

- Lakes: SS17b, SS1590, SS906; three enclosures per lake sampled at start and end.
- Dust treatment: 3 mesocosms per lake received dust; 3 served as controls; arrangement in a 3×2 grid within a wooden frame.
- Enclosure details: polythene tubes ~60 cm diameter, ~1 m depth; water inside enclosures 49–84 cm deep.
- Measurements and sampling:
  - In situ water measurements (conductivity, temperature, DO) in the upper water column.
  - Water and phytoplankton sampling from the mesocosms at start and end.
  - Surface sediment collection from each mesocosm at start and end.
  - Terracotta pot with artificial substrate for phytobenthos; pot sampling at the end.
  - Phytoplankton sampling conducted at start and end.

## Collection, generation, and transformation methods

- Water samples: filtered in the field through GF/F filters; filtrates stored refrigerated for dissolved nutrient analysis.
- Chlorophyll analyses: chlorophyll a measured spectrophotometrically; filters kept for pigment analyses.
- Terracotta pots: biofilms scraped, rinsed, and suspended material frozen for later analysis.
- Sediments: surface sediments stored frozen prior to analysis.
- Sample handling: total sample volume recorded; aliquots removed volumetrically for quantitative analysis.

## Analytical methods and units

- Water chemistry:
  - Soluble reactive phosphorus (SRP) via molybdenum blue method (colorimetric).
  - Ammonium (NH4-N), silicate, total phosphorus (TP) via analogous colorimetric methods; total nitrogen analyzed at University of Maine.
  - Units: µg/L or mg/L for silicate.
  - Major ions analyzed by ion chromatography.
- Chlorophyll analyses:
  - Water, phytobenthos (pot scrapes), and sediments: chlorophyll a via trichromatic method.
  - Units: µg/L (water), µg/cm2 (phytobenthos), µg/g (sediments).
- Pigment and carotenoid analyses (HPLC):
  - Pigments extracted from sediments and pot scrapes; pigments quantified against standards.
  - Units:
    - Nanomoles per gram of sediment (sediments).
    - Nanomoles per square centimeter (pots/phyto-scrapes).
  - Pigment suite includes chlorophylls (a, b, c2), carotenoids (β-carotene, fucoxanthin, lutein, zeaxanthin, canthaxanthin, diadinoxanthin, diatoxanthin, alloxanthin, pheophytin a/b, pheophytin a/b), and others.
  - Detection and quantification details: UV/visible spectra 350–750 nm; 435 nm for quantification; retention times validated with stability checks.
- Data units and structure:
  - Water measurements captured at start and end (e.g., chlorophyll a, TP, SRP, NH4-N, NO3-N, silicate).
  - Sediment analyses include pigments (Chla, Chlb, Chlc, pheophytin variants, carotenoids) in nmol/g.
  - Pot scrape analyses include chlorophylls and pigments in nmol/cm2.
  - 46 variables cover water chemistry, surface sediments, and pot scrape pigment data; 37 rows in the dataset.

## Quality control

- Calibration and standards:
  - Colorimetric analyses: new calibration curves run with each batch; analyses discarded if r2 < 0.998.
  - Ion chromatography: 10-point calibration.
  - YSI probes: daily pH and DO calibrations; DO calibrated weekly; conductivity calibrated with one-point standard.
  - HPLC pigments: 8-point pigment calibrations; stability checks with an extract from green plants at start/end of each run; manual identification and baseline integration by a trained expert.
- Overall emphasis on data integrity across chemical analyses, pigment identification, and quantification.

## Data structure and variables

- Dataset size: 37 rows and 46 data columns.
- Core structure:
  - Columns 1–5: experimental descriptors (e.g., Lake code, Dust treatment, Replicate, Time point, Sample date).
  - Columns 6–17: water measurements at start and end (chlorophyll a, nutrients, etc.).
  - Columns 18–31: surface sediment analyses (pigments and related metrics).
  - Columns 32–46: artificial substrate (terracotta pot) scrape analyses (pigments and associated metrics).
- Example variable categories include:
  - Lake code, dust treatment, replicate, time point, sample date.
  - Water Chla; Water TP, SRP, NH4-N, NO3-N; WaterSilicate; Temperature; DO; Conductivity; pH.
  - Surface sediment pigments (e.g., Chl a, Chl b, Chl c2, fucoxanthin, diadinoxanthin, diatoxanthin, lutein, zeaxanthin, alloxanthin, pheophytin a/b, etc.).
  - Terracotta pot scrape pigments (same pigment suite) and related metrics (β-carotene, etc.) plus wet density.

## References

- APHA (2005). Standard methods for the examination of water and wastewater.
- Chen, N., et al. (2001). Historical trends of hypoxia on the Louisiana shelf: pigments as biomarkers.
- Parsons, TR; Strickland, JD (1963). Discussion of spectrophotometric determination of marine-plant pigments.