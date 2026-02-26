# Prediction of 137 Cs deposition from atmospheric nuclear weapons tests within the Arctic

- Overview
  - Many authors report that deposition rates of long-lived radionuclides (including 90Sr, 137Cs, 239/240Pu) from atmospheric nuclear weapons tests correlate with precipitation.
  - For the UK prior to the Chernobyl accident, deposition estimation uses the approach outlined in Wright et al. (1999).

- Data sources and key sites
  - Measurements from the UK Atomic Energy Authority (AEA) program: 19 UK stations and 20 abroad (1955–1997).
  - Complete quarterly 137Cs deposition records (1955–1985) from Gibraltar, Singapore, and Milford Haven (Wales, UK); Milford Haven used as the representative UK site.

- Step 1: 137Cs deposition data
  - Use Milford Haven quarterly 137Cs deposition and Milford Haven quarterly precipitation (1955–1985) to derive a deposition-to-precipitation ratio.

- Step 2: Quarterly deposition-to-precipitation ratio
  - Compute the ratio of 137Cs deposition per millimetre of precipitation for each quarter at Milford Haven.

- Step 3: UK precipitation data
  - UK Met Office gridded climate data (5 × 5 km resolution) based on 30-year baseline period (1961–1990).
  - UKCIP provided monthly total precipitation to represent spatial variability in UK-wide precipitation.

- Method (data synthesis and spatial modelling)
  - For each quarter:
    - Combine the Milford Haven deposition/precipitation ratio with the UK-wide average total precipitation to estimate spatial variability of quarterly 137Cs input across the UK at 5 × 5 km resolution.
  - Accumulate deposition:
    - Add quarterly 137Cs deposition to previously predicted deposition and apply decay correction (Cs-137 half-life = 30.2 years) to estimate cumulative 137Cs deposition for the UK at 5 × 5 km resolution for 1955–1985.

- Output
  - Spatially explicit, decay-corrected cumulative 137Cs deposition map for the UK (1955–1985) at 5 × 5 km resolution.

- Reference
  - Wright, S.M., Howard, B.J., Strand, P., Nylen, T., & Sickel, M.A.K. (1999). Prediction of 137Cs deposition from atmospheric nuclear weapons tests within the Arctic.

- Data-support perspective relevance
  - Demonstrates integrating heterogeneous data sources (nuclear deposition records, precipitation data, gridded UK climate data) to produce a usable data product.
  - Illustrates handling of temporal and spatial alignment, data normalization (deposition per precipitation), and decay corrections to create a self-serve deposition dataset.
  - Highlights potential for challenges such as relying on a single representative site ( Milford Haven) for UK-wide estimates and using baseline climate data to capture spatial variability.