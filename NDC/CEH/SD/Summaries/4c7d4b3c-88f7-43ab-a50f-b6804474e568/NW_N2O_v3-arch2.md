# Details of data structure to 'NW_N2O.csv'

## Overview
- Supplement to the supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Details the data structure of NW_N2O.csv, a 6-column, 608-row N2O emissions dataset from a grassland fertiliser trial (2016) at North Wyke Research Station (Rothamsted Research)
- N2O fluxes measured using manual static chambers

## Dataset contents
- 6 columns, 608 rows
- Focus: N2O emissions dataset from grassland fertiliser trial 2016

## Data structure (columns and units)
- Time: Date & time of N2O sampling
- N_app: 1|2|3 indicating fertiliser application; 1st & 2nd applications of 90 kg N ha-1, 3rd application of 60 kg N ha-1
- Block: 1|2|3|4 blocking factor of randomised block design
- Plot: Experimental unit
- Treatment: AN|IU|U|C representing N fertiliser type; AN = ammonium nitrate (Nitram), U = urea, IU = inhibited urea (agrotain), C = 0N Control
- Flux_N2O: N2O flux for each chamber measurement, in g N2O-N ha-1 day-1

## Data processing and quality
- Flux data with R2 < 0.6 and all negative Flux_N2O values replaced with 0

## Context and use
- Data are intended for environmental monitoring and analysis of emission responses to fertiliser treatments
- Supplementary to the primary documentation, enabling standardized interpretation and potential integration with other datasets and monitoring outputs

## Source reference
- Tied to Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf and its associated data series