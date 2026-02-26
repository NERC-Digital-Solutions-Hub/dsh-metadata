# Information can explain the dynamics of group order in animal collective behaviour

## Objective and scope
- Investigates how information drives group order dynamics in animal collective behaviour using controlled experiments with sticklebacks.
- Emphasizes rigorous data collection, processing, and documentation to enable analysis and reproducibility.

## Study design and subjects
- Species: Three-spined sticklebacks (Gasterosteus aculeatus); 96 individuals used.
- Source and housing: Collected from the River Cary (Somerset, UK); housed in three tanks (~50 fish per tank) for 10 months with enriched holding conditions.
- Experimental design: Complete random block design; twelve groups of eight fish each, ensuring representation from all holding tanks to minimise group-level bias.
- Habituation and replacements: Six days of habituation in holding tanks; occasional replacement of individuals due to injury or death, with 24-hour acclimation.

## Experimental setup and procedure
- Arena: Oval trial arena with four entry holes for stimuli; walls and lighting arranged to minimize disturbances and reflections.
- Stimulus: Visual mimic of a bloodworm produced by a pipette end wrapped in red tape; stimulus presented when the group is on the opposite half of the arena from the stimulus hole.
- Trial timing: Conducted over four weeks (late July–August 2017); groups tested in two alternating sets; each group no more than once every two days; sessions between 09:45 and 16:00.
- Trial procedure: 2-minute acclimation, followed by up to six stimulus presentations per trial with minimum 3-minute intervals to allow normal swimming between presentations.

## Environmental and care conditions
- Temperature: 16°C to avoid reproductive condition.
- Water depth and quality: 10 cm depth; consistent conditions across trials.
- Feeding: Bloodworms provided after each trial day and ad libitum on weekends; ensures health regardless of trial outcomes.

## Data collection and processing
- Video capture: 4K video from above (25 frames per second) with standardized camera setup to minimize glare.
- Recording and processing: Raw video converted to MPEG-4 HD; automated 2D tracking to obtain (x_i, y_i) coordinates for each fish at each time step.
- Individual identification: Reuse of fingerprint-based identifiers across trials to maintain fish identities within groups.

## Metadata, data structure, and accessibility
- Data format: Each file contains one trial for a single eight-fish group; explicit mapping of coordinates to eight individuals (x.1..x.8 and y.1..y.8).
- Frame and time indexing: Includes frame number; ensures traceability of positional data over time.
- Quality indicators: NA used where tracking fails for one or more fish in a frame.
- Data organization: Detailed file naming and group assignments to support traceability across the experimental period.

## Data quality and governance considerations
- Quality control: Data provided in raw form; missing data flagged as NA; limited on-board data cleaning.
- Data handling implications: Public sharing of underlying data is not described; potential barriers noted in monitoring contexts include data accessibility, metadata adequacy, and data governance requirements.
- Reproducibility and transparency: Clear documentation of randomization, experimental conditions, and data structure supports reproducibility and secondary analyses.

## Related work
- Primary reference: MacGregor, H.E.A., Herbert-Read, J.E., & Ioannou, C.C. Information can explain the dynamics of group order in animal collective behaviour. Nature Communications (2020).
- Ongoing work: MacGregor & Ioannou on collective motion dynamics over time (in press, Royal Society Open Science).