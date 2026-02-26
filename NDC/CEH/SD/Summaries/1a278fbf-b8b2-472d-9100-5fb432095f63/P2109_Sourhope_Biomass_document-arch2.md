# NERC Soil Biodiversity Thematic Programme

## Objective and scope
- Established in 1999 to understand soil biodiversity and the functional roles of soil organisms in key ecological processes.
- Aims to combine study of biological diversity with ecosystem processes, spanning multiple organisms from bacteria to macro-fauna.

## Research design and scope
- 24 separate research projects funded to investigate soil structure, carbon and nitrogen cycles, and roles of micro-, meso-, and macro-fauna (Bacteria, Nematoda, Protozoa, Fungi, Collembola, Acari, Tipulid larvae, Scarabeid larvae, Enchytraeidae, Megradili, Mollusca, Coleoptera).
- Primary field site: Sourhope, Macaulay Land Use Research Institute (now James Hutton Institute) in the Scottish Borders.

## Methods and data collection
- Above-ground biomass (vegetation biomass) measurements conducted in 1999–2002:
  - 5 sampling occasions per year across 1999–2002.
  - 50 x 50 cm cells within each main plot; vegetation cut to ground level, sorted by species, oven-dried at 80°C, weighed.
  - Mineral nutrient analyses (N, Ca, K, Mg, P, Al) performed for July 1999 cuts.
  - Laboratory analyses by MLURI ( Aberdeen).
- Data structure and standardization:
  - Two CSV data files provided:
    - Biomass values, 1999–2001: P2109_VEG_BIOMASS_1999_2002.csv
    - Mineral nutrient analysis, 1999: P2109_BASELINE_99_VEG_MIN_ANAL.csv
  - Field definitions include: MEASID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, MEAS_DATE, BIOMASS; and for baseline: VEG_ID, CUT_DATE, NITROGEN, CALCIUM, POTASSIUM, MAGNESIUM, PHOSPHORUS, ALUMINIUM, with detection limits.

## Key findings
- Biomass showed a consistent hierarchy across treatments with peak production in July/August.
- Notable biomass increase in 2001, likely due to a change in personnel and a switch from manual cutting to mechanical shears.
- Normalization against a reference control (C1) recommended to assess lasting effects of nitrogen and lime on productivity.
- ANOVA on ln-transformed biomass data indicated:
  - Significant differences between improved (N and/or L added) vs. non-improved plots.
  - Significant interaction between treatment and year.
  - No significant differences between blocks.

## Data availability, structure, and usage
- Data are stored in clearly described datasets with defined variable names and units.
- Metadata describes measurement methods, treatments, and sampling design, enabling reuse for ecological monitoring and comparative analyses.
- Related documentation: Scott et al., 2003 (SOURHOPE FIELD DATA HANDBOOK 2003), available via the EIDC catalogue.

## Quality control and limitations
- Verification procedures included numeric range checks, format conformity, and logical integrity checks.
- Laboratory analyses conducted under MLURI quality procedures.
- The data are quality-assured but not warranted for accuracy by NERC; no liability for fitness-for-use is assumed by the program or data providers.

## Implications for monitoring and data practices
- Demonstrates a rigorous, standardized approach to environmental monitoring data, with explicit QA steps and transparent data structure.
- Highlights challenges and opportunities relevant to Analysts Monitoring the Environment:
  - Increasing the value of monitoring datasets by combining with additional relevant data.
  - Enabling broad access to underlying data used to generate outputs and ensuring datasets are stored in accessible portals.