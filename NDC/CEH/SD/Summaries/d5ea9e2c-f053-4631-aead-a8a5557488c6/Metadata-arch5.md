# Malaysian heath forest tree DBH growth and change in leaf chemistry after fertilization.

## Overview and Aim
- Investigates how soil pH and soil nitrogen influence tree growth (DBH) and leaf element concentrations in a Bornean heath forest.
- Conducted in Kabili-Sepilok Forest Reserve, Sabah, Malaysia, using N and lime fertilization to assess responses in ten common tree species.

## Experimental Design and Sampling
- 16 plots (15 m x 15 m) established in 2016.
- Four fertilization treatments with four replicates each: Control, N addition, lime (CaCO3) addition, and N + lime.
- Lime application rates adjusted to avoid excessive pH increase; first lime application in 2016, with subsequent adjustments in 2017 and 2018.
- Nitrogen applied uniformly (1.215 kg urea per plot per event; ~50 kg N ha-1 yr-1) to offset rapid losses.
- Focused on the ten most common species (representing 57% of stems ≥1 cm DBH).
- Leaf sampling: about ten leaves per focal species per plot, before fertilization and at specified times (April 2016 baseline; February 2017, July 2017, June 2018), using the same individual trees when possible.
- DBH measured for each tree in 2016, 2017, and 2018; notes record deaths, missing trees, and measurement adjustments (e.g., broken stems, new measurement locations).

## Data Collected and Measurements
- DBH data: DBH_2016, DBH_2017, DBH_2018 for each tree; fields include Plot, Treatment, Tree_Field_Number, Family, Genus, species; Comments capture mortality or measurement caveats.
- Leaf chemistry data: for the same plots and trees, monthly sampling time points (Month, Year) with Tree_Field_Number, Taxonomy columns, and 16 elemental concentrations (N, C, Mg, P, Al, Ca, Cu, Fe, K, Mn, Na, Ni, S, Zn) plus CN and NP ratios.
- Analytical methods: leaf digestion and ICP-OES for most elements; CN analysis for carbon and nitrogen; use of blanks and certified reference materials to ensure accuracy.
- Data notes: some identifications missing for new recruits; dummy Tree_Field_Number used if field number lost; one Pimelodendron griffithianum leaf sample had a missing field number and was assigned 636.665 as a placeholder.

## Data Structure and Files
- Data stored as comma-separated value (.csv) files with headers in the first row (no quoted headers).
- Heath forest DBH growth file:
  - Plot (a–p), Treatment (Control, N, CaCO3, N+CaCO3), Tree_Field_Number (unique tag-based ID), Taxonomy (Family, Genus, species; may be empty for some recruits), DBH_2016, DBH_2017, DBH_2018, Comments.
  - Notes on measurement placement and interpretation for growth calculations (e.g., broken, regrown; liana status).
- Leaf chemistry file:
  - Plot, Treatment, Month, Year, Tree_Field_Number, Taxonomy (Family, Genus, species), 16 element concentration columns (N, C, Mg, P, Al, Ca, Cu, Fe, K, Mn, Na, Ni, S, Zn), plus CN (ratio) and NP (ratio).
  - Acknowledge data gap: one missing Tree_Field_Number for a leaf sample; a dummy number used as a placeholder.
  - Coordinates not provided; stems not geolocated.

## Data Quality Assurance and Processing
- Consistent sampling protocols across plots and years.
- Use of standardized lab procedures (microwave digestion, ICP-OES, CN analyzer) with blanks and certified references to validate accuracy.
- Consistent tagging and identification of focal species; explicit handling instructions for missing or damaged measurements to ensure data integrity.
- Documentation notes address potential data quality issues (e.g., measurement location changes, dead or not found trees, liana status).

## Accessibility, Sharing, and Reuse
- Data are organized into clearly defined CSV files with explicit column semantics and units described in the dataset documentation.
- Metadata within the data files cover plot identifiers, treatments, sampling times, taxonomy, and measurement methods, facilitating discovery and reuse.
- Although not stated, the structure supports integration into data portals and catalogues; however, coordinates and some provenance details are limited within the files.

## Data Stewardship Considerations and Challenges
- Alignment with data governance aims: clear data structure, standardized treatments, consistent metadata, and documented QA procedures.
- Challenges highlighted by the study context that affect stewardship:
  - Incomplete or updated understanding of user needs (e.g., potential users may require coordinates or broader taxonomic coverage).
  - Timely access to data across multiple years and plots, with updates during and after fertilization events.
  - Variability across many systems and formats (field tagging conventions, missing taxonomy, non-geolocated plots).
  - Large, multi-year, multi-species datasets with detailed measurement records and occasional data gaps (missing Tree_Field_Numbers, new recruits).
  - The need to document data provenance, measurement methods, and any deviations from protocols to enable correct interpretation and reuse.

## References
- Sellan, G., Thompson, J., Majalap, N. & Brearley, F.Q., 2019. Soil characteristics influence species composition and forest structure differentially among tree size classes in a Bornean heath forest. Plant and Soil 438, 173-185.
- Sellan, G., 2019. Ecological Responses of a Bornean Heath Forest (kerangas) to Experimental Lime and Nitrogen Addition. PhD Thesis, Manchester Metropolitan University, UK.
- Sellan, G., Thompson, J., Majalap, N., Robert, R. & Brearley, F.Q., 2020. Impact of soil nitrogen availability and pH on tropical heath forest organic matter decomposition and decomposer activity. Pedobiologia 80, 150645.