# HF_soil_minN.csv

## Overview
- 11 columns and 608 rows
- Contains soil NH4-N and NO3-N + NO2-N concentrations, soil moisture contents, soil pH, and soil electrical conductivity (EC)
- Data from grassland fertiliser trial 2016, Henfaes Research Station (Bangor University)

## Dataset structure (columns)
- Date: Date of sampling
- N_app: 1|2|3 denotes fertiliser application; 1st & 2nd application 90 kg ha-1, 3rd application 60 kg ha-1
- Block: 1|2|3|4 blocking factor of randomised block design
- Plot: 1–16 plot number
- Treatment: AN|U|IU|C representing N fertiliser type (AN = ammonium nitrate, U = urea, IU = inhibited urea, C = 0N control)
- Soil_NH4_mgNkg: ammonium concentration in soil; mg NH4-N kg-1; dry weight basis
- Soil_NO3_mgNkg: nitrate concentration in soil; mg NO3-N kg-1; dry weight basis
- moisture_dry: soil moisture on a dry weight basis; g H2O g dry soil-1
- moisture_wet: soil moisture on a wet weight basis; g H2O g wet soil-1
- pH: soil pH
- EC: soil electrical conductivity; µS cm-1

## Sampling and laboratory methods
- Soil sampled from 0–10 cm depth using a 1 cm diameter corer; six samples per plot were bulked
- Extraction: 5 g soil with 25 ml 0.5 M K2SO4; shaken 30 minutes at 200 rpm
- Nitrate analysis: colorimetric method (Miranda et al. 2001)
- Ammonium analysis: method (Mulvaney 1996)
- Moisture determination: dried at 105°C for 24 hours
- pH and EC: measured with standard electrodes using a 1:2.5 soil to deionised water suspension

## Experimental design
- Grassland fertiliser trial conducted in 2016
- Randomised block design with blocks 1–4
- Plots numbered 1–16
- Treatments correspond to N fertiliser types (AN, U, IU, C)
- N_app captures sequence and rate of fertiliser applications across the trial

## Data usage notes
- Units and basis clearly defined (dry vs. wet weight; pH, EC in specified units)
- Data can support analyses of fertiliser effects on ammonium, nitrate, moisture, pH, and EC across treatments and blocks
- Linked to supporting documentation for CINAg experiments (see original sources for detailed methods and provenance)