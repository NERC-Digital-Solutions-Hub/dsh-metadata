# Data overview:

- Study context
  - Insect visitation to flowers from wildflower seed mixes tested on two farms: Church Farm, Oxfordshire and Lee Farm, West Sussex.
  - Plot design: 20 x 5 m contiguous plots receiving four different seed mixes plus a control fallow.
  - precise locations recorded (lat/long) for both farms.

- Data collection timeline and procedure
  - Surveys conducted April–August in 2019, 2020, and 2021.
  - Each year had eight survey periods; surveys occurred every 2–3 weeks.
  - On each survey period, farms were visited on two separate days.
  - Within each survey, each plot was walked centrally; insects visiting flowers within 2 m were observed on the wing or captured for lab identification.

- Taxonomic scope and identification
  - Insect visits recorded at a broad taxonomic level (Insect.taxa) and, where possible, identified to genus and species for bees, hoverflies, and butterflies.
  - Groups recorded: hoverfly, other fly, solitary wasp, solitary bee, bumblebee, honeybee, beetle, butterfly.
  - Specimens not identifiable in the field were sent to experts for confirmation: bee identifications by Steven Falk and hoverfly identifications by Ellen Rotheray; sub-samples used to ensure accuracy.

- Data structure and variables
  - Data stored in InsectData.csv with 14 columns:
    - Year, Date, Month, Period
    - Farm, PlotID
    - Mix (seed mix treatment), Replicate
    - Flower.family, Flower.species
    - Insect.taxa, Insect.genus, Insect.species
    - Sex (sex of the insect)
  - Field-collected observations include visits to flowers by insect groups, with species-level detail for some taxa.

- Quality control and data integrity
  - Visual identifications reinforced by lab verification and expert consultations to ensure species accuracy across the dataset.
  - Use of sub-samples for verification and referral of uncertain identifications to specialists.

- Analytical potential
  - Assess how different seed mixes influence visitation by specific insect groups and species.
  - Compare visitation patterns across farms, years, and survey periods.
  - Evaluate relationships between flower family/species and insect visitation.
  - Explore temporal trends and potential interactions between management treatments and pollinator groups.

- Limitations and considerations for analysts
  - Data are plot-level observations from only two farms, potentially limiting generalizability.
  - Taxonomic resolution is highest for targeted groups (bees, hoverflies, butterflies) but may be coarser for other taxa.
  - Geographic and temporal scope limited to 2019–2021 within two field sites.
  - Right-scale ecological inferences depend on consistent sampling effort and accurate alignment of Mix/Replicate with plot-level data.