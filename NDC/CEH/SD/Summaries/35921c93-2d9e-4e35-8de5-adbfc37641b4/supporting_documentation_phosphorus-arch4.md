# Experimental design

- Purpose and context
  - Long-term grassland nutrient manipulation experiment (established 1995) at Wardlow, Peak District National Park, UK.
  - Two grassland types: limestone grassland (Festuca-Avenula CG2d) and acidic grassland (Festuca-Agrostis-Galium U4e).
  - Objective: study effects of nutrient treatments and elevated CO2 on soil properties, including microbial biomass phosphorus (MBP).

- Experimental setup
  - Nine square metre plots (9 m2) per treatment, with replication across Grassland types.
  - Treatments per plot: no treatment (distilled water only, control), phosphorus addition (P: 35 kg P ha−1 y−1), and nitrogen additions at two levels (LN: 35 kg N ha−1 y−1, HN: 140 kg N ha−1 y−1).
  - Monoliths: ten 0.35 × 0.35 m fragments per treatment, excavated in 2017 and transplanted into mesocosm boxes at Bradfield Environment Laboratory.
  - Mesocosms: maintained outside, embedded in native soil; fully enclosed sides/bottom; free draining through a mesh voile base to prevent root ingress/egress.

- CO2 enrichment
  - Experimental design with elevated CO2 (eCO2) and ambient CO2 (aCO2) within miniFACE rings.
  - Each ring contained one of the four nutrient treatments; 8 mesocosms in total (2 grassland types × 4 treatments) per CO2 level.
  - miniFACE system: five 1.6 m diameter rings and five controls; automated CO2 delivery controlled by sensors and microprocessors.
  - Fumigation period: 2018–2020, daylight target ~600 ppm CO2 during Apr–Oct; ambient ~410 ppm in the surrounding environment.

- Soil collection and processing
  - Annual soil sampling (Sept–Oct) from each mesocosm.
  - In acidic grassland, soils separated into A and B horizons; cores 2 cm diameter, triplicate per mesocosm.
  - Samples dried and prepared: passed through 10 mm sieve, roots removed, then 2 mm sieve; subsamples dried at 105°C for moisture content.

- MBP (microbial biomass phosphorus) determination
  - Method: chloroform fumigation as per Vance et al. (1987).
  - Process: compare fumigated vs. non-fumigated extracts; extraction with 0.5 M NaHCO3 (pH 8.5); quantify phosphorus via ICP-OES.
  - MBP calculation: (P_fumigated − P_nonfumigated) / 0.4 (per Brookes et al. 1982).
  - Data issues: one non-fumigated sample missing; some MBP values negative and were removed.

- Data structure and units
  - Location/Description: Mesocosm unique ID; Location/Units: String.
  - Year/Description: Year; Year/Units: Numeric.
  - Depth/Description: Depth increment of soil profile; Depth/Units: 0–10 cm, 10–20 cm.
  - Grass/Description: Grassland type; Grass/Units: Acid, Calc.
  - Treat/Description: Nutrient treatment; Treat/Units: P, 0N, LN, HN.
  - Pair/Description: Experimental block; Pair/Units: Numeric.
  - CO2/Description: CO2 level; CO2/Units: A (ambient), E (eCO2).
  - Position/Description: Position within FACE ring; Position/Units: Numeric.
  - Soil_P/Description: Soil extractable phosphorus; Soil_P/Units: mg kg−1.
  - MBP/Description: Microbial biomass phosphorus; MBP/Units: mg kg−1.
  - BulkDensity/Description: Soil bulk density; BulkDensity/Units: g cm−3.

- Key measurements and variables
  - Soil extractable phosphorus (Soil_P).
  - Microbial biomass phosphorus (MBP) via fumigation-extraction.
  - Soil bulk density (BD).
  - Soil moisture content (via oven-dried weight).
  - Depth-resolved sampling (0–10 cm and 10–20 cm horizons where applicable).

- Data quality, gaps, and notes
  - Missing non-fumigated MBP sample prevented MBP calculation for that plot.
  - Some MBP values negative and were removed to maintain data integrity.
  - Data derived from controlled mesocosm experiments with explicit CO2, nutrient, and grassland-type factors.

- References for methods
  - Vance, Brookes, & Jenkinson (1987) for MBP fumigation method.
  - Brookes, Powlson, & Jenkinson (1982) for MBP measurement methodology.