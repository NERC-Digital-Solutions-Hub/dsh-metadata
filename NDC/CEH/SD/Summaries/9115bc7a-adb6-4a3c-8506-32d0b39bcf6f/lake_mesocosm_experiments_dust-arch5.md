# Overview of the data

- A mesocosm experiment conducted in three lakes in the Kangerlussuaq area, West Greenland, to assess the effects of dust addition on water chemistry and phototrophs in water and sediments. Data collected by Suzanne McGowan and Amanda Burson.

## Experimental design and sampling regime

- Location and setup:
  - Three lakes, each with six mesocosms (enclosures embedded in lake sediments; water depth 49–84 cm).
  - Dust treatment: three mesocosms received dust at 0.196 g/L (approx. 25–35 g per enclosure, adjusted for depth); three served as controls.
  - Enclosures arranged in a 3×2 layout within a wooden frame.
- Timeline:
  - Experiment started in July 2018 and ran for 14 days.
  - Sampling at start and end of the experiment; some samples only at end if destructive.
- Measurements and sampling:
  - In situ measurements: specific conductivity, temperature, and dissolved oxygen using a YSI multiprobe (upper 20 cm water).
  - Water and phytoplankton: collected from mesocosm water at start and end using a plastic suction tube.
  - Sediments: surface sediments collected from each mesocosm at start and end (three replicates per mesocosm) using an extended syringe.
  - Artificial substrate: terracotta plant pots placed at the bottom of each enclosure; sampling from pots at the end.
  - Phytoplankton sampling conducted at start and end.
- Timings by site:
  - Lake SS17b: start 08-07-2018; end 22-07-2018 (14 days).
  - Lake SS1590: start 09-07-2018; end 23-07-2018 (14 days).
  - Lake SS906: start 10-07-2018; end 24-07-2018 (14 days).

## Collection, generation and transformation methods

- Water sample handling:
  - In-field filtration through GF/F glass fibre filters.
  - Filtrates refrigerated and analyzed for dissolved nutrients within a few days.
  - Chlorophyll a analyzed from filter paper.
- Sediments and substrates:
  - Terracotta pots removed at end; biofilms scrubbed and rinsed; suspended material frozen until analysis.
  - Surface sediments stored frozen prior to analysis.
- Sample records:
  - Weighed total sample volume; aliquots removed volumetrically for analyses.

## Analytical methods and units of recorded values

- Water chemistry:
  - Soluble reactive phosphorus (SRP): colourimetric (molybdenum blue, APHA 2005), µg/L.
  - Ammonium (NH4-N): colourimetric (phenate, APHA 2005), µg/L.
  - Silicate: colourimetric (molydate yellow, APHA 2005), mg/L.
  - Total phosphorus (TP): colourimetric after persulfate digestion, µg/L.
  - Total nitrogen (TN): measured at University of Maine (USA).
- Chlorophyll and pigments:
  - Chlorophyll a (Chl a) from water, phytobenthos (pot scrapes) and sediments using trichromatic method (Parsons & Strickland, 1963); units: water µg/L, phytobenthos µg/cm2, sediments µg/g.
  - Pigments (chlorophylls and carotenoids) analyzed by HPLC with detailed extraction and separation protocol; pigment concentrations reported as nanomoles per gram of sediment or per cm2 for pot scrapes (and related pigment concentrations for artificial substrate samples).
- Instrumentation and calibration specifics:
  - Ion chromatography calibrated with 10-point standards.
  - YSI probes: pH calibrated daily, DO calibrated daily (air), conductivity calibrated weekly.
  - HPLC pigment calibrations: 8-point calibration; stability checks with plant extract at start and end of each run; manual peak identification by an expert.

## Quality control

- Colorimetric analyses: calibration curves required to have r2 ≥ 0.998; otherwise data discarded.
- Ion chromatography: calibrated with 10-point curve.
- YSI probes: daily pH and DO calibrations; weekly conductivity calibration.
- HPLC pigments: 8-point calibration; stability checks via plant extract before/after each run; manual verification of peak identification and integration.

## Details of data structure

- Data record: 37 rows and 46 data columns.
- Column organization:
  - Columns 1–5: experimental descriptors (Lake_lake_code, Dust_treatment, Replicate, Time_point, Sample_date).
  - Columns 6–17: water measurements (start and end) from mesocosm water.
  - Columns 18–31: surface sediment analyses from mesocosms.
  - Columns 32–46: analyses from artificial substrate (terracotta pot scrapes).
- Example descriptors and units:
  - Lake_SS_lake_code; Dust_treatment; Replicate; Time_point (start/end); Sample_date (dd/mm/yyyy).
  - WaterChla (µg/L), WaterTP-P (µg/L), WaterSRP-P (µg/L), WaterNH4-N (µg/L), WaterNO3-N (µg/L), WaterSilicate (mg/L), and in situ measurements (e.g., Temperature °C, DO %, Conductivity µS/cm, pH).
  - Sediment and pot-scrape pigments reported as nanomoles per gram sediment or nanomoles per cm2, with related chlorophylls and carotenoids (e.g., Chl a, Chl b, fucoxanthin, lutein, zeaxanthin, diadinoxanthin, diatoxanthin, alloxanthin, violaxanthin, etc.).
  - Wet density and Chl a on potscrape (µg/cm2 or mg/cm2, as relevant).
- Metadata structure supports cross-linking start/end conditions, treatment, and replicates across three matrices (water, sediments, artificial substrate).

## References

- APHA (2005). Standard methods for the examination of water and wastewater.
- Chen et al. (2001). Historical trends of hypoxia on the Louisiana shelf: pigments as biomarkers.
- Parsons TR, Strickland JD (1963). Spectrophotometric determination of marine-plant pigments; pigment identification and quantification methods.