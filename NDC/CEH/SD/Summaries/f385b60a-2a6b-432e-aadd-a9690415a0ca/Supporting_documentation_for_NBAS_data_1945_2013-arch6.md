# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from North Basin of Windermere 1945 to 2013

## Summary
- Long-term monitoring dataset for the North Basin of Windermere, covering measurements from 1945 to 2013 (with variable start years differing by parameter).
- Variables include physical, chemical, and biological indicators: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH (PH), nutrients (NH4N, NO3N, PO4P, TOTP, SIO2), and phytoplankton chlorophyll a (TOCA).
- Data collected weekly or fortnightly from a boat at the deepest lake location; samples integrated over depth horizons that changed over time (0-5 m; 0-10 m; 0-7 m).
- Data are provided in raw form (not calibrated or quality controlled beyond visual checks; duplicates from 2005 onward have been quality checked).
- Structure and format designed to support data discovery and self-serve analysis, with accompanying references to scientific outputs using the dataset.

## Data scope and time period
- Geographic focus: North Basin of Windermere, Cumbria, England.
- Timeframe: February 1945 through 2013 (with variable availability by parameter).
- Sampling frequency: weekly or fortnightly.

## Sampling regime and collection methods
- Initial data collection by the Freshwater Biological Association; since 1989, collected by the Centre for Ecology & Hydrology (CEH) and its predecessor Institute of Freshwater Ecology.
- Measurement location: from a boat at the deepest part of the lake (buoy reference).
- Depth integration over time:
  - 0 to 5 m (1945–1962)
  - 0 to 10 m (1962–1964)
  - 0 to 7 m (1964 onward)

## Variables, units, and data structure
- TEMP: Surface temperature in degrees Celsius (°C)
- OXYG: Surface oxygen saturation in percent air-saturation (%)
- SECC: Secchi depth in metres (m)
- ALKA: Alkalinity in micrograms per litre as CaCO3 (µg CaCO3 per L)
- PH: pH
- NH4N: Ammonium in micrograms N per litre (µg N L⁻¹)
- NO3N: Nitrate in µg N L⁻¹
- PO4P: Soluble reactive phosphate in µg P L⁻¹
- TOTP: Total phosphorus in µg P L⁻¹
- SIO2: Dissolved reactive silicon in µg SiO2 per litre
- TOCA: Phytoplankton chlorophyll a in µg per litre
- sign_if_LT_LOD: Indicator for values below detection limit (presence of a "<" sign)

- Data file structure: Comma separated values (CSV) with columns:
  - sdate (Date of measurement)
  - variable, Description (name and description of the parameter)
  - value, Description (measurements in their respective units)
  - sign_if_LT_LOD, Description (indicator when below detection limit)

## Quality control, limitations, and caveats
- The dataset is raw and has not been quality controlled or calibrated (except for duplicate entries from 2005 onward).
- Data have been visually checked, but formal quality control and calibration have not been applied.
- Caution advised when combining across years due to changes in depth integration and raw-data status.

## Data provenance and lineage
- Original collection: Freshwater Biological Association.
- Current stewardship: Centre for Ecology & Hydrology (CEH) and its predecessor Institute of Freshwater Ecology since 1989.
- Documentation includes a clear description of sampling regime, depth integration changes, and the data structure to facilitate reuse.

## Using the dataset
- Suitable for long-term time-series analyses of physical, chemical, and biological water quality indicators in Windermere.
- Enables exploration of trends in surface temperature, oxygen, water transparency, nutrient availability, and phytoplankton chlorophyll a over nearly seven decades.
- Can be combined with other Windermere datasets, provided attention is paid to changes in depth integration and raw-data status.
- Useful in conjunction with cited publications that have leveraged the dataset for ecological and climate-related research.

## Example publications and usage references
- Do early warning indicators consistently predict non-linear change in long-term ecological data? (Journal of Applied Ecology, 2016)
- Insights into perch population and community biology from a 70-year lake study (Biology of Perch, 2015)
- Pathogens trigger top-down climate forcing on ecosystem dynamics (Oecologia, 2016)
- Phytoplankton phenology and drivers of change in large lakes (Freshwater Biology, 2012)
- Environmental DNA and long-term freshwater fish community assessments (Molecular Ecology, 2016)
- Additional related studies across climate, nutrient dynamics, and lake ecology (various 2012–2016 publications)