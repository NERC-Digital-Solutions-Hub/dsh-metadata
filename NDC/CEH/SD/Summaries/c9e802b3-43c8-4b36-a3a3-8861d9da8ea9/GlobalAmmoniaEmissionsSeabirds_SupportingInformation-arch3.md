# Ammonia Global Emissions from Seabirds (AGES) version 1

- Purpose: Provide NH3 emissions estimates from seabird colonies globally to inform environmental health monitoring, policy scrutiny, and decision-making. The dataset supports evaluating ammonia budgets and guides future actions.

- Data characteristics:
  - Spatial resolution: 0.1 degree latitude/longitude grid cells.
  - Units: megagrams of NH3 per grid cell per year (Mg NH3 gridcell-1 year-1).
  - Data precision: rounded to 2 significant figures.
  - Publication requirement: any use of the data must cite the accompanying publication.

- Scenarios for emissions factors:
  - Scenario 1: Emission factors based on mid-latitude measurements applied globally (independent of colony temperature).
  - Scenario 2: Emission factors with thermodynamic temperature dependence (dependent on temperature at seabird colonies; uses Henry's Law and dissociation equilibria).
  - Scenario 3 (best estimate): Limited temperature dependence; mean of Scenarios 1 and 2.

- Publication citation:
  - S. N. Riddick, U. Dragosits, T. D. Blackall, F. Daunt, S. Wanless and M. A. Sutton (2012) The global distribution of ammonia emissions from seabird colonies. Atmospheric Environment (in press) DOI:10.1016/j.atmosenv.2012.02.052

- Implications for monitoring and governance:
  - Provides a global spatially explicit input for air quality and environmental health assessments, enabling policy evaluation of seabird-derived NH3 contributions.
  - Useful for scenario analysis and trend assessment in ammonia budgets, supporting decisions on emissions controls and ecological risk.
  - Highlights the need for clear data provenance, versioning, and citation to ensure traceability and reproducibility in monitoring programs.

- Data quality, access, and governance considerations for adopters:
  - Metadata availability and completeness are essential to verify applicability to monitoring needs.
  - The requirement to publicly quote the dataset’s publication may influence data sharing and reuse policies.
  - Data users should be aware of the rounding (2 sig figs) which affects precision and uncertainty characterization.
  - Systems should capture and communicate the three scenario options, with transparent rationale for selecting the best-estimate approach in reporting.

- Practical considerations for monitoring frameworks:
  - Integrate the dataset with metadata standards and data provenance records.
  - Ensure mechanisms to access, transform, and visualize gridded NH3 emissions data.
  - Establish data governance processes to manage updates, version control, and citation requirements.