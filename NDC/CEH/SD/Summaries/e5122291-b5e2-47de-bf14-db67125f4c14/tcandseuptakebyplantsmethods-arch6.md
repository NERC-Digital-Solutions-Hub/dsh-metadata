# Tc and Se Uptake By Higher Plants - Meta Data

- Overview
  - 61 plant species, 5 replicates each, grown in 12 cm pots with saucers.
  - Growing medium: Levington's F2S compost with supplementary lighting and heating; watered on demand to field capacity.
  - Experimental design focuses on three major clades of the APGIII angiosperm phylogeny (labeled a, b, c in a separate jpg file TcAndSeUptakeByPlantsSpeciesSampling).
  - pH and nutrient context: compost is peat-based with lime and ammonium sulfate (~3%); pH ~6.2; P ~50 mg/L; K ~50 mg/L; nitrate ~10 mg/L.

- Experimental design and sampling
  - Plants arranged in randomised blocks, processed in batches until in exponential growth phase.
  - Radiolabelling performed by applying 25 mL of solution containing 107 kBq/L 99Tc and 95 kBq/L 75Se evenly onto the compost surface.

- Radiolabelling details and harvest
  - Mean activity in the compost: ~17.8 kBq/kg for Tc-99 and ~15.8 kBq/kg for Se-75.
  - Harvest: after 48 hours, above-ground shoot material dried and digested (0.1 g per sample) in 5 mL nitric acid and 5 mL H2O2.

- Measurement and data collection
  - Post-digestion counting: gamma emissions from Se-75 and beta emissions from Tc-99.
  - Se-75 counts decay-corrected to the labelling date.

- Data file and column explanations
  - Data file: TcAndSeUptakeByPlantsData
  - Block: species grown together in a random block design.
  - CPM1 beta: counts per minute of beta emissions from Tc-99.
  - CPM1 gamma: counts per minute of gamma emissions from Se-75.
  - Decay corrected: counts per minute for Se-75 decay-corrected to the time of labelling.

- Metadata and usage notes
  - A mapping JPG exists (TcAndSeUptakeByPlantsSpeciesSampling) to relate species to clades a, b, c.
  - Contextual variables include growth stage, tissue sampled (above-ground shoots), and digestion/counting protocol.
  - For data support: ensure proper interpretation of decay correction (Se-75) and alignment of blocks with species/clade mapping; units are CPM for emissions and kBq for initial activity.