# Data describing pollination of tomatoes by the bees Bombus terrestris and Lasioglossum spp.

## Overview
- Experimental dataset assessing how three pollinator treatments affect tomato fruit set and average fruit size.
- Treatments: Bombus terrestris alone; Lasioglossum spp. alone; additive combination of both species.
- Experimental setting: field cages in Earth Trust, Little Whittenham, UK; 2017; funded by CEH Commercial Innovation Fund (National Capability), Project NEC06344.
- Purpose aligns with evaluating environmental health measures to inform policy and decision-making on pollination services.

## Experimental design and methods
- Design: three pollinator treatment combinations within field cages; plus a control condition with no pollinators.
- Replication: batches of five tomato plants per treatment, repeated four times (total experiments conducted April–June 2017).
- Pollination setup: B. terrestris provided as a 30–40 worker colony; Lasioglossum spp. nest populations identified in arable field corners; cages used to manage pollinator exposure.
- Density and logistics: two cages with Lasioglossum spp., one cage with an added B. terrestris colony, and a third cage with a B. terrestris colony accessible to Lasioglossum nests (Treatment 3). Overall Lasioglossum nest density ~4.2 ± 0.8 nests m^-2.
- Plant material and conditions: tomato variety Moneymaker; plants grown under greenhouse conditions with pollinators excluded before exposure; nectar sources provided by a small number of Asteraceae plants to support pollinators.
- Exposure and measurements: after 4-day exposure periods, plants returned to greenhouse; mature fruit counted (up to 5 per stem) and individual fruit mass measured.

## Data collected and structure
- Plant-level measurements focusing on fruit set and size under each pollination treatment.
- Key data fields (metadata provided) include:
  - Unique_ID: plant-level identifier.
  - Treatment: additive pollinator treatment (Lasioglossum only, Bombus only, or both).
  - C_* fields: measurements from the control (no bees), including C_Flow_N, C_Flow_set, C_Prop_set, C_Mass_ave, and masses for up to five control fruits (C1_mass to C5_mass).
  - T_* fields: measurements from exposure to bees, including T_Flow_N, T_Flow_set, T_Prop_set, T_Mass_ave, and masses for up to five fruits (T1_mass_mass to T5_mass_mass).
  - C1_mass through C5_mass and T1_mass_mass through T5_mass_mass capture per-fruit masses where present; zeros indicate no fruit set.
  - Description/Units: categorical descriptions and numerical units (e.g., grams for mass; discrete/batch levels for replication).

## Data governance, quality, and accessibility considerations
- Metadata is detailed, enabling interpretation of per-plant and per-fruit outcomes across treatments and temporal replicates.
- The original documentation discusses common barriers for monitoring data (data availability, metadata quality, data sharing constraints, and data governance). This dataset provides explicit metadata and a clear experimental provenance, which supports reuse for policy-relevant monitoring and comparative assessments.
- Data are derived from a controlled, replicable experimental design, facilitating standardized indicators of pollination service effectiveness on crop yield metrics.

## Potential use for monitoring and policy evaluation
- Enables evaluation of the relative and additive effects of different pollinator assemblages on crop performance (fruit set and fruit mass).
- Provides a structured example of measuring pollination services within a managed system, informing decisions on pollinator management, crop yield optimization, and related environmental health indicators.
- The explicit control and treatment comparisons support policy-relevant indicators of pollination reliability and capacity in agricultural settings.

## References and provenance
- Dag A. (2008) Bee pollination of crop plants under enclosure conditions. J. Apic. Res.
- Greenleaf S.S. & Kremen C. (2006) Wild bee species increase tomato production and respond to land use. Biological Conservation.
- Funding: CEH Commercial Innovation Fund (National Capability), Project NEC06344.
- Location: Earth Trust, Little Whittenham, UK (field experimental site).