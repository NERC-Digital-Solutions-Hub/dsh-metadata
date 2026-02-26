# Supporting Documentation for EIDC_SA_9209af2c-24f6-4e37-98fe-550032e97a2c.rtf

## Purpose and scope
- Model potential carbon storage in urban areas of Milton Keynes/Newport Pagnell, Bedford, and Luton/Dunstable, UK.
- Use InVEST 3.1.0 ecosystem service model to quantify carbon storage as an urban ecosystem service.
- Compare model results across two input data scales (5 m and 25 m) to assess scale effects.
- Deliver outputs as GeoTIFF raster maps (kg C per m2) with accompanying metadata suitable for GIS use.

## Methods and data sources
- Modeling framework
  - InVEST 3.1.0 used to estimate carbon storage across study area.
  - Goal: assess carbon storage as an ecosystem service and explore how input data scale affects results.
- Spatial data and resolutions
  - 5 m resolution: land cover map created from colour infrared aerial photography (cir) with 0.5 m original resolution; imagery from LandMap Spatial Discovery project; dates: Bedford (2009), Luton (2009/2010), Milton Keynes (2007/2009); processing included NDVI thresholding to separate vegetation from non-vegetation and UK Ordnance Survey MasterMap for buildings/water; vegetation classified into broadleaf trees, coniferous trees, and grass/herbaceous via eCognition segmentation; resampled to 5 m for modelling.
  - 25 m resolution: raster version of OS Land Cover Map 2007 (Digimap 2007) used to represent widely available data for some modellers.
- Carbon storage values
  - Published literature values used for urban land cover types:
    - Aboveground carbon: Davies et al. (2011).
    - Soil carbon: Edmondson et al. (2014).
  - Landscape-scale carbon storage expressed in kg C per m2.
- Model provenance and tools
  - InVEST (Integrated Valuation of Environmental Services and Tradeoffs) 3.1.0, developed by the Natural Capital Project (http://www.naturalcapitalproject.org/invest/).
  - eCognition (Trimble 2011) used for image segmentation; CIR aerial imagery processed to derive land cover.
- Documentation and metadata
  - Outputs provided as two GeoTIFF raster maps plus metadata and spatial information files required by GIS software.
  - Data and metadata designed to be viewable/manipulable in Geographic Information Systems.

## Quality, validation, and governance
- Quality control
  - Conducted informally; no local empirical validation due to lack of comparable soil/biomass measurements at the required scale.
  - Emphasis on theoretical soundness of model parameters and comparability with published studies.
- Validation context
  - Model results compared to published literature from other UK/European locations to assess plausibility.
- Data provenance and transparency
  - Clear description of data sources, processing steps, and transformations to enable traceability.
  - Metadata and spatial information accompany raster outputs to support data governance and reuse.

## Outputs and accessibility
- Deliverables
  - Two GeoTIFF raster maps representing potential carbon storage at 5 m and 25 m input scales.
  - Associated metadata and spatial information files required by GIS software.
- Format considerations
  - Unit of measurement: kilograms of carbon per square meter (kg C/m2).
  - Outputs are suitable for viewing, analysis, and integration into broader urban environmental monitoring frameworks.

## Relevance to monitoring framework practitioners
- Data scale and interoperability
  - Demonstrates impact of input data resolution on carbon storage estimates, informing decisions about data selection in monitoring programs.
- Data provenance and openness
  - Thorough documentation of data sources, processing, and model parameters aligns with data governance and transparency goals.
- Stakeholder and literature alignment
  - Uses widely cited literature values to anchor estimates, enabling comparability across studies and informing policy assessments.
- Practical limitations and improvements
  - Absence of local validation highlights a need for targeted data collection (soil and biomass measurements) to strengthen monitoring evidence.
  - Highlights ongoing data needs: local datasets, robust metadata, and potential updates as new carbon storage values or higher-resolution data become available.

## Limitations and potential improvements
- Empirical validation gap
  - No direct ground-truth measurements of soil or aboveground carbon at the study scale to validate model outputs.
- Data source variability
  - Use of two distinct input data scales introduces potential modal differences; future work could harmonize datasets or evaluate additional scales.
- Data sharing and governance
  - While metadata is provided, explicit open-data sharing considerations and governance arrangements would strengthen reuse and transparency in monitoring contexts.

## Selected references cited
- Davies ZG, Edmondson JL, Heinemeyer A, et al. (2011). Mapping an urban ecosystem service: Quantifying above-ground carbon storage at a city-wide scale. Journal of Applied Ecology.
- Edmondson JL, Davies ZG, McCormack SA, et al. (2014). Land-cover effects on soil organic carbon stocks in a European city. Science of the Total Environment.
- Grafius DR, Corstanje R, Warren PH, et al. (2016). The impact of land use/land cover scale on modelling urban ecosystem services. Landscape Ecology.
- Tallis HT, Ricketts T, Guerry AD, et al. (2014). InVEST 3.1.0 User’s Guide.
- Landmap; Bluesky (2014). Colour Infrared (CIR) data for England and Wales.
- Digimap (2007). Land Cover Map 25m. 1:250,000.
- Trimble (2011). eCognition Developer.