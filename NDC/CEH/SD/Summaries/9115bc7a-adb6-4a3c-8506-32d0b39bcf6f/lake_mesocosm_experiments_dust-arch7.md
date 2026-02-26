# Overview of the data

- Mesocosm experiment conducted in three lakes in the Kangerlussuaq area, West Greenland, to study effects of added dust on water chemistry and phototrophs in water and sediments.
- Researchers: Suzanne McGowan and Amanda Burson.

## Experimental design and sampling

- Location: In situ in three lakes (Lake SS17b, SS1590, SS906) with specified latitude/longitude coordinates.
- Setup: 6 enclosures per lake (60 cm diameter, ~1 m depth, embedded in lake sediments); 3 enclosures receive dust, 3 serve as controls.
- Dust treatment: 0.196 g/L dust (25–35 g per enclosure, adjusted for water depth/volume); dust sourced from a thawed snowbank, filtered, and freeze-dried.
- Arrangement: Dust and control enclosures alternated within a 3x2 layout inside a wooden frame.
- Duration and sampling: 14 days; sampling at start and end (or end only for destructive sampling). In situ measurements of conductivity, temperature, and dissolved oxygen with a YSI multiprobe.
- Sampling within mesocosms: integrated depth water samples, surface sediments (3 replicates per mesocosm), artificial substrate (terracotta pots) for phytobenthos sampled at the end.
- Timings by lake: Day 0 setup; final day sampling around day 14; specific dates provided per lake and per mesh site.

## Collection/Transformation/Preparation

- Water samples filtered on site through GF/F filters; filtered water stored for nutrient analysis; Chlorophyll a estimated from filtrates.
- Terracotta pots: biofilms scraped, suspended material frozen for later analysis.
- Sediments: surface samples stored frozen prior to analysis.
- Recorded total sample volumes and analyzed aliquots volumetrically.

## Analytical methods and units

- Water chemistry (from filtered water): soluble reactive phosphorus (SRP) by molybdenum blue; ammonium by phenate; silicate by molybdate yellow; total phosphorus by molybdenum blue after persulfate digestion; total nitrogen analyzed elsewhere.
- Instruments/units: nutrients in µg/L or mg/L (silicate); major ions by ion chromatography.
- Chlorophyll analysis: spectrophotometric method for water, phytobenthos, and sediments; reported as µg/L (water), µg/cm2 (phytobenthos), µg/g (sediments).
- Pigments: HPLC analysis for chlorophylls and carotenoids; pigments quantified as nanomoles per g (sediments) or per cm2 (pots/sediments), with detailed extraction and separation conditions described.
- Specific pigments measured in sediments and pots include Chl a, Chl b, and several carotenoids (e.g., fucoxanthin, diadinoxanthin, diatoxanthin, zeaxanthin, lutein, canthaxanthin, etc.).
- Pigment quantification references: calibration against commercial standards; spectral scanning (350–750 nm); peak areas calibrated to standards; results reported with pigment-specific units.

## Data structure and content

- Dataset composition: 37 rows x 46 data columns.
- Column grouping:
  - Columns 1–5: descriptors for experimental conditions (lake code, dust treatment, replicate, time point, sample date).
  - Columns 6–17: water measurements in mesocosms at start and end.
  - Columns 18–31: analyses of surface sediments in mesocosms.
  - Columns 32–46: analyses of artificial substrate (terracotta pot scrapes).
- Example variables (selected): WaterChla (µg/L), WaterTP-P (µg/L), WaterSRP-P (µg/L), WaterNH4-N (µg/L), WaterNO3-N (µg/L), WaterSilicate (mg/L); Sediment pigments (nanomoles/g or nmol/cm2); Potscrape pigment concentrations and pigment-related metrics; Pot density and Chl a on substrate.
- Notes on column labels and units are provided for interpretability, with explicit descriptions for each variable (e.g., time point start/end, sample date, replicate number, etc.).

## Quality control and assurance

- Calibration and QC: colorimetric analyses calibrated with fresh curves; r2 threshold > 0.998; ion chromatography calibrated with 10-point curve; YSI probes calibrated daily (pH, DO) and weekly for conductivity.
- Pigment QA: 8-point pigment calibration; stability checks with plant extract at start/end of each HPLC run; manual verification of pigment identifications and peak integration to ensure accuracy.

## Spatial and GIS relevance

- Geographic scope: three lakes with precise coordinates; enclosure-level sampling enables spatial analysis within each lake.
- GIS-ready potential: data can be linked to spatial layers (lake boundaries, bathymetry, sediment types) to map spatial patterns of water chemistry and pigment composition across enclosures and lakes.
- Temporal aspect: two-time-point design (start and end) allows assessment of changes over the experimental period and spatially across sites.
- Data integration: compatible with GIS workflows for environmental monitoring and policy-relevant spatial analyses due to well-defined units (lakes, enclosures, depths) and standardized measurement units.

## References

- APHA (2005). Standard methods for the examination of water and wastewater.
- Chen et al. (2001). Historical trends of hypoxia on the Louisiana shelf: pigments as biomarkers.
- Parsons & Strickland (1963). Spectrophotometric determination of marine-plant pigments.