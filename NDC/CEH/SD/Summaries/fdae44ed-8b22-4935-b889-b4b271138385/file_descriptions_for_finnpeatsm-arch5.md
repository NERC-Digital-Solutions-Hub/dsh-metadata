# Supporting information Fire emissions data for Southeast Asian fires for 2004, 2006, 2009, 2012, 2014 and 2015. The files cover the area from 15°S to 15°N and from 95°E to 125°W

## Summary
- Provides fire emission datasets for Southeast Asian fires across six years, including peat-fire contributions and a restored-peatland scenario.
- Geographic extent: 15°S to 15°N, 95°E to 125°W; data aligned with MOZART4 species emission structure.
- Two file types per year: original FINNv1.5-based emissions with peat additions, and a restoration scenario variant.

## Data contents and purpose
- Emissions cover a wide range of species and pollutants:
  - Gases: CO2, CO, H2, NO, NO2, SO2, NH3, CH4
  - NMOCs and detailed VOCs: NMOC and numerous individual species (e.g., C2H4, C2H6, ISOP, MACR, MEK, TOLUENE, etc.)
  - Particulates: PM25, PM10, OC (organic carbon), BC (black carbon)
- Each fire record includes metadata for temporal and spatial context.
- Based on active-fire data with peat-fire additions using defined peat properties; Malaysian peat fires are explicitly excluded.

## File types and structure
- FINNpeatSM emissions: FINNpeatSM_SEAS_YYYY_MOZ4.txt
- After-restoration scenario: FINNpeatSM_SEAS_after_restoration_YYYY_MOZ4.txt
- Structure: identical to FINNv1.5 with MOZART4 speciation
  - Header line with variable names
  - One row per fire
- Core variables (sampled per fire):
  - DAY (Julian day), TIME (UTC)
  - GENVEG (vegetation type), LATI, LONGI
  - AREA (burned area in m2)
  - Emissions for each species (in moles/day for gases; kg/day for NMOC, PM2.5, OC, BC)
  - Additional species-specific columns listed in the dataset

## Variables and units
- Spatial/temporal: DAY, TIME, LATI, LONGI
- Fire size: AREA (m2)
- Emissions (example units):
  - CO2, CO, H2, NO, NO2, SO2, NH3, CH4, C2H4, C2H6, ISOP, MACR, MEK, MVK, TOLUENE, etc. (moles/day)
  - PM25, PM10, OC, BC (kg/day)
  - Numerous VOCs and NMOC species with mole or kg/day units as appropriate
- Bibliographic alignment: MOZART4 speciation codes used for emissions output

## Methodology and key assumptions
- Basis: Fire emissions from the NCAR Fire Inventory (FINN, v1.5) with added peat-fire emissions.
- Peat-fire emissions calculation for each hotspot:
  - Es = BA × BD × ρ × EFs
  - BA: burned area, BD: burn depth, ρ: peat density
  - EFs: emission factor for species s
- Peat-specific assumptions:
  - Peat area burned per peat hotspot: 40 ha (versus 100 ha for vegetation fires in FINNv1.5)
  - Peat density: 0.11 g/cm3
  - Burn depth: moisture-dependent, derived from ESA CCI soil moisture; range 0.15–0.25 m3/m3 moisture, scaled linearly from 5 cm to 37 cm depth
  - Emission factors (average values): CO2 = 1670 g/kg, PM2.5 = 22.3 g/kg, OC = 11.5 g/kg, BC = 0.07 g/kg
- Emissions for peat fires released on the detection day; no long-term smoldering effects included
- File naming and structure mirror FINNv1.5 MOZART4 alignment to facilitate model use

## Data provenance and references
- Core methodology and emissions updates described in Kiely et al. 2019, 2020
- Restoration scenario details and limitations described in Kiely et al. 2021
- Supporting literature for emission factors and ancillary data (e.g., combustion emissions, peat properties, soil moisture datasets) cited within the dataset documentation

## Data quality, limitations, and caveats
- Malaysian peat-fire emissions are not included
- Peat-fire emissions rely on several literature-based parameters (density, burn depth, moisture estimates) with inherent uncertainty
- Restored-peat scenario is a hypothetical construct and should not be interpreted as observed reality
- Temporal resolution: emissions released on the day of fire detection; no residual smoldering or post-fire emissions beyond that day
- Some inputs (e.g., soil moisture and burn depth) are averaged at 2° resolution, which may mask finer-scale variability
- Data are intended for use with atmosphere/air-quality models (MOZART4) and require appropriate metadata handling

## Access, usage notes, and governance
- Data provide a well-documented, standards-aligned emissions dataset suitable for large-scale model assimilation
- Clear distinction between real-fire emissions and scenario-based restoration emissions; users should apply the restoration data only for scenario analyses
- Users should cite Kiely et al. (2019, 2020, 2021) as the primary methodological sources and Kiely et al. for restoration details
- The dataset adheres to a consistent naming convention and file structure to support reproducibility and data discovery

## Reproducibility and maintenance
- File structure and variable set are consistent with FINNv1.5 MOZART4 specifications to enable seamless integration into existing workflows
- Documentation provides explicit formulas and parameter choices for peat emissions, enabling re-computation or sensitivity analyses if required
- Ongoing maintenance would involve updating peat properties, emission factors, and restoration parameters as new studies become available