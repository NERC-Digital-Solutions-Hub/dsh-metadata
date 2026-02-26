# Nitrous oxide emissions from a peatbog after thirteen years of experimental nitrogen deposition - Materials and methods

## Overview
- describes the field site, experimental design, data collection, instrumentation, calibration, and data products for a long-term N deposition experiment on nitrous oxide (N2O) flux and related soil/vegetation variables.
- focuses on the methods used to apply nitrogen, collect soil‑water chemistry and gas flux data, and produce multiple data products suitable for GIS and spatial analysis.

## Field site and experimental layout
- Location: Whim bog, Scottish Borders, UK; transition between lowland raised bog and blanket bog.
- Peat: 3–6 m deep; very acidic (pH ~3.4).
- Climate/conditions: mean air/soil temperatures ~8.6°C/7.7°C (2003–2009), annual rainfall ~1092 mm, water table near surface in hollows.
- Vegetation: Calluna vulgaris–Eriophorum vaginatum blanket mire with mosaics of Calluna, Sphagnum spp., Erica tetralix, and mosses.
- Spatial design: 72 chamber locations arranged across plots; experimental grid includes Wet, Dry, and Ozone conditions (per Table 2 and Figure 1).
- Coordinates: each chamber has recorded longitude and latitude.

## Experimental treatments
- Dry deposition ( NH3): free-air release system releasing NH3 from a 10 m pipe; active under SW wind direction (180–215°), above-freezing temperatures, wind speed >2.5 m s-1.
  - Gradient downwind measured with passive samplers at 0.1 m above vegetation at 8–60 m from source.
  - Deposition calculated from concentration measurements and interpolated across the area using ordinary kriging, assuming spatially homogeneous deposition velocity.
- Wet deposition (NH4+ and NO3−): randomized block design with four blocks.
  - Four treatment levels (including ambient control) to achieve total N deposition of 16, 32, 64 kg N ha-1 y-1, plus ambient 8 kg N ha-1 y-1.
  - NH4Cl or NaNO3 solutions sprayed on plots using a centralized sprayer system; about 120 applications per year.
  - Treatments applied to 28 plots (seven plots per block across four blocks).

## Data collection methods

### Soil water chemistry
- Timing: soil water samples collected with dipwells concurrently with gas flux measurements.
- Analytes: NH4+ and NO3− concentrations by ion chromatography; detection limits ~0.014 mg L−1 (NH4+-N) and ~0.062 mg L−1 (NO3−-N).
- Vegetation data: percent cover of species recorded within each chamber location at intervals of a few years.

### Greenhouse gas exchange (N2O)
- Method: static chamber technique (Hutchinson & Mosier 1981).
- Chamber setup: PVC collars (38 cm diameter, ~25 cm high) installed in peat; lids sealed for 30–40 minutes per sampling.
- Sampling: four 20 mL gas samples per chamber per occasion.
- Frequency: typically monthly.
- Analysis: gas chromatograph (HP 5890 II) with standard reference gases.

## Instrumentation, calibration, and quality control

- Calibration: 4-point calibration using standards with mole fractions 0.199, 0.285, 0.490, 0.975 μmol mol−1; standards run ~every 20 samples.
- Flux calculation: F = (dC/dt0) × (ρV)/A, where dC/dt0 is the initial concentration change rate, ρ is air density, V is chamber volume, A is ground area.
- Data processing: dC/dt0 estimated using linear and non-linear (asymptotic) regression; best-fit method chosen based on fit statistics and visual inspection.
- Uncertainty: time resolution ~10 minutes; potential underestimation of fluxes due to non-linearity not fully captured.
- Statistical approach: linear mixed-effects models to relate N2O flux to soil temperature, water table depth, and N deposition (NH3, NH4+, NO3−), with random effects for chamber location within blocks.

## Nature and units of recorded values / data products

- Ancillary data by chamber (Table 2): ChamberID, chamberCode, ExperimentalGrid (Wet/Dry/Ozone), deposition form (Wet/Dry), BlockID, PlotNumber, SubPlotNumber, longitude, latitude, deposition fluxes (Fnh3, Fnh4, Fno3), total N deposition (Ndep-total).
- Ancillary data by chamber by date (Table 3): chamberCode, date, Tair, Tsoil, WTdepth (water table depth), Fnh3, Fnh4, Fno3, Ndep-total, and location identifiers.
- RCfluxOutput (Table 4): flux estimates by multiple models (linear, quadratic, asymptotic, HMR, best-fit) and associated statistics (confidence intervals, adjusted R², best-fit method code).
- Vegetation percent cover (Table 5): per-chamber percent cover for each species (e.g., Calluna vulgaris, etc.).
- Soil chemistry by date (Tables 6–8): chemistry NH4 (mg N L−1), NO3 (mg N L−1), and soil water pH by chamber and date.
- Figure 1: layout of N deposition plots (plan.pdf).

## GIS and spatial analysis considerations

- Spatial data points: 72 chambers with precise lon/lat coordinates; plots organized into 28 treatment plots within 4 blocks.
- Deposition surfaces: dry NH3 deposition modeled with kriging; wet deposition applied discretely but linked to chamber locations.
- Data integration: link gas flux (N2O) and soil chemistry to chamber geolocations and to time-stamped environmental variables (Tair, Tsoil, WTdepth).
- Potential GIS workflows:
  - Create point features for each chamber with N2O flux and soil chemistry attributes per date.
  - Develop interpolation surfaces (e.g., deposition fields, flux surfaces) for visualization of spatial patterns.
  - Overlay vegetation composition and soil chemistry to explore spatial associations with N2O flux.
  - Analyze treatment effects spatially by aggregating by ExperimentalGrid (Wet/Dry/Ozone) and Block/Plot.

## How to use this dataset effectively

- Build a geospatial dataset of chamber locations with associated fluxes (N2O) and deposition inputs (NH3, NH4+, NO3−) across time.
- Combine with soil temperature, water table depth, and vegetation cover to assess spatial drivers of N2O flux.
- Compare model outputs (linear, quadratic, asymptotic, HMR, best-fit) to identify robust spatial patterns and uncertainties.
- Use ancillary data to contextualize flux measurements with site conditions and deposition regimes.

## Limitations and considerations

- Spatial interpolation for dry NH3 deposition assumes homogeneous deposition velocity, which may introduce uncertainty in surfaces away from the source.
- Temporal resolution of gas flux measurements (monthly to several times per month) may affect detection of short-term flux dynamics.
- Data gaps or irregular sampling may exist in certain dates or chambers; ensure alignment of date fields across tables when linking datasets.