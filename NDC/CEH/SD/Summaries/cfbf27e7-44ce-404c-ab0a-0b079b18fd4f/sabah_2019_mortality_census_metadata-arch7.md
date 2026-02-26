# Collection methods

- Data collected by revisiting all large trees (>30 cm stem diameter) in permanent field plots to determine alive/dead status.
- For dead trees, recorded mode of death (mostly standing dead or uprooted/snapped). If uprooted/snapped, recorded direction of fall and estimated canopy gap size.

## Nature and Units of recorded values

- Alive/dead recorded as logical values.
- Direction of fall recorded in degrees from North.
- Canopy gap size estimated as small, medium, or large.

## Quality control

- None; data are provided as recorded in the field.

## Details of data structure

- Each site has a single CSV file.
- Danum Valley (50 ha plot):
  - Columns: Tag, Species, Dbh (diameter at breast height, ~1.3 m), Hom (height of measurement when 1.3 m not possible, e.g., buttresses), Alive_2019, Direction_of_fall, Gap_size, Notes.
- Sepilok Reserve (nested 4 ha plots with 1 ha and 20x20 m subplots):
  - Hierarchy: PlotID_4ha, Forest, PlotID_1ha, Subplot, Quadrat, TreeNo, Tno (multi-stem indicator), IDNo2 (unique tree ID), Species, Diameter_1 (approx. 2010), Remarks_1, Diameter_2 (approx. 2015), Remarks_2, Remarks_2019 (mortality status), Mode_of_death (snapped or dead standing), Direction_of_fall, GapSize (small/medium/large).