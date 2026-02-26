## Neuropil volumes for sensory structures in ithomiini butterflies (Lepidoptera, Nymphalidae, Danainae) in eastern Ecuador

- Objective
  - A dataset of neuropil volumes in sensory brain structures of ithomiine butterflies from eastern Ecuador, to understand how sensory environments influence investment in brain regions.
  - Builds on prior work (Montgomery & Ott 2015; Wainwright & Montgomery 2022; Wainwright et al. 2024) and ties to mimicry ecology and sensory specialization.

- Field site and specimen collection
  - Fieldwork conducted along trails around Estación Científica Yasuní, Parque Nacional Yasuní, Ecuador (primary lowland Amazon rainforest).
  - Time frame: samples collected in 2011–2012 and 2022 under multiple permits; approx. 60 local ithomiine species recorded.
  - Specimens: wild-caught individuals used for neuroanatomy, with voucher wings preserved; specimens identified to species and sexed.

- Neuroanatomy measurements and anatomical scope
  - Sample: 392 individuals across 49 species for sensory brain structure analysis.
  - Brain regions measured (optic lobe): five of six primary optic lobe neuropils
    - Medulla, Lobula plate, Lobula, Accessory medulla, Ventral lobula
    - Total optic lobe volume is the sum of these; lamina excluded due to thinness and damage risk.
  - Central brain controls: anterior optic tubercle (AOTu) and antennal lobe (primary olfactory center) measured to test for olfactory investment; volumes used to compute a "rest of central brain" allometric control by subtracting AOTu and antennal lobe from central brain volume.
  - Other notes: ventral lobula absent in many individuals, especially females.

- Imaging, staining, and volume reconstruction
  - Tissue processing: dissection in HEPES-buffered saline, fixation in ZnFA, rehydration, immunostaining for synapsin (pre-synaptic marker) with specific antibodies, and secondary antibody labeling.
  - Clearing and imaging: brains cleared in methyl salicylate and imaged with confocal laser-scanning microscopy; stacks captured from anterior and posterior sides.
  - Segmentation: manual segmentation of neuropils in Amira 2021.2 using synapsin signal; interpolation used to fill unsegmented sections; volumes extracted via measure statistics.
  - Corrections: z-dimension adjusted by 1.52x to account for artificial shortening; volumes log10-transformed for analysis.
  - Data prepared for five optic lobe neuropils, AOTu, and antennal lobe; a composite “optic lobe” volume sums the five neuropils.

- Data processing and transformation
  - All volumes log10 transformed (µm^3).
  - Rest of central brain used as allometric control by subtracting AOTu and antennal lobe from central brain volume.
  - Data consistency: procedures aligned with Montgomery & Ott (2016); damaged or poorly stained samples excluded.
  - Quality control: multiple measures per species; damaged/poorly stained samples removed; standardized methodology across species.

- Dataset structure and metadata (columns)
  - Year collected; Individual ID; Subtribe; Species; Sex; Mimicry ring (based on Elias et al. 2008)
  - log10(rest of central brain volume µm^3)
  - log10(medulla volume µm^3)
  - log10(lobula plate volume µm^3)
  - log10(lobula volume µm^3)
  - log10(accessory medulla volume µm^3)
  - log10(ventral lobula volume µm^3)
  - log10(antennal lobe volume µm^3)
  - log10(anterior optic tubercle volume µm^3)
  - log10(optic lobe volume µm^3) (combined optic lobe neuropils)

- Quality control and reproducibility
  - Individual-level data provide multiple measures per species.
  - Excludes damaged or poorly stained samples; uses established, consistent measurement methodology.

- Relevance and potential analyses
  - Enables correlational and comparative analyses of sensory brain investment relative to ecological factors such as mimicry ring, habitat light environment, and species-specific sensory demands.
  - Facilitates cross-species and cross-group comparisons of olfactory versus visual processing investment, and tests of allometric scaling in relation to central brain size.

- Funding and provenance
  - Dataset created as part of NERC Independent Research Fellowship NE/N014936/1.

- References (contextual)
  - Elias et al. 2008; Montgomery & Ott 2015; Wainwright & Montgomery 2022; Wainwright et al. 2024.