# National Plant Monitoring Scheme survey data (2015-2017)

- Purpose: A volunteer-based habitat-focused plant monitoring scheme (NPMS) designed to detect changes in plant abundance and habitat quality across the UK, Isle of Man, and Channel Islands. The data support assessing habitat change, drivers, and contribute to UK biodiversity indicators. Data are held in CEH Wallingford and are shared publicly for independent review.

- Organisers and collaborators: Botanical Society of Britain and Ireland (BSBI), Centre for Ecology and Hydrology (CEH), Joint Nature Conservation Committee (JNCC), and Plantlife.

- Key outputs: An annually updated NPMS database with a snapshot of plant communities and habitat condition; field guidance and data quality assurance (EQA) processes; and public access to data for researchers and policymakers.

- Data governance and QA emphasis: Strong focus on design and methodological transparency, uncertainty estimation, documentation, version control, and data management. Verification supported by iRecord and a formal data management approach, with data published for public scrutiny.

- Data access and submission: Data can be entered online via the NPMS portal; if online entry is not possible, paper forms can be mailed to NPMS coordinators. Public data sharing is part of the model, with controls on sensitive information.

- Data provenance and structure: Four main CSV files form the dataset, each linked by IDs:
  - locations_2015to2017.csv: unique location identifiers and survey plot types.
  - sampleInfo_2015to2017.csv: sampling events at each location, including survey type, date, location_id, spatial reference (entered_sref and entered_sref_system), creation metadata (created_on, created_by_id).
  - sampleAttributes_2015to2017.csv: additional attributes collected per sample, linked to sampleInfo via sample_id.
  - occurrences_2015to2017.csv: species occurrences with taxon data, dominance (domin) values, verification status (record_status: C, V, R), and sensitivity (sensitivity_precision).

- Data quality assurance (EQA) framework:
  - Supported by peer-reviewed papers, technical reports, and internal project documentation.
  - Design and plot sampling strategies developed with statistical and botanical expertise; robust random plot placement at habitat scales.
  - Data input validation includes species dictionaries, date standardization, spatial controls, and geographic range checks; iRecord provides expert verification for unusual records.
  - Outputs are reviewed by scientists to ensure claims are evidence-based; data are open to external critique and publication in scientific venues.
  - Documentation, versioning, and data tracking follow a Data Management Plan and PRINCE2 project management standards; all design work is archived and backed up off-site.

- How the survey works (scope and methodology):
  - Target: 28 fine NPMS habitats (10 broad categories) with up to 30 target species per habitat; volunteer surveyors record plants in fixed plots.
  - Plots: 
    - Square plots: 5x5 m (woodlands 10x10 m), located within allocated kilometre squares; plots ideally across different NPMS habitats.
    - Linear plots: 1x25 m for features like arable margins, water bodies, hedgerows, etc.
  - Frequency and levels:
    - Two visits per year (late spring/early summer and late summer).
    - Three survey levels: Wildflower Level (fewer species), Indicator Level (robust set of habitat indicator species), Inventory Level (all vascular plants present).
  - Plot selection and relocation: Preference for pre-selected plots, but Self-Selecting Protocol A allows placement in representative habitat areas. Plots must be relocatable over years, with sketches, photos, and GPS support.
  - Ponds, flushes, and distinctive features: Linear plots used for ponds/flushes; specific guidance for positioning and measurement to maximize habitat representation.
  - Data capture tools: Online data entry, field recording forms, species lists, and photographic documentation to aid relocation and interpretation.

- Recording and data capture details:
  - For each plot, record species presence and estimate percent cover using the Domin scale (1-10) with explicit guidance on translating area coverage to percent cover.
  - Record additional attributes (optional but recommended): vegetation height classes, woodedness, aspect, slope, and management signs (e.g., grazing, mowing, hedge management) with standardized categories.
  - Documentation to support data interpretation: field sketches with compass direction, up to two photos per plot, GPS coordinates (where available), and notes about plot relocation features.
  - Special habitat notes: guidelines for arable margins, road verges (where relevant), hedgerows, standing waters, rivers, springs, and screes with plot dimension adaptations and safety considerations.
  - Data entry and submission: Primary submission through online NPMS portal; alternatives via mailed forms for offline submission.

- Data use and dissemination:
  - Data entered online contribute to annual reporting on habitat state and change across the UK.
  - Outputs are subject to scientific review to ensure claims are supported by evidence; data may be used in newsletters and peer-reviewed publications.
  - Location and sensitivity handling: Some records flagged as sensitive (sensitivity_precision) may be spatially blurred (e.g., 10 km) to protect sensitive sites.

- Access rights, responsibilities, and safety:
  - Participants are encouraged to respect land access rights, public rights of way, and landowner permissions; safety and personal responsibility are emphasized.
  - Health and safety: guidance for weather, risky habitats (steep slopes, cliff edges, tidal areas), and field safety, including buddy systems and proper gear.
  - Data privacy: recorder identities are anonymized in publicly shared datasets; unique recorder IDs are used to link records while protecting individuals.

- Appendices and habitat taxonomy (Appendix 1):
  - Detailed habitat types and their corresponding species lists to guide survey choices and data interpretation.
  - Domin Scale definitions and guidance for converting observed cover into standardized dominance scores.
  - Notes on habitat-specific plot arrangements and species recording protocols.

- End-state and ongoing relevance:
  - NPMS aims to provide statistically robust long-term data on plant communities and habitat condition to inform conservation and policy.
  - The dataset supports monitoring change across habitat types, addressing uncertainties through model-based analyses, and maintaining transparent documentation and data management practices for long-term usability.