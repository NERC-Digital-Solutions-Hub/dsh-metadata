# Malaysian heath forest tree DBH growth and change in leaf chemistry after fertilization.

- Purpose and GIS relevance
  - Study of how soil pH and nitrogen influence heath forest tree growth and leaf element concentrations after lime (CaCO3) and nitrogen fertilization.
  - Data suitable for map-based analysis of treatment effects across a grid of plots and for linking spatial patterns to species composition and leaf chemistry.

- Study area and sampling design
  - Location: Kabili-Sepilok Forest Reserve, Sabah, Malaysia.
  - Environment: equatorial climate, approx. 26°C mean temp, ~3000 mm annual rainfall.
  - Experimental setup: 16 plots, each 15 m x 15 m; four fertilization treatments (Control, N, CaCO3, N+CaCO3) with four replicates per treatment.
  - Plot identifiers: plots labeled a to p.
  - Trees: stems ≥1 cm DBH tagged and identified to species; initial homogeneity checks across plots prior to treatment.

- Datasets and data structure (GIS-ready framing)
  - Heath forest DBH growth file
    - Key fields: Plot, Treatment, Tree_Field_Number, Family, Genus, species, DBH_2016, DBH_2017, DBH_2018, Comments.
    - Notes: Tree_Field_Number is a unique field-tag identifier; some stems added or re-tagged with decimal suffixes (e.g., 818.2) to indicate proximity to existing trees or recruit status. No coordinates are provided for individual stems; no mapping of tree positions.
    - Data quality: DBH measurements include special cases (death, not found, broken/regrown), which may affect growth calculations; some measurements taken at alternative stem locations.
  - Leaf chemistry file
    - Key fields: Plot, Treatment, Month, Year, Tree_Field_Number, Family, Genus, species, 16 elemental concentrations (N, C, Mg, P, Al, Ca, Cu, Fe, K, Mn, Na, Ni, S, Zn) with units, plus CN and NP ratios.
    - Notes: One leaf sample has a dummy Tree_Field_Number (636.665) due to missing original number; stems not georeferenced in this dataset.
  - Data format and provenance
    - CSV format with headers in the first row; no quotation marks in headers.
    - Leaves collected in 2016 and 2017, and 2018 (months specified for leaf sampling); DBH measured in 2016, 2017, and 2018.

- Spatial and GIS considerations
  - Plot-level spatial units: 16 plots with fixed boundaries; no internal tree coordinates in dataset.
  - Linking datasets: Tree_Field_Number serves as the key to join DBH and leaf data at the species level within plots and treatments.
  - Mapping opportunities and limitations:
    - Create plot-level maps showing treatment groups, mean DBH growth by year, and plot-level leaf chemistry summaries by species.
    - Linking to richer spatial data (e.g., soil pH, plot boundaries) would enable broader map-based analyses, but individual tree locations are not provided.

- Taxonomy and species context
  - Focused on the ten most common species across plots (representing substantial fractions of stems and basal area).
  - Species list includes Actinodaphne borneensis, Chionanthus pluriflorus, Cotylelobium melanoxylon, Diospyros fusiformis, Dracaena elliptica, Gaertnera junghuhniana, Pimelodendron griffithianum, Syzygium sp., Ternstroemia aneura, and Tristaniopsis obovata.

- Temporal scope and data coverage
  - DBH measurements: three time points (June 2016, August 2017, August 2018).
  - Leaf chemistry: sampling in 2016 (before treatment) and multiple time points in 2017 and 2018 (specific months noted in dataset).
  - Treatments and plotting: factorial combination of N and lime with four replicates per treatment.

- Data quality controls and caveats for GIS use
  - Initial homogeneity tests performed to ensure comparable starting conditions across plots.
  - Some DBH entries may be affected by measurement location (and not suitable for growth calculations) indicated in the Comments field.
  - Missing coordinates for stems; plot-level spatial analysis is feasible, but precise tree-level mapping requires additional spatial data.
  - One leaf sample has a placeholder tree number, highlighting potential linking considerations across datasets.

- Practical GIS applications
  - Create a plot-level treatment map and overlay with plot-level DBH growth statistics across years.
  - Visualize leaf nutrient profiles by plot and by dominant species, and examine how N and CaCO3 fertilization affects leaf chemistry over time.
  - Link DBH and leaf chemistry through Tree_Field_Number to build integrated datasets for spatial trend analysis by species and treatment.
  - Combine with external soil or environmental layers (pH, nitrogen availability, soil type) to explore drivers of growth and foliar chemistry in a geospatial context.

- References and acknowledgments (contextual, not GIS-critical)
  - Background literature and related datasets cited; study funded by Manchester Metropolitan University and Sabah-based partners.