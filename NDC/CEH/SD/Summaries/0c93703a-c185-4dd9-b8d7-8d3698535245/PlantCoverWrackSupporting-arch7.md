# Plant cover in a Floridian foredune following hurricane Irma: effect of experimental wrack removal

## Overview
- A field-based dataset documenting plant cover by species in a Floridian foredune following hurricane Irma, with an experimental wrack removal treatment to assess effects on plant communities.
- Observations collected across multiple time points to evaluate temporal changes in cover.

## Location and context
- Field site: foredune area of Anastasia State Park, south of St. Augustine, Florida, USA.
- Context: Hurricane Irma (October 2017) deposited storm wrack (seaweed, plant rhizomes, wood, etc.) on the site; experimental wrack manipulation was conducted to study its influence on vegetation.

## Experimental design
- Layout: five experimental blocks established in March 2018 within the storm wrack zone (within 1 km).
- Plots: in each block, three 10 x 10 m plots.
- Treatments (per plot): 
  - Control (undisturbed)
  - Procedural control (wrack removal and replacement)
  - Removal (wrack removal without replacement)

## Sampling schedule
- Baseline observations: March 2018 (immediately after setup).
- Follow-ups: August 2018, October 2018, January 2019.

## Variables and measurements
- Primary response: plant percentage cover by species; total plant cover per quadrat.
- Species coverage: Uniola paniculata (and other species tracked via additional columns).
- Spatial units: observations recorded within nine 0.5 x 0.5 m quadrats per plot.
- Data structure: total cover per quadrat is the sum of all species’ covers.

## Data collection procedures
- Estimation method: visual estimation of percent cover for each species within each quadrat.
- Quadrats: nine per plot, across all three plots within each block.
- Derived metric: total cover per quadrat is the sum of species covers.

## Data quality and validation
- Data checks: distributions of variables screened for unusual values; cross-checked against field notebooks.

## Data formats and dataset structure
- File formats: Excel and CSV.
- Key fields (examples): 
  - sampling_period (month and year)
  - plot_id (unique identifier for each plot)
  - block (block number)
  - plot (plot number within block)
  - treatment_type (experimental treatment)
  - quadrat_number (within-plot quadrat identifier)
  - plant_cover (total plant cover)
  - uniola_paniculata (cover of Uniola paniculata)
  - additional species columns (19 other species)

## Site visuals and documentation
- Figure 1A: Google Earth image showing replicates within the ASP site (30/10/2018).
- Figure 1B: Schematic of plots and data collection points within a plot boundary. 

## Personnel
- Staff responsible: Matthew Joyce, John Griffin.

## GIS relevance and use
- Spatial framework: clear block, plot, and quadrat identifiers enable mapping of plant cover patterns across the foredune and over time.
- Supports analysis of how wrack deposition/removal influences vegetation structure and species distribution in a coastal dune system.
- Suitable for integration with GIS workflows to visualize treatment effects, temporal change, and spatial gradients at multiple scales.