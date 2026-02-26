# Hydroscape chlorophyll abs data

## Purpose and scope
- Dataset documents chlorophyll absorbance measurements collected from multiple water bodies (lakes, streams, and rivers) for a hydroscape study.
- Includes two main data streams: PHYT (phytoplankton bioassays) and PERI (periphyton samples from nutrient diffusing periphytometers).
- Data are intended to support map-based visualization and spatial analysis of chlorophyll-related primary production indicators.

## Sampling design and sites
- Sampling focused on deepest points in lakes and selected river/stream locations, with detailed site names and coordinates provided.
- Surface water samples collected using long-handled poles from designated depths and distances from banks (varied by site type).
- Periphyton filters obtained from diffusing periphytometers deployed in streams for approximately two weeks, then retrieved and frozen.
- Water samples for PHYT bioassays were incubated with treatment combinations to assess nutrient effects.

## Laboratory processing and measurements
- PHYT samples: water filtered to remove grazers/debris, then distributed into tubes with nutrient treatments (P, N, N+P, ammonium, silica, and controls) at specified concentrations; incubated for several days at around ambient incubation temperatures.
- Post-incubation, contents resuspended and filtered onto GF/C filters; samples frozen for analysis.
- PERI samples: periphyton filters collected from nutrient diffusing devices and also subjected to analysis after incubation.
- Absorbance measurements obtained using a UV-Vis spectrophotometer at multiple wavelengths (632 nm, 652 nm, 665 nm, 696 nm, 750 nm) with a methanol baseline correction, auto-zero, and blank subtraction.

## Data structure and attributes
- The dataset comprises 16 data headers describing each record, including:
  - System: group of sites
  - Site: site name
  - Algae: bioassay type (PHYT or PERI)
  - Deployment: order of seasonal deployments (1–4; 0 for trial)
  - DateStart / DateStop: incubation period dates
  - Vol_or_Area: volume (ml) for PHYT or area (cm2) for PERI
  - DataFlag: data quality indicator (1 = known issue, 0 = none)
  - DOSE: nutrient treatment level (0–6; codes differ for PHYT vs PERI)
  - REPLICATE: replicate identifier (e.g., a–c; sometimes a–d)
  - 632nm, 652nm, 665nm, 696nm, 750nm: absorbance readings
  - Dilution_factor: dilution correction (1 = no dilution, 2 = 50% dilution)
- Site names and precise coordinates (Eastings/Northings) are provided for spatial referencing.

## Quality control
- Triplicate measurements for each treatment.
- Baseline wavelength scans performed before absorbance readings; instrument auto-zeroed with methanol as reference.
- Blank corrections applied to absorbance values.

## Spatial coverage and coordinates
- Site list includes multiple lakes, lochs, tarns, streams, and bays with corresponding Eastings and Northings.
- Spatially explicit data enable GIS-based mapping of chlorophyll absorbance across the study area (e.g., Bassenthwaite Lake, Derwentwater, Wroxham Broad, Esthwaite Water, Grasmere, and others).

## GIS considerations and usage
- Data are suitable for joining with spatial layers (sites, hydrology, land use) to map spatial patterns of chlorophyll absorbance and inferred primary production.
- Mixed data types (PHYT and PERI) may require standardization prior to GIS analysis.
- Data gaps and variable resolutions (different site types and deployment counts) should be accounted for in spatial analyses.

## Limitations and notes
- Some fields contain garbled text in the original methods description; the core structure includes detailed sampling, treatment, and wavelength measurements.
- The “Known issues with data” flag indicates data quality considerations at the record level; users should consult DataFlag for each entry.
- Exact incubation durations and certain parameter units may require confirmation from the data dictionary or accompanying metadata.