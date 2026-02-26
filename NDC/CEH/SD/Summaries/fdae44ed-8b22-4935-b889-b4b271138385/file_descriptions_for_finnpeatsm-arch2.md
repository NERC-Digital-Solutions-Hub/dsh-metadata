# Fire emissions data for Southeast Asian fires for 2004, 2006, 2009, 2012, 2014 and 2015

- Scope and area
  - Southeast Asian fires for years 2004, 2006, 2009, 2012, 2014 and 2015
  - Spatial extent: 15°S to 15°N, 95°E to 125°W
  - Two file types:
    - FINNpeatSM_SEAS_YYYY_MOZ4.txt (FINNpeatSM emissions)
    - FINNpeatSM_SEAS_after_restoration_YYYY_MOZ4.txt (FINNpeatSM after restoration)

- Data basis and purpose
  - Emissions are based on the Fire Inventory from NCAR (FINNv1.5) with added peat-fire emissions
  - Daily fire emissions at 1 km resolution
  - For peat detections (identified using a peatland map from WRI), additional peat emissions are calculated using Es = BA × BD × ρ × EFs
  - Malaysian peat fires are not included
  - No long-term smouldering effects; peat emissions are allocated to the detection day
  - Peat-specific assumptions:
    - Peat burned area per hotspot: 40 ha
    - Peat density: 0.11 g cm-3
    - Burn depth: moisture-dependent (0.25 to 0.15 m3/m3 soil moisture; mapped to 5 cm to 37 cm burn depth)
  - Emission factors (average EF from multiple studies):
    - CO2: 1670 g kg-1
    - PM2.5: 22.3 g kg-1
    - OC: 11.5 g kg-1
    - BC: 0.07 g kg-1

- After restoration scenario
  - Scenario assumes 2.49 million hectares of Indonesian peatland had been previously restored
  - Reduces burned area to reflect restoration effects and increases soil moisture by the observed average in Kalimantan national parks
  - Recalculates emissions using the same method as FINNpeatSM
  - Note: These emissions do not reflect real fires; intended for scenario analysis as described in Kiely et al. (2021)

- File structure and variables
  - Structure mirrors FINNv1.5 with MOZART4 speciation
  - Each file contains:
    - Header line with variable names
    - One row per fire event
  - Key variables include:
    - DAY (Julian day), TIME (UTC)
    - GENVEG (vegetation type), LATI, LONGI
    - AREA (burned area, m2)
    - Emissions per species (e.g., CO2, CO, H2, NO, NO2, SO2, NH3, CH4, NMOC, PM25, OC, BC, PM10, etc.)
    - Additional emission species listed with specific column names (e.g., C10H16, C2H4, C2H5OH, C2H6, C3H6, C3H8, CH2O, CH3CHO, etc.)
  - Species and proxies are aligned with MOZART4 gas/particle speciation

- Methodological context and references
  - Emissions and methods described in Kiely et al. (2019, 2020)
  - Peat-fire emissions and assumptions based on multiple foundational studies (e.g., Christian et al. 2003; Hatch et al. 2015; Stockwell et al. 2016; Nara et al. 2017; Wooster et al. 2018; Smith et al. 2018)
  - Restoration scenario methodology detailed in Kiely et al. (2021)
  - Soil moisture and data sources referenced include ESA CCI SM and related merging/derivation studies (Liu et al. 2012; Dorigo et al. 2017; Gruber et al. 2017)

- Data use notes and limitations
  - Files are designed for environmental monitoring and analysis of fire emissions with standardized formatting for integration into emissions models
  - Malaysian peat fires are excluded from these emissions
  - The restoration scenario is a modeled, hypothetical case and not a record of actual events
  - Data quality assurance and storage practices align with standard monitoring workflows, ensuring reproducibility and accessibility of underlying data and outputs

- Practical considerations for analysts
  - Use standardized temporal (daily) and spatial (1 km) resolution for trend analyses and policy evaluation
  - Compare FINNpeatSM emissions with non-peat fire emissions to assess peatland contributions
  - Leverage the restoration scenario to explore potential air quality and health co-benefits of peatland restoration
  - Ensure attribution to the MOZART4 species set when integrating with atmospheric chemical transport models

- Related outputs and availability
  - Emission data are organized per-fire with comprehensive species coverage
  - Emission outputs are suitable for integration into atmospheric chemistry models and health impact assessments
  - Archival references provide methodological transparency and context for replication or scenario testing