# Malaysian heath forest tree DBH growth and change in leaf chemistry after fertilization.

## Aim
- Investigate the role of soil pH and soil nitrogen on heath forest tree growth.
- Examine how leaf element concentrations change in response to soil pH and nitrogen increases via a fertilization experiment in Kabili-Sepilok Forest Reserve, Sabah, Malaysia.

## Study system and context
- Heath forests are tropical, low-productivity systems on acidic, nutrient-poor soils (spodosols) with high endemism.
- Location: Kabili-Sepilok Forest Reserve, Sabah, Malaysia; equatorial climate (~26°C, ~3000 mm annual rainfall).
- Focus on ten most abundant tree species (representing 57% of stems ≥1 cm DBH and 49% of basal area).

## Experimental design and sampling regime
- Timeframe and plots:
  - 16 plots (15 m x 15 m) established in 2016.
  - Four fertilization treatments in July 2016: Control, Nitrogen (N) addition, Lime (CaCO3) addition, N + CaCO3, with four replicates per treatment.
- Nutrient treatments:
  - Lime pH adjustments based on pre-treatment soil pH measurements to avoid excessive pH rise; lime applications followed by nitrogen additions.
  - Lime application schedule: 75 kg plot-1 (Jul 2016) → 50 kg plot-1 (Feb 2017) → 25 kg plot-1 (Jul 2017) → no lime (Jan 2018) → 25 kg lime (Jul 2018).
  - Nitrogen (N) added with lime at 1.215 kg urea plot-1 per application (50 kg N ha-1 yr-1); applied with lime across the same time points.
- Measurements and sampling:
  - DBH measured three times: 2016, 2017, 2018.
  - Leaf sampling from the ten focal species in each plot: before fertilization (Apr 2016) and before each fertilizer application (Feb 2017, Jul 2017, Jul 2018); no sampling in Jan 2018.
  - Individual trees monitored across years; if a sampled tree died or was not found, replacement sampling used from same species within the plot.
  - Leaves collected from ~7 m height, oven-dried at 50°C, ground per tree per collection.

## Measurements and analyses
- Tree measurements:
  - DBH at 1.3 m (DBH_2016, DBH_2017, DBH_2018).
  - Data include notes on mortality, missing finds, or measurement details (e.g., broken, regrown) affecting growth calculations.
- Leaf chemistry:
  - Elements measured per leaf sample: Al, Ca, Cu, Fe, K, Mg, Mn, Na, Ni, P, S, Zn; plus carbon (C) and nitrogen (N).
  - Methods: acid microwave digestion followed by ICP-OES for most elements; CN elemental analyzer for C and N.
  - Quality controls: blanks and certified reference materials included in each batch.
  - Data include 16 element concentrations and two ratio metrics (CN, NP) for each sample.
- Data structure specifics:
  - Two main CSV files:
    - Heath forest DBH growth file: Plot, Treatment, Tree_Field_Number, Family, Genus, species, DBH_2016, DBH_2017, DBH_2018, Comments.
    - Leaf chemistry file: Plot, Treatment, Month, Year, Tree_Field_Number, Family, Genus, species, and 16 element columns plus CN and NP ratios.
  - Tree Field Numbers:
    - Unique identifiers; some plots include inserted entries for newly recruited trees; some entries use decimal suffixes (e.g., 818.2) to indicate proximity to another tagged tree.
  - Taxonomy fields may be blank for newly recruited individuals when identification was not possible.
  - Coordinates not recorded; stems not mapped to a geographic location within plots.

## Data details and caveats
- A dummy tag (636.665) was used for a leaf sample missing its original tree field number.
- Some DBH measurements were taken at different stem positions or on broken/regrown sections; such entries should be treated cautiously when computing stem growth.
- Leaves were collected from select individuals per plot; not every species present in all plots was sampled in every collection.
- Data are organized with headers in the first row of each CSV; column headers are not quoted.

## Key datasets and accessibility
- Two CSV datasets:
  - DBH growth across three census years (2016, 2017, 2018) by plot and treatment.
  - Leaf chemistry profiles across months/years, plots, treatments, and tree identifiers, including elemental concentrations and CN/NP ratios.
- Metadata describes plot identifiers (A–P), treatment codes, tree tagging conventions, and measurement protocols.

## Acknowledgments and funding
- Funded by Manchester Metropolitan University’s Environmental Science Research Centre.
- Acknowledges Sabah Biodiversity Council and staff across soil chemistry, ecology, wood science, herbarium, and laboratory facilities for field and lab assistance.

## References
- Sellan, G., Thompson, J., Majalap, N. & Brearley, F.Q., 2019. Soil characteristics influence species composition and forest structure differentially among tree size classes in a Bornean heath forest. Plant and Soil 438, 173-185.
- Sellan, G., 2019. Ecological Responses of a Bornean Heath Forest (kerangas) to Experimental Lime and Nitrogen Addition. PhD Thesis, Manchester Metropolitan University, UK.
- Sellan, G., Thompson, J., Majalap, N., Robert, R. & Brearley, F.Q., 2020. Impact of soil nitrogen availability and pH on tropical heath forest organic matter decomposition and decomposer activity. Pedobiologia 80, 150645.