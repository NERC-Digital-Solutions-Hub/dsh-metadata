# BF Protocol

## Aim
- Record the phenology of spawning of the common frog (Rana temporaria) in selected ponds and ditches.
- Use the number of egg masses as an indicator of frog population health.
- Identify significant changes in populations and measure pond characteristics that may affect breeding success.

## Rationale
- The common frog is used as an example of a ubiquitous amphibian indicator within ECN.
- Breeding occurs in shallow water; populations are influenced by land conditions as well as water bodies.
- Historical declines linked to drainage, habitat modification, pollution, and acidification; spawn counts provide a rough proxy for colony size.

## Method
### Site and Timing
- One or more shallow ponds or ditches, selected where frogs have bred recently and are accessible for frequent visits.
- Monitoring window varies by year and location.

### Biological (Spawn Monitoring)
- Weekly checks for male frogs congregating and calling; daily visits when feasible until first eggs hatch.
- If daily visits aren’t possible, minimum weekly visits until hatch.
- Record the date spawning is first seen.
- Daily or weekly records of new spawn masses; mark each new mass with a colored thread to avoid double counting.
- For masses >100 or infrequent visits, estimate total water surface area occupied by spawn masses.
- Record the date embryos first hatch; continue weekly monitoring until metamorphosed frogs leave or 16 weeks from first spawning, whichever is shorter.
- Pond surface area and spawn mass counts used to approximate colony size when counts are impractical.

### Physico-chemical (Water Chemistry and Environment)
- At first spawning, collect a 250 ml water sample from the spawning area for baseline chemical analysis.
- Conductivity and pH measured on unfiltered water; after filtration, analyze dissolved ions and compounds (Na+, K+, Ca2+, Mg2+, Fe2+, Al3+, NH4+-N, Cl-, NO3--N, SO4 2-, PO4 3--P, alkalinity, dissolved organic carbon).
- If unexplained mortality occurs, collect an additional water sample for the same analyses.
- Record pH, temperature, and water depth weekly from first spawning to when metamorphosed frogs are observed leaving the pond.

### Specific Field Measurements
- pH: measured weekly at three random positions just outside the spawning area near the edge at 50 mm depth using a field pH meter.
- Temperature: maximum/minimum thermometer placed in open water at 50 mm depth, read weekly.
- Water depth: measured weekly near the center of the spawn area.

## Location and Equipment
- Use ponds/ditches with known recent breeding and convenient access.
- Field equipment includes a field pH meter, maximum/minimum thermometer, and a water depth pole or comparable depth measurement tool.

## Recording and Data Standards
- Core, consistent data collection with explicit recording conventions:
  - The first four key parameters to uniquely identify each record are:
    - Site Identification Code (unique to ECN Site, e.g., T05)
    - Core Measurement Code (e.g., BF - frog spawn)
    - Location Code (replicate sampling location within the site)
    - Sampling Date/Time (with time element if sampling is more frequent than daily)
- Core measurement: vertebrates - frog spawn (BF Protocol)
- Daily pond monitoring (spawn monitoring) and weekly pond monitoring (environmental parameters) with standardized fields for pH, conductivity, and other chemical determinands.
- Data values follow specified precision and units (e.g., pH, temperatures in °C, depth in cm, concentrations in mg L-1 where applicable).
- Data transfer and formats are defined in ECNCCU’s accompanying Data Transfer documentation; access via restricted Site Managers' extranet (ecnccu@ceh.ac.uk for access).

## Recording Forms
- A standard field recording form is available from the CCU; an example is provided in Appendix II.

## Authors and References
- BF Protocol: Beattie, Tyler-Jones, Sykes; Beattie et al. (ecology and amphibian studies) cited for methods and rationale.

## Summary for GIS Specialists
- The protocol yields time-stamped, site-specific, pond-level data linking:
  - Spatial identifiers: Site ID, Location Code, pond/area reference.
  - Temporal identifiers: dates of first spawning, hatch, metamorphosis, and weekly/ daily observation dates.
  - Biological data: number of spawn masses, surface area of water occupied by spawn, mortality/disease indicators.
  - Environmental data: pH, conductivity, major ions, alkalinity, temperature, and depth measurements.
  - Sampling metadata: sampling time, sampling location within pond, and chemistry determinands.
- Data are designed to be integrated with GIS: unique codes facilitate joins to pond polygons or ECN site layers; time-series analyses per pond; potential baseline chemical characterizations across the network.
- Emphasizes standardized data formats, precise measurement codes, and documented data transfer processes to support reliable GIS analyses and cross-dataset integration.