# Supporting information Fire emissions data for Southeast Asian fires for 2004, 2006, 2009, 2012, 2014 and 2015.

## Overview
- Provides fire emissions data for Southeast Asia for the years 2004, 2006, 2009, 2012, 2014 and 2015.
- Geographic extent: 15°S to 15°N and 95°E to 125°W.
- Two file types: FINNpeatSM_SEAS_YYYY_MOZ4.txt and FINNpeatSM_SEAS_after_restoration_YYYY_MOZ4.txt.
- Emissions are based on the Fire Inventory from NCAR (FINNv1.5) with added peat-fire emissions; designed for use in atmospheric models at 1 km resolution.

## Emissions data types and methodology
- Finite annual and daily fire emissions are derived from FINNv1.5 data (active fires, biomass burned, emission factors).
- Peat-fire emissions are added using: E_s = BA × BD × ρ × EF_s, where:
  - E_s = emissions of species s
  - BA = burned area
  - BD = burn depth
  - ρ = peat density
  - EF_s = emission factor for species s
- Malaysian peat fires are not included.
- For peat-defined areas, assume all peat within the burned area and depth combusts.
- Peat-specific parameters:
  - Burned area: 40 ha per hotspot for peat, smaller than 100 ha for vegetation fires (FinNv1.5 basis).
  - Peat density: 0.11 g/cm³ (average from multiple sources).
  - Burn depth: function of soil moisture; range 0.15–0.25 m³/m³, linearly scaling from 5 cm (moisture 0.25) to 37 cm (moisture 0.15).
  - Emission factors (average from multiple studies): CO2 1670 g/kg, PM2.5 22.3 g/kg, OC 11.5 g/kg, BC 0.07 g/kg.
- Emissions are assigned on the day the fire was detected, with no long-term smouldering effects.
- References for emissions factors and methods are provided within the document.

## FINNpeatSM after restoration
- Provides emissions for a scenario in which 2.49 million hectares of Indonesian peatland have been restored.
- Restoration scenario approach:
  - Identify top-emitting peatland areas (largest 2004–2015 fire emissions) for restoration.
  - Reduce burned area to match the average reduction seen in Kalimantan national parks.
  - Increase soil moisture by the observed Kalimantan parks’ average.
  - Recalculate emissions using the same FINNpeatSM methodology.
- Important caveats:
  - These emissions do not reflect real fires; they illustrate potential outcomes of restoration (as described in Kiely et al., 2021).

## File structure and variables
- Structure mirrors FINNv1.5 with MOZART4 speciation.
- Format: header line with variable names, followed by one row per fire.
- Key variables include:
  - DAY (Julian day), TIME (UTC), GENVEG (vegetation type), LATI, LONGI (coordinates)
  - AREA (m² burned)
  - Emissions by species (CO2, CO, H2, NO, NO2, SO2, NH3, CH4, NMOC, BIGALD, BIGALK, BIGENE, C10H16, C2H4, C2H5OH, C2H6, C3H6, C3H8, CH2O, CH3CHO, CH3COCH3, CH3COCHO, CH3COOH, CH3OH, CRESOL, GLYALD, HYAC, ISOP, MACR, MEK, MVK, HCN, CH3CN, TOLUENE, PM25, OC, BC, PM10, HCOOH, C2H2)
- Emission units include moles per day for most gases and kg/day for PM-related species.

## Data usage notes
- The FINNpeatSM data provide high-resolution (1 km) daily emissions suitable for atmospheric modelling and impact assessments.
- The after-restoration data enable scenario analyses of restoration benefits on emissions.
- Data sources and method details are linked to an extensive set of peer-reviewed references.

## Limitations and caveats
- Excludes Malaysian peat-fire emissions in the peat-fire component.
- Peat properties (density, burn depth, moisture-based scaling) rely on literature-based defaults and regional calibration.
- The restoration scenario is a simulated, not real-world, scenario intended for impact assessment.
- File comments indicate the need to treat these as model inputs rather than observed events.

## References and related work
- Key methodological and context references include Kiely et al. (2019, 2020, 2021), Christian et al. (2003), Hatch et al. (2015), Stockwell et al. (2016), Jayarathne et al. (2018), and others cited in the document.
- Emission factors and validation efforts against biomass burning and peat-fire studies are summarized within the file and associated references.