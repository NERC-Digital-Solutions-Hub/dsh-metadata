# Metadata for Woody species

- Overview
  - A crosswalk of codes to species names and associated functional groups/life forms for woody plant species.
  - Each entry links a code (e.g., ANAGFOET) to its scientific name (e.g., Anagyris foetida L.) and a functional group or life form when provided (e.g., Legume). Some entries have blank functional form.
  - Some taxa include notes such as “2 subspecies – not differentiated” or “subsp. … not differentiated,” indicating subspecies are not separated in this metadata.

- Examples of entries
  - ANAGFOET → Anagyris foetida L.; Functional group/life form = Legume
  - CALIVILL → Calicotome villosa (Poiret) Link.; Functional group/life form = Legume
  - COROVALE → Coronilla valentina L. (3 subspecies - not differentiated); Functional group/life form = Legume
  - JUNIPHOE → Juniperus phoenicea L. (2 subspecies - not differentiated); Functional group/life form = 
  - DAPHGNID → Daphne gnidium L.; Functional group/life form = 
  - Several entries feature blank functional group/life form, indicating missing data for that attribute.

- Notable patterns
  - Focus on woody taxa common to the study area, with many Legume assignments.
  - Some taxa are listed with subspecies notes or unresolved differentiation in this dataset.

# Metadata for herbaceous species

- Overview
  - A comprehensive mapping of codes to herbaceous species, including scientific names and a functional trait/growth form field.
  - The Functional trait/growth form column captures growth form categories (e.g., Graminoid, Forb, Legume, Geophyte/forb), with many entries having a defined form and some with blanks.

- Examples of entries
  - AGROPOUR → Agrostis pourretii Willd.; Functional trait/growth form = Graminoid
  - ALLICOMM → Allium cf. commutatum Guss.; Functional trait/growth form = Geophyte/forb
  - ANTHTETR → Anthyllis tetraphylla L.; Functional trait/growth form = Legume
  - DIANSYLV → Dianthus sylvestris Wulfen subsp. longicaulis (Ten.) Greuter & Burdet var. godronianus ...; Functional trait/growth form = Forb
  - OPUNFICU → Opuntia ficus-indica (L.) Mill.; Functional trait/growth form = Forb
  - Numerous entries list a second field as blank or not provided, indicating missing growth-form data for those taxa.

- Notable patterns
  - Wide range of herbaceous taxa covered, including grasses (Graminoid), forbs, geophytes, and legumes.
  - Many entries include subspecies or varietal designations; some lack a defined growth-form.
  - The dataset supports trait- or form-based analyses alongside taxonomic identity.

# Metadata for spatial and environmental data

- Core spatial variables
  - LATITUDE: Latitude in decimal degrees
  - LONGITUDE: Longitude in decimal degrees
  - ALTITUDE: Altitude in metres
  - SLOPE: Slope in degrees
  - Aspect: Aspect in compass degrees
  - ROCKCROP: Percent rock outcropping

- Soil and environmental context
  - SOILPH: Soil pH for 50 sites
  - GRAZING index: Ranked grazing intensity with four levels
    - 1) unbrowsed
    - 2) lightly browsed
    - 3) moderate to heavy browsing
    - 4) severely clipped

- Olive-tree metrics (site-level or plot-level measurements)
  - OLIVDIAA, OLIVDIAB, OLIVDIAC, OLIVDIAD, OLIVDIAE: Olive diameter categories at 30 cm height (0–5 cm up to >20 cm)
  - OLIVBREA, OLIVBREB, OLIVBREC, OLIVBRED, OLIVBREE: Olive diameter categories at breast height (0–5 cm up to >20 cm)
  - MEAN30: Mean number of olive trees (30 cm height)
  - MEANDBH: Mean number of olive trees (breast height)
  - FREQ30: Frequency of olive trees (30 cm height)
  - FREQDBH: Frequency of olive trees (breast height)

- Usage implications
  - Enables linking species data (woody and herbaceous) with exact site locations and environmental context.
  - Supports analyses of species distribution in relation to altitude, slope, aspect, soil pH, and grazing pressure.
  - Facilitates ecological modelling and spatial analyses that incorporate olive-tree inventory alongside broader vegetation data.