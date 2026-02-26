# Experimental design and methods for measuring soil microbial biomass phosphorus under CO2 enrichment in grassland mesocosms

- Objective and scope
  - Establish environmental health measures to scrutinise policy-relevant questions about soil microbial phosphorus (MBP) and nutrient dynamics under climate manipulation (CO2 enrichment) in grassland ecosystems.
  - Compare two grassland types (limestone and acidic) under varying nutrient additions and CO2 levels to understand how microbial P responds to combined abiotic and anthropogenic drivers.

- Experimental design and site context
  - Source: Intact soil-turf monoliths from a long-term nutrient manipulation experiment (established 1995) at Wardlow, Peak District National Park, UK.
  - Grassland types:
    - Limestone grassland (Festuca-Avenula CG2d) on shallow ranker transitioning from humic rendzina.
    - Acidic grassland (Festuca-Agrostis-Galium U4e) on cryptic podzol with a ~10 cm organic-rich A horizon.
  - Treatments on field plots: no treatment (natural P limitation, water only), P addition (35 kg P ha-1 y-1), N addition low (LN, 3.5 g N m-2 y-1) and high (HN, 14 g N m-2 y-1).
  - Monolith handling: Ten replicate monoliths (0.35 × 0.35 m) removed per treatment in Feb–Mar 2017; excavated to 10 cm (limestone) or 20 cm (acidic) and transplanted into polypropylene mesocosms at the Bradfield Environment Laboratory.
  - Mesocosm setup: Embedded in native soil, fully enclosed sides/base, free-draining with a mesh voile base to prevent particulate loss and root ingrowth from surrounding soils; limestone base added for limestone mesocosms to mimic field conditions.

- CO2 enrichment and experimental layout
  - CO2 treatments: Elevated CO2 (eCO2) and ambient CO2, with each mesocosm receiving one of the four nutrient treatments (P, 0N, LN, HN).
  - miniFACE system: Five 1.6 m diameter FACE rings and five control rings; each ring had one mesocosm per nutrient treatment.
  - CO2 delivery and monitoring: CO2 sensors (GTM222) with microprocessors controlling delivery to maintain target concentrations; daytime target of 600 ppm for 2018–2020 (April–October); ambient CO2 averaged ~410 ppm.

- Soil sampling and processing
  - Sampling frequency: Annually (September–October) from each mesocosm.
  - Sampling method: Triplicate 2 cm diameter cores collected from random locations within each mesocosm; acid grassland samples were further divided into A and B horizons.
  - Sample preparation: Soil passed through 10 mm and then 2 mm sieves; roots removed; moisture determined from oven-dried subsamples at 105°C.

- Key measurements
  - Soil microbial biomass phosphorus (MBP)
    - Method: Chloroform fumigation-extraction (Vance et al. 1987).
    - Procedure: Fumigated and non-fumigated subsamples extracted with 0.5 M NaHCO3 (pH 8.5); concentrations measured by ICP-OES after extraction.
    - Calculation: MBP = (P_fumigated − P_non-fumigated) / 0.4.
    - Quality notes: One non-fumigated sample missing (NA); some MBP values removed due to impossible negative values (NA).

  - Additional soil properties recorded
    - Soil extractable phosphorus (Soil_P) from NaHCO3 extracts.
    - Bulk density (g cm-3).
    - Gravimetric moisture content (via oven drying).
  - Data structure and units
    - Dataset fields include: Location (mesocosm ID), Year, Depth (0–10 cm; 10–20 cm for deeper profiles), Grassland (Acid or Calc/Limestone), Treat (P, 0N, LN, HN), Pair (experimental block), CO2 (A = ambient, E = eCO2), Position within ring, Soil_P (mg kg−1), MBP (mg kg−1), Bulk density (g cm−3).

- Data considerations and gaps
  - Missing data: Some MBP values missing due to non-fumigated sample absence and negative values removed from dataset.
  - Metadata and data handling: Detailed data structure provided to support traceability and clarity of measurements; method descriptions enable reproducibility of MBP and associated soil measurements.

- References for methods
  - Vance, E. D., Brookes, P. C. & Jenkinson, D. S. (1987) for chloroform-fumigation extraction of microbial biomass-C.
  - Brookes, P. C., Powlson, D. S. & Jenkinson, D. S. (1982) for microbial biomass phosphorus measurement.