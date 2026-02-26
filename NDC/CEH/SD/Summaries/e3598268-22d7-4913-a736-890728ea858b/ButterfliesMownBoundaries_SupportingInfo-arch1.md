# Data collection methods and description of Lepidoptera data from a mown boundary experiment within the Stonehenge landscape, UK

## Overview
- Presents raw data on the behavior and distribution of Lepidoptera (butterflies and day-flying moths) at the Stonehenge Landscape in 2012.
- Includes Lepidoptera flight-path data and botanical data (number of flowering units and percentage cover in quadrats).
- Data quality assurance performed to identify outliers/anomalies using pivot tables and exploratory analysis.

## Study site
- Location: National Trust Stonehenge Landscape within the Stonehenge World Heritage Site, Wiltshire, UK.
- Context: Long-term landscape-scale grassland restoration since 2000; seed from calcareous grassland donor patches on Salisbury Plain.
- Habitat mosaic: Chalk grassland fragments, grassland re-creation fields, semi-improved pasture, arable land, and woodland.
- Visuals: Map and site descriptions accompany the data (Figure references included).

## Experimental setup
- Field: Seven Barrows grassland re-creation field sown in 2000 with chalk grassland seed; most similar plant community to chalk grassland target habitat.
- Boundaries: Two large 40 m x 50 m grassy areas with eight 20 m survey boundaries (1-8). Four boundaries are treatment (edge of mown area) and four are control (dummy boundaries in continuous grassland).
- Blocks: Two blocks labeled as ‘sheltered’ and ‘exposed’ (relative to woodland and wind). Boundary arrangement minimizes variation in microclimate and plant community.
- Spacing and constraints: Boundaries close to each other; total mown area capped at 400 m2; experimental area fenced to 100 m across. Boundaries located to minimize confounding effects from fences and edge proximity.
- Survey window: Boundaries surveyed 24 July–23 August 2012; time between survey periods ~10 days; randomization of boundary order and survey timing to reduce pseudoreplication.

## Lepidoptera surveys
- Method: Surveyor tracks flight paths at the boundary, within 10 m on either side of a 20 m x 20 m survey area.
- Duration: Each Lepidoptera observed for 3 minutes; total boundary survey time 20 minutes per survey period; three survey periods across five weeks.
- Boundaries: Each boundary surveyed for all three periods; order randomized; equal effort on both sides of the boundary.
- Data collected per sighting: species, start and finish location (within unmown/mown sides or boundary edge), flight path, and behavior (Cross, Following, Avoiding, Staying).
- Periods: Three survey periods occurred within the peak imago abundance window; weather conditions aligned with UK Butterflies Monitoring Scheme standards.

## Environmental variables
- Vegetation: Eight 0.5 m x 0.5 m quadrats per boundary area (four in unmown side, four in mown side, plus corresponding control sides) to measure vegetation height/density (drop-disc method) and nectar flower availability (flowering units by family).
- Timing: Botanical measurements on 19 July, 10 August, and 23/24 August.
- Meteorology: Wind speed and direction from the nearest station (Boscombe Down) by hour; cloud cover estimated by eye.

## Plant and Lepidoptera nomenclature
- Plant taxonomy: Stace (2010) New Flora of the British Isles.
- Lepidoptera taxonomy: Langmaid et al. (1989) and Heath & Emmet (1985); field identification supported by standard field guides.

## Data structure and key columns
- Data captures for Lepidoptera and environmental context, including:
  - Date, temperature, wind speed and direction, cloud cover.
  - Grid square (Edge or Control), plot type (Mown, Chalk unmown, or Edge) and side (West/East).
  - Survey edge ID, start and end times.
  - SPECIES and SPECIES CODE; SEX; BEHAVIOUR (Follow, Avoid, Cross, Stay); START HABITAT TYPE and END HABITAT TYPE; DIRECTION OF MOVEMENT; NOTES; NECTARING ON.
  - For plants: FLOWERING UNITS and COVERAGE; species codes and associated habitat details.
- Data sets referenced as UK-1, UK-2, UK-3, and UK-4 corresponding to Lepidoptera and flowering plant data collection sheets.

## Lepidoptera and flowering plant species
- Comprehensive tables listing Lepidoptera species surveyed, with scientific names, common names, and abbreviated codes (e.g., Maniola jurtina – Meadow Brown; Zygaena filipendulae – 6-spot Burnet Moth; Pieris spp., Polyommatus icarus, etc.).
- Extensive list of flowering plant species with scientific names, common names, and species codes (covers grasses, forbs, and nectar sources such as Lotus corniculatus, Primula veris, Trifolium spp., etc.).
- Nectar plant categories tied to resource measurements used in environmental variable assessments.

## Key considerations, limitations, and interpretation
- Edge effects and proximity to mown areas may influence Lepidoptera behavior at transect boundaries.
- Small-scale experimental layout (2.5 m from mown edge; 15 m minimum from fences) may introduce edge-associated responses.
- Control boundaries are designed to mimic edge conditions but are dummy boundaries; interpretation requires careful consideration of boundary-specific context.
- Sampling window focuses on peak adult butterfly activity but represents a subset of the annual flight season; possible under-sampling of other species or timings.
- Data accessibility and standardization are addressed through metadata and codes to facilitate cross-study comparisons.

## References
- Campbell (2009); Hardy et al. (2007); Heath & Emmet (1985); Langmaid et al. (1989); Pemberton (2011); Pollard & Yates (1993); Ries & Debinski (2001); Rodwell (1992); Stace (2010); Stewart et al. (2001); Young et al. (2009).