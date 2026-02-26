# Supporting information for: Eddy covariance measurements of carbon dioxide, energy and water fluxes at an organically managed grassland, Berkshire, UK, 2017 to 2019

- Purpose and licensing
  - Data usage requires citation: Morrison et al. (2019), NERC EIDC. DOI provided.
  - Full terms of use are available at the specified DOI link.
  - Clear citation guidance helps ensure data provenance and traceability.

- Dataset overview
  - Time series of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ), plus ancillary weather and soil physics observations and turbulence descriptors.
  - Primary data: 30-minute flux averages derived from high-frequency (20 Hz) EC measurements.
  - Ancillary data include meteorology and soil parameters; dataset designed to characterise atmospheric turbulence.
  - Site code: BD-OG; dataset file: BD-OG_Organic_Grassland_2017_2019.csv.
  - Gap-filled and partitioned data (e.g., NEE_filled, GEP, TER) are provided alongside raw observations.

- Study site
  - Location: BD-OG flux tower at Sheepdrove Organic Farm, Berkshire Downs, UK (approx. 4.0 km NE of Lambourn).
  - Coordinates and elevation: 51°31'48.78" N, 1°28'54.99" W, 184 m amsl.
  - Climate and soils: temperate maritime climate; shallow chalky, silty loams with flints; bulk density and soil organic carbon provided; representative vegetation is organically managed, extensively grazed grassland.
  - Site details referenced from Evans et al. (2016) for context.

- Sampling regime and data acquisition
  - Automated flux, meteorological and soil measurements: 2017-01-01 00:30 to 2019-11-16 00:00.
  - Eddy covariance setup: open-path EC system at 2.0 m above canopy; sensors include Windmaster ultrasonic anemometer and LI-7500 CO2 sensor.
  - Data logging: raw 20 Hz measurements stored with CR3000 Micrologger; includes wind components, sonic temperature, water vapor, and CO2 densities.
  - Ancillary measurements from a COSMOS-UK Station: Ta, barometric pressure, RH, net radiation (Rnet), short/long-wave components, soil heat flux (G), soil moisture (VWC), soil temperature, precipitation.

- Data processing and quality control
  - Processing tool: EddyPRO v6.1; fluxes computed as 30-minute averages.
  - QC steps: automated quality control of 20 Hz data, angle-of-attack correction, 2D rotation for terrain, corrections for cospectral attenuation, humidity effects, density corrections; random uncertainties computed via standard methods.
  - Additional quality checks: footprint analysis (ART Footprint Tool) ensuring >80% flux contribution from target grassland; weekly visual QC; removal of clearly erroneous values.
  - Random uncertainties and derived turbulence metrics (u*, TKE, L, z/L) calculated with EddyPRO.

- Gap-filling and flux partitioning
  - Gap filling: Marginal Distribution Sampling approach (Reichstein et al., 2005) with Ta-driven partitioning (GEP and TER).
  - Partitioning method: based on Reichstein et al. (2005).
  - Tools: REddyProc package in R (for gap-filling and partitioning).

- Data structure and units
  - Data delivered as a single CSV with columns described in Table 1 (DateTime in yyyy-mm-dd HH:MM; NEE, LE, H, Tau and their uncertainties; storage terms; meteorological and soil variables; wind metrics; footprint fraction; Ustar; TKE; L; zL; and gap-filled equivalents NEE_filled, LE_filled, H_filled, TER, GEP).
  - Missing data represented by -9999.
  - Metadata describing each variable, including units and descriptions, aligns with LI-COR-derived and Reichstein et al. conventions.

- Data accessibility and documentation
  - Primary data access via DOIs; licensing and use terms listed at the data’s access page.
  - Comprehensive variable descriptions and data structure documented to facilitate discovery and reuse.

- Acknowledgments and references
  - Funded by Natural Environment Research Council (NE/R016429/1) under UK-SCAPE; COSMOS-UK data contributions acknowledged.
  - Landowners’ permission and field/technical support acknowledged.
  - Key references cover EC processing standards, quality control, footprint modeling, and data processing tools (EddyPRO, REddyProc, and related methodological papers).

- Reliability, limitations, and governance considerations for Data Stewards
  - Footprint and representativeness: fluxes flagged by footprint analysis; ensure users are aware of spatial representativeness constraints.
  - Data gaps: gap-filled products provided; users should consider uncertainties associated with gap filling and partitioning.
  - Interoperability: metadata structured to support integration with standard micrometeorological datasets; variable naming and units aligned with established conventions.
  - Versioning and provenance: detailed processing steps and QC procedures documented to support traceability and reproducibility.
  - Licensing and citation requirements: explicit citation guidance to preserve dataset provenance and credit.

- Practical implications for use
  - Useful for studies of carbon, energy, and water fluxes in managed grassland ecosystems.
  - Enables analysis of ecosystem processes (NEE, GEP, TER) alongside meteorology and soil physics under organic grazing management.
  - Data suitable for cross-site comparisons given standardized processing and QC workflow.