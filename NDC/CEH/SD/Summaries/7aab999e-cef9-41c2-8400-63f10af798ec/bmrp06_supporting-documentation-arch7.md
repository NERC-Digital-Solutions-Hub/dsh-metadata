# Theoretical model of exploitative leadership in collective violence

## Overview
- A theoretical expansion of the hawk-dove model to pairwise intergroup interactions where a randomly selected leader steers the group toward aggressive (hawk) or peaceful (dove) tactics.
- Allows for unequal sharing of fitness payoffs, giving leaders a larger share of benefits or reduced costs relative to followers.
- Shows how extreme intergroup aggression can evolve when initiators influence whole-group behavior and gain disproportionate benefits or incur lower costs.
- Explains how destructive warfare can arise from leaders being decoupled from the costs they induce.

## How the model works (analytical methods)
- Pairwise encounters between groups of size n; a leader is randomly chosen per encounter.
- Leader’s decision determines the group’s tactic (hawk or dove) via their disproportionate influence.
- Group payoffs mirror the classic model but include unequal sharing: followers receive a smaller share of benefits, and leaders incur a reduced share of costs.
- Key prediction: high aggression emerges when initiators can trigger whole-group conflicts and benefit more or suffer fewer costs; results from decoupling leaders from incurred costs.

## Data and visualization implications for GIS
- Conceptualizable as spatially explicit processes: model groups as locations (nodes) with potential intergroup conflicts (edges) influenced by leader decisions.
- Representable GIS attributes:
  - Leader influence proxy (likelihood of hawk vs dove).
  - Payoff sharing modifiers (leader vs follower benefits and costs).
  - Frequency or probability of intergroup initiations.
- Visualization opportunities:
  - Map patterns of predicted aggression across space under different parameter settings.
  - Compare scenario outcomes (e.g., varying leader advantage) using thematic layers and time- or scenario-based maps.
- Potential GIS products:
  - Spatial risk maps of intergroup violence risk.
  - Decision-support visuals for policymakers illustrating how leadership dynamics shape conflict likelihood.

## Data quality, standards, and workflow considerations
- Quality control note: the script was checked for coding errors and results were plotted to visualize results and check for inconsistencies.
- GIS-relevant practice:
  - Reproducibility: ensure the analytical workflow can be rerun with different spatial and parameter inputs.
  - Data lineage: document how group sizes, initiator frequencies, and payoff shares map to spatial attributes.
  - Validation: perform sensitivity analyses to assess how changes in leadership influence alter spatial risk patterns.

## Implementation details and access
- Model type: Mathematica script (Mathematica, 2022).
- Licence: Open Government Licence v3.
- Access options: Wolfram Cloud or local Mathematica installation; DOI provided for citation and access.
- Citation requirements: cite Johnstone, R.A.; Thompson, F.J.; Cant, M.A. (2022) Theoretical model of exploitative leadership in collective violence.

## Data structure details
- File format: Mathematica script stored as a text file.
- Data file: BMRP06_01_theoretical_model_collective_violence (single TXT file).

## References
- Mathematica. (2022). Retrieved from Wolfram.com.
- Wolfram Cloud. (2022). Retrieved from wolframcloud.com.