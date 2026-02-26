# Sampling scheme

- Field setting and timing
  - Fieldwork conducted at Kielder Forest, Northumberland, England (55.24N, 2.61W).
  - Winter storms in 2021–2022 (notably Storm Arwen) caused widespread windthrow; surveys began in June 2022.
  - Storms Dudley, Eunice, and Franklin followed in early 2022, influencing post-storm conditions.

- Study design
  - 10 sites identified within Kielder Forest, each site defined by homogeneous stand composition and topography yet with spatially varying storm impacts.
  - Within each site, a transect (minimum 100 m, maximum 400 m) was laid; observations every 20 m along the transect.
  - A 50 m × 50 m sampling plot was centered on each observation point.
  - Disturbance categorization near each observation point based on the 10 nearest trees: undisturbed, moderately disturbed (≥50% snapped/fallen with no soil disturbance), severely disturbed (≥50% snapped/fallen with soil pits/mounds from uprooting).

- Plot allocation and sampling
  - 22 plots surveyed across 10 sites: 10 undisturbed, 3 moderately disturbed, 9 severely disturbed.
  - All sites contained an undisturbed plot; seven sites included a severely disturbed plot; one site included a moderately disturbed plot; two sites included plots for all three disturbance classes.

- Data types collected in the field
  - Tree inventory: number and species identity of trees; recording whether trees were fallen or snapped.
  - Soil and below-ground context: depth of soil pits where present.
  - Soil and root sampling structure: two perpendicular 10 m transects per plot; sampling points at intersections and every 2.5 m along transects.

- Sample collection per plot
  - Soil cores: bulk soil sample to 20 cm depth at each sampling point along transects (9 cores per plot across 22 plots → 396 total samples).
  - Root blocks: 10 cm × 10 cm × 20 cm blocks excavated at each sampling location; roots retained with adhering soil; roots divided into two portions (air-dried + weighed; wet weighed and stored in 80% ethanol for DNA extraction).
  - Rhizosphere soil: soil brushed from roots into a new container; subsamples stored at -80°C and remainder air-dried for chemical analysis.
  - Moisture and weights: gravimetric moisture content measured for roots to convert ethanol-preserved root weight to dry weight; total dry mass calculated by summing dry masses of root portions.

- Sample handling and storage
  - Samples kept on ice in coolers during transport to the laboratory.
  - Subsamples stored at -80°C; remaining samples air-dried for analyses.
  - Roots for DNA extraction preserved in 80% ethanol; moisture measurements used to convert weights to dry mass.

- Laboratory methods and instrumentation
  - Soil moisture: determined by mass loss after drying at 65°C for 72 hours.
  - Soil carbon and nitrogen: soil samples ground, acidified with 6% H2SO3 to remove carbonates, oven-dried at 65°C, and analyzed for total organic carbon and nitrogen with a ThermoFlash EA 1112 Elemental Analyzer.

- Variables measured and units
  - Soil nitrogen content: percent (%).
  - Soil carbon content: percent (%).
  - Gravimetric soil moisture: percent (%).
  - Dry root mass: mass per volume unit (mg cm^-3) in a 10 × 10 × 20 cm soil core.
  - Additional field data: counts and identities of tree species; disturbance class; soil pit depth.

- Data quality control
  - Carbon and nitrogen peaks manually inspected to ensure data quality.
  - Instrument runs included at least two standards.
  - To avoid inflating degrees of freedom, plot-level transect data were averaged; the four or five soil cores along a transect were treated as analytical replicates rather than true replicates.
  - No outliers were removed from the data.

- Data structure and final data products
  - Data provided as arithmetic means of values obtained from soil cores along each within-plot transect.
  - Each plot’s data reflect the averaged measurements across its contained sampling points/cores.
  - Subsamples and analytical replicates are organized per plot/transect, enabling downstream aggregation to site or disturbance-class levels.

- Data governance and stewardship considerations for Data Stewards
  - Provenance and traceability: capture site ID, disturbance class, plot ID, transect ID, sampling date, operator, and sampling point coordinates.
  - Metadata and standards: document sampling design, methods, units, instrumentation (ThermoFlash EA 1112), calibration standards, and QC procedures.
  - Data processing notes: clearly record that core-level data were averaged to plot-level means; 4–5 cores per transect serve as analytical replicates.
  - Data compatibility and reuse: provide both raw core-level data (where available) and aggregated plot-level means; flag that no outliers were removed to preserve data integrity.
  - Storage and preservation: maintain primary samples (soil cores, root blocks, rhizosphere material) with clear storage locations and conditions (-80°C for subsamples; - for ethanol-preserved roots) to support potential future analyses (e.g., DNA, isotopes).
  - Limitations and caveats: the dataset emphasizes means by transect and may not reflect within-plot variability; ensure users understand the averaging and replication treatment when reusing data for reanalysis.