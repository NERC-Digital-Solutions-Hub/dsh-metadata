# Procedure for Polymerase Chain Reaction (PCR) NERC project NE/N019555/1

## Purpose
- PCR amplifies a targeted DNA sequence to produce many copies quickly. This procedure explains sample preparation and execution to avoid contamination and template denaturation, ensuring high-quality amplified products.

## Safety
- Use universal precautions.
- Maintain the PCR hood regularly and record results in a dedicated file.

## Materials

### Chemicals
- 10X concentrated PCR reaction buffer
- dNTPs
- Forward and reverse primers
- Taq polymerase
- 70% Ethanol
- 10% Sodium hypochlorite
- Autoclaved filtered deionized water

### Equipment
- PCR hood with UV light
- Thermal cycler
- Vortex
- Rotor
- Refrigerator (2–8°C)
- Freezer (-20°C)

### Other supplies
- Parafilm
- Micropipettes (range 0.5–1000 µl)
- Pipette tips
- Microcentrifuge tubes (1.5 ml, 200 µl)
- Gloves
- Ice
- PCR racks
- Glass marker

## PCR Protocol

- Conduct all reaction setup in an area separate from DNA preparation or PCR product analysis.
- Prepare a dNTP mix with 10 mM of each dNTP; store aliquots at -20°C.
- Thaw 10x PCR Buffer, dNTP mix, and primer solutions.
- Prepare a master mix (contains all components except template DNA); include at least one negative control per setup to detect contamination.
- Mix the master mix thoroughly and dispense into PCR tubes; mix gently by pipetting up/down.
- Add template DNA (2.0 µl per tube) to the tubes with the master mix.
- Program the thermal cycler with the heated lid according to manufacturer instructions.
- Optimize temperatures and cycling times for each new target or primer pair for maximum yield and specificity.
- Typical cycling program:
  - Initial activation: 95°C for 10–15 minutes
  - Denaturation: 94°C for 0.5–1 minute
  - Annealing: 50–68°C for 0.5–1 minute
  - Extension: 72°C for 1 minute
  - Number of cycles: 25–35
  - Final extension: 72°C for 10 minutes
  - Hold: 4°C
- After cycling, store tubes at 4°C or -20°C for long-term storage.

### Table 1 – Example reaction composition (using Taq polymerase)
- 19.0 µl water
- 2.5 µl PCR Buffer (10x) with MgCl2 (50 mM)
- 0.5 µl dNTP mix (10 mM each)
- 0.4 µl Primer -A (10 pmol/µl)
- 0.4 µl Primer -B (10 pmol/µl)
- 0.2 µl Taq Polymerase (5 U/µl)
- 2.0 µl Template DNA

## Quality control of the method

- Positive and negative controls are run for each PCR sample set.

### Negative Control
- Reagents without any DNA.
- Should produce no band on the gel; presence of a band indicates contamination and the run fails QA/QC.

### Positive Control
- DNA known to produce a clear band.
- If needed, diluted to yield a strong, distinct band.

### QA/QC outcome
- The combined results of the positive and negative controls determine if the gel passes QA/QC:
  - If controls behave as expected (positive bands and no bands in negatives), the run passes.
  - Any deviation indicates failure and requires redoing the affected samples.

## Data leadership perspective (relevance to Data Leaders)
- Emphasizes rigorous data integrity and reproducibility through:
  - Clear separation of work areas to prevent contamination, supporting data validity.
  - Detailed documentation of reagents, volumes, and conditions for auditability and future reuse.
  - Mandatory controls (positive/negative) to ensure data-driven results are trustworthy.
  - Stored results and protocol steps enabling traceability and potential cross-project data sharing.
- Supports data governance by enabling metadata capture (reagents, concentrations, temperatures, times) and facilitating standardized, reproducible workflows across collaborations.