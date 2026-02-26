# The Glastir Monitoring and Evaluation Programme (GMEP) The unified peat map

- Purpose and aims
  - Establish a monitoring programme (since 2013) to evaluate the effects of the Glastir agri-environment scheme on the environment.
  - Collect evidence on the effectiveness of bundles of management interventions related to climate change, biodiversity, soil and water quality, and woodland expansion.
  - Quantify the status and trends in the Welsh environment and identify how drivers of change (land use, climate, pollution) interact with Glastir interventions.

- The unified peat map: objective
  - Develop an updated map of peat extent and condition for Wales to support GMEP and inform understanding of peat-related greenhouse gas emissions.
  - Highlight the wide distribution of peatlands across Wales, including large upland bogs and numerous small lowland peat units, and identify areas of significant biodiversity interest.

- Generation methods (datasets and integration)
  - Combined four data sources to create a unified peat map of peat >45 cm thick:
    - i) Areas mapped as peat in the British Geological Survey (BGS) superficial geology map (1:50,000).
    - ii) Soil codes 8a–14w from Forestry Commission Wales soil mapping, indicating peat >45 cm.
    - iii) Ground-based delineations of deep peat (>0.5 m) from the Lowland Peatland Survey of Wales.
    - iv) Habitat polygons indicative of deep peat presence (E classes excluding E2) from the Habitat Survey of Wales (Phase I).
  - Data layers were merged sequentially using the UNION function in ArcMap GIS to produce a final multipart polygon shapefile.

- Quality control and caveats
  - Final quality depends on the input data quality; inputs come from national agencies and are judged appropriate for the product.
  - Deep peat boundaries are well-supported in lowlands via direct survey; upland boundaries are less precise due to mosaics of mire and non-mire vegetation.
  - The product provides a derived representation of peat extents (peat bodies ≥0.5 m), with explicit notes on reliability and source data.

- Output and data product
  - GMEP_Unified_Peat_Map.shp: ESRI Shapefile (multipart polygon) showing peat soil outlines in Wales.
  - Key attributes include:
    - FID: Unique polygon identifier
    - SHAPE_AREA: Area of each polygon
    - SHAPE_LEN: Perimeter length
    - DESC_: Description of polygons (e.g., 'Peat')
  - The dataset encompasses peat boundaries and area information suitable for analysis and mapping.

- Context and significance
  - The unified peat map represents a substantial advance over previous Welsh peat mappings and yields a larger peat extent than estimates based on the Soil Survey of England and Wales alone (ECOSSE, 2007).
  - The map reveals substantial peat distribution in both upland and lowland Wales, including notable peat sites (e.g., Cors Fochno, Cors Caron, Fenn’s and Whixall Moss) and widespread lowland peat units in Anglesey, Pen Llŷn, coastal Ceredigion, Pembroke, and Carmarthenshire.
  - Outputs support GMEP's goal of informing policy decisions, monitoring ecosystem responses to land-use changes, and assessing climate-related impacts.

- References and sources
  - Cited datasets and reports from BGS, Forestry Commission Wales, CCW/NRW Lowland Peatland Survey, and Habitat Survey of Wales.
  - Related works: Evans et al. (2015), Lawley (2009), Pyatt (1982), Kennedy (2002), Jones et al. (2011), Bosanquet et al. (2013), Blackstock et al. (2010), ECOSSE (2007), and Glastir Monitoring & Evaluation Programme reports (2010–2017).