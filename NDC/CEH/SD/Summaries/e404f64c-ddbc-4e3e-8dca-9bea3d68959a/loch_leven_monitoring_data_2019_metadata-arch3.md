# Loch Leven long-term monitoring dataset

- Overview
  - Dataset from Loch Leven, a lowland Scottish lake, collected as part of a long-term monitoring programme that began in 1968 and is ongoing.
  - Observations conducted by staff from NERC and later the NERC/UK Centre for Ecology & Hydrology.
  - Describes data nature, sampling/analysis methods, data processing, and output format; tied to project UK-SCAPE WP7 LEVEN.

- Sampling regime
  - Fortnightly sampling with two main sites per occasion: Reed Bower (RB) and Sluices (L).
  - RB: boat-access only; L: boat or shore sampling feasible.
  - Weather/resource constraints can prevent sampling; in some cases only one site or neither site is sampled.
  - Measurements taken in the field or in the laboratory from field samples.

- Sampling sites
  - Harbour (H), Reed Bower (RB/RB5), and Sluices/Outflow (L/Sl8) with UK National Grid coordinates.
  - Site codes appear in data columns and tables to identify measurements by location.

- Measurements and analyses
  - In situ measurements: conductivity, pH, temperature at most sites; Secchi depth at Reed Bower.
  - Water sampling: two 2 L duplicates per site; integrated sampling at RB using a weighted PVC tube; surface sampling at L with a bottle.
  - Laboratory analyses (from filtered and unfiltered aliquots): soluble reactive phosphorus (SRP), total soluble phosphorus (TSP), total phosphorus (TP), soluble reactive silicate, total diatom silica, and chlorophyll a.
  - Phosphorus measurements based on established methods (Murphy & Riley 1962 for SRP; Wetzel & Likens 2000 for TP/TSP) with standard digestion for TP.
  - Weather data recorded at Reed Bower when possible; wind force linked to a detailed Beaufort-based table.

- Crustacean & zooplankton
  - Densities of crustacean zooplankton collected at RB and L, measured as individuals per litre (ind/L) for taxa including Daphnia hyalina, Eudiaptomus gracilis, Eudiaptomus nauplii, Cyclopodidae, Cyclops abyssorum, Cyclops vicinus, Bosmina longirostris, Leptodora kindti, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus.
  - Sampling methods: RB (4 m net haul, 120 µm mesh); L (surface water filtered through 120 µm net).
  - Samples preserved in 4% formaldehyde, analyzed in the lab by subsampling and counting under a microscope; taxa identified to species level where possible; counts converted to ind/L and archived.

- Data processing
  - Data imported with an R script that applies predefined sensibility rules.
  - Wind force: when presented as a range (e.g., 4-5), the first value is used.
  - Probe replicates (conductivity, pH, DO, and related temps): replicated values retained if within Median ± MAD; extreme cases excluded according toMAD logic; pH values transformed for median/MAD calculation and back-transformed for final value; other measurements rounded (pH/DO to 2 decimals, conductivity and temps to 1 decimal).
  - Quality assurance: automated and manual checks for entry errors and out-of-range values; anomalies investigated and corrected.
  - Replicates and measurement handling described in detail to ensure traceability.

- Format and metadata
  - Data stored in a single CSV file with columns detailing determinand, site conditions, lake chemistry, and crustacean/zooplankton counts.
  - Missing data values are marked as NA.
  - Column descriptions (Table 3) provide full meanings, units, site associations, and the relation of columns to measurements (e.g., Date, Week_of_Year, various site-specific measurements, and taxa densities).

- Column descriptions and structure
  - Column names encode determinand, site, and units; examples include Date, Week_of_Year, Weather/Cloud conditions, site-specific conductivity, temperature, dissolved oxygen, pH, TP/SRP/TSP, chlorophyll a, and zooplankton densities.
  - Includes both replicated measurements (e.g., RB1/RB2) and site-level aggregates; table documents provide detailed interpretation.

- References and methodological foundations
  - Field and laboratory methods anchored to established references (e.g., Murphy & Riley 1962; Wetzel & Likens 2000; Golterman et al. 1978) and standard hydrobiological identification guides.

- Relevance for monitoring and governance
  - Provides long-term, multi-parameter environmental health indicators (water chemistry, clarity, temperature, biological communities) across two key sites.
  - Demonstrates comprehensive data processing, QA, and metadata practices essential for policy scrutiny, data sharing, and transparent reporting.
  - Highlights the integration of chemical and biological monitoring with standardized documentation to support policy evaluation and future decision-making.