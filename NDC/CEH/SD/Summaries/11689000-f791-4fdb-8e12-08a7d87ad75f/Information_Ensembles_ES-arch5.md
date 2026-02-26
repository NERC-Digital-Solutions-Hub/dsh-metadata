# Details of data-structure

- 12 TIFF raster layers with Mean, Median, and Standard Error of Mean (SEM) for Ecosystem Service model ensembles across stored carbon, grazing use, and non-timber forest products (firewood and charcoal), plus two shapefiles for water supply in catchments delineated for weirs (DWS in South Africa and GRDC globally). A third shapefile provides per-country water use per capita. Overlapping polygons are separated by delineation origin.
- Raster grid and projection: 1,000 m x 1,000 m grid; 1-band, 32-bit floating point values; projection is WGS-1984 Lambert Azimuthal Equal Area (EPSG 9820), units in metres; all inputs re-projected to this definition before calculations.
- Area and coverage: All continental Africa for 36 countries (largely Sub-Saharan, including Madagascar); islands and non-contiguous areas omitted; catchments crossing area boundaries may extend outside; No Data value is -999 (outside area or LCM mask per service).
- Data naming: rasters named <Ensemble type_Service>; shapefiles named <Ensembles_delineation source>.
- Processing and formatting: underlying inputs resampled to 1 km grid, standardized extents and alignment; outputs exported as ASCII then processed in MATLAB, re-exported to ArcGIS as TIFFs. The code to reproduce ensembles is at https://github.com/dhooftman72/ES_Ensembles.
- Normalisation and data handling: all model outputs are log10-transformed (except stored carbon), then linearly normalised to 0–1 using the 95th percentile to reduce influence of extreme values (winsorising). This enables comparability across models and services.
- Model frameworks included (per service): Water availability and water use each combine up to six frameworks (InVEST, Co$ting Nature, WaterWorld, Benefits transfer, LPJ-GUESS, Scholes models, with some models not publicly available); Stored carbon uses four frameworks; Firewood/Charcoal use five; Grazing six. Some notes indicate beneficiary-based models and carbon-derived outputs used for certain services.
- Data scope and model coverage: not all models cover the entire study area; a minimum of three model outputs per gridcell is required to compute ensemble statistics; gridcells without three valid models are set to No Data (-999).
- Publication and provenance: ensembles are based on Willcock et al. (2019) “A Continental-Scale Validation of Ecosystem Service Models” and the WISER project (NE/L001322/1) funded by ESPA; some underlying model outputs are not published due to rights restrictions.
- Output statistics: ensembles provide mean (Emn), median (Emd), and Standard Error of the Mean (SEM) per gridcell (1 km²), per catchment, or per country polygon, depending on the service; values represent relative service delivery normalised to 0–1.
  
## Origin of individual model outputs (Willcock et al. 2019)

- Originates from the WISER project (nearly 6 ecosystem services) and uses six modelling frameworks: InVEST, Co$ting Nature, WaterWorld, Benefits transfer, LPJ-GUESS, and Scholes models (with some bespoke or beneficiary-based adaptations).
- Normalisation approach: log10 transformation (except stored carbon), then 0–1 scaling using the dataset’s 95th percentile to mitigate outliers; values above the 95th percentile are set to 1.
- Service definitions and masking: per-hectare for most services; non-water services use land cover masks to restrict where services can occur; values outside masks set to No Data.
- Publication rights: Willcock et al. (2019) provide the methodological basis; underlying model outputs are not all published due to rights.

## Analytical methods of generating Ensemble Models

- Ensembles are formed by combining available model outputs per service, per gridcell or polygon, producing:
  - Emn(x): mean of all available models for cell x
  - Emd(x): median of all available models for cell x
  - SEMx: standard error of the mean across available models for cell x
- Model availability per cell: number of models with valid values is tracked; an ensemble is computed only for cells with at least three valid model outputs.
- Spatial units: grids are 1 km²; polygons (catchments or countries) differ in size, but calculations follow the same approach.
- Data processing workflow: layers clipped to a standard area shape, aligned, exported as ASCII, combined in MATLAB to produce mean, median, and SEM matrices, re-normalised to 0–1, redrawn in ArcGIS, and exported as TIFFs.
- Reproducibility: the code used for ensemble calculations is available in the cited GitHub repository.

## Frameworks included in the ensembles (per service)

- Available water supply: 6 frameworks (InVEST, Co$ting Nature, Light/Benefit transfer, WaterWorld, LPJ-GUESS, Scholes Growth days model); note some outputs are not publicly available.
- Water usage: 6 frameworks (InVEST, Co$ting Nature, WaterWorld, Benefits transfer, LPJ-GUESS, Scholes Growth days model).
- Stored carbon: 4 frameworks (InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS).
- Non-Timber Forest Product – firewood: 5 frameworks (InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS, Scholes firewood model).
- Non-Timber Forest Product – charcoal: 4 frameworks (InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS).
- Grazing: 6 frameworks (InVEST, Co$ting Nature, Benefits transfer, LPJ-GUESS, Scholes grazing models).

## Funding Information

- Supported by the WISER project (NE/L001322/1) funded by ESPA (EsPA website) and by the EnsemblES project (NE/T00391X/1).

## References Used

- Araújo & New (2007)
- Costanza et al. (2014)
- Kareiva (2011)
- Marmion et al. (2009)
- McKenzie et al. (2012)
- Mulligan (2013, 2015)
- Scholes (1998)
- Smith et al. (2001, 2014)
- Verhagen et al. (2017)
- Willcock et al. (2019)

## Data Stewardship and governance notes

- Provenance: clear lineage from Willcock et al. 2019 and the WISER ESPA project; multiple model frameworks and their handling are documented.
- Metadata and licensing: rights restrictions apply to some underlying model outputs; users should reference the Willcock et al. (2019) work and ESPA sources and respect data use constraints.
- Data completeness and updates: ensembles require at least three models per location; some areas or services may have No Data due to model coverage or masking.
- Data sharing and storage: outputs are stored as standardized TIFFs and ASCII intermediates, with accompanying code to reproduce the process; ensure versioning and traceability for updates or re-processing.
- User needs alignment: the dataset is designed to enable spatial prioritization and optimization (e.g., identifying most important or sensitive areas) by providing comparable ensemble estimates across services.