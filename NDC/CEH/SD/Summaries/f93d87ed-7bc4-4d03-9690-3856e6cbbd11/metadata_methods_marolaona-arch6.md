# Metadata and methods for the dataset: Hydrometric data and stable isotope data for streamflow and rainfall in the Marolaona catchment, Madagascar, 2015-2016

## Overview
- Study area: Marolaona catchment (31.7 ha) in the Ankeniheny Zahamena Corridor, eastern Madagascar.
- Timeframe: February 3, 2015 to March 3, 2016.
- Data types: hydrometric measurements (rainfall, streamflow, perched groundwater, soil moisture) and stable isotope analysis (δ18O, δ2H, and deuterium excess) of water samples.
- Objective: provide detailed metadata and methods to support data discovery, quality assessment, and reuse for hydrology and hydro-ecology analyses.

## Data components
- HydrometricData_Marolaona.csv
  - 5-minute interval data covering Feb 3, 2015 to Mar 3, 2016.
  - Measured variables include rainfall (downstream and upstream gauges), streamflow at downstream and upstream weirs, perched water tables, and volumetric soil moisture and temperature at three sites (TF2, EUC, TSF).
  - Perched water tables are reported as mm above the low-permeability layer located 300 mm below the surface.
  - Table 1 describes all columns, units, and explanations.
- IsotopeData_Marolaona.csv
  - Stable isotope samples (δ18O, δ2H, D-excess) from streamflow, overland/plot runoff, and rainfall.
  - Sampling locations and water types captured in Table 2.
  - δ-values referenced to Vienna Standard Mean Ocean Water (VSMOW) with stated precision: ±0.16‰ for δ18O and ±0.6‰ for δ2H.
  - Table 2 describes all columns, units, and explanations.

## Data collection and processing
- Rainfall
  - Two tipping-bucket gauges (0.2 mm tip; downstream and upstream) connected to HOBO loggers.
  - Installation: ~1.2 m above soil surface; data converted to 5-minute totals.
  - Issue: upstream gauge had battery failure July 1 to August 17, 2015.
- Hydrometric measurements
  - Streamflow: weirs at catchment outlet (31.7 ha) and upper catchment (7.11 ha).
  - Water-level observations at 5-minute intervals; two measurement methods across periods (Decagon CTD-10 and STS DL/N 70 sensor).
  - Rating curves derived from salt-dilution-slug-injection method and validated with bucket measurements; upper catchment rating uses truncated-triangular sharp-crested weir equations.
- Soil moisture and perched groundwater
  - Soil moisture: Decagon ECHO-EC-TM sensors at 5, 15, and 30 cm depths at TF2, EUC, and TSF plots; 1-minute logging with 5-minute averages.
  - Perched groundwater: three fully screened wells at 0.30 m depth at TF1, EUC, TSF (plus TF2 up the slope); water levels logged at 1-minute (CTD-10) and some sites at 5-minute (Keller DCX-18).
  - Sensor orientations and installation details specified (upslope distance from lower boundary, etc.).
- Isotope sampling and analysis
  - Water samples collected from streamflow (upstream of weirs) and overland flow at TF2, EUC, TSF; rainfall samples collected daily during Jan-Feb 2016, plus event-driven samples using a sequential sampler.
  - Amounts: 39 rainfall samples; 209 water samples from streams/plot runoff.
  - Isotope analysis performed with a CRDS instrument (Picarro L2130-i) at Freiburg; results in δ18O, δ2H, and D-excess.

## Temporal coverage and data quality notes
- Hydrometric data
  - Primary 5-minute hydrometric data window: 2015-02-03 to 2016-03-03.
  - Missing data indicated as NaN in the dataset.
  - Upstream rainfall data gap due to battery failure (2015-07-01 to 2015-08-17).
  - Two separate periods of complete stream level data (Feb 15–May 13, 2015; Dec 12, 2015–Mar 3, 2016) due to sensor availability.
- Isotope data
  - Isotope samples collected across rainfall, streamflow (outlet and upper sub-catchment), and overland flow with defined sampling dates and locations.
  - Reporting uses delta notation relative to VSMOW with published precision limits.

## Data formats, structure, and provenance
- CSV data files
  - HydrometricData_Marolaona.csv: structured with columns for Datetime, rainfall (down/up, amount and intensity), streamflow (down/up), perched water tables (TF2, EUC, TSF), soil moisture and temperature at all depths per site.
  - IsotopeData_Marolaona.csv: columns for Location, Water_type, DateTime, Delta18O, Delta2H, DEx.
- Column definitions and units are provided in Tables 1 and 2 within the document, enabling consistent interpretation and integration with other data sources.
- Provenance
  - Data collected by a collaboration of researchers from The Netherlands, Madagascar, New Zealand, and Switzerland.
  - Background methods and context referenced to Zwartendijk et al. (2020, 2023) for related hydrological dynamics in the same region.

## Potential uses and data products
- Combine hydrometric time series with isotope data to analyze rainfall-runoff processes, origin of streamflow, and subsurface storage dynamics in a tropical catchment with slash-and-burn land use.
- Develop self-serve data products (dashboards, pivot tables) for end users to explore rainfall, streamflow, soil moisture, and perched groundwater relationships.
- Cross-compare surface water and overland flow isotopic signatures to identify mixing processes and source areas within the catchment.
- Use the detailed measurement metadata to assess data quality, reproduce analyses, or integrate with complementary datasets.

## References
- Zwartendijk, B.W. et al. (2020, 2023): foundational studies on soil moisture, overland flow dynamics, and rainfall–runoff responses in the Marolaona catchment and related work cited for methods and context.
- Supporting methodological references for measurement techniques include standard IRR methods for streamflow rating curves and isotopic analysis instrumentation.