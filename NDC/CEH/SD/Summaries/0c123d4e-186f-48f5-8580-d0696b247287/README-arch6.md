# Plant abundance estimates for leaf area, floral units and seeds on Norwood Farm, Somerset, UK (2007-2008)

## Overview
- Dataset of plant abundance estimates (leaf area, floral units, seeds) and habitat areas from field sampling on a single organic farm (Norwood Farm, Somerset, UK) during 2007 and 2008.
- Used to study ecological interactions (food webs and plant-pollinator networks); primary reference Pocock et al. (2012); dataset published in Dryad (DOI provided).
- Full methodological details and study description available in Pocock et al. (2012) and its Supplementary Online Material (SOM).

## Data files and structure
- leafarea.csv: leaf area of each plant taxon by habitat and sampling month/year; fields include SamplingRound, Month, Year, HabitatCode, PlantTaxon, PlantFamily, LEAFAREA_square_metres.
- floralunits.csv: number of floral units per taxon, habitat, and month/year; fields include SamplingRound, Month, Year, HabitatCode, PlantTaxon, PlantFamily, FLORALUNITS_total.
- seeds.csv: seed counts, mass, and energy by habitat, season, and taxon; fields include Season, HabitatCode, PlantTaxon, PlantFamily, SEEDS_TotalCount, SEEDS_MassInKg, SEEDS_EnergyInKJ.
- habitatarea.csv: habitat codes, descriptions, and area by year (Year1 and Year2); clarifies Year1 = 2007 (leafarea/floralunits) and winter/spring/summer 2007 seeds; Year2 = 2008 (leafarea/floralunits) and autumn 2007 seeds.
- Acknowledgements and References: funding sources and bibliographic context; Dryad publication linked; Extract_from_SOM.rtf referenced for methods details.

## Methods and processing
- Leaf area (LAI) estimation: transects (up to four 9 x 1 m in each habitat/month); leaf area index apportioned among species by abundance × height; total scaled by habitat area. LAI measurement used LAI-2000 instrument ( woodland leaves inferred from literature where needed).
- Floral units: counted along transects (three to four per habitat/month), with transects sized 25 x 1 m (2007) or 50 x 1 m (2008); floral units defined as entities that flower-visiting insects fly between.
- Seeds: up to 39 samples per habitat per month via vacuum sampler (soil surface; 7 seconds); seeds oven-dried, identified by specialists; large samples sub-sampled and upscaled; under-sampling corrected with a factor from Evans et al. (2009). Seed mass measured from site samples; energy content from existing databases (Evans et al. 2011/related sources); totals scaled by habitat area.
- Data processing enables cross-habitat comparisons and integration into ecological-network analyses.

## Habitat and temporal mapping
- Habitat codes linked to descriptions in habitatarea.csv; areas provided for Year1 and Year2 to support scaling.
- Temporal mapping: Year1 corresponds to 2007 data for leafarea/floralunits and winter/spring/summer 2007 seeds; Year2 corresponds to 2008 data for leafarea/floralunits and autumn 2007 seeds.

## Provenance and references
- Core references: Pocock, Evans, Memmott (2012) Science; Pocock et al. (2010, 2012) and Evans et al. (2009, 2011).
- Data publication: Dryad Digital Repository; DOI provided in the general information.
- Supplementary material: Extract_from_SOM.rtf for additional methodological details.

## Usage considerations
- Intended to support exploration of plant-resource availability and to underpin analyses of ecological networks (e.g., plant-pollinator interactions) across habitats and seasons.
- Can be combined with the associated ecological-network interaction dataset for comprehensive analyses.
- Important caveats: patchy data across habitats/months, measurement uncertainties inherent in LAI estimation, floral-unit definitions, and seed-sampling corrections; consult the referenced papers and SOM for detailed methodology and limitations.

## Access and Acknowledgments
- Data files: leafarea.csv, floralunits.csv, seeds.csv, habitatarea.csv.
- Acknowledged funding: UK BBSRC (grant no. BBD0156341) and Defra (grant no. BD2303).
- Study location: Norwood Farm, Somerset, UK (51.3128N, -2.3206W).