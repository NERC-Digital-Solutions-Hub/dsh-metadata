# UrineNExcretionPerPatch.csv ReadMe

- Purpose and scope
  - Describes a dataset of nitrogen excretion per urine event (g N) in sheep, across semi-improved and improved pastures, for the Uplands-N2O project (grant NE/M015351/1).
  - Aimed at enabling environmental monitoring of N excretion and associated N losses, with clear provenance and data handling notes.

- Data collection and project context
  - Project: Uplands-N2O
  - Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick
  - Data reuse: fully cite the original source.

- Data processing and filtering
  - Observations with zero urination events were excluded.
  - Two replicate sheep (sheep 1 and 5) were removed due to relatively infrequent urine events.
  - Daily N excretion calculations assume the time spent in the urine collection apparatus (typically 10:00–16:00) represents a 24 h period.

- Variables and data structure
  - Data headers (columns):
    - Site: Semi-improved or improved pasture
    - Season: Spring, summer or autumn at the semi-improved site; autumn at the improved site
    - Sheep_ID: Identifier for the replicate sheep
    - Date: Date of urine collection (dd/mm/yyyy)
    - Vol_ml: Volume of an individual urine event (ml)
    - NContent: Nitrogen content of the urine event (g N L-1)
    - Nexcreted: Total nitrogen excreted in the urine event (g N)

- Calculation and interpretation notes
  - Nexcreted per event is provided as grams of nitrogen excreted.
  - Daily N excretion is derived from per-event data by assuming the 10:00–16:00 collection period is representative of a full 24 h day.

- Site and season definitions
  - Sites: Semi-improved pasture and improved pasture
  - Seasons: Spring, summer or autumn (for semi-improved site); autumn (for improved site)

- Data usage notes
  - Data are intended for monitoring environmental health and policy performance related to nitrogen excretion and potential N losses.
  - When reused, ensure full citation of the dataset.

- Quality assurance and data handling
  - Explicit filtration criteria (removal of zero-urination observations and certain low-frequency replicates) and documentation of the time window used for daily extrapolation.