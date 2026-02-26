# Sampling scheme

- Context: Fieldwork at Kielder Forest, Northumberland, England, following major winter storms (Storm Arwen 2021 and Dudley, Eunice, Franklin 2022) with large areas of windthrow and windthrow-related disturbance.
- Study design: Ten sites identified (June 2022) defined by homogeneous stand and varying storm impacts; within each site, a transect (100–400 m) with observation points every 20 m.
- Disturbance classification: Based on the 10 nearest trees at each point — undisturbed, moderately disturbed, severely disturbed. Selection of 22 plots (10 undisturbed, 3 moderately disturbed, 9 severely disturbed) across sites.
- Plot layout: Randomly selected observation points centered 50 m × 50 m sampling plots; distribution included at least one undisturbed plot per site; some sites included multiple plots per disturbance class.

## Field sampling and measurements

- Field data collected per plot: number and species identity of all trees; recorded fallen/snapped status and soil pit depth.
- Vegetation sampling: Two perpendicular 10 m transects across each plot; at intersections and at 2.5 m intervals, bulk soil samples collected to 20 cm depth with a soil corer.
- Root sampling: Excavation of a 10 cm × 10 cm × 20 cm root block; roots and adhering soil retained, then separated into root material and soil.
- Replicates and sample counts: 22 plots; 9 soil cores and 9 root blocks per plot; total of 396 samples.
- Storage and subsampling: Samples kept on ice; subsamples frozen at -80°C; rhizosphere soil brush-extracted; remaining soil air-dried for chemical analysis. Roots split into two portions: air-dried for mass measurement and wet-weight measured before storage in 80% ethanol for DNA extraction.
- Moisture and weight: Gravimetric moisture content measured on a subsample to convert wet root mass to dry weight.

## Laboratory methods and instrumentation

- Soil moisture: Determined by drying at 65°C for 72 hours.
- Elemental analysis: Ground soil, acidified with 6% H2SO3 to remove carbonates, oven-dried at 65°C, then analyzed for total organic carbon and nitrogen using a ThermoFlash EA 1112.
- Units recorded: Soil nitrogen content (%), soil carbon content (%), gravimetric soil moisture (%), dry root mass in mg cm^-3.

## Quality control and data handling

- QC checks: Visual inspection of carbon and nitrogen peaks; use of at least two standards per instrument run.
- Statistical treatment: To avoid inflating degrees of freedom, plot-level transect data were averaged; 4–5 soil cores along a transect treated as analytical replicates (not true replicates).
- Outliers: No data points removed.

## Data structure and outputs

- Data representation: Arithmetic means of values obtained from soil cores along each within-plot transect.
- Scope: 396 samples across 22 plots, with additional storage and DNA-preserved root material.

## Implications for data leaders

- Data provenance and metadata: Requires clear documentation of site, disturbance class, plot and transect identifiers, sampling dates, and storage conditions to enable reproducibility and cross-site comparisons.
- Data quality and reproducibility: Standardized field and laboratory protocols, QC checks, and explicit treatment of replicates to avoid pseudo-replication.
- Data architecture and accessibility: Structured data outputs (plot-level means) alongside raw core-level data and preserved samples (for potential re-analysis) support flexible analyses and future data use.
- Data governance considerations: Clear recording of units, methods, and transformations (e.g., converting wet to dry weights) essential for interoperable datasets in broader data ecosystems.