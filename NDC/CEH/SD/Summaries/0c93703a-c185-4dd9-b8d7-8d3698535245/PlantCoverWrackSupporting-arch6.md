# Plant cover in a Floridian foredune following hurricane Irma: effect of experimental wrack removal

## Overview
- A field-analysed dataset documenting plant cover by species in foredunes at Anastasia State Park, Florida, following hurricane Irma and subsequent wrack deposits.
- Monitored to assess the effect of wrack removal on plant communities over time.
- Staff: Matthew Joyce, John Griffin.

## Experimental design and settings
- Location: Foredune area of Anastasia State Park, south of St. Augustine, Florida, USA.
- Event context: Hurricane Irma (October 2017) left storm wrack (seaweed, rhizomes, wood, etc.).
- Experimental setup (March 2018):
  - Five blocks established in the wrack zone within 1 km.
  - In each block, three 10 x 10 m plots assigned randomly to:
    - Control (undisturbed)
    - Procedural control (wrack removal and replacement)
    - Removal (wrack removal without replacement)
- Monitoring schedule:
  - Baseline: March 2018 (immediately after setup)
  - Follow-ups: August 2018, October 2018, January 2019

## Data collection, variables, and format
- Sampling method:
  - Plant cover estimated visually within nine 0.5 x 0.5 m quadrats per plot.
  - Total cover per quadrat is the sum of all species’ covers.
- Response variables:
  - Plant_cover: total plant cover per quadrat
  - Uniola_paniculata: cover of Uniola paniculata per plot/quadrat
  - Additional species columns: 19 other species represented (total of ~20 species columns)
- Data structure and identifiers:
  - sampling_period: Month and year of sampling (e.g., 2018-03)
  - block: Block number (1–5)
  - plot: Plot number within a block
  - plot_id: Unique identifier for each plot
  - quadrat_number: Quadrant/quadrats numbered within a plot (1–9)
  - treatment_type: Experimental treatment (Control, Procedural control, Removal)
  - plant_cover: Total plant cover per quadrat
  - uniola_paniculata: Cover of Uniola paniculata per quadrat/plot
  - Other_species: Covers for additional species across subsequent columns
- Data formats:
  - Excel
  - CSV
- Data quality checks:
  - Distributions screened for unusual values
  - Cross-checked against field notebooks

## Data quality, provenance, and structure
- Field notes used to validate observations; observations conducted by trained staff.
- Observations are per quadrat, per plot, per block, across four time points, enabling temporal and treatment-based analyses.
- Potential data considerations:
  - Total cover is derived by summing species-specific covers, which can exceed 100% per quadrat due to overlapping canopies or estimation approach.
  - Visual estimation may introduce observer bias; consistency across observers assumed in this dataset.

## How to use and potential analyses
- Compare wrack removal treatments (Removal vs Procedural control vs Control) to assess effects on overall plant cover and species composition over time.
- Analyze species-specific responses, focusing on Uniola paniculata and other key species across time points.
- Use the hierarchical structure (blocks → plots → quadrats) to account for spatial replication and random effects.
- Potential outputs:
  - Time-series of total plant cover by treatment
  - Species composition shifts over time by treatment
  - Quadrat-level analyses to examine within-plot variability
- Practical considerations:
  - Merge data across sampling periods using sampling_period, block, plot, and quadrat identifiers.
  - Ensure careful handling of the 20-species coverage columns when computing totals or relative abundances.

## Additional notes
- Figures referenced:
  - Figure 1A: Google Earth image showing replicates (blocks) at the ASP site
  - Figure 1B: Plot schematic showing data collection points within a plot
- Dataset authors: Matthew Joyce, John Griffin
- Location metadata ties to post-Irma storm wrack context, relevant for studies on disturbance recovery and dune plant community dynamics.