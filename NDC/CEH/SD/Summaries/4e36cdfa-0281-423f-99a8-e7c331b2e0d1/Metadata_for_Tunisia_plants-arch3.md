# Metadata for Woody species

- Provides code-to-scientific-name mappings for woody taxa (e.g., ANAGFOET = Anagyris foetida L.; CAPPSPIN = Capparis spinosa L.; COROVALE = Coronilla valentina L. with 3 subspecies not differentiated).
- Each entry lists the Scientific Name and a Functional group/life form field; many entries have this field blank, while some indicate Legume.
- Notes indicate subspecies not differentiated in several cases (e.g., Juniperus phoenicea subspecies not differentiated) and occasional unidentified species placeholders (UNIDENTA, UNIDENTB) with two variants.
- Structure supports data integration by providing standardized taxonomic codes alongside scientific names and life-form information.
- Gaps and ambiguities exist where functional groups are missing or subspecies differentiation is not applied, highlighting metadata completeness issues.

# Metadata for herbaceous species

- Parallel metadata structure to woody species: each entry maps a code to Scientific Name and a Functional trait/growth form (e.g., ANAGARVE = Anagallis arvensis L. – Forb; ANTHTETR = Anthyllis tetraphylla L. – Legume).
- Numerous entries show a blank for Functional trait/growth form, while others are explicitly labeled (e.g., Forb, Legume, Geophyte/Forb).
- Codes cover a wide range of herbaceous taxa (e.g., AGROPOUR, ALLICOMM, ARISVULG, CAMPERIN, DIANSYLV, ONONALBA, TRIFANGU, VULPSPEC, etc.), with occasional two-part flags (e.g., 1 = primary designation, 2 = alternate/secondary designation).
- Some entries include subspecies or varietal notes, but many remain at higher-level taxon labels, reflecting incomplete differentiation in metadata.
- Purpose: to standardize herbaceous plant metadata for monitoring, enabling consistent data capture and cross-site comparability.

# Metadata for spatial and environmental data

- Core spatial variables: LATITUDE, LONGITUDE, ALTITUDE, SLOPE, and Aspect (compass degrees).
- Habitat context variables: ROCKCROP (% rock outcropping) and SOILPH (soil pH measured at 50 sites).
- Grazing index: a ranked scale with four levels describing browsing intensity (unbrowsed to severely browsed), used to contextualize vegetation data.
- Olive tree metrics (site-level context): OLIVDIAA, OLIVDIAB, OLIVDIAC, OLIVDIAD, OLIVDIAE (olive diameter segments at 30 cm height); OLIVBREA, OLIVBREB, OLIVBREC, OLIVBRED, OLIVBREE (diameter at breast height); MEAN30 and MEANDBH (mean counts at 30 cm height and at breast height); FREQ30 and FREQDBH (frequency of olive trees at 30 cm height and at breast height).
- The collection of these variables supports environmental characterization and tree-specific measurements within monitoring frameworks.
- This section demonstrates integration of spatial, environmental, and species data to support holistic environmental health assessments and decision-making.

Overall relevance for monitoring frameworks

- The document illustrates a structured metadata schema essential for data quality, interoperability, and governance within monitoring programs.
- It emphasizes the need for complete metadata (taxon codes, scientific names, functional traits, and site-level environmental variables) to enable verification, data sharing, and transparent reporting.
- It also highlights common challenges faced by authors of monitoring frameworks: data gaps, inconsistent or missing metadata, data silos, and barriers to public data sharing, all of which impede timely and reliable environmental health assessments.