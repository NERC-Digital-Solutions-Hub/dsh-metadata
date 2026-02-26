# Amazon Fertilization Experiment (AFEX)

## Overview
- Study conducted in the BDFFP KM41 reserve, about 100 km from Manaus, Brazil.
- Site characteristics: clay-rich Ferralsols soils; annual rainfall 1900–2500 mm with a pronounced dry season (June–October); above-ground biomass (AGB) ~322 ± 54 Mg ha-1; mean wood density ~0.67 g cm-3; ~280 species (≥10 cm DBH) per ha.
- Focus: measurements of CO2 fluxes and related respiration processes within an Amazon forest fertilization experiment.

## Experimental design and scope
- AFEX is a full factorial fertilization experiment started March 2017.
- Design: eight treatments with four replicates each (32 plots) arranged in four independent blocks at least 200 m apart.
- Treatments: Control; nitrogen (N); phosphorus (P); cations; N+P; N+cations; P+cations; N+P+cations.
- Fertilization rates (per year): N 125 kg/ha, P 50 kg/ha, cations 50 kg/ha (as KCl) plus 50 kg/ha of Ca and Mg from dolomitic limestone.
- Plot size: 50 × 50 m, with minimum 50 m between plots.
- AFEX 2.0 involved plot delineation enhancements and ensured similar soil, vegetation, and topography across plots.

## Data collection and measurement methods
- Stem respiration (CO2 efflux):
  - Sample: 320 trees with DBH > 25 cm; 10 trees per plot.
  - Timing: October 2019.
  - Instrument: infrared gas analyser (EGM-4); chamber sealed to collar; measurements over 2 minutes.
- Soil respiration (autotrophic and heterotrophic):
  - Instrument: Li-Cor Li-8100A with a 20 cm survey chamber.
  - Two collar types to partition respiration components:
    - Short collar (10 cm): captures all flux components (roots, rhizosphere, soil).
    - Long collar (25 cm) with a window to exclude roots and mycorrhizae (no atmosphere exchange barriers described).
  - In 2017, collars deployed at two random points per plot; depth/window configuration varied.
  - 2017 collection dates: Jun–Jul, Sep, Oct, Nov.
  - 2018 collection: monthly through Sep.
  - 2019 collection: Jan, Feb, Apr, Jul, Oct.
  - Rhizosphere respiration estimated as the difference between 25 cm depth (excluded roots) and surface-only measurements.
- Data management of measurements:
  - Stem CO2 data and soil CO2 data are stored as separate spreadsheets deposited in the EIDC system, with detailed field definitions provided.

## Data assets and access
- Two primary datasets deposited in the EIDC system:
  - Stem CO2 efflux dataset (tree-level respiration data).
  - Soil CO2 efflux dataset (soil respiration data, including collar type and measurement context).
- Data files include metadata and descriptive field definitions to support reuse and interpretation.

## Data schema and metadata (high-level)
- Stem CO2 efflux dataset:
  - Key fields include: tree identifier, Plot/Block, Plot, DBH, Initial_CO2, Final_CO2, Date, PlotID.
  - Purpose: track tree-level stem respiration across plots and time.
- Soil CO2 efflux dataset:
  - Key fields include: Census/Campaign, File.Name, Date, Block, Plot, Group (collar set), Type (shallow surface; deep with window; deep without window), PlotID, Date_IV, Obs, Lin_Flux.
  - Collar types defined as:
    - T: shallow surface collars (roots not cut).
    - M: deep collars with window (roots excluded; mycorrhizae ingrowth possible until 2018).
    - S: deep collars with no windows (roots and mycorrhizae excluded).
  - Measurements reported as Lin_Flux in μmol m^-2 s^-1.
- Metadata notes:
  - Documentation includes column-level definitions and the physical meaning of measurement setups.
  - Data are organized by block and plot, with explicit treatment and measurement context.

## Data quality, standards, and usability
- Strengths:
  - Consistent, long-term measurement program across multiple years (2017–2019) and two data streams (stem and soil respiration).
  - Clear experimental design with replication, plot-level metadata, and explicit fertilization treatments.
  - Use of standardized instrumentation (EGM-4 IRGA, Li-8100A) and explicit collar-based partitioning to separate respiration components.
  - Data are stored with explicit field names, units, and measurement dates in an accessible repository (EIDC).
- Considerations for Data Leaders:
  - Some collar designs changed over time (roots ingress observed in 2018 for the M-type collar), which may affect cross-year comparability of soil respiration components.
  - Data consistency across years relies on uniform sampling protocols and complete metadata (plot, block, treatment, collar type, date, and measurement values).
  - Data discoverability and interoperability are supported by the centralized EIDC deposition and explicit schema descriptions, but users should verify any schema updates or changes in measurement protocols when integrating across datasets.

## Context and references
- References cite foundational work on Amazon forest structure, species richness, and soils relevant to interpreting the AFEX study site context.