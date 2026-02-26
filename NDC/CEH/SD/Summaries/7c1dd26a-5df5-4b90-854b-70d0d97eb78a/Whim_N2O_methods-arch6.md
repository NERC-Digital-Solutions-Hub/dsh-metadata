# Nitrous oxide emissions from a peatbog after thirteen years of experimental nitrogen deposition - Materials and methods

- Long-term field experiment conducted at Whim bog, Scottish Borders, UK, to study how nitrogen deposition affects nitrous oxide (N2O) emissions from peatland. The site features deep peat, acidic conditions (pH ~3.4), and a mosaic vegetation community. Temperature and rainfall statistics are provided for context (2003–2009 means: air 8.6°C, soil 7.7°C; rainfall ~1092 mm).

- Experimental design
  - Dry deposition system: ammonia (NH3) released from a free-air release system to create an NH3 deposition gradient downwind. Emission was selectively active under specific wind directions, temperatures above freezing, and wind speeds above 2.5 m/s.
  - Wet deposition system: replicated plots receiving dissolved NH4+ or NO3− via rainfall-like spray. Four blocks with one treatment level per block, totaling 28 plots across three target total N deposition rates (16, 32, 64 kg N ha−1 y−1) plus ambient-control (8 kg N ha−1 y−1).
  - Treatments began in 2002 and operated year-round except near freezing.
  - NH3 exposure profile established via passive samplers at multiple distances (0.1 m above vegetation; 8–60 m downwind) and across vertical/horizontal gradients; deposition interpolated with ordinary kriging assuming homogeneous deposition velocity.

- Data collection and measurements
  - Soil water chemistry: monthly soil water samples from dipwells across plots; NH4+ and NO3− measured by ion chromatography; detection limits 0.014 mg L−1 (NH4+-N) and 0.062 mg L−1 (NO3−-N). Vegetation percent cover recorded within chamber locations periodically.
  - Greenhouse gas exchange: N2O fluxes measured using static chambers (38 cm diameter, ~25 cm high) inserted into peat; sampling typically monthly. Four 20-ml samples collected per chamber, stored for analysis.
  - Lab analysis: gas samples analyzed with a GC (HP 5890 II) with standard gases for calibration.
  - Calibration and quality control: four-point calibration for mole fractions; standards run roughly every 20 samples. Flux calculation uses initial concentration change and chamber geometry with the formula F = (dC/dt0) × (ρV/A). Multiple regression approaches (linear, quadratic, asymptotic, and other models) applied to time-series data to determine dC/dt0; the best-fit regression method selected per measurement to account for non-linearity; time resolution (~10 minutes) may still underestimate fluxes in some cases.

- Data processing and analysis
  - Primary statistical framework: linear mixed-effects models to relate soil N2O fluxes to environmental drivers and deposition rates, with random effects for chamber location nested within experimental blocks.
  - Fixed-effect predictors include soil temperature, soil-water depth, NH3 deposition rate, NH4+ deposition rate, and NO3− deposition rate.
  - Data handling includes removal of outliers and reporting of model fits with associated uncertainty measures.

- Data products and structure (files)
  - ancilliaryData-byChamber.csv: per-chamber metadata and flux totals (e.g., Fnh3, Fnh4, Fno3, Ndep-total), chamber codes, block/plot information, geographic coordinates.
  - ancilliaryData-byChamber-byDate.csv: chamber-by-date metadata linked to raw data, including gas-name (N2O), filenames, dates, and flux-related fields (Fnh3, Fnh4, Fno3, Ndep-total), plus environmental covariates (Tair, Tsoil, WT depth).
  - RCfluxOutput.csv: flux estimates for each chamber/date computed by multiple models (linear, quadratic, asymptotic, HMR, best-fit); includes confidence intervals, R2 metrics, and a code for the best-fit method.
  - vegetation-speciesPercentCover-Whim-byChamber.csv: percent cover data per species within each chamber (and possibly monthly data for vegetation-related metrics).
  - chemistry-NH4mgNperl-Whim-byChamber-byDate.csv: soil water ammonium concentrations by chamber and date.
  - chemistry-NO3mgNperl-Whim-byChamber-byDate.csv: soil water nitrate concentrations by chamber and date.
  - chemistry-pH-Whim-byChamber-byDate.csv: soil water pH by chamber and date.
  - Figure 1: layout of N deposition plots (plan.pdf) illustrating experimental design.

- Key variables and units
  - Fluxes: N2O fluxes (various representations across models) in nmol N2O m−2 s−1.
  - Environmental drivers: soil temperature (Tsoil, °C), air temperature (Tair, °C), water-table depth (WTdepth, cm).
  - Nitrogen deposition: FNH3 (NH3 flux, kg N ha−1 y−1), FNH4 (NH4+ flux, kg N ha−1 y−1), FNO3 (NO3− flux, kg N ha−1 y−1), Ndep-total (total N deposition, kg N ha−1 y−1).
  - Gas sampling and data: chamber codes, Plot and SubPlot identifiers, coordinates (lon, lat), and block/experimental design metadata.
  - Vegetation and soil chemistry: species percent cover, NH4+ and NO3− concentrations (mg N L−1) in soil water, and pH of soil water.

- Data quality, limitations, and uncertainty
  - Flux estimates rely on models to estimate dC/dt0; non-linearity accounted for via regression selection, but the ~10-minute sampling cadence may underrepresent some non-linear flux dynamics.
  - Outliers removed from flux dataset prior to analysis (specific thresholds noted).
  - Uncertainty in deposition-velocity assumptions and spatial interpolation (kriging) acknowledged as part of the data interpretation.

- Access, context, and references
  - The dataset accompanies a peer-reviewed methods paper detailing the experimental setup, measurement approaches, calibration, and analysis framework.
  - References provide foundational methods for dry/wet deposition, chamber flux measurements, calibration procedures, and flux uncertainty analysis.
  - A figure (plan.pdf) maps the experimental layout and treatments.

- Relevance to data support goals
  - Demonstrates end-to-end data workflow: from field deposition treatments and in situ gas flux measurements to laboratory analyses, data curation, and multi-model flux estimation.
  - Provides comprehensive metadata and structured data files suitable for re-use, meta-analysis, or integration with other long-term peatland N deposition studies.
  - Highlights data-quality considerations, uncertainty quantification, and the need to understand Ask-what data is needed, data formats, and reproducible analysis for end users.