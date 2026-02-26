# BF Protocol

## Aim
- Record the phenology of spawning of the common frog (Rana temporaria) in selected ponds and ditches by counting egg masses as an indicator of population health.
- Identify significant changes in frog populations and measure pond characteristics that may affect breeding success.

## Rationale
- The common frog is an ubiquitous predator with breeding tied to shallow ponds/ditches and land conditions.
- Monitoring adult populations is difficult; spawning activity (egg masses) serves as a practical proxy.
- Breeding success is influenced by water chemistry, acidity, temperature, and land-use changes; historical declines noted due to drainage, pollution, and acidification effects on embryos and tadpoles.

## Method

### Equipment
- Field pH meter, maximum/minimum thermometer, and simple water depth pole or equivalent.

### Location
- One or more shallow ponds or wet ditches known to breed frogs, chosen for convenient access for regular visits.

### Biological (monitoring schedule and procedures)
- Timing: weekly visits starting around January (or as local knowledge dictates) to determine when males congregate and begin calling; daily visits if possible until first eggs hatch; minimum weekly visits if daily are not feasible.
- Spawn counting: record date of first spawn and, on subsequent visits, the number of new spawn masses (each mass marked with colored thread to avoid double-counting).
- Measures: estimate total surface area of pond occupied by spawn; estimate percentage of dead or diseased eggs.
- If visits are infrequent or spawn masses exceed 100, count and record only the total surface area occupied by spawn.
- Post-hatching: record the date embryos hatch; continue weekly monitoring until metamorphosed frogs leave the pond or for up to 16 weeks from first spawning, whichever is shorter.

### Physico-chemical (water quality)  
- At first spawning: collect a 250 mL pond-water sample for baseline chemical analysis (conductivity and pH on unfiltered water; after filtering, analyze for a suite of ions and compounds).
- Analytes (after filtration): Na+, K+, Ca2+, Mg2+, Fe2+, Al3+, NH4+-N, Cl-, NO3--N, SO4 2-, PO4 3--P, alkalinity, and dissolved organic carbon.
- If unexplained mortality occurs, take an additional sample for the same analyses.
- pH, temperature, and depth: measure weekly from first spawning to the date newly metamorphosed frogs are seen leaving.
  - pH: measured at three random positions near the edge of the pond at 50 mm depth.
  - Temperature: maximum/minimum thermometer submerged at 50 mm depth, read weekly.
  - Depth: measure depth at the centre of the spawning area weekly.

## Recording and data standards

### Key identifying variables (required for all datasets)
- Site Identification Code (e.g., T05)
- Core Measurement Code (e.g., PC)
- Location Code (e.g., 01)
- Sampling Date/time (with time element if sampling is more frequent than daily)

### Core measurement: vertebrates – frog spawn (BF Protocol)
- Annual, pond-based monitoring with:
  - Daily spawn monitoring from first congregation/date seen
  - Weekly pond environment measurements (pH, temperature)
  - Annual pond water chemistry determinands from a single early-spawn water sample
- Data to capture includes:
  - Pond ID, dates of first congregation, first spawning, first hatching, and first metamorphosed frogs leaving
  - Pond water sample data (pH, conductivity, and listed determinands with specified precision)
  - Depth at centre of spawning area and temperature readings (minimum/maximum)
  - pH at multiple positions, spawn mass counts, total surface area covered, number of new spawn masses, percentage dead/diseased eggs
- Note: Detailed data precision and formatting are defined in the ECN dataset specifications and accompanying documentation.

### Data transfer and forms
- Recording data follow the ECN dataset formats; documentation and sample recording forms are available via the ECNCCU restricted extranet.
- Contact ecnccu@ceh.ac.uk for access to data standards and transfer documentation.
- A standard field recording form is available (Appendix II).

## GIS and data integration considerations (for GIS Specialists)

- Spatial representation:
  - Pond locations as point sites; spawn mass locations as sub-features within a pond, with time-stamped events.
  - Pond boundaries and surface-area measurements usable as polygons for habitat extent analyses.
- Temporal dimension:
  - Daily spawn events and weekly environmental measurements enable time-series analyses of phenology and habitat conditions.
- Data integration:
  - Link biological (spawn counts) and physico-chemical data with site codes and location codes to enable cross-layer analyses (e.g., relationships between water chemistry, spawning success, and temperature).
- Data quality and standards:
  - Adherence to standardized core measurement codes, site/location identifiers, and reporting formats ensures interoperability across sites and with GIS platforms.
  - Ensure consistent spatial referencing and coordinate systems when importing into GIS; maintain linkages to the ECN dataset and restricted data documentation.
- Practical GIS uses:
  - Visualize spatial distribution of spawn sites and chronological spawning waves.
  - Analyze correlations between pond chemistry (pH, ions) and spawn mass counts or mortality.
  - Overlay with land-use, drainage, and pollution data to study drivers of population changes.