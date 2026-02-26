# GMEP_TOPSOIL_MESOFAUNA_2013_14.csv

## Aim and scope
- Wales-wide soil mesofauna monitoring as part of the Glastir Monitoring and Evaluation Programme (GMEP).
- 4-year rolling survey (2013–2016) to assess soil health, climate, biodiversity, and land-use drivers; aims to quantify status and trends in soil quality beyond Glastir interventions.
- Two components: Wider Wales (baseline and national trends) and Targeted (Glastir priority areas); common 1 km grid for integration.

## Survey design and sampling framework
- 300 x 1 km squares sampled over the 4-year cycle.
- Sampling approach mirrors Countryside Survey of Great Britain for robust national and sub-national estimates.
- Exclusion criteria: squares with >75% urban land or >90% sea.
- Sampling units mapped and plotted with confidentiality (data aggregated to 10 km for maps).
- Sampling within each square: 5 pre-determined random locations for soil cores.

## Sample collection and processing
- Soil sampling: 5 cores per square, collected using white plastic 8 cm core (F-core) at vegetation survey locations.
- Cores sent promptly to Centre for Ecology & Hydrology (CEH), Lancaster for faunal extraction.
- Dry extraction: Tullgren funnels used to extract soil fauna over ~5 days; 70% ethanol preservative in collection bottles.
- Data collection fields captured on sheets and entered into Excel (e.g., SQXN, depth, start/stop times).
- Equipment and preparation: core extractor, Tullgren funnels, ethanol, labeling, and recording materials.

## Invertebrate identification and data recording
- Objective: separate mesofauna from debris and identify to broad groups (mites, Collembola, etc.) as defined in the protocol.
- Identification categories include Oribatid mites (Box and Other), Mesostigmatid mites, Poduromorph Collembolans, Entomobryoid Collembolans, Symphypleona/Neelipleona, and total counts for mites, Collembola, and mesofauna.
- Processing steps: rinse, sort under a stereomicroscope, allocate specimens into labeled blocks, tally in recording notebook, and transfer to glass vials with SQXN labels.
- Quality control: 1 in 20 samples double-checked by a second staff member to ensure consistency; data later entered into Excel.
- Training: minimum one-week familiarisation with broad-group identification and mock samples.

## Data management, QA, and integration
- Data management and QA embedded in the workflow; outputs integrated into CEH Bangor database.
- QA framework aligned with the DEFRA Joint Code of Practice for Research (JCoPR); cross-check process documented.
- Data entry practices emphasize timely transfer from recording notebooks to Excel.

## Data structure and variables (CSV content)
- Core dataset: GMEP_TOPSOIL_MESOFAUNA_2013_14.csv (Counts of soil mesofauna from 1 km plot squares across Wales; 2013–2014).
- Key variables include:
  - YEAR (2013-2014)
  - SQ_ID (1 km square identifier)
  - PLOT_TYPE (e.g., main vegetation plot)
  - PLOTNUM (plot number within square)
  - EASTING_10KM/NORTHING_10KM (OSGB 1936 coordinates at 10 km resolution)
  - LC (ITE Land Classification)
  - CORE_TAKEN (Yes/Not received)
  - MITE_ORIB_BOX (Oribatid box mites count)
  - MITE_ORIB_OTHER (Other Oribatid mites)
  - MITE_MESO (Mesostigmatid mites)
  - MITE_OTHER (Other Acarids)
  - COL_POD (Poduroid Collembolans)
  - COL_ENTO (Entomobryoid Collembolans)
  - COL_SYMP (Symphypleona/Neelipleona Collembolans)
  - ENCHY (Enchytraeid count; noted as potentially unreliable)
  - OTHERS (Other invertebrates)
  - MITE_ORIB_TOTAL (sum of Oribatid mites)
  - TOTAL_MITES (sum of mite groups)
  - TOTAL_COLL (sum of Collembola groups)
  - TOTAL_MESO (total mites and Collembola)
  - TOTAL_INVERT (TOTAL_MITES + TOTAL_COLL)
- Totals are derived aggregates for quality control and downstream analyses.

## Roles, responsibilities and field teams
- Appendix 1 outlines the project and field team roles, including lead scientists, data managers, field coordinators, sample sorting, and data tracking.
- Field survey teams comprise numerous named personnel across Wales, with designated field coordination and sample sorting duties.

## Health, safety, and training
- Health and safety: ethanol handling and storage; risk assessments in place for ethanol-containing samples.
- Training: formal training plan for staff to ensure competency in identification, sorting, and data handling; emphasis on QA and mock sample practice.

## References and context
- References include landscape classification (ITE Land Classification), soil fauna keys, and Glastir Monitoring & Evaluation Programme reports, establishing methodological precedent and integration with national surveys.

## Appendix highlights
- Roles and field team lists provide organizational structure for sample handling, data management, and field operations.