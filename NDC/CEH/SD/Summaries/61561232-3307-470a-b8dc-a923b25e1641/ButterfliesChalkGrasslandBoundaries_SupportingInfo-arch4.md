# Raw data sets on the behaviour and distribution of Lepidoptera (butterflies and day flying moths) at the Stonehenge Landscape in 2011

## Overview
- Describes raw data sets on Lepidoptera behaviour and distribution at the Stonehenge Landscape during 2011.
- Adapted from Grace Twiston-Davies’s PhD work (Landscape Connectivity) and detailing background, data collection methods, and data structure.
- Data quality assurance included checks for outliers and anomalies via pivot tables and exploratory analysis.

## Study site
- Location: Stonehenge World Heritage Site, Wiltshire, UK.
- Landscape: Former arable land undergoing habitat creation with locally sourced chalk grassland seed mixtures.
- Fragments surveyed (four): Full-moon Bank, Luxenborough Bank, Winterbourne Stoke Group, Fargo Barrow; all within the Stonehenge Landscape estate (National Trust).
- Habitat layout: Small chalk grassland fragments (0.22–1.98 ha) on slopes with adjacent land uses including arable and grassland restoration.
- Survey design: Four 20 m x 20 m boundary survey areas per fragment, plus corresponding control surveys in continuous habitat; total of fourteen survey boundaries.

## Data collected

### Lepidoptera surveys
- Timing: May to July; surveys between 10:00 and 16:00; efforts varied across the day to minimize time-of-day effects.
- Protocol: Based on Ries & Debinski (2001); each boundary survey area is 20 m x 20 m, centered on the boundary between chalk grassland fragment and adjacent habitat.
- Data captured per Lepidoptera instance: species, start and finish location (within fragment or adjacent land), and flight path; exiting behaviour categorized as crossing, following, or avoiding the boundary; otherwise, staying if not exiting or path too convoluted.
- Behavioural categorization: Exit-edge based (crossing from boundary into habitat, following along the perpendicular edge, avoiding along the boundary). Staying if non-exitable or unclear path.
- Pseudoreplication mitigation: avoided recapturing the same individual by choosing different species or sex per flight path; approximately 15 days between replicates at each site.
- Replication and weather: Acceptable weather conditions per UK Butterfly Monitoring Scheme standards; three replicates per boundary across May, June, and July; total field effort limited by fragment size.

### Vegetation and nectar data
- Vegetation and nectar availability measured in eight 0.5 m x 0.5 m quadrats per boundary (four on chalk side, four on adjacent land cover).
- Recorded metrics per quadrat: vegetation height and density (drop-disc method), percentage bare ground, and nectar flower availability (number of flowering units) across specified plant families.
- Botanical assessment: Conducted on two occasions between May and August.

### Climate context
- Wind: Average wind speed and direction recorded using the nearest meteorological station (Boscombe Down, 6.5 km SW).
- Temperature and cloud: Temperature (air) and cloud cover recorded at start of each survey; cloud cover estimated by eye.

## Data structure and nomenclature

### Data sheets and columns
- Data sheets referenced include:
  - DATA Lepidoptera Behaviour
  - DATA Resources Behaviour
- Columns cover: date, time, location, replicate, habitat type (edge, chalk, arable, restoration), shelter/exposed, side of location, survey type, species, sex, behaviour, start/end habitat, movement direction, nectar plant details, and other notes.
- Location coding and transects: Location codes (e.g., WSG, Fargo, Full, Lux) with side indicators (West, East), sheltering status (Sh, Ex), and grid references (BNG, SU).
- Boundary vs control: Distinct survey types and locations for boundary edge surveys and control surveys within the Chalk Grassland or restoration contexts.
- Data dictionaries: Separate tables list Lepidoptera species with codes and common names, as well as flowering plant species with codes and common names.

### Taxonomy and nomenclature
- Plants: Nomenclature aligned with Stace (2010) New Flora of the British Isles.
- Lepidoptera: Nomenclature aligned with Langmaid et al. (1989) and Heath & Emmet (1985); field identifications guided by standard FSC guides.
- Species and plant codes provided for consistent data entry (e.g., Ads.sta for Adscita statices; Pie.rap for Pieris rapae; etc.).

## Data quality and limitations

- Quality assurance: Outliers and anomalies sought through pivot tables and exploratory analysis (details not shown in this document).
- Data scope: Raw, non-capture data; no mark-release-recapture to avoid altering flight paths.
- Pseudoreplication risks acknowledged; mitigated by rotating species/sex per flight path and spacing replicates (~15 days apart).
- Practical constraints: Small fragment sizes limited survey areas; larger scales or more frequent sampling were not feasible within study design.

## References and data lineage

- Data collection and methods contextualized by:
  - Pollard & Yates (1993) UK Butterfly Monitoring Scheme guidelines
  - Ries & Debinski (2001) edge responses
  - Stace (2010) plant nomenclature
  - Stewart et al. (2001) sward height assessment methods
  - Hardy et al. (2007); Heath & Emmet (1985); Langmaid et al. (1989) for Lepidoptera and plant references
  - Twiston-Davies, Grace (PhD thesis, 2014) underpinning the data adaptation

## References
- Hardy, P. B., et al. 2007
- Heath, J. H., and A. M. Emmet 1985
- Langmaid, J. R., et al. 1989
- Pollard, E., and T. J. Yates 1993
- Ries, L., and D. M. Debinski 2001
- Stace, C. 2010
- Stewart, K. E. J., et al. 2001