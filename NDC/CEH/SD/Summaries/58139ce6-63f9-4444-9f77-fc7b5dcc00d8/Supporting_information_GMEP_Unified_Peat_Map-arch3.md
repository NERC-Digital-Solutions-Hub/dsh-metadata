# The Glastir Monitoring and Evaluation Programme (GMEP)

- Purpose and scope
  - Welsh Government monitoring programme established in 2013 to assess the effects of the Glastir agri-environment scheme on the environment.
  - Aims to collect evidence on the effectiveness of bundles of management interventions related to climate change, biodiversity, soil and water quality, and woodland expansion.
  - Also seeks to quantify overall environmental status and trends, and to identify how drivers of change (land use, climate, pollution) impact Wales beyond Glastir interventions.

- The unified peat map: objective and significance
  - Developed to support GMEP with an updated, comprehensive map of peat extent and condition for Wales.
  - Provides analysis of land-use, peatland condition, and associated greenhouse gas emissions.
  - Represents a substantial improvement over earlier peat maps, revealing wide peat distribution across Wales, including upland blanket bog and numerous small lowland peat units.
  - Highlights major peat resources in areas such as Migneint, Berwyn, Cambrian Mountains, Cors Fochno, Cors Caron, and Fenn’s and Whixall Moss, among others.
  - Aids understanding of peat cover in relation to biodiversity and carbon dynamics, supporting monitoring and policy.

- Generation methods (how the unified peat map was produced)
  - Integrated four datasets to create the unified peat map:
    - i) Areas mapped as peat in the British Geological Survey (BGS) superficial geology map (1:50 000).
    - ii) Soil mapping derived from Forestry Commission Wales paper survey records, with soil codes indicating peat >45 cm thickness.
    - iii) Boundary of deep peat (>0.5 m) from the Lowland Peatland Survey of Wales (CCW/NRW).
    - iv) Habitat polygons indicative of deep peat presence from the Habitat Survey of Wales (Phase I).
  - All layers were combined sequentially using the UNION function in ArcMap GIS to produce the final multipart polygon shapefile.

- Output and data format
  - GMEP_Unified_Peat_Map.shp (ESRI Shapefile; multipart polygons) detailing the outline location of peat soils in Wales.
  - Attribute structure includes unique polygon identifiers and geometry metadata (area and length) along with a description field.

- Quality control and limitations
  - The final product’s quality depends on the quality of input datasets; sources come from national agencies and are deemed appropriate for use.
  - Deep peat boundaries are more precise in lowlands and less so in uplands due to vegetation mosaics and mapping limitations.
  - The reliability of the map is linked to the underlying data sources cited in accompanying documents (e.g., Lawley 2009; Pyatt 1982; Kennedy 2002; Jones et al. 2011; Bosanquet et al. 2013; Blackstock et al. 2010).

- Data governance and usage
  - Any product derived from or incorporating the peat data must acknowledge the source with a specified copyright statement.
  - Data includes contributions from the British Geological Survey and Natural Resources Wales, with formal acknowledgments required for usage.

- Stakeholders and partnerships
  - Welsh Government (funding and programme oversight)
  - UK Centre for Ecology & Hydrology (CEH)
  - British Geological Survey (BGS)
  - Natural Resources Wales (NRW)
  - Countryside Council for Wales (CCW), involved via the Lowland Peatland Survey

- References and further reading
  - The document cites a range of foundational studies and reports (e.g., Blackstock et al. 2010; Bosanquet et al. 2013; Evans et al. 2015; Jones et al. 2011; Kennedy 2002; Lawley 2009; Pyatt 1982; Taylor & Tucker 1968) to support methods and context.
  - Acknowledgment statements are required for data provenance, including Crown copyright and BGS data attributions.