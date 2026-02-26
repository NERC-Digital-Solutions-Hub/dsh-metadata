# Tc and Se Uptake By Higher Plants - Meta Data

- A metadata record for an experimental study measuring uptake of Tc-99 and Se-75 by 61 higher plant species.
- Each species had 5 replicate 12 cm pots planted in randomised blocks, grown in Levington's F2S compost with controlled lighting/heating, and watered to field capacity.
- Species sampling is hierarchical across three major APGIII angiosperm clades, labeled a, b, and c (mapping in TcAndSeUptakeByPlantsSpeciesSampling).
- Compost and growth conditions: peat-based substrate with lime and ammonium sulfate; pH ~6.2; P ~50 mg/L; K ~50 mg/L; nitrate ~10 mg/L.

- Radiolabelling and uptake protocol: 25 mL solution containing 107 kBq/L 99Tc and 95 kBq/L 75Se applied to the surface; mean activity in compost was 17.8 kBq 99Tc/kg and 15.8 kBq 75Se/kg.
- Harvest and processing: after 48 hours, above-ground shoots were harvested, dried, and digested with nitric acid and hydrogen peroxide; digests counted for emissions.
- Detection: 75Se gamma-emissions counted; 99Tc beta-emissions counted after mixing digest with scintillant; counts decay-corrected to the labelling date.

- Data file TcAndSeUptakeByPlantsData includes column explanations:
  - Block: species grown together in a random block design.
  - CPM1 beta: counts per minute for beta emissions from Tc-99.
  - CPM1 gamma: counts per minute for gamma emissions from Se-75.
  - Decay corrected: Se-75 counts corrected to time of labelling.

- Potential GIS relevance: the dataset provides structured measurements by species within a block design, enabling spatially-informed visualization of uptake patterns when block locations and clade assignments are mapped.

- Notes for GIS preparation:
  - Link Block identifiers to spatial coordinates if greenhouse layout data are available.
  - Use clade/category (a, b, c) and species mapping from TcAndSeUptakeByPlantsSpeciesSampling to enable clade- and species-level choropleth or cluster visualizations.
  - Include units and decay-correction status as attributes for accurate temporal/spatial interpretation.

- Limitations and scope:
  - Greenhouse-based, not field-based; results are controlled by experimental design and may not generalize to natural settings.
  - Data capture focuses on radiolabel emissions (beta for Tc-99, gamma for Se-75) post-digestion; actual tissue-specific uptake values depend on digestion/counting protocol.
  - Availability of the species-to-clade mapping file is required to fully interpret clade-level patterns.