# Ammonia concentration and deposition data from Glencorse experimental site near UKCEH, Edinburgh (2023)

- A study at Glencorse woodland (Birch plantation) to investigate how high atmospheric ammonia (NH3) affects forest vegetation, bryophytes, lichens, and soil.
- NH3 enhancement system operated in 2022–2024, releasing NH3 only when wind and threshold speeds align with monitoring quadrats (275–345 degrees, ~0.31 m/s threshold).
- NH3 concentrations measured at 1.5 m height along monitoring transects using ALPHA passive samplers; monthly analyses from January 2023 to December 2024.
- Deposition and emission estimates for soil, understory vegetation, tree trunks, and tree canopy using a four-layer canopy compensation point model (bi-directional resistance framework).

- Data and modelling approach

  - Deposition flux model: Fχ(z) = χa / Rt, where Rt is total resistance to dry deposition; deposition to soil uses boundary-layer resistance Rbg; to trunks uses quasi-laminar boundary layer resistance around trunks; stomatal and cuticular pathways modelled with Rs and Rw parameterizations, including LAI dependencies; multiple cuticular deposition parameterizations (Massad 2010, Jones 2007, DEPAC 2010, Sutton 1998) are used and compared.
  - The deposition process accounts for stomatal compensation point, soil re-emission potential, and phenological variation affecting LAI-dependent resistances.
  - An improved model version now uses ambient NH3 concentration to drive deposition when NH3 is not released, and concentration peaks during release periods to estimate deposition, representing an advancement over previous mean-monthly-concentration-based approaches.
  - Data cover 108 measurements of 17 parameters, with deposition fluxes (soil, understory, trunks, canopy) and NH3 concentrations at multiple heights (soil surface, understory, trunk surfaces, canopy).

- Data collection details

  - Location: Glencorse experimental site near Edinburgh (55.8539°, -3.2151°; altitude ~200 m).
  - Height and sampling: NH3 concentration measured at 1.5 m height along transects; monthly sampling.
  - Data structure: CSV file with 108 rows (measurements) and 17 parameters, including distance from NH3 source, month, NH3 concentrations at various layers, and cumulative deposition fluxes (negative values indicate emission).

- Data quality and governance

  - Quality control: visual checks; removal of obvious instrument/metering errors; gaps due to scheduled power cuts and occasional sensor replacements.
  - Metadata and clarity: detailed parameter descriptions, units, and data descriptions for each column to support verification and reuse.
  - Data provenance and transparency: the dataset builds on prior work (2022 dataset) and connects to published methodologies; the improved deposition model provides better representation of NH3 release events.
  - Accessibility considerations: the document discusses data sharing barriers generally; the dataset itself provides comprehensive metadata and structure to facilitate reuse and evaluation by policymakers and researchers.

- Funding and context

  - Facility funding from UKRI GCRF South Asian Nitrogen Hub and UKCEH National Capability for UK Challenges Programme, reflecting government-backed support for monitoring infrastructure and data generation.

- Relevance for monitoring frameworks and policy decisions

  - Demonstrates a transparent, model-driven approach to quantify deposition and emission fluxes across ecosystem components, enabling evaluation of policy-relevant NH3 emission scenarios.
  - Provides a robust data pipeline: careful data collection, multi-pathway deposition modelling, explicit handling of phenology via LAI, and comprehensive QC, which helps avoid data gaps and misinterpretation.
  - Highlights practical challenges in environmental monitoring data: data gaps due to power outages, need for rich metadata, and the importance of publicly sharing underlying datasets to maximize reuse and governance.
  - Aligns with monitoring framework aims by delivering standardized, well-documented measures of NH3 concentration and deposition suitable for informing future policy and management decisions regarding forest ecosystems and nitrogen deposition.