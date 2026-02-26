# Overview of the data

- In situ mesocosm experiment conducted in three Greenland lakes (SS17b, SS1590, SS906) near Kangerlussuaq. Six mesocosms per lake (60 cm diameter, ~1 m depth) embedded in sediments; dust added to three mesocosms at 0.196 g/L (25–35 g per enclosure, adjusted for depth/volume); three mesocosms served as controls. Dust sourced from a thawed spring snowbank.
- Experiment setup in July 2018, running for 14 days. Sampling at the start and end (or end-only for destructive sampling). Measurements include water chemistry, phytoplankton biomass (chlorophyll a), phytobenthos on artificial substrate, and surface sediments.
- In situ measurements of conductivity, temperature, and dissolved oxygen were taken with a YSI multiprobe in the upper 20 cm of the water column.
- Sampling included water and phytoplankton from mesocosms, surface sediments from each mesocosm, and terracotta plant pots placed at the bottom to support phytobenthos; pot samples collected at the end.

Experimental design and timing

- Lakes: three sites with geographic coordinates provided; six enclosures per lake (3 dust-treated, 3 control) arranged in a 3x2 layout.
- Sampling times per site: Day 0/setup and Day 14/end; some measurements only at end due to sampling type.
- Timings listed for each lake and mesocosm (dates in July 2018) corresponding to setup, final sampling, and duration (14 days).

Collection, generation, and transformation methods

- Water samples filtered in the field through GF/F filters; dissolved nutrients analyzed later in the lab. Chlorophyll a estimated from filter papers.
- Terracotta pots with biofilms scraped at end; suspended material frozen for later analysis. Surface sediments collected with an extended syringe; three replicates per mesocosm.
- Phytoplankton sampling conducted at start and end.

Analytical methods and units

- Water chemistry: soluble reactive phosphorus (SRP), ammonium, silicate, total phosphorus, total nitrogen. Units: µg/L or mg/L for silicate; total nitrogen measured at University of Maine; major ions via ion chromatography.
- Chlorophyll analysis: spectrophotometric determination of chlorophyll a in water, phytobenthos, and sediments (units: µg/L for water, µg/cm2 for phytobenthos, µg/g for sediments).
- Pigment analysis (HPLC): pigments from phytobenthos and sediments quantified; results reported as nanomoles per cm2 (phytobenthos) or per gram (sediments). Pigment groups include chlorophylls and carotenoids (e.g., Chl a, Chl b, fucoxanthin, diadinoxanthin, alloxanthin, lutein, zeaxanthin, canthaxanthin, pheophytins, etc.).
- HPLC method details: extraction solvents, chromatographic conditions, calibration with standards, spectral scanning, and manual peak identification by a trained expert.
- Data columns include a range of water, sediment, and pot-scrape measurements with explicit units and descriptions.

Quality control

- Colorimetric water analyses: calibration curves checked (r2 ≥ 0.998); analyses discarded if below threshold.
- Ion chromatography: 10-point calibration; daily YSI pH and DO calibrations; weekly DO calibration.
- HPLC pigments: eight-point calibration; stability checks with plant extract at run start and end; manual verification of identifications and peak integration to ensure accuracy.

Details of data structure

- Dataset contains 37 rows and 46 data columns.
- Columns 1–5: experimental descriptors (lake code, dust treatment, replicate, time point, sample date).
- Columns 6–17: water measurements at start and end (e.g., WaterChla, WaterTP-P, WaterSRP-P, WaterNH4-N, WaterNO3-N, WaterSilicate, plus several derived measured parameters such as temperature, DO, conductivity, pH).
- Columns 18–31: surface sediment analyses (various pigments and chlorophyll-related metrics).
- Columns 32–46: artificial substrate (terracotta pot) scrape analyses (pigments, chlorophyll, and associated metrics) and related metrics like wet density.
- Descriptions cover specific labels, units, and notes for each column (e.g., Descriptors for experimental conditions, measurement types, and sampling times).

References

- APHA (2005). Standard methods for the examination of water and wastewater.
- Chen et al. (2001). Historical trends of hypoxia on the Louisiana shelf: pigments as biomarkers.
- Parsons & Strickland (1963). Discussion of spectrophotometric determination of marine-plant pigments; revised equations for chlorophylls and carotenoids.