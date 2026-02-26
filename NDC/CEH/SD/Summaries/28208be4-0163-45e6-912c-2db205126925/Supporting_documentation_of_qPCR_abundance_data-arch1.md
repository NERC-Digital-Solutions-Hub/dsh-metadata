# Abundance of airborne pollen for nine grass species, measured by qPCR, UK, 2016-2017

## Data access and licensing
- Data are available under the Open Government Licence.
- Access URL: https://doi.org/10.5285/28208be4-0163-45e6-912c-2db205126925
- Usage must cite Brennan, G.; Creer, S.; Griffith, G. (2020). Abundance of airborne pollen for nine grass species, measured by qPCR, UK, 2016-2017. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/28208be4-0163-45e6-912c-2db205126925

## Data collection
- Method: qPCR using QuantStudio 6 Flex Real-Time qPCR machine.
- Targets: nine grass species via ITS2 region primers, including Anthoxanthum odoratum, Arrhenatherum elatius, Cynosurus cristatus, Dactylis glomerata, Lolium perenne, Phleum pratense, Poa pratensis, grass genera Alopecurus/Agrostis; one degenerate probe unable to discriminate all species.
- Analysis: copy number quantified using standard curves provided by Primer Design (range 2 to 2×10^5 copies/µl).

## Timing
- Sampling during grass pollen seasons of 2016 and 2017.
- 2016: 25 May–28 August; 2017: 5 May–10 September.
- Exact dates varied slightly by site.

## Location
- 13 sites across the UK; coordinates provided in the data file.
- Sites on exposed rooftops (4–6 storeys) to sample mixed air flow; away from ventilation inlets/outlets or obstructions.
- Bangor was not part of the Met Office network but used the same pollen count methodology.

## Research sample
- Aerial particles (pollen and other plant-derived material) collected with Burkard Automatic Multi-Vial Cyclone Samplers.
- Flow: 16.5 L/min; collection into 1.5 ml vials on a carousel via mini-cyclone technology.
- Only plant-origin aerial particles targeted with qPCR primers/probes.

## Sampling strategy
- Sites selected to cover broad geographic areas with varied soils/land use.
- Sampling units mounted alongside seven-day Burkard volumetric traps from the Met Office UK Pollen Monitoring Network.
- Bangor site used the same pollen count methodology despite not being in the Met Office network.

## Data exclusions
- From 1,400 daily aerial samples, 1,210 advanced to molecular analysis.
- Exclusions: poor DNA extraction due to rainwater; qPCR efficiency outside 85–115%; high replicate variability (>6.95 upper quartile range); amplification outside 10–38 cycles (to reduce false positives/negatives).

## Reproducibility
- Reliability assessed using positive and negative controls.

## Randomization
- Bangor samples randomized for DNA extractions; DNA extracts randomized on a single 96-well or 384-well plate for qPCR.

## Data structure
- Data file: "qPCR_copy_number_abundance_data_aerial_DNA.csv".
- Header descriptions provided in Table 1, including: qPCRID, Site, Target.Name, Task, ID, start.date, end.date, number.of.days.pooled, year, qPCR standard curve metrics (Y.Intercept, R^2, Slope, Efficiency), Quantity.Mean/SD/var/SE, CT.Mean/SD/var/SE, Day/Month, Year-Month, MaxPoaceaeConc, Latitude, Longitude, number.of.days.
- Columns capture sample identifiers, sampling metadata, qPCR metrics, and geographic/time details for downstream analysis.