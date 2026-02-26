# Estimation of the deposition of 137 Cs from atmospheric nuclear weapons tests in the UK prior to the Chernobyl accident

- Many authors have found that deposition rates of long-lived radionuclides (e.g., 90Sr, 137Cs, 239/240Pu) from atmospheric nuclear weapons tests correlate with precipitation patterns and rates.

- The UK-focused estimation uses the approach from Wright et al. (1999) to derive UK-specific deposition prior to the Chernobyl accident.

## Key data sources

- Measurement programs and stations
  - UK Atomic Energy Authority (AEA/AERE) operated 19 UK stations and 20 international stations (1955–1997).
  - Complete quarterly 137Cs deposition records for Gibraltar, Singapore, and Milford Haven (1955–85); Milford Haven chosen as representative for the UK.

- Precipitation and climate data
  - Milford Haven quarterly deposition data linked to quarterly precipitation totals (1955–85).
  - UK Meteorological Office gridded baseline climate data for the UK (5 × 5 km resolution) derived from 30-year climate data (1961–1990).
  - UKCIP monthly total precipitation used to represent spatial variability in UK precipitation.

- Reference framework
  - Wright, S.M., Howard, B.J., Strand, P., Nylen, T., & Sickel, M.A.K. (1999). Prediction of 137Cs deposition from atmospheric nuclear weapons tests within the Arctic. Environmental Pollution, 104, 131-143. DOI: 10.1016/S0269-7491(98)00140-7.

## Methodology

- Quarter-by-quarter approach
  - Use Milford Haven 137Cs deposition records to establish a quarterly deposition/precipitation relationship.
  - Combine Milford Haven deposition with UK quarterly precipitation to derive a deposition per millimetre of precipitation ratio for each quarter.

- Spatial extrapolation to UK
  - Apply the Milford Haven deposition/precipitation ratios to the UK-wide average total precipitation (from UKCIP data) to calculate spatial variability in quarterly 137Cs deposition at 5 × 5 km resolution.

- Temporal accumulation and decay correction
  - Add quarterly 137Cs deposition to pre-existing predicted 137Cs deposition.
  - Correct for physical decay of 137Cs (half-life 30.2 years) to produce cumulative deposition estimates for the UK at 5 × 5 km resolution for 1955–1985.

## Output characteristics

- Produces a spatially resolved (5 × 5 km grid), quarterly time-series deposition dataset for 137Cs across the UK (1955–1985).
- Decay-corrected cumulative deposition estimates suitable for GIS mapping and spatial analysis.
- Method relies on representative Milford Haven data to infer UK-wide patterns and on gridded UK precipitation data to distribute deposition spatially.

## Applications and considerations for GIS work

- Provides a map-based data product showing historical 137Cs deposition across the UK at high spatial resolution (5 × 5 km) for GIS visualization and analysis.
- Illustrates integration of disparate data sources (point deposition records, precipitation measurements, and gridded climate data) into a coherent spatial dataset.
- Highlights the importance of selecting a representative site (Milford Haven) and the need for consistent data standards across data sources.