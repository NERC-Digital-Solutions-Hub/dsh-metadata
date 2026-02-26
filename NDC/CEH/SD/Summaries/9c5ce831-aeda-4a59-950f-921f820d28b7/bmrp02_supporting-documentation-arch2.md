# Sampling regime and collection methods

- Study context and scope
  - Banded Mongoose Research Project studying a wild banded mongoose population on the Mweya Peninsula, Queen Elizabeth National Park, Uganda, ongoing since 1995.
  - Population typically 10–12 social groups; groups of ~20 adults plus offspring; individuals uniquely marked for long-term observation.
  - Data collected cover group composition, life history, reproduction, cooperative behaviour, escorting of pups, and genetic parentage.

- Data collection regime
  - Regular trapping every two months; radio collars fitted to 1–2 individuals per group to enable group location; most groups habituated to observers.
  - Groups visited every 1–3 days for at least 20 minutes to record data on composition, life history, reproduction, and cooperative behaviour.
  - Reproductive monitoring includes ultrasound to confirm pregnancy; synchronized oestrus within groups; communal birth timing and den emergence of pups around 30 days.
  - Pup marking, tissue sampling for genetics (tail tip), and DNA genotyping using 43 microsatellite markers.
  - Escorting period: pups receive extensive adult care for ~60 days post-den emergence; data collected on escorting behaviour and social interactions.
  - Weight measurements obtained weekly using portable electronic scales; animals weighed before foraging.

- Experimental design (provisioning manipulation)
  - Split-plot design: pregnant females in a group randomized to provisioned (fed) or non-fed (control) within breeding attempts.
  - Randomized assignment with methodological rules to minimize carryover effects; each manipulated breeding attempt followed by an unmanipulated control breeding attempt.
  - Feeding protocol: fed females receive ~50 g of egg per day (average), with randomization of daily amount (0, 50, or 100 g) and time of day (morning or evening).
  - Study span: 34 breeding attempts across 7 groups from 2013–2016; 101 fed pregnancies and 97 non-fed pregnancies.
  - Outcomes include 50 treatment pups (fed) and 50 control pups (non-fed) with maternity assignments via genetic pedigree (probability ~90%).

- Fieldwork instrumentation
  - Data collection app (Mongoose 2000) on Samsung Galaxy tablets; data imported to MS Access database.
  - Weighing scales (Sartorius TE6100); radio collars (~30 g; 20 cm antenna).
  - Pregnancy detection via ultrasound (SIUI CTS-900V prior to 2017; Sonoscape S6BW thereafter).

- Calibration and quality assurance
  - Field instruments calibrated to factory settings.
  - In-app internal checks to reduce data collection errors (e.g., presence required for further behavioural data).
  - Data quality checks conducted using MS Access queries and bespoke R scripts to detect inconsistencies (e.g., multiple death records).

- Data structure and content
  - Data stored across 15 CSV files, capturing a comprehensive set of variables related to females, offspring, and social dynamics.
  - Example content areas include:
    - Female weight change from pre-pregnancy baseline to pregnancy, post-pregnancy, and during escorting.
    - Maternal and escorting behaviour (adult male/female escorting effort, age, escort counts, and escort frequency).
    - Pup data (weights, early growth, per-pup escorting, and survival outcomes at 90 days, 180 days, and 365 days).
    - Pairwise relatedness data between pups and adults, to quantify kin associations in escorting.

- Analytical methods (key outcome measures)
  - Assess the effect of provisioning on female condition (weight change across pregnancy, post-pregnancy, and escorting periods).
  - Measure adult escorting effort during the escorting period (by sex, age, and group context).
  - Examine how provisioning influences the allocation of escorting to pups (fed vs non-fed parents, by individual and litter).
  - Evaluate pup growth and weight variance within litters, and pup growth trajectories (30–90 days) with respect to escorting.
  - Quantify the rate and quality of escorting to pups (escort frequency, feeding rate, and proximity metrics).
  - Determine pup survival up to 90, 180, and 365 days, with contextual metrics (survival status, end age, and helper ratio).

- Data outputs and accessibility
  - Outputs include datasets on maternal weight change, escorting behaviour, pup growth, escorting toward pups, and pup survival.
  - Data management emphasizes storing processed datasets in a standardized format for reuse and cross-study comparability.
  - Challenges acknowledged include increasing dataset value by integrating with other data sources and enabling broad access to underlying data used to generate outputs.