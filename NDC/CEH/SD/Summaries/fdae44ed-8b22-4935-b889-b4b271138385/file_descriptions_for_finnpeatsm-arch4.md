# Supporting information Fire emissions data for Southeast Asian fires for 2004, 2006, 2009, 2012, 2014 and 2015. The files cover the area from 15°S to 15°N and from 95°E to 125°W

## Data products and coverage
- Two file types:
  - FINNpeatSM_SEAS_YYYY_MOZ4.txt
  - FINNpeatSM_seas_after_restoration_YYYY_MOZ4.txt
- Coverage: Southeast Asia, 15°S to 15°N and 95°E to 125°W
- File structure and variables match FINNv1.5 MOZART4 speciation

## Data origin and methodology
- Based on the Fire Inventory from NCAR (FINN v1.5) with added peat-fire emissions
- Spatial and temporal resolution: daily emissions at 1 km resolution
- Peat-fire detection:
  - Detections identified as peat using a peatland distribution map (WRI)
  - Additional peat-emission calculations for detected peat fires
- Emissions on the day of fire detection; no long-term smoldering effects
- Malaysian peat fires are not included

## Peat emission calculation details
- Emissions for peat fires: Es = BA × BD × ρ × EFs
  - Es: emissions of species s (mole/day)
  - BA: burned area
  - BD: burn depth (dependent on soil moisture)
  - ρ: peat density (0.11 g/cm3, from multiple literature sources)
  - EFs: emission factors for species s
- Assumptions for peat areas:
  - Burned area per peat hotspot: 40 ha
  - Burn depth scales with soil moisture (ESA CCI SMv04.4), using an average of 0.25 to 0.15 m3/m3 soil moisture
  - Burn depth range: 5 cm (moisture 0.25) to 37 cm (moisture 0.15)
- Emission factors (average values used):
  - CO2: 1670 g kg⁻¹
  - PM2.5: 22.3 g kg⁻¹
  - OC: 11.5 g kg⁻¹
  - BC: 0.07 g kg⁻¹
- Key references for EF values include Christian et al. (2003), Hatch et al. (2015), Stockwell et al. (2016), Nara et al. (2017), Wooster et al. (2018), among others

## FINN peat SM after restoration scenario
- Scenario: 2.49 million hectares of Indonesian peatland restored
- Restoration logic:
  - Areas chosen as those with the greatest 2004–2015 fire emissions
  - Simulated by reducing recorded burned area to match average reductions seen in Kalimantan national parks and increasing soil moisture accordingly
  - Recomputed emissions using the same method as FINNpeatSM
- Important note: These emissions do not reflect real-life fires; intended for scenario analysis as described in Kiely et al. (2021)

## File structure and variables
- Structure and variable naming mirror FINNv1.5 with MOZART4 speciation
- Data sections include:
  - DAY: Julian day
  - TIME: UTC time of observation
  - GENVEG: Generic vegetation type where fire occurred
  - LATI / LONGI: Location (decimal degrees)
  - AREA: Area burned (m2)
  - Emissions for multiple species per day, including:
    - CO2, CO, H2, NO, NO2, SO2, NH3, CH4
    - PM25, OC, BC, PM10
    - Numerous NMOC and VOCs (e.g., C2H4, ISOP, MACR, MEK, TOLUENE, etc.)
- All emissions reported as mole/day or kg/day as appropriate per species

## Data quality, limitations, and scope
- Region-limited dataset to Southeast Asia; does not cover all global peat fires
- Malaysia peat fires are excluded
- Uncertainties in:
  - Peat-specific emission factors and burn-depth estimates
  - Peat density assumption
  - Burn-depth calculation from soil moisture (ESA SM v04.4)
- Shortcoming for generalization beyond the given years and regions
- Restoration scenario is a modeling construct, not observational data

## Usage and considerations for data leaders
- Useful for:
  - Integrating peat fire emissions into regional air-quality or climate analyses
  - Scenario planning to assess potential air-quality and health benefits of peatland restoration
  - Cross-referencing with other datasets that use MOZART4-species inventories
- Good practice:
  - Treat FINNpeatSM results as model-based emissions with stated assumptions
  - Clearly separate real-fire data from restoration-scenario outputs in analyses
  - Align metadata and documentation with MOZART4 formats for discoverability and interoperability
- Data provenance and citations include Kiely et al. (2019, 2020, 2021) and supporting literature for emission factors and peat properties

## References and provenance (selected)
- Kiely et al. 2019; Kiely et al. 2020; Kiely et al. 2021
- Christian et al. 2003; Hatch et al. 2015; Stockwell et al. 2016; Nara et al. 2017; Wooster et al. 2018
- Additional climate and soil moisture sources (ESA CCI SMv04.4; Driessen & Rochimah 1976; Gruber et al. 2017; Liu et al. 2019; etc.)