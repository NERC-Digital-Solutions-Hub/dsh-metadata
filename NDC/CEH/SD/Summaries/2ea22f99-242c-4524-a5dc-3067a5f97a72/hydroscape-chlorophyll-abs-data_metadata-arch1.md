# Hydroscape chlorophyll abs data

## Quick overview
- Dataset of chlorophyll absorbance linked to phytoplankton bioassays (PHYT) and periphyton samples (PERI) from multiple sites in England.
- Includes nutrient treatment experiments, replicate measurements, and detailed site metadata (locations, deployment order, and timing fields).

## Data collection and measurement methods
- Sampling locations include Bassenthwaite Lake, Decoy Broad, Derwentwater, Grasmere, Etshwaite Water systems, Ranworth Broad, Wroxham Broad, and others, covering lakes, tarns, and streams.
- Phytoplankton (PHYT) samples: surface dip water samples collected at the deepest point in each lake; incubated in laboratory with nutrient treatments.
- Periphyton (PERI) samples: periphyton filters deployed in streams using nutrient diffusing periphytometers for two weeks, then retrieved and frozen.
- Sample processing: initial filtration through a 1 µm mesh to remove grazers; aliquots spiked with nutrient treatments or left as controls; incubation (PHYT: days; PERI: two-week deployment), followed by extraction and filtration onto GF/C filters; extracts stored at -20°C.
- Post-incubation measurements: absorbance measured with a spectrophotometer at multiple wavelengths using methanol extraction and 1 cm cuvettes.
- Brief quality steps: baseline wavelength scans and auto-zeroing/blank corrections prior to absorbance readings.

## Data structure and content
- Data columns include:
  - System: group of sites
  - Site: site name
  - Algae: type of bioassay (PHYT or PERI)
  - Deployment: deployment order (1–4, with 0 for trial deployments)
  - DateStart / DateStop: incubation start/stop dates
  - Vol_or_Area: volume (ml) for PHYT or area (cm2) for PERI
  - DataFlag: indicates known issues (1 = issues present, 0 = no issues)
  - DOSE: nutrient treatment level (0–6) with scheme differing for PHYT (0 initial, 1 control, 2 P, 3 Nitrate, 4 NP, 5 Ammonium, 6 Silica) and PERI (1 control, 2 P, 3 Nitrate, 4 Ammonium, 5 NP, 6 Silica)
  - REPLICATE: replicate identifier (usually A–C; sometimes A–D)
  - 632nm, 652nm, 665nm, 696nm, 750nm: absorbance readings at specified wavelengths
  - Dilution_factor: dilution level (1 = no dilution, 2 = 50% dilution)
- Site names and coordinates table provides Eastings/Northings for mapping and geographic context.
- The dataset focuses on chlorophyll a extraction and absorbance rather than direct chlorophyll concentration values.

## Measurements, units, and quality control
- Absorbance values are recorded in optical density units at the specified wavelengths.
- Quality control includes triplicate analyses for each treatment, baseline scans, instrument blanking, and blank-corrected absorbance values.

## Spatial and temporal coverage
- Spatial: broad coverage across multiple lakes, tarns, and broads in the region, with precise site coordinates provided.
- Temporal: fields for DateStart and DateStop allow tracking of incubation periods; deployments occur in seasonal sequences (1–4, with 0 as trial), though exact dates are not enumerated in the metadata excerpt.

## Data usage notes and considerations
- Data are structured to support analysis of nutrient impacts on chlorophyll-related absorbance for phytoplankton and periphyton communities across diverse freshwater sites.
- The DOSE scheme and PERI/PHYT distinctions enable comparative analyses of nutrient limitation and community responses.
- Known issues flag (DataFlag) helps identify rows requiring caution or further validation.
- The dataset accommodates mapping and spatial analyses via site coordinates, facilitating cross-site comparisons and regional assessments.

## Practical implications for analysts
- Enables correlation analyses between nutrient treatments and absorbance responses across sites and biomes.
- Supports development of predictive models for nutrient-induced changes in chlorophyll-related signals in freshwater ecosystems.
- Requires careful handling of replicate identifiers and interpretation of DOSE coding differences between PHYT and PERI datasets.