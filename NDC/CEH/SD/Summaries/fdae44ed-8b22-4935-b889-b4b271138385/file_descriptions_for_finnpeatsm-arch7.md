# Fire emissions data for Southeast Asian fires for 2004, 2006, 2009, 2012, 2014 and 2015. The files cover the area from 15°S to 15°N and from 95°E to 125°W

- Scope and data types
  - Provides Southeast Asian fire emissions data for the years 2004, 2006, 2009, 2012, 2014 and 2015
  - Area covered: 15°S to 15°N and 95°E to 125°W
  - Two file types:
    - FINNpeatSM_emissions (FINNpeatSM_SEAS_YYYY_MOZ4.txt)
    - FINNpeatSM after restoration (FINNpeatSM_SEAS_after_restoration_YYYY_MOZ4.txt)
  - Based on FINN v1.5 with MOZART4 speciation; emissions are provided per fire event with a header and a row for each fire

- Geographic and temporal scope
  - Region-focused dataset for Southeast Asia
  - Temporal resolution: daily emissions per fire hotspot
  - Emissions exist for six years (2004, 2006, 2009, 2012, 2014, 2015)

- Peat-fire emphasis and emissions calculation
  - Peat-fire emissions added to the standard FINNv1.5 framework
  - Peat-specific parameters:
    - Burned peat area per hotspot: 40 hectares (peats) vs. 100 ha for vegetation fires in FINNv1.5
    - Peat density: 0.11 g/cm3
    - Burn depth varies with soil moisture; averaged to 2° resolution using ESA CCI SM data
    - Burn depth range: 5 cm (moisture 0.25) to 37 cm (moisture 0.15)
  - Assumptions for peat areas:
    - Assumes the entire burned peat area and depth combusted
    - Malaysian peat fires are explicitly not included
  - Emission factors for peat fires (average EFs from multiple studies):
    - CO2: 1670 g/kg
    - PM2.5: 22.3 g/kg
    - OC: 11.5 g/kg
    - BC: 0.07 g/kg
  - Emissions for non-peat components follow FINNv1.5 methodology

- Restoration scenario (FINNpeatSM after restoration)
  - Simulates restoration of 2.49 million hectares of Indonesian peatland
  - Reduces recorded burned area to reflect average reductions seen in Kalimantan national parks
  - Increases soil moisture by the average moisture increase seen in Kalimantan parks
  - Recalculates emissions using the same peat-fire method
  - Important: these emissions are not real-fire estimates; intended for scenario analysis per Kiely et al. (2021)

- File structure and variables
  - Structure mirrors FINNv1.5 with MOZART4 speciation
  - Each file has:
    - A header line with variable names
    - One row per fire event
  - Core variables (examples):
    - DAY: Julian day of year
    - TIME: Observation/satellite overpass UTC time
    - GENVEG: Generic vegetation type at fire location
    - LATI / LONGI: Latitude and longitude (decimal degrees)
    - AREA: Area burned (m2)
    - Emissions per species (moles/day): CO2, CO, H2, NO, NO2, SO2, NH3, CH4, NMOC, BIGALD, BIGALK, BIGENE, C10H16, C2H4, C2H5OH, C2H6, C3H6, C3H8, CH2O, CH3CHO, CH3COCH3, CH3COCHO, CH3COOH, CH3OH, CRESOL, GLYALD, HYAC, ISOP, MACR, MEK, MVK, HCN, CH3CN, TOLUENE
    - Particles: PM25 (kg PM2.5/day), OC (kg/day), BC (kg/day), PM10 (kg/day)
    - Other species: HCOOH, C2H2, etc.
  - Data units:
    - Emissions by day per fire are in moles/day (gas species)
    - PM2.5, OC, BC, PM10 are in kg/day

- How to use in GIS
  - Per-fire, per-day event data with precise location (LAT/LONG) and timing (DAY/TIME)
  - Suitable for mapping fire emission sources, emissions intensity, and spatial-temporal analyses
  - Can be joined with peatland maps, soil moisture layers, and land cover data to explore drivers and impacts
  - The GENVEG field allows filtering by vegetation type to refine visualisations
  - The two file variants enable scenario comparisons (baseline FINNpeatSM vs. restoration scenario)

- Data provenance and references
  - Core methodology and emissions approach described in Kiely et al. (2019, 2020)
  - Restoration scenario detailed in Kiely et al. (2021)
  - Supporting emissions factors and sources include: Akagi et al. 2011; Andreae & Merlet 2001; Christian et al. 2003; Dorigo et al. 2017; and others (referenced in metadata)

- Important caveats
  - Malaysian peat fires are not included in this dataset
  - The restoration scenario does not reflect real events; it is a modeled scenario for evaluating potential emissions reductions
  - Emissions are released on the day of fire detection; there is no long-term smouldering component in these files
  - Spatial resolution and assumptions are tied to peatland distributions and ESA soil moisture products; uncertainties exist due to data sources and simplifications

- Key takeaways for GIS specialists
  - Two complementary datasets: current peat-fire emissions and a restoration-based scenario
  - Rich per-fire, per-day emissions data with comprehensive species coverage
  - Ideal for creating map-based visualisations of peat-fire emissions across Southeast Asia and for scenario planning related to peatland restoration
  - Aligns with MOZART4 speciation and FINNv1.5 structure, enabling integration with broader atmospheric and land-surface datasets