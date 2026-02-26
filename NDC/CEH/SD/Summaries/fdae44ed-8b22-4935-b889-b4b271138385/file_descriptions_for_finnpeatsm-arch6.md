# Fire emissions data for Southeast Asian fires for 2004, 2006, 2009, 2012, 2014 and 2015. The files cover the area from 15°S to 15°N and from 95°E to 125°W

- Overview
  - Provides fire emission data for Southeast Asia for six years (2004, 2006, 2009, 2012, 2014, 2015) over a defined geographic extent.
  - Two file types available: FINNpeatSM (FINNpeatSM_SEAS_YYYY_MOZ4.txt) and FINNpeatSM after restoration (FINNpeatSM_SEAS_after_restoration_YYYY_MOZ4.txt).
  - Data structure and variables align with the FINNv1.5 MOZART4 emissions framework.

- FINNpeatSM emissions (peat-aware)
  - Based on the Fire Inventory from NCAR (FINNv1.5) with added peat-fire emissions.
  - Fire detections on peat are identified via a peatland map (WRI); peat emissions computed as Es = BA × BD × ρ × EFs.
  - Malaysian peat fires are not included.
  - Assumptions
    - For peat areas: burned area per hotspot set to 40 ha.
    - Peat density set to 0.11 g/cm3 (source consensus from multiple studies).
    - Burn depth varies with soil moisture (derived from ESA CCI SM v04.4), averaged to 2° resolution; valid range mapped to 0.15–0.25 m3/m3 soil moisture, yielding burn depths from ~5 cm to ~37 cm.
    - Species emission factors (EFs) drawn from multiple studies; representative values used: CO2 1670 g/kg, PM2.5 22.3 g/kg, OC 11.5 g/kg, BC 0.07 g/kg.
  - Emission timing: emissions released on the day the fire is detected; no long-term smouldering contributions.

- FINNpeatSM after restoration (scenario)
  - Simulates a scenario where 2.49 million hectares of Indonesian peatland have been restored.
  - Method: reduce burned area to match observed reductions in peatland burning within Kalimantan national parks and increase soil moisture accordingly; emissions re-calculated using the same method as FINNpeatSM.
  - Purpose: illustrate potential emissions reductions from peatland restoration.
  - Important note: these are not real events; intended for scenario analysis and described in Kiely et al. (2021).

- File structure and variables
  - Format mirrors FINNv1.5 with MOZART4 spec; each file contains:
    - DAY: Julian day
    - TIME: UTC observation time
    - GENVEG: Generic vegetation type at fire location
    - LATI, LONGI: coordinates
    - AREA: burned area (m2)
    - Emissions for multiple species per day per fire, including CO2, CO, H2, NO, NO2, SO2, NH3, CH4, NMOC, and a wide set of VOCs and PM components (e.g., PM25, OC, BC, PM10, etc.)
  - Extensive list of species-level emissions (e.g., C2H4, C2H5OH, C2H6, C3H6, C3H8, CH2O, CH3CHO, CH3COCH3, CH3COCHO, CH3OH, TOLUENE, etc.) and large set of trace gases and particulates.
  - File references and emissions factors are anchored to a broad literature base (e.g., Akagi et al., Christian et al., Kiely et al., and others).

- Data quality, scope, and caveats
  - Peat emissions are computed with specific assumptions (area per hotspot, density, moisture-influenced burn depth) and do not include Malaysian peat fires.
  - The restoration scenario does not reflect real-world events; it is a modeled scenario intended to explore emissions reductions from peatland restoration.
  - Outputs are provided at daily resolution per fire event, enabling integration into atmospheric modeling or cross-dataset analyses.
  - The dataset is designed to be self-serve for data users needing high-resolution Southeast Asian fire emissions and to support comparative analyses with and without peatland restoration.

- Usage and integration notes
  - Aligns with FINNv1.5 MOZART4 specifications, facilitating integration with existing emission inventories and atmospheric chemistry models.
  - Suitable for data products that require per-fire and daily emission profiles, regional attribution, or scenario analyses related to peatland management.
  - Users should cite Kiely et al. (2019, 2020) for the FINN-based methodology and Kiely et al. (2021) for the restoration scenario context.