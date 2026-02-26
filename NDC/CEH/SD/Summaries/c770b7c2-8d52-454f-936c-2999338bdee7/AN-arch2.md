# AN Protocol

## Aim
- Detect and define changes in periodic mean atmospheric concentrations of nitrogen dioxide (NO2).
- NO2 is the primary health and ecosystem-relevant NOx in urban atmospheres; major urban sources are fuel combustion from vehicles, power generation, heating, and industrial processes.
- NO2 exposure is a respiratory irritant and toxic at high levels; it also contributes to photochemical smog, acid rain, and ecological nitrogen inputs.
- Measure NO2 using passive diffusion tubes; method is well researched, reliable, low-cost, requires no on-site power, and is replicated to account for tube variability.

## Scope and Potential Extensions
- Consideration of extending ECN measurement to ammonia, sulfur dioxide, and ozone; currently no reliably passive methods for these gases.

## Equipment and Sampling Method
- Diffusion tubes: stainless steel mesh discs (1 cm diameter) coated with NO2 absorbent, housed in plastic tubes with coloured and clear caps; prepared as specified (acid washes, Decon 90, etc.).
- Field setup: three diffusion tubes mounted in clips, at about 1.5 m above ground, near a bulk precipitation collector or within a meteorological enclosure if available.
- Sampling procedure: deploy with white cap removed, tubes oriented vertically with open ends downward; collect for two weeks; replace white caps before retrieval; include three blank tubes prepared but not exposed; blanks and samples stored refrigerated during the sampling period.
- Labeling: unique reference codes including ECN Measurement Code (AN), ECN Site ID, Location Code, tube code (E1–E3 for exposed; B1–B3 for blanks), and Sampling Date; essential for data transfer to the ECN database.

## Analytical Procedure (Appendix I)
- Absorbent extracted to determine total NO2 absorbed; convert to mean NO2 concentration over the sampling period.
- Safety: wear gloves; rinse diffusion tubes after analysis to prevent cross-contamination.
- Reagents: sulphanilamide, N-1-naphthylethylene-diamine dihydrochloride (NEDA); prepare Reagents X and Y; prepare stock and working standards daily.
- Procedure: prepare standards (0.25–1.25 µg/mL NO2), mix samples with Reagent Y, react, and measure absorbance at 542 nm against a water blank; calculate NO2 mass and convert to NO2 concentration (ppb) using tube geometry and exposure time.

## Materials and Equipment Details
- Discs, diffusion tubes, coloured and clear caps; supplier: Gradko International Ltd.

## Data and Recording Conventions
- Core measurement: atmospheric chemistry - nitrogen dioxide (AN).
- For each sampling occasion at an ECN site, record fortnightly for three experimental tubes and three blanks.
- Required core data fields:
  - Site Identification Code
  - Core Measurement Code (AN)
  - Location Code
  - Setting out date and time (GMT)
  - Sampling date and time (GMT)
  - Tube code
  - Weight NO2 (µg)
- Data formats and transfer align with ECNCCU documentation; standard field forms available. 
- Tube coding reminder: experimental tubes E1, E2, E3; blanks B1, B2, B3.