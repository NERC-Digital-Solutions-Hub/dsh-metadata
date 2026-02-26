# Experimental design: Intact soil-turf monoliths were taken from a long-term grassland nutrient manipulation experiment that was established in 1995 at Wardlow, Peak District National Park, UK.

## Objective
- Document a long-term, standardized experiment to monitor soil health and microbial phosphorus under varying nutrient and CO2 conditions.
- Produce data outputs suitable for environmental health assessment, policy performance review, and data interoperability.

## Experimental design and setup
- Location and soil types
  - Limestone grassland (NVC Festuca-Avenula CG2d) on shallow rendzina.
  - Acidic grassland (NVC Festuca-Agrostis-Galium U4e) on cryptic podzol.
- Treatments and replicates
  - On each grassland, 9 m2 plots with four treatments: no treatment (natural P limitation), P fertilization (P), low N (LN; 35 kg N ha-1 y-1), and high N (HN; 140 kg N ha-1 y-1).
  - Ten replicate monoliths per treatment were excavated in 2017 and transported to Bradfield for mesocosm setup.
- Mesocosm construction
  - Limestone monoliths placed in polypropylene mesocosm boxes; limestone base added for the limestone grassland to mimic field soil conditions.
  - Fully enclosed sides and base with a drainage mesh voile to prevent soil exchange while allowing drainage.
  - Embedded in native soil at Bradfield to maintain thermal buffering; climate is similar to Wardlow.

## CO2 enrichment
- Experimental design
  - Each mesocosm ring assigned to either ambient or elevated CO2 (eCO2) conditions, with four nutrient treatments represented in each CO2 level (8 mesocosms total).
- miniFACE system
  - Five 1.6 m diameter FACE rings and five control rings; CO2 delivered via micro-holes in PVC tubes controlled by sensors and automated regulators.
  - Daylight target CO2: 600 ppm during measurement period.
  - Study years for CO2 enrichment: 2018–2020; ambient CO2 averaged ~410 ppm.

## Soil collection and processing
- Sampling
  - Annual soil sampling in September–October from each mesocosm.
  - Triplicate 2 cm diameter cores collected; in the acidic grassland horizons A and B separated.
- Preparation
  - Soil passed through 10 mm, roots removed, then ground through 2 mm sieve.
  - Subsamples oven-dried at 105°C to determine soil moisture content.

## Determination of soil microbial biomass phosphorus (MBP)
- Method
  - Chloroform-fumigation-extraction (Vance et al., 1987) to determine MBP.
  - Subsample testing: fumigated vs. non-fumigated, followed by extraction in 0.5 M NaHCO3 (pH 8.5), shaking, filtration.
  - MBP calculation: MBP = (P_fumigated - P_non-fumigated) / 0.4 (Brookes et al., 1982).
- Data notes
  - Some samples missing MBP data; a few had negative values and were removed from MBP calculations.
  - Gravimetric water content determined from 105°C oven-dried subsamples.

## Data structure and units
- Variables and descriptions
  - Location (Mesocosm unique ID), Year (numeric), Depth (0-10 cm, 10-20 cm increments; defined per horizon), Grass (Acid or Calc), Treat (P, 0N, LN, HN), Pair (experimental block), CO2 (A = ambient, E = eCO2), Position (within FACE ring).
  - Soil_P (mg kg-1): extractable phosphorus.
  - MBP (mg kg-1): microbial biomass phosphorus.
  - Bulkdensity (g cm-3): soil bulk density.
- Representative units
  - P treatment: 3.5 g m-2 y-1 (equivalent to 35 kg P ha-1 y-1).
  - LN: 3.5 g m-2 y-1 N; HN: 14 g m-2 y-1 N.

## Data quality, issues, and caveats
- Missing MBP data for one non-fumigated sample; some MBP values were negative and removed.
- Data are structured to facilitate comparison across grassland types, nutrient treatments, CO2 levels, and soil depths.

## Data management and accessibility
- Data collection and processing follow standardized methods to ensure consistency across years.
- Outputs are prepared in clear formats (reports, charts) and stored for access through appropriate data portals, enabling broader use and interoperability.

## References
- Vance, E. D., Brookes, P. C. & Jenkinson, D. S. (1987). Chloroform fumigation method for soil microbial biomass-C.
- Brookes, P. C., Powlson, D. S. & Jenkinson, D. S. (1982). Measurement of microbial biomass phosphorus in soil.