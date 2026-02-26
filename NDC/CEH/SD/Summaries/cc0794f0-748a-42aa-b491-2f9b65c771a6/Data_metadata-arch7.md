# STUDY SPECIES

- Overview of species studied and abbreviations:
  - Thomson gazelle, Gazella thomsonii (Tho)
  - Grant gazelle, Gazella granti (Gra)
  - Impala, Aepyceros melampus (Imp)
  - Common warthog, Phacochoerus aethiopicus (War)
  - Ostrich, Struthio camelus (Ost)
  - Topi, Damaliscus lunatus (Top)
  - Hartebeest, Alcelaphus buselaphus (Har)
  - Blue wildebeest, Connochaetes taurinus (Wil)
  - Plains zebra, Equus quagga (Zeb)
  - African buffalo, Syncerus caffer (Buf)
  - Common eland, Tragelaphus oryx (Ela)
  - Giraffe, Giraffa camelopardalis (Gir)

- Behavioral and experimental focus:
  - Vigilance behaviour: quantify species-specific vigilance rates via video of monospecific foraging groups (min 5 minutes per group). For each visible individual, record number and duration of vigilance bouts; compute mean vigilance parameters per group.
  - Predator simulations: expose groups to life-sized lateral photos of five predators (lion, spotted hyena, leopard, cheetah, black-backed jackal) and a reedbuck control. Stimulus delivered by driving a car past hidden models; record occurrence of alarm calls within 5 minutes.
  - Playback experiments: present alarm calls of other study species (except Eland) to assess responsiveness; include dove non-alarm call as control. Use three recordings per stimulus; focal animal chosen from relaxed foragers; loudspeaker ~65 m away at 90-degree angle; analyses via Behavioural Observation Research Interface Software.
  - Species counts: 66 censuses across three study plains (totaling 54 km2) along predefined tracks to assess relative abundance, group sizes, and mixed-species group occurrence.

- Data products (datasets) and primary variables:
  - Data_VigilanceBehaviour: Species; NumberHeadUps; VigilancePerMinute; GroupSize.
  - Data_PredatorSimulations: Species; Date; Model; Call; DistanceModel; GroupSize; NumberOffspring.
  - Data_PlaybackResponse: FocalSpecies; CallerSpecies; Date; Response; FirstResponse; DurationResponse; SpeedHeadUp; NOScratch; NOShake; NOHeadUps; NOAlarm; Wind; Temperature; GrassHeight; DistanceCover; DistanceFocal; GroupSize; Full.
  - Data_SpeciesCounts: Date; StudyPlain; Group; Tho; Gra; Imp; War; Zeb; Top; Wil; Har; Ela; Gir; Buf; Ost.

- Spatial and study extents:
  - Three plains, total coverage 54 km2; censuses along predefined tracks; group-level observations with distances measured (laser range finder) where relevant (e.g., DistanceModel, DistanceFocal, DistanceCover).

- Data provenance and references:
  - Primary source: Meise, K.; Franks, D. W.; Bro-Jørgensen, J. (2018). Multiple adaptive and non-adaptive processes determine responsiveness to heterospecific alarm calls in African savannah herbivores. Proc. R. Soc. B. 285(1882): 20172676.

- Practical GIS considerations:
  - Potential GIS use: map plains and census points; create species abundance rasters or point datasets; link group sightings with environmental layers (grass height, wind, temperature) and proximity to playback/predator stimuli; analyze spatial patterns of vigilance, alarm responses, and interspecific communication.
  - Data integration: align species abbreviations with spatial features; join vigilance, predator response, and playback metrics to group-level locations; integrate with environmental rasters and habitat maps for richer visuals and analyses.