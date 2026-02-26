# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) soil bulk density from three soil depths on salt marsh sites at Morecambe Bay and Essex

- The dataset measures bulk density (g/cm-3) at three soil depths (0-10 cm, 10-20 cm, 20-30 cm) across salt marsh sites in Essex and Morecambe Bay.
- Field campaign conducted in Winter and Summer 2013, with additional Essex sampling 2–6 March 2013.
- Sampled locations include:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Site coordinates (approximate): 
  - Essex: AH (51°47′N, 0°52′E), FW (51°49′N, 0°58′E), TM (51°41′N, 0°56′E)
  - Morecambe Bay: CS (54°10′N, 3°0′W), WS (54°8′N, 2°48′W); West Plain location described but coordinates not provided
- Habitat types represented: Saltmarsh and Mudflat; contrasted by soil type (clay in Essex; sandy in Morecambe Bay) and grazing regimes.
- Sampling units: quadrats with bulk density measured in three depths per quadrat; slight variations in sampling windows per site.
- Data format: Excel workbook; NA entries indicate missing data.

## Data content and structure

- Core variables (Dataset Field descriptions):
  - Row Number: numeric sort key
  - Season: Winter (W) or Summer (S)
  - Location: Morecambe (M) or Essex (E)
  - Site: Morecambe: CS, WS, WP; Essex: AH, FW, TM
  - Habitat: Mudflat (MF) or Saltmarsh (SM)
  - Quadrat Number: 1–22
  - Scale: A = 1 m; B = 1–10 m; C = 10–100 m; D = 100 m to upper
  - BD_D1: Bulk density at 0–10 cm
  - BD_D2: Bulk density at 10–20 cm
  - BD_D3: Bulk density at 20–30 cm
- Primary measurement formula: Bulk density = dry soil mass / core volume
- Core methodology: Bulk density rings (3.1 cm height, 7.5 cm diameter), dried at 105°C for 72 hours prior to measurement
- Data provenance: Observations taken during Winter/Summer 2013; Essex winter samples collected in an extended sampling window
- Quality and calibration: Calibration procedures noted as None; data checking procedures are listed but specific methods are not provided
- Data completeness: NA cells indicate missing data in the dataset

## Data use for GIS and mapping

- Suitable for creating point or polygon-based maps of soil bulk density across salt marsh sites, with depth-specific attributes (BD_D1, BD_D2, BD_D3).
- Spatial aggregation options:
  - Use Quadrat Number and Scale to place data at precise quadrat centers or aggregate to larger map units per scale category (A–D).
  - Join to habitat or site polygons to visualize relationships with habitat type or grazing regime.
- Potential GIS workflows:
  - Import the Excel workbook as a tabular layer; create point features for quadrat centers (if coordinates are available or inferred from Scale and Quadrat Number).
  - Alternatively, convert to gridded data by aggregating quadrat-level BD values to raster layers at different depths.
  - Symbolize by depth (three layers) or by combining depths to show vertical soil density profiles.
  - Overlay with other CBESS layers (biodiversity, ecosystem services, inundation frequency, vegetation types) for integrated analyses.

## Considerations and limitations

- Temporal context: Data from 2013; consider temporal relevance for current analyses and potential changes in grazing, vegetation, or hydrology.
- Spatial specifics: Exact quadrat coordinates are not provided; use Scale, Quadrat Number, and Site/Habitat data to reconstruct positions if precise geolocations are necessary.
- Data quality notes: Limited detail on QA/QC procedures; calibration details are listed as None.
- Missing data: Some fields contain NA values, requiring handling during GIS integration.

## Access and integration guidance

- File format: Excel workbook
- Fields to extract for GIS: Season, Location, Site, Habitat, Quadrat Number, Scale, BD_D1, BD_D2, BD_D3
- Best practice: Document any assumptions used to place quadrats spatially (e.g., center coordinates per quadrat and scale) and note data age in metadata. Include provenance to Hilary Ford as staff contact.