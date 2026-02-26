# Long-term vegetation monitoring data from the Hard Hill burning plots, Moor House, 1954-2013. Rose, R.J., Marrs, R.H., O'Reilly, J. & Furness, M.

## Experimental design
- Location: Moor House National Nature Reserve, OS grid NY730320.
- Four replicate blocks (A–D) with altitude from 594 m to 625 m.
- Randomized split-plot layout: each block contains fenced (excludes grazing) and unfenced strips (grazed by sheep), each 90 m by 60 m, further divided into two 90 m by 30 m strips.
- Within each strip, three 30 m by 30 m cells were assigned to sub-treatments: no burning (N), short rotation burn (S, every ~10 years), and long rotation burn (L, every ~20 years).
- All plots were burnt initially in 1954; subsequent burns occurred in 1954/55, 1964/65, 1974/75, 1984/85, 1994/95, 2006/07, and 2016/17 (with the 2006/07 burn slightly delayed).
- Burning aimed to remove surface vegetation and litter without deep peat combustion.

## Initial sampling regime and data collection (1961 and 1965)
- Post-burn vegetation recorded using quadrats and the DOMIN cover scale (9–1).
- 1961: twenty-five 1 m² quadrats per plot positioned on a 5 m grid across all plots in each block (quadrats 1–25).
- 1965: measurements limited to N, fenced, and unfenced treatments; quadrats reduced to 10 per plot (recording points 6–15).
- Quadrats used the DOMIN scale for cover estimates; early data labeled with Year, Block, Treatment, Fenced status, Quadrat, DOMIN score, Species number, and Species name (updated nomenclature where needed).

## Data collection methods and instrumentation (1972 onwards)
- From 1972, vegetation recorded with pin quadrats during the 8th growing season (July–August); years: 1972, 1982, 1992, 2001, 2013.
- Plot structure: within each 30 m × 30 m cell, a central recording plot of 14 m × 6 m, with 7 transects and 6 quadrats per transect (positions 1–6 along the transect; side A or B).
- Each plot contains 82 1 m × 1 m quadrats in total.
- Pin frame: 1 m long frame with 10 pin positions at 10 cm intervals. For each quadrat, 5 frame positions are used, and one pin is recorded at each position (1–5 along the frame). Pins are randomly assigned to frame positions.
- Vegetation stratification: four height strata recorded for vascular plants ( >30 cm, 20–30 cm, 10–20 cm, 0–10 cm). Non-vascular plants, bryophytes, lichens, and non-living material are recorded as unstratified (designated 99) with presence/absence or touches depending on the data type.
- Sampling: 20 quadrats per treatment per block per survey (4 treatments × 4 blocks = 16 quadrats; 20 quadrats per treatment per block per survey yields 480 quadrats per survey year).
- Data details: within each quadrat, 5 frame positions and 10 pin positions recorded; scores reflect the number of touches per species within each height strata (for vascular plants). Non-vascular and unstratified data use presence/absence or 1-touch conventions as applicable.

## Fieldwork and laboratory instrumentation
- Permanent fences indicate the main blocks; smaller wooden markers define treatment extents and the central vegetation recording plot (14 m × 6 m).
- Equipment includes the quadrat methods (1961/1965) and the pin frame with standardized positioning and stratification.

## Quadrat method (1961 and 1965)
- Data type: species area/abundance within 1 m² quadrats.
- Datasets: single CSV with columns for Year, Block (A–D), Treatment (N, L, S), Fenced (UF, F, grazed), Quadrat (1–25), DOMIN score, Species number, Species name.

## Pin method (1972 onwards)
- Data type: absolute counts (number of pin touches) per species across four height strata or presence/absence (depending on survey date and block).
- Non-vascular plants and non-living material recorded by un-stratified presence/absence; vascular plants recorded in strata when applicable.
- Datasets: single CSV with columns for Year (1972, 1982, 1992, 2001, 2013), Block, Treatment (N, L, S), Fenced (UF, F, grazed), Stratified (s or u), Transect (A–B across 7 transects), Quadrat (1–6), Frame (1–5), Pin (position along frame), Strata (1–4 or 99), Score (touch counts where applicable), Species number, Species name.

## Quality control and data integrity
- Surveys conducted by experienced botanical surveyors in pairs using standardized methods and equipment to ensure consistency across years.

## Datasets and metadata structure
- Quadrat method (1961/1965): CSV with Year, Block, Treatment, Fenced, Quadrat, DOMIN score, Species number, Species name.
- Pin method (1972 onwards): CSV with Year, Block, Treatment, Fenced, Stratified, Transect, Quadrat, Frame, Pin, Strata, Score, Species number, Species name.
- Species codes align with the Environmental Change Network (ECN) database (VESPAN numbers).

## Related resources
- Supporting documents include: 
  - Marrs et al. (1986) Long-term studies of vegetation change at Moor House NNR: guide to recording methods and the database.
  - Adamson & Kahl (2001) Changes in vegetation at Moor House within sheep exclosure plots established 1953–1972.
  - www.ecn.ac.uk