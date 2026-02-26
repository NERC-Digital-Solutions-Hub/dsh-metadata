# Lepidoptera data from transects within the Stonehenge landscape, UK 2010-2011

- Overview: A dataset of raw Lepidoptera (butterflies and day-flying moths) survey data and accompanying botanical data collected in the Stonehenge Landscape during 2010–2011. Adapted from Grace Twiston-Davies’ PhD work (2014). Includes quality assurance steps (outlier/anomaly checks via pivot tables and exploratory analysis).

- Study site context:
  - Location: National Trust Stonehenge World Heritage Site, Wiltshire, SW UK.
  - Landscape features: mosaic of chalk grassland fragments, grassland restoration fields (started 2000), arable land, semi-improved pasture and woodland.
  - Restoration background: seed transfer from calcareous donor patches to ex-arable fields (2000–2012) to protect archaeological features and ecological value.

- Data collection and survey design:
  - Lepidoptera surveys:
    - Transect-based surveys (adapted from the Butterfly Monitoring Scheme).
    - 17 transects, mostly 200 m long (one 100 m transect noted), surveyed June–September 2010 across habitats and grassland restoration ages.
    - Survey protocol: walk slowly along transect; record Lepidoptera observed within 5 m of the transect, plus nectar plant observations if feeding; surveys conducted three times during the field season.
    - Habitat types covered: chalk grassland fragments on slopes and barrows, older/newer grassland recreations (years 2000–2009), arable land, semi-improved pasture, and adjacent features (barrow groups, Cursus and King Barrows).
  - Habitat quality and plant resources:
    - Vegetation characteristics: height/density (drop-disc method), percent bare ground, percent dead vegetation.
    - Nectar resources: number and percent cover of flowering units; nectar resources tallied by plant families (Dipsacaceae, Fabaceae, Asteraceae).
  - Weather and timing: hourly weather data from nearby Boscombe Down meteorological station; surveys conducted across different times of day to mitigate diurnal effects.
  - Plant and Lepidoptera nomenclature: standardized references for plants and Lepidoptera (Stace 2010; Langmaid et al.; Heath & Emmet; Field Studies Council guides).

- Data structure and metadata:
  - Multi-sheet data organization:
    - Lepidoptera 2010 and Lepidoptera 2011 sheets with location, transect, side of fragment, grid references, and transect details.
    - Resources 2010 and Resources 2011 sheets with habitat/matrix details, drop discs, nectar resources, bare ground, dead vegetation, and flowering units by quadrat.
    - UK-2 to UK-9 tables provide keys and column descriptions for Lepidoptera and flowering plant data, including species codes, sex, date, time, transect, segment, replicate, temperature, wind, cloud cover, behavioral states (flying, feeding, courting, mating, basking, resting), and totals.
  - Data columns and coding:
    - Lepidoptera data: species code, scientific/common name, sex, date, start/end times, transect, segment (20 m), replicate, temperature, wind, cloud cover, behavioral observations, and totals.
    - Flowering plant data: plant species codes, flowering unit counts or percentage cover, nectar-related metrics by family (Asteraceae, Fabaceae, Dipsacaceae).
    - Location and transect identifiers use codes (e.g., WSG, Fargo, Full, Lux) with grid references (SU/BNG) and transect lengths.
  - Nomenclature:
    - Plants follow Stace (2010) and related flora references; Lepidoptera follow Langmaid et al. and Heath & Emmet; field identifications guided by Field Studies Council guides.

- Data quality assurance and provenance:
  - QA processes targeted outliers and anomalies using species occurrence expectations and exploratory data analysis (pivot tables mentioned; specifics not shown).
  - Documentation covers data collection methods, measurement techniques (e.g., drop-disc for vegetation height, nectar plant counting), and data column definitions to support reproducibility.

- Data access, sharing, and reuse considerations for Data Stewards:
  - Metadata richness: extensive field metadata (location codes, transect details, habitat type, dates, times, weather, quadrat-level measurements) supports discoverability and reuse.
  - Standardization needs: rinse-and-repeat metadata schema across years (2010 and 2011) and across multiple sheets; ensure consistent unit definitions (e.g., drop-disc in cm, nectar counts, percent cover).
  - Interoperability: dataset spans multiple habitat types and management regimes; harmonize transect codes, location codes, and grid references for cross-study comparisons.
  - Provenance and versioning: adapt from a PhD study; clarify data custodianship, version control, and any downstream updates or corrections.
  - Access considerations: the document does not specify a digital repository or licensing; Data Stewards should establish a persistent identifier, licensing (e.g., open with attribution), and a data access plan.
  - Potential uses: biodiversity monitoring, landscape-scale habitat restoration evaluation, species-habitat associations, and nectar resource analyses; suitable for integration with other Stonehenge landscape datasets.
  - Limitations for reuse: incomplete field-season details in one or more transects, year-to-year methodological consistency considerations, and potential gaps where some transects were not surveyed in all years.

- Key references (context and methodology):
  - Carvell 2002; Hardy et al. 2007; Heath & Emmet 1985; Langmaid et al. 1989; Pollard & Yates 1993; Stace 2010; Stewart et al. 2001; Young et al. 2009.