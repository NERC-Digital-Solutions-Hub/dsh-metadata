# Ammonia concentration and deposition data from a peatland nitrogen pollution experiment, Whim Bog, Scotland, UK, 2002-2022

## Overview
- Long-term dataset from an NH3 enhancement experiment at Whim Moss ombrotrophic bog (2002–2022) to study effects on vegetation, bryophytes, lichens, and soil, with deposition flux estimates.
- Experiment controlled by wind direction and speed, releasing NH3 only when wind carries it toward monitoring quadrats.
- Data support monitoring and evaluation of environmental health responses to ammonia exposure and deposition.

## Methods: Data collection and flux calculations
- Location: Whim Moss, Scotland (55.76566°, -3.27155°), altitude 316 m.
- NH3 enhancement activated when wind direction is 180–215° and wind speed > 2.5 m/s.
- NH3 measured along monitoring transect using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; monthly analyses from May 2002 to December 2022.
- Sampling locations (lateral and vertical) changed over time to align with study needs.
- Dry deposition to vegetation estimated with a unidirectional resistance model: Fχ(z) = χa / Rt; Rt = Ra + Rb + Rc (total resistance).
- Resistance components:
  - Ra (aerodynamic) calculated from wind speed and friction velocity using height-based equations.
  - Rb (boundary-layer) computed via parameterization involving Reynolds number and Schmidt number for NH3.
  - Rc (canopy) determined separately for day and night using constants and chi, with Rc0, α, b derived from prior work; during NH3 release, Rc depends on χ; during no-release periods, Rc is fixed at 20 s m-1.
- Deposition flux per 15-minute period derived from 15-minute χ values; monthly averaging applied to obtain deposition flux.
- Complete methodology and analysis detailed in cited references (Leith et al. 2004; Jones et al. 2007; Cape et al. 2008).

## Quality Control
- Visual checks to remove data affected by instrument failure, damage, sample loss, or power interruptions.
- Monthly NH3 concentrations lower than ambient removed to avoid negative deposition values.
- Missing data due to sampler relocation reflected as gaps.

## Data structure
- Dataset contains 6296 measurements of 6 parameters, provided in CSV format.
- Columns include:
  - Month (year and month)
  - ID (sample label; includes E/W, Con/Amb)
  - Distance (m; negative = upwind, positive = downwind)
  - Height (m; measurement height)
  - NH3_conc (1 = µg m^-3; 2 = monthly average NH3 concentration)
  - Dep_kg_ha (1 = kg ha^-1 month^-1; 2 = monthly total NH3 deposition)
- Metadata note: NA values in NH3_conc indicate missing NH3 concentration data; NA in Dep_kg_ha indicate missing deposition due to data gaps.

## Funding
- Natural Environment Research Council (NERC) Award NE/R016429/1, part of the UK-SCAPE programme delivering National Capability.

## References
- Cape et al., 2008; Fowler, 1978; Garland, 1977; Jones et al., 2007; Leith et al., 2004; Smith et al., 2000; Sutton et al., 1993; Tang et al., 2001; Wesely & Hicks, 1977.

## Relevance to Monitoring Frameworks
- Provides an illustrative example of end-to-end monitoring: from controlled exposure experiments to measured concentrations and modeled deposition fluxes, with explicit data products (monthly NH3 concentrations and deposition flux).
- Demonstrates data governance considerations (metadata, data sharing, quality assurance) and challenges (siloed data, data lineage, need for up-to-date, well-documented metadata).
- Highlights practical issues for policymakers and program managers:
  - Ensuring data quality and standardization for reuse in policy evaluation.
  - Balancing openness with data sensitivity and methodological detail.
  - Addressing gaps and changes in sampling schemes over long-term monitoring efforts.
- Useful for informing future monitoring design, data management, and governance to support environmental health decision-making.