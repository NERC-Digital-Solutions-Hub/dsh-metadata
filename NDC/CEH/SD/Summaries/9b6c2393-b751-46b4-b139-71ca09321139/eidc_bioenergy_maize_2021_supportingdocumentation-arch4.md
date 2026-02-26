# Growing-season eddy covariance measurements of carbon dioxide, energy and water fluxes from a bioenergy maize crop, Yorkshire, UK, 2021

- Purpose and scope
  - Provides 30-minute observations of land–atmosphere exchange: net ecosystem CO2 exchange (NEE) and sensible (H) and latent heat (LE) fluxes over a bioenergy maize crop in Yorkshire, UK, during the 2021 growing season (02/06/2021–10/10/2021).
  - Includes weather and soil physics measurements to support ecological and meteorological analyses.

- Study site
  - Location: University of Leeds Research Farm (coordinates given in the dataset description).
  - Climate and soil context: temperate oceanic climate; well-drained loamy calcareous brown earth soil; soil pH 6.9; bulk density 1.3 g cm-3; 0–30 cm soil carbon 39.5 g kg-1 and nitrogen 2.3 g kg-1.
  - Management: rainfed arable field, maize planted 02/06/2021 at 110,000 seeds ha-1, harvested 10/10/2021; received 22.5 kg N ha-1 at planting.
  - Environment: long-term rotation since 1970; mean annual temperature ~9.5°C and ~885 mm precipitation (1992–2022).

- Measurements and instrumentation
  - Flux measurements: eddy covariance (EC) system with LI-7200RS CO2/H2O analyser and Gill Windmaster 3D sonic anemometer; sensor height adjusted over the season to maintain ≥2 m above canopy; data at 10 Hz, processed to 30-minute means.
  - Ancillary measurements: SN-500 net radiometer (Rnet, SWin, SWout, LWin, LWout); HMP155 temperature/humidity probe (Tair, RH); TEROS-11 soil temperature and moisture at 5 cm depth; all as 30-minute means.
  - Data processing: EddyPro 7 for flux calculations; includes conditioning, angle-of-attack correction, time-lag adjustment, and spectral correction; random uncertainty estimates following established methods.

- Data processing and quality control
  - Flux calculation and uncertainty: standardized processing and quality checks to ensure reliability of NEE, H, and LE.
  - Quality-control criteria: remove data based on statistical outliers, anomalously high LI-COR signal, footprint not representative of the site, implausible flux values (bounds for H, LE, NEE), and low friction velocity (u* < 0.14 m s-1).

- Gap-filling and flux partitioning
  - Gap-filling and partitioning of NEE performed with REddyProc (R package) using marginal distribution sampling.
  - Uncertainty in gap-filled values estimated as the standard deviation from the data used to fill gaps.

- Data structure and variables
  - Primary file: Yorkshire_Bioenergy_Maize_GS_2021.csv.
  - Data columns include:
    - NEE and NEE_unc; LE and LE_unc; H and H_unc; Tau and Tau_unc (momentum flux); CO2_strg, LE_strg, H_strg (storage terms); Pa (barometric pressure); Tair; RH; VPD; SWin, SWout; LWin, LWout; Rnet; PAR; G, GPP (partitioned components); Tsoil, VWC, windspeed, winddir, Ustar (friction velocity), TKE, Tstar, L, (z-d)/L, stability parameter; NEE_f and NEE_f_sd (gap-filled NEE and its sd); Reco, GPP (partitioned components).
  - Temporal and measurement metadata: Date and Time in GMT; units and descriptions provided for each variable.
  - Additional context: table includes both raw (before gap-filling) and processed (gap-filled) fluxes and associated uncertainties.

- Accessibility and acknowledgments
  - Data collection funded by the Leeds–York–Hull Natural Environmental Research Council (NERC) DTP Panorama (grant NE/S007458/1).
  - Acknowledges University of Leeds Research Farm and Rob Yardley for management information.
  - References list key instruments, processing tools, and methods used (EddyPro, REddyProc, standard eddy covariance processing and quality-control procedures).

- Relevance for data governance and reuse
  - Demonstrates end-to-end data workflow: instrument deployment, high-frequency data capture, rigorous processing, quality control, gap-filling, and partitioning into biological flux components.
  - Provides a comprehensive metadata-rich dataset suitable for cross-site comparisons, model validation, and investigations of crop-ecosystem energy and carbon fluxes under bioenergy maize production.