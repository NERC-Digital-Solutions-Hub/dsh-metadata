# Collection methods

- Objective and scope
  - Re-check all large trees (>30 cm stem diameter in the most recent inventory) in permanent field plots to determine alive or dead status.
  - If dead, record mode of death (mostly standing dead or uprooted/snapped); if uprooted/snapped, record direction of fall and the approximate canopy gap size.
  - Danum Valley covers a contiguous 50 ha plot; Sepilok Reserve uses multi-scale plots (4 ha, 1 ha, 20x20 m subplots, and 5x5 m quadrats).

- Nature and units of recorded values
  - Alive/Dead: logical (binary) values.
  - Direction of fall: recorded in degrees from North.
  - Canopy gap size: qualitative categories (small, medium, large).

- Quality control
  - No formal quality control; data are provided as recorded in the field.

- Data structure and access
  - Each site provides a single CSV file containing the collected data.

- Danum Valley (50 ha plot)
  - Columns include: Tag (tree ID), Species, Dbh (Stem diameter at breast height, ~1.3 m), Hom (measurement height when 1.3 m not possible), Alive_2019 (mortality status), Direction_of_fall (degrees from North), Gap_size (small/medium/large), Notes.

- Sepilok Reserve (structured 4 ha plots with nested spatial scales)
  - Columns include: PlotID_4ha, Forest, PlotID_1ha, Subplot, Quadrat, TreeNo, Tno, IDNo2, Species, Diameter_1 (approx. 2010), Remarks_1, Diameter_2 (approx. 2015), Remarks_2, Remarks_2019, Mode_of_death (snapped or standing death), Direction_of_fall (degrees from North), GapSize (small/medium/large).

- Data linking and interpretation
  - Danum: Tag can be matched to census data for integration.
  - Sepilok: Uses multiple identifiers (PlotID_4ha, PlotID_1ha, Subplot, Quadrat, TreeNo, IDNo2) to identify individual trees across time; mortality status in 2019 is captured in Remarks_2019 and Mode_of_death.