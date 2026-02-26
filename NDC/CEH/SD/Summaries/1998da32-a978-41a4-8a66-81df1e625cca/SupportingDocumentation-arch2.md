# Supporting Documentation

## Scope and Content
- Dataset contains results of 17 electrical resistivity tomography (ERT) surveys in the Makutapora Basin, central Tanzania.
- Survey period: 28/06/2019 to 16/07/2019.
- Coordinates and survey geometry are in Supp_Table_for_Survey.csv; this file also includes line name suffixes and locations.

## Data Collection Methods
- Instrument: AGI SuperSting R8 resistivity meter.
- Configuration: dipole-dipole; electrode spacings and related parameters listed in Supp_Table_for_Survey.csv.
- Raw .stg files converted to uploaded .dat dataset files using bespoke Python code.
- More detailed methodology available in the associated paper.

## Quality Control and Data Processing
- Negative values removed from raw data.
- Each apparent resistivity measurement taken in normal and reciprocal configurations; final value is the mean of the two.
- Any values where normal and reciprocal measurements differ by more than 5% from the mean are removed.
- Data aim to delineate superficial geological structures to understand their role in mediating surface–groundwater interactions within the Makutapora wellfield and their influence on groundwater recharge.
- Survey design and data collection oversight conducted by the corresponding authors, E. Zarate and M.O. Cuthbert.

## Data Access and Availability
- Raw .stg files can be provided on request from the corresponding author.

## Context and Purpose
- The dataset supports understanding how superficial geological structures influence surface–groundwater interactions and groundwater recharge in the Makutapora wellfield.