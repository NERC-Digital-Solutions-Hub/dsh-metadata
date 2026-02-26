# Vegetation work

- Four 50 cm x 50 cm quadrats placed randomly around the site; used for visual estimation of species percent cover.
- Species richness and percent cover of grasses and forbs calculated by summing across the four quadrats.
- Biomass: biomass clipped at ground level from each quadrat, dried at 80°C for 24 hours, weighed, and summed across the site to yield g biomass per m².
- Diversity: Shannon's Diversity index calculated (Shannon & Weaver, 1963).

## Greenhouse gas flux

Net ecosystem CO2 exchange, photosynthesis and respiration
- Four plastic collars (25 cm diameter) embedded in the soil; transparent chambers attached to an IRGA (EGM-4) to measure CO2 influx over two minutes; a reflective cover used to obtain dark efflux.
- Simultaneous measurements of soil moisture, soil temperature (WET sensor), and photosynthetically active radiation (PAR) in triplicate.
- CO2 flux calculated from the 27 CO2 concentration measurements over two minutes to mg CO2 m⁻² h⁻¹.
- Additional formula-based steps describe converting measured values to flux, including time-based predictions and constants (e.g., chamber volume, area).

Methane (CH4), CO2 and nitrous oxide (N2O)
- Chambers covered with reflective material placed in the collars; 9 ml air samples collected at 0, 10, 20, and 30 minutes and injected into evacuated vials.
- Gases analysed with a Gas-Chromatograph (Agilent 7890B).
- Final gas flux values calculated using the same approach as for IRGA-derived CO2 flux.

## Soil sampling

- Six soil samples per site collected with a 4 cm diameter auger to a depth of 10 cm.
- Samples passed through a 2 mm sieve to remove stones and roots; stored at 5°C until processing.

## KCl extractable N and potential mineralisation

- 5 g fresh soil weighed, mixed with 25 ml of 1 M KCl, shaken at 150 rpm for 1 hour; filtrate diluted 2:1 and analysed for DIN (NH4⁺ and NO3⁻) using an autoanalyser.
- Extracts adjusted for soil moisture to calculate DIN mg/kg: DIN value adjusted by water content and dilution relative to dry weight.
- A separate 5 g soil sample incubated at 25°C for 14 days; extracts analysed as above.
- Mineralisation calculated as (NO3⁺NH4) × bulk density ÷ number of days, expressed as g m⁻² d⁻¹.

References:
- Shannon, C.E. and Weaver, W. (1963) The Mathematical Theory of Communication, University of Illinois Press, Urbana.

## Data management considerations for Data Stewards

- Data provenance and metadata
  - Capture and document instrument models (e.g., IRGA EGMs, PAR sensors, WET sensors), collar diameters, chamber volumes, and measurement timings.
  - Record site identifiers, GPS coordinates, dates, times, replicates, and sampling order for all measurements.
  - Include processing steps: biomass drying conditions, soil sieving, extraction volumes, dilution factors, and calculation formulas used to derive outputs (biomass g m⁻², Shannon index, CO2/CH4/N2O flux, DIN mg/kg, mineralisation g m⁻² d⁻¹).

- Data formats and units
  - Standardize units across datasets (e.g., biomass in g m⁻², percent cover in %, CO2/CH4/N2O flux in mg m⁻² h⁻¹, DIN in mg N kg⁻¹, mineralisation in g m⁻² d⁻¹, volumes in mL, temperatures in °C).
  - Document any deviations or unit conversions applied during processing.

- Quality assurance and data processing
  - Implement QA steps prior to sharing: verify measurement ranges, instrument calibrations, and consistency across replicates (e.g., triplicate soil moisture and PAR readings).
  - Record any data cleaning, transformations, or derivations (e.g., calculations for DIN, biomass, Shannon index, and gas flux).
  - Maintain versioning of datasets and all derived variables.

- Data storage, sharing, and governance
  - Store raw and processed data with clear, stable identifiers; preserve chain of custody and sample IDs.
  - Prepare data dictionaries and methodological notes to accompany datasets; reference the original protocols and any amendments.
  - Upload and catalogue datasets in appropriate portals or data repositories; include embargo or access restrictions if applicable.
  - Consider including metadata compatible with ecological data standards (e.g., Ecological Metadata Language or other domain-specific schemas) to facilitate discoverability and reuse.

- Data challenges to manage
  - Aligning user needs with available data: ensure datasets capture sufficient detail for reuse (e.g., measurement intervals, QA procedures, and instrument specifics).
  - Handling large or complex data streams (e.g., high-frequency IRGA data, gas chromatograph outputs) and potential interoperability issues across systems.
  - Managing legacy equipment or outdated databases; plan for data modernization and metadata completeness to support long-term discovery and use.

- End notes
  - The document references Shannon and Weaver (1963) for diversity metrics; ensure citation metadata is included in the data records.