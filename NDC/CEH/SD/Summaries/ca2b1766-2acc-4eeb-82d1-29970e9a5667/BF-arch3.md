# BF Protocol

## Aim
- Record the phenology of the spawning of the common frog (Rana temporaria) in selected ponds and ditches.
- Assess the number of egg masses as an index of frog population health.
- Identify significant changes in populations and measure pond characteristics that may influence breeding success.

## Rationale
- The common frog serves as an indicator species for amphibian health in Britain; populations have declined due to drainage, habitat modification, and pollution.
- Amphibians are affected by both aquatic and terrestrial conditions; spawning in shallow water makes monitoring feasible.
- Spawn counts (with a simple expansion assumption) provide a rough colony size estimate; monitoring focuses on timing and habitat factors that influence breeding success.

## Method

### Equipment
- Field-appropriate pH meter and maximum/minimum thermometer.
- Optional: water depth measurement pole.

### Location
- One or more shallow ponds or wet ditches known to have bred frogs recently, chosen for convenient frequent visits.

### Biological (Monitoring design and schedule)
- Check sites weekly from about 1 January (adjust for local knowledge) to determine when males gather and begin calling.
- If possible, visit daily after spawning begins; at minimum weekly until first eggs hatch.
- Data collected:
  - Date of first spawn observed.
  - Daily or weekly counts of new spawn masses (each mass marked with colored thread to avoid double-counting).
  - Total surface area of water occupied by spawn masses.
  - Percentage of dead or diseased eggs.
  - After embryos hatch, continue weekly monitoring until metamorphosed frogs are seen leaving the pond, or for up to 16 weeks from the first spawn (whichever is shorter).

### Physico-chemical (water quality and habitat context)
- At first spawn, collect a 250 ml water sample for baseline chemical analyses.
- In situ measurements (unfiltered water): pH and conductivity, following ECN methods; after filtration, analyze dissolved ions: Na+, K+, Ca2+, Mg2+, Fe2+, Al3+, NH4+-N, Cl−, NO3−-N, SO4 2−, PO4 3−-P, alkalinity, and dissolved organic carbon (DOC).
- If unexplained mortality occurs, collect a follow-up sample using the same analyses.
- In situ weekly measurements between first spawning and metamorphs leaving:
  - pH: measured at three random positions near the spawning edge at 50 mm depth.
  - Temperature: maximum/minimum thermometer positioned to measure at 50 mm depth; record initial spawning temperature and re-check weekly.
  - Water depth: measured weekly near the center of the spawning area.

## Recording conventions and data standards

### Core data structure
- Core measurements pertain to vertebrates – frog spawn (BF Protocol).
- A single pond water sample is collected at first spawning and analysed as an annual baseline.
- Weekly records of pond pH and temperature; daily spawn monitoring and counting; date-related milestones (first congregating, first spawning, first hatching, first metamorphosis leaving).

### Key data fields (examples)
- Site Identification Code (unique ECN Site code)
- Core Measurement Code (unique code for the BF Protocol)
- Location Code (replicate sampling location within the site)
- Sampling Date/Time (date and time of sample or observation)
- Pond-related and chemical measurements (pH, conductivity, alkalinity, Na+, K+, Ca2+, Mg2+, Fe2+, Al3+, NH4+-N, Cl−, NO3−-N, SO4 2−, PO4 3−-P, DOC)
- Biological milestones (date first congregating, date first spawning, date first hatching, date newly metamorphosed frogs first seen leaving)
- Spawn metrics (pond ID, number of new spawn masses, total surface area covered, percentage dead/diseased eggs)
- Depth at center of spawning area; minimum and maximum temperature; weekly pH measurements at specified positions

- Data formats and exact precision requirements are specified in ECN dataset documentation (Data Transfer docs) and Site Managers’ extranet; standard recording forms are available from the CCU.

### Recording forms
- A standard field recording form is provided by the CCU (Appendix II).

## Recording forms, data transfer, and governance
- Data are intended for transfer to ECNCCU using standardized formats; proper metadata and data governance practices are required.
- Public sharing of underlying data is accommodated via defined metadata and data-sharing arrangements.

## Author references
- Beattie, Tyler-Jones & Baxter; Cooke; Cummins and colleagues; and related ECN documentation (varying years) underpin the protocol’s rationale, measurements, and analytical approaches.