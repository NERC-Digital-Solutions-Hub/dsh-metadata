# Supporting Documentation

- This dataset contains results of 17 electrical resistivity tomography (ERT) surveys collected in the Makutapora Basin, central Tanzania, from 28/06/2019 to 16/07/2019.
- Coordinates and survey geometry are provided in Supp_Table_for_Survey.csv, which also includes line name suffixes and locations.
- Data collection methods:
  - Instrument: AGI SuperSting R8 (STING) resistivity meter.
  - Configuration: dipole-dipole.
  - Electrode spacings and associated parameters are included in Supp_Table_for_Survey.csv.
- Data processing:
  - Raw .stg output files were converted to uploaded .dat dataset files using bespoke Python code.
  - The Python code and converted data can be provided on request by contacting the corresponding author.
- Quality control:
  - Negative values were removed.
  - Each apparent resistivity measurement was obtained in normal and reciprocal configurations; the measurement value used is the mean of the two.
  - Any values where normal and reciprocal measurements differ by more than 5% from the mean were removed.
  - Details are described in Section 2.2 of the associated paper.
- Purpose:
  - Data were collected to examine and delineate superficial geological structures to understand their role in mediating surface–groundwater interactions within the Makutapora wellfield and their influence on groundwater recharge.
- Authors and oversight:
  - Survey design and oversight of data collection by E. Zarate and M.O. Cuthbert.