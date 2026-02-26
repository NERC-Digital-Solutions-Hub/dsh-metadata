# General information

- This dataset provides estimates of plant abundance (leaf area, floral units, seeds by mass and energy) from field-based sampling on Norwood Farm, Somerset, UK (51.3128N, -2.3206W) during 2007 and 2008, when the farm was managed organically at relatively low intensity.
- Primary references: Pocock et al. (2012); the dataset of interactions published in Dryad Digital Repository (doi:10.5061/dryad.3s36r118); full study details and site description in Pocock et al. (2012) and Supplementary Online Material (Extract_from_SOM.rtf).
- Data files describe methods and metadata for map-based data products and spatial analyses of plant abundance across habitats on the farm.

## Data files and schema

- leafarea.csv
  - Columns include SamplingRound, Month and year, HabitatCode (see habitatarea.csv), PlantTaxon, PlantFamily, LEAFAREA_square_metres.
  - Leaf area estimated for up to four 9 x 1 m transects per habitat per month; leaf area index (LAI) measured or inferred; leaf area apportioned among species according to abundance x height and scaled by habitat area.
- floralunits.csv
  - Columns include SamplingRound, Month and year, HabitatCode, PlantTaxon, PlantFamily, FLORALUNITS_total.
  - Floral units (flowers that attract pollinators) counted from transects (25 x 1 m in 2007; 50 x 1 m in 2008); defines what constitutes a floral unit for each taxon.
- seeds.csv
  - Columns include Season, HabitatCode, PlantTaxon, PlantFamily, SEEDS_TotalCount, SEEDS_MassInKg, SEEDS_EnergyInKJ.
  - Seeds sampled via vacuum method, oven-dried, seeds identified; under-sampling correction applied (based on Evans et al. 2009); mass and energy drawn from site data and databases; totals scaled by habitat area.
- habitatarea.csv
  - Columns include HabitatCode, HabitatDescription, Area_in_Year1_square_metres, Area_in_Year2_square_metres.
  - Provides habitat definitions and the area of each habitat for year 1 (2007) and year 2 (2008); useful for spatial weighting and mapping.
- A map of the farm referenced in Evans et al. (2011) is cited as a spatial context resource.

## Spatial and temporal context

- Location: Norwood Farm, Somerset, UK.
- Spatial units: habitat codes with corresponding areas; data designed to be integrated into map-based visualizations by habitat.
- Temporal coverage: 2007 and 2008, with leafarea and floralunits aligned to Year 1 (2007) and Year 2 (2008); seeds data aligned to winter, spring, summer 2007 (Year 1) and autumn 2007 (Year 2) as described.
- Data are suitable for cross-habitat and habitat-aggregated GIS analyses, enabling visualization of plant abundance across space and time.

## Data collection, processing, and quality

- Leaf area
  - Measured via transects; LAI measured with LAI-2000 or inferred from literature for woodland habitats.
  - Leaf area apportioned among taxa according to their relative abundance and height; scaled by habitat area.
- Floral units
  - Flowers counted as floral units across transects; transect sizes varied by year (2007 vs 2008).
  - Floral units defined to reflect ecologically relevant foraging units for pollinators.
- Seeds
  - Seed counts, mass, and energy measured from up to 39 samples per habitat per month; samples processed with vacuum sampler; seeds identified by specialists.
  - Under-sampling corrections applied using a site-derived factor (Evans et al. 2009); mass and energy derived from site data and external databases (Evans et al. 2011).
- General notes
  - Full methodological details are in Pocock et al. (2010, 2012) and the Supplementary Online Material (Extract_from_SOM.rtf).
  - Data are designed to be integrated with other ecological network data (e.g., plant-pollinator interactions) and mapped by habitat and time.

## GIS use and integration considerations

- Keys for integration
  - Join leafarea.csv, floralunits.csv, and seeds.csv to habitatarea.csv on HabitatCode and (where applicable) Year/Season to enable per-habitat spatial visualizations over time.
  - Use PlantTaxon and PlantFamily as taxonomic attributes for thematic mapping and filtering.
  - Use Area_in_Year1/Area_in_Year2 to weight spatially across habitats when aggregating by map units.
- Potential visualizations
  - Map leaf area or LAI by habitat and month to show spatial distribution and temporal trends.
  - Map floral units by habitat and month to illustrate pollinator resources.
  - Map seed abundance, mass, and energy by habitat and season to assess resource availability.
- Data quality and standards considerations
  - Ensure consistent habitat coding using habitatarea.csv; verify that Year/Season alignments are correct across files.
  - Be aware of resolution differences and ensure unit consistency (area in square metres; LAI-derived calculations).
  - Consider potential under-sampling corrections for seeds when interpreting abundance or energy metrics.

## Access and references

- Dataset and related publications:
  - Pocock et al. (2012). The robustness and restoration of a network of ecological networks. Science.
  - Evans, D.M., McLeod, J.J., Pascoe, L., & Memmott, J. (2009). Seed sampling method details.
  - Evans, D.M., Pocock, M.J.O., Brooks, J., & Memmott, J. (2011). Seeds in farmland food-webs.
  - Pocock, M.J.O., Evans, D.M., & Memmott, J. (2010). Farm management and leaf area index.
  - Dataset available in Dryad at http://dx.doi.org/10.5061/dryad.3s36r118.
- Supplementary materials with full study details: Extract_from_SOM.rtf.