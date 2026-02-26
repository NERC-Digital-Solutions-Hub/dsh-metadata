# Collection methods

- Data collection involved re-visiting all large trees (>30 cm stem diameter in the most recent inventory) in permanent field plots to determine alive/dead status.
- For dead trees, the mode of death was recorded (mostly standing dead or uprooted/snapped).
- If uprooted or snapped, the direction of fall and the estimated canopy gap size (small, medium, large) were recorded.

## Nature and Units of recorded values

- Alive_2019 and Dead: logical values indicating the living status.
- Direction_of_fall: recorded in degrees from North.
- Gap_size: qualitative canopy gap size (small, medium, large).

## Quality control

- None: data are provided exactly as recorded in the field (no post-collection quality control).

## Details of data structure

- Each site provides data in a single CSV file.

### Danum Valley
- Covers the entire contiguous 50 ha plot.
- Key columns:
  - Tag: tree ID (matchable to census data)
  - Species
  - Dbh: stem diameter at breast height (≈1.3 m)
  - Hom: height of measurement when 1.3 m measurement not possible (e.g., due to buttresses)
  - Alive_2019: mortality status (dead or alive)
  - Direction_of_fall: direction of fall (from North)
  - Gap_size: approximate canopy gap size (small, medium, large)
  - Notes

### Sepilok Reserve
- Structure includes nested plots: 4 ha plots (PlotID_4ha), 1 ha subplots (PlotID_1ha within each 4 ha plot), 20x20 m subplots (Subplot within each 1 ha), and 5x5 m quadrats ( Quadrat within each 20x20 m subplot).
- Key columns:
  - PlotID_4ha: ID of the 4 ha plot
  - Forest: forest type
  - PlotID_1ha: ID of the 1 ha subplot within the 4 ha plot
  - Subplot: ID of the 20x20 m subplot within the 1 ha subplot
  - Quadrat: ID of the 5x5 m quadrat within the 20x20 m subplot
  - TreeNo: tree ID within the 4 ha plot
  - Tno: unique ID for multi-stemmed trees (not used)
  - IDNo2: unique tree ID
  - Species
  - Diameter_1: initial diameter measurement (≈2010)
  - Remarks_1: descriptive status (e.g., snapped, missing)
  - Diameter_2: second diameter measurement (≈2015)
  - Remarks_2: descriptive status (e.g., snapped, missing)
  - Remarks_2019: mortality status in 2019
  - Mode_of_death: whether the tree snapped or died standing
  - Direction_of_fall: direction of fall in degrees from North
  - GapSize: qualitative gap size (small, medium, large)

## How the data can be used (data support perspective)

- Enable cross-site comparisons of mortality and fall direction, and analysis of canopy disturbance via gap sizes.
- Link with census data (Tag matches) to analyse relationships between growth (diameter) and mortality.
- Build self-serve data products (dashboards, pivot tables) for stakeholders to inspect alive/dead status, mode of death, and canopy disturbance by plot.
- Combine the Danum Valley and Sepilok datasets to explore broader patterns across different forest types and plot designs.

## Considerations for data users

- No post-collection quality control is provided; data reflect field records as recorded.
- Each site’s data is stored in a single CSV file, facilitating straightforward ingestion and joining with other datasets via identifiers (e.g., Tag, Plot IDs).