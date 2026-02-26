# Pollinator Abundances in Sunyani and Techiman, Brong Ahafo, Ghana (Aug–Nov 2016)

- Overview
  - What: Dataset on abundances of bees, wasps, Lepidoptera, beetles and flies; bee genera and morphospecies; and bee functional traits.
  - Where: In and around Sunyani and Techiman, Brong Ahafo, Ghana.
  - When: August to November 2016.
  - Why: Collected as part of a project on urban ecosystem services.
  - Who: Collected and interpreted by Solène Guenat; precise sampling locations are absent due to ethical considerations.

- Study Design
  - Sampling regime: 126 greenspaces sampled across an urbanisation gradient with three management types (amenity land, farmed greenspace, informal greenspace). Sites were distributed to represent rural, urban, and peri-urban landscapes, with a minimum 1 km distance between sites.
  - Land-cover data: Derived from Sentinel-2 imagery (December 2015) using a two-step classification to estimate built infrastructure within a 250x250 m grid; urbanisation category defined by the proportion of built infrastructure within 600 m of each site.
  - Site selection: 42 sites randomly chosen along the gradient, ensuring equal representation of rural, urban, and peri-urban areas; rural areas limited to within 10 km of the city and accessible by paved roads or dirt paths.

- Field Methods
  - Pollinator trapping: Five pan-traps per site (colors: fluorescent yellow, blue, white), deployed for 24 hours at ground level (0–0.5 m), separated by 5 m, with up to five greenspaces sampled concurrently.
  - Specimen handling: Specimens stored in 70% alcohol; identification to order in the field; bees identified to genus and sub-genus (where possible) and then classified into morphospecies due to limited species-level resources in Sub-Saharan Africa.
  - Bee functional diversity: Assessed using traits such as habitat, pollen specialization, nesting behavior, body size (intertegular distance), tongue length, and sociality.
  - Habitat and floral context: Visual estimates of six habitat features within a 200 m radius; floral resources in a 1 m radius around the trap (species richness, floral area, and abundance); crop types noted in farmed sites.

- Data and Variables
  - Data files: Four CSV files
    - PollinatorAbundances.csv (39 columns): sampling date, city, management, urbanisation metrics, environmental variables, habitat features, floral resources, and abundances by overall pollinators and groups.
    - BeeGeneraAbundances.csv (37 columns): entries for sampling data plus abundances by bee genera.
    - BeeMorphospeciesAbundances.csv (95 columns): morphospecies-level abundances with genus/subgenus/morphospecies nomenclature.
    - BeeFunctionalTraits.csv (24 columns): genera with functional trait data (e.g., intertegular distance, tongue length, pollen specialization, sociality, nest location, habitat).
  - Core variables: SamplingDate, City, Management, PerCentGreen600m (proportion built infrastructure within 600 m), Urbanisation, Altitude, CloudCover, Temperature, WindSpeed, Rainfall, various habitat components (GroundLayerVegetation, ShrubLayerVegetation, TreeLayerVegetation, Concrete, MownVegetation, BareGroundCover), FloralResources, FloweringPlantsSpeciesRichness, Abundances by group (Bees, Lepidoptera, Wasps, Beetles, Flies), Taxon-specific abundances (genera and morphospecies), intertegular distance, tongue length, pollen specialisation, sociality, nest location, and habitat.
  - Data structure notes: Each line represents a sampling location; taxa are organized by file with increasing taxonomic resolution from orders to genera, morphospecies, and functional traits. Some taxa names include formatting variations consistent with the original taxonomy sources.

- Analytical and Monitoring Context
  - Output intent: Provide a standardized dataset to assess environmental health and pollinator community responses across an urban–rural gradient, enabling time-series and spatial comparisons as part of urban ecosystem services monitoring.
  - Applicability for analysts: Clear data schema, standardized sampling protocol (pan-traps, timing, habitat contextualization), and harmonized trait data support cross-site comparisons, trend analysis, and integration with other environmental datasets.
  - Accessibility considerations: Ethical constraints limit precise sampling location details; emphasis on storing and sharing the derived datasets through appropriate portals; data completeness and taxonomic resolution reflect resource constraints and taxonomic references used.