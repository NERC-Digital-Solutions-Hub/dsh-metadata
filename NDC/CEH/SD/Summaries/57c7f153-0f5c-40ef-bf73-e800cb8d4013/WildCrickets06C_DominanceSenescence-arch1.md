# WildCrickets06C_DominanceSenescence Description of content

- The dataset captures success per fight for individual male wild crickets, focusing on dominance interactions and aging (senescence).

- Key fields:
  - Year: Calendar year of the fight event.
  - Year when the cricket was alive: The year within the cricket’s lifespan (context for life-stage analyses).
  - ID: Unique identifier for each individual cricket.
  - Age: Age at the fight, in days.
  - AgeDiff: Difference in age relative to the opponent, in days (positive means older than opponent).
  - SizeDiff: Difference in body size relative to the opponent, in grams.
  - Won: Binary outcome of the fight (1 = won, 0 = did not win).

- Purpose of the data:
  - To analyze how age and relative age (senescence) affect fight outcomes.
  - To assess whether size differences with opponents influence dominance and success.

- Analytic opportunities for researchers:
  - Predictive modeling of fight outcome (Won) using Age, AgeDiff, SizeDiff, and Year.
  - Mixed-effects models with ID as a random effect to account for multiple fights per individual.
  - Interaction analyses (e.g., Age x AgeDiff, Age x SizeDiff) to explore how aging modulates advantage from age or size differences.
  - Longitudinal assessment of dominance trends across an individual’s lifespan (senescence trajectory).
  - Survival-type analyses for the probability of winning over age or life-stage.

- Data quality and considerations:
  - Potential missing values or measurement errors in age, size, or opponent comparisons.
  - Year alive field helps contextualize life-stage but may require careful interpretation if births or lifespans are uncertain.
  - Lack of information on opponent identity beyond age/size, environmental conditions, or fight context may limit causal inference.

- Practical implications:
  - Enables correlations and predictions about how aging and relative traits influence dominance outcomes in crickets.
  - Provides a basis for comparing across individuals and years to identify consistent patterns in senescence and competitive advantage.