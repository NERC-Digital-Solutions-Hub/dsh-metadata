# PHE Endotoxin Analysis

## Overview and context
- Characterisation of bioaerosol emissions from commercial compost conducted in a controlled 20 m^3 test chamber.
- Materials used: final grade (PAS 100) compost, stored at 4°C; visit 2 also used chicken litter stored at 4°C.
- Purpose: quantify endotoxin in aerosolized bioaerosols across size fractions under different aerosolisation conditions.

## Experimental design and materials
- Experimental runs used 25–50 g of compost or chicken litter aerosolised with a purpose-built aerosol generator.
- Distribution of aerosols aided by a fan; mixes of no aerosolisation and aerosolisation runs; each run lasted 30 minutes.
- Environmental conditions during sampling: 22–24°C and 46–60% relative humidity (monitored with a Testo meter).

## Sampling, preparation, and handling
- Depyrogenation of sampling materials (filters, tweezers, glassware) at 250°C for ≥2 hours before sampling.
- Endotoxin collection: eight-stage non-viable Andersen sampler with GF/A 8 mm glass fiber filters; flow maintained at 28.3 L/min for 30 minutes.
- Post-sampling handling: filters stored in 15 mL of LAL water (single filters) or 40 mL (multiple filters).
- Fractionation: nine size fractions obtained; some filters combined to yield four ranges (10.0–9.0 μm, 9.0–2.1 μm, 2.1–0.43 μm, <0.43 μm).

## Endotoxin extraction and analysis
- Extraction: filters shaken for 1 hour at 25°C; liquid centrifuged at 1000 × g for 15 minutes to remove glass fiber.
- Assay preparation: clear supernatant assayed for endotoxin.
- ELISA-like quantification: kinetic chromogenic Limulus Amebocyte Lysate (LAL) assay.
  - 50 μL sample + 50 μL lysate reconstituted with glucashield to prevent glucan interference.
  - Standard curve: control standard endotoxin from 5 to 0.005 EU/mL.
  - Incubation: plate at 37°C with 405 nm read for 90 minutes; reads collected via microplate reader.
  - Replication and controls: samples assayed in duplicate; include pyrogen-free water controls and blanks.

## Data produced and measurement details
- Endotoxin concentrations determined for each sample and size fraction.
- Data generated include: aliquot endotoxin values, standard curve data, duplicate measurements, and control results.
- Important metadata elements implicit in the process: sampler type and setup, flow rate, sampling duration, fractionation scheme, extraction conditions, and assay parameters (kit, reagents, incubation times, and detection wavelength).

## Data quality, provenance, and governance implications
- QA practices embedded in the protocol:
  - Depyrogenation of all sampling components to minimize contamination.
  - Use of controls and blanks alongside duplicates to gauge assay reliability.
  - Replication (duplicates) enhances measurement reliability.
- Provenance and traceability requirements:
  - Record sample identifiers, material type (compost vs. chicken litter), batch details, and mass aerosolised per run.
  - Document environmental conditions (temperature, humidity), sampler model/version, filter lot numbers, and LAL water volumes.
  - Capture extraction steps (shaking time, temperature), centrifugation parameters, and aliquot handling.
  - Log LAL kit lot numbers, glucashield usage, and standard endotoxin lot/date for reproducibility.
- Data management considerations for stewards:
  - Preserve complete metadata for each run and size fraction to enable re-analysis and cross-study comparison.
  - Store raw assay reads, calculated endotoxin concentrations, and associated standard curves with clear data dictionaries.
  - Ensure versioning and traceability of any data transformations (e.g., fraction groupings).

## Practical implications for data sharing and reuse
- To enable discovery and reuse, datasets should include:
  - Comprehensive metadata (materials, amounts, environmental conditions, sampling apparatus/settings, and assay chemistry).
  - Clear measurement units (EU/mL, fraction ranges in μm, flow rates in L/min, times in minutes).
  - Documentation of QA/QA steps, replication status, and control results.
  - Links to assay kit details, reagents, and standard endotoxin reference values.
- Potential limitations to note for users:
  - Fractionation and pooling of some filters may affect direct comparability across all size fractions.
  - Assay interference mitigations (glucan issue addressed with glucashield) should be considered when interpreting results across different matrices.