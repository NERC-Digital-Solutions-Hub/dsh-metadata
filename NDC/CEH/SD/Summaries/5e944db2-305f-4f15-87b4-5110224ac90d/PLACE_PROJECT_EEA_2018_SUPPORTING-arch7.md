# Extra cellular enzyme activity from the PLACE project

## Overview
- Data describe soil extracellular enzyme potential activities (EEA_FINAL) measured from autumn 2018 soil samples.
- Analysis performed in Wageningen University.
- Part of the PLACE project investigating phosphorus limitation and ecosystem responses to elevated CO2.
- Experimental design uses turf mesocosms within a long-term nutrient manipulation experiment in the Peak District, UK.

## Experimental setup and location
- Location: Wardlow Hay Cop, Peak District, UK.
- Experimental plot: two adjacent P-limited grasslands on calcareous/limestone soil and acidic soil.
- Timeframe: nutrient manipulation ongoing for >20 years; mesocosms measured in autumn 2018.
- CO2 treatments: ambient (~410 ppm) or elevated (~600 ppm).

## Data structure and variables
- LOCATION, Description: Experimental plot ID (string); location reference for GIS.
- PAIR, Description: Block (numeric).
- CO 2, Description: CO2 fumigation level; Units: string (A = ambient, E = 600 ppm).
- GRASS, Description: Grassland ecosystem type; Units: string (acid = acidic, calc = calcareous).
- TREAT, Description: Nutrient treatment; Units: string (P = phosphorus fertilization; 0N = control; LN = low nitrogen; HN = high nitrogen).
- DEPTH, Description: Depth of soil sample; Units: string (0-10 cm, 10-20 cm).
- FL_MATRIX, Description: Fluorescent matrix; Units: string (MUF, AMC).
- ENZYME, Description: Extracellular enzyme; Units: string (BG, CB, NAG, LAP, AP).
- EEA_FINAL, Description: Rate of enzyme activity; Units: Nmol g^-1 h^-1.

## Measurements and units
- EEA_FINAL represents the measured rate of extracellular enzyme activity in soil, expressed as nanomoles of product per gram of soil per hour (nmol g^-1 h^-1).

## Potential GIS applications
- Map spatial patterns of enzyme activity across plots for different CO2 treatments, grassland types, depth intervals, and nutrient treatments.
- Visualize interactions between CO2 enrichment and nutrient manipulation on enzyme activity.
- Integrate with plot-level attributes (plot ID, block) to support stratified analyses and decision-making in ecosystem management.

## Notes
- Data are specifically chandeliered to experimental plot IDs and blocks, enabling linking with other spatial or environmental datasets from the PLACE experiment.
- Detailed variable definitions support consistent data integration and GIS mapping, though no spatial coordinates are provided directly in the metadata.