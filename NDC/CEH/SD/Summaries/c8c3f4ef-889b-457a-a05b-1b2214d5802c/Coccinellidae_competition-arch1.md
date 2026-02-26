# Supporting documentation for Hentley, W.T; Brien, M.N (2016). Coccinellidae competition. NERC Environmental Information Data Centre. http://doi.org/10.5285/c8c3f4ef-889b-457a-a05b-1b2214d5802c

## Aim and scope
- Document the methods and data for laboratory experiments examining interactions among coccinellid species and their prey (the invasive Harmonia axyridis as predator; native Coccinella septempunctata and Adalia bipunctata as prey).
- Provide details on insect culturing, experimental design, data collection, quality control, and analytical approaches to enable data reuse and replication.

## Study organisms and culture conditions
- Predator: Harmonia axyridis (invasive) and native prey: Coccinella septempunctata and Adalia bipunctata.
- Field collection: Oxfordshire, UK, May 2013; Adalia bipunctata supplemented from a biocontrol supplier due to low field numbers.
- Rearing: All coccinellids reared for at least one laboratory generation in controlled conditions (20 ± 1°C, 16 h photoperiod) with mixed-age Acyrthosiphon pisum as food; field- and lab-reared Adalia bipunctata mixed to minimise source effects.
- Prey for experiments: Amphorophora idaei (rus­berry aphid) maintained on raspberry cv. Malling Landmark; aphid colony established at James Hutton Institute (JHI), Dundee, UK, and maintained for multiple generations (20 ± 1°C, 16 h photoperiod).
- Experimental controls: Aphids used only once per replicate arena.

## Experimental design

### Experiment 1: prey-stage preferences
- Objective: Identify coccinellid larval-stage preferences for aphid nymphal stages.
- Setup: Arena is a circular dish (185 mm diameter, 25 mm high) with a glass lid.
- Treatments: 50 aphids per arena—ten apterous adults and ten individuals from each aphid nymphal stage (I–IV).
- Procedure: A single larval-stage coccinellid introduced at center; allowed to feed for 1 hour; larvae removed and aphids consumed by stage counted.
- Replications: 120 bioassays total (10 replications per larval stage across 3 coccinellid species); randomized into 12 temporal blocks (10 assays per block).
- Outcome measured: Number of aphids of each nymphal stage consumed by coccinellid larval stage.

### Experiment 2: competition on shared prey
- Objective: Assess impact of interspecific and intraspecific competition on feeding when prey is shared.
- Setup: Circular arena; aphid cadavers (killed by chilling) placed at 25 points around the circumference.
- Treatments: Two coccinellid larvae (larval stage IV) in focal pairings, with hetero- and conspecific combinations; a control with no competing individuals.
- Procedure: One larva in each pair randomly marked for identification; 1-hour observation with video recording to quantify aphid nymphal stages eaten by each focal and competitor larva. Pairs reversed to swap focal species; additional 10 controls.
- Replications: 90 bioassays total (including all combinations and controls).
- Outcome measured: Number of aphid nymphal stages eaten by the focal species and by the competitor; presence/absence of paint mark for ID.

## Data and metadata

### Experiment1.csv
- Fields include: id, individual coccinellid ID, block, ladybird_stage, Coccinellid lifestage, aphid_stage, aphid lifestage, number_eaten, species, max.

### Experiment2.csv
- Fields include: arena, metal dish / arena - unit of replication, aphid_lifestage, Aphid lifestage, focal_species, Focal coccinellid species, pred_species, Competing coccinellid species, eaten, painted, eaten_comp, total_aphid.

## Data quality and management
- Quality control: Datasets manually checked for errors; no further quality control required.
- Data handling: Aphids and coccinellids were handled to preserve tissue integrity for accurate counting (e.g., chilled aphids in Experiment 2); video analysis used for precise determination of consumption.

## Analytical methods
- Data analysis performed in R (version 3.0.2) using the gamm4 package (for generalized additive mixed models and related analyses).
- Data structure supports comparisons of feeding rates across-life stages, species combinations, and competition conditions.

## Notes on data provenance and applicability
- Experimental design emphasizes randomization, temporal blocking, and replication to enable robust inference about predator–prey interactions and interspecific competition.
- Datasets are prepared with metadata to facilitate reuse and replication, aligning with practices for making datasets discoverable and usable.