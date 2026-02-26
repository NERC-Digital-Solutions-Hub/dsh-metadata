# Collection methods

- Purpose and approach
  - Revisit all large trees (>30 cm stem diameter) in permanent field plots to determine alive vs dead status.
  - For dead trees, record mode of death (mostly standing dead or uprooted/snapped).
  - If a tree has uprooted or snapped, record direction of fall and approximate canopy gap size.

- Nature and units of recorded values
  - Alive/Dead: logical values.
  - Direction_of_fall: recorded in degrees from North (0–360).
  - Gap_size: qualitative category (small, medium, large).

- Quality control
  - No formal quality control documented; data are provided as recorded in the field.

- Details of data structure
  - Danum Valley (50 ha plot)
    - Data file: single CSV per site.
    - Columns:
      - Tag (tree ID; matchable to census data)
      - Species
      - Dbh (Diameter at breast height; ~1.3 m)
      - Hom (Height of measurement when 1.3 m measurement not possible, e.g., due to buttresses)
      - Alive_2019 (mortality status: dead or alive)
      - Direction_of_fall (if fallen; from North)
      - Gap_size (approximate; small/medium/large)
      - Notes
  - Sepilok Reserve (multiple nested plots)
    - Data columns reflect a hierarchical sampling design (4 ha plots, 1 ha subplots within 4 ha plots, 20×20 m subplots within 1 ha, and 5×5 m quadrats within 20×20 m).
    - Core columns include:
      - PlotID_4ha, Forest, PlotID_1ha, Subplot, Quadrat
      - TreeNo (Tree ID within the 4 ha plot)
      - Tno (multi-stemmed tree identifier; not used)
      - IDNo2 (unique tree ID)
      - Species
      - Diameter_1 (initial diameter around 2010)
      - Remarks_1 (categorical description; e.g., snapped or missing)
      - Diameter_2 (diameter around 2015)
      - Remarks_2 (categorical description)
      - Remarks_2019 (mortality survey description)
      - Mode_of_death (snapped or died standing)
      - Direction_of_fall (degrees from North)
      - GapSize (qualitative estimate of gap size: small/medium/large)

- Additional context on datasets
  - Danum Valley collects a focused set of fields for a single contiguous plot, enabling straightforward matching to census data.
  - Sepilok Reserve provides a multi-level, multi-year history of diameter measurements and mortality indicators across a nested plot system, with explicit changes in diameter and mortality descriptors over time.

- Key phenomena captured
  - Mortality status of large trees, modes of death, directional context of windthrow or failure, and associated canopy gaps.
  - Temporal perspective through multi-year diameter data (where available) and 2019 mortality survey results.