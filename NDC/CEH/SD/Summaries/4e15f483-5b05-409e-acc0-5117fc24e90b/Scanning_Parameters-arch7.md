# Scan and Segmentation Details

- Note on processing: All image stacks were down-sampled from original 16-bit depth to 8-bit and cropped to region of interest to reduce processing. Voxel size was reduced where indicated to further manage large stacks.
- Institutional abbreviations: NHMUK = The Natural History Museum, UK; NMS = National Museums Scotland.

## Data Processing and Formats

- Scanning setup: Nikon Metrology HMX ST CT used to scan specimens along the axial axis.
- Data reconstruction: Originally produced as 16-bit VGStudio Max VOL files; output converted to 8-bit BMP stacks (and in some cases 8-bit MCS or 16-bit DCM stacks) for downstream use.
- Endocranial and other segmentation: Endocranial cast segmentation performed; flocculus cast removal conducted for many specimens (segmentation and removal work credited to Stig Walsh or collaborators).
- Final resolutions and scope: Final image stack resolutions reported per specimen range from about 10 µm to 88 µm, with image grids and field of view varying (examples include 1506 x 1211 grid reduced to 764 x 940; other specimens with grids around 571 x 637, 832 x 1014, etc.).
- Slices and field of view: Number of slices per specimen ranges from roughly 429 to 1997; field of view spans approximately 13.52 mm to 82.17 mm, depending on specimen and processing steps.

## Data Sources and Personnel

- Primary institutions contributing data: The Natural History Museum, UK (NHMUK); National Museums Scotland (NMS); The University of Abertay, Scotland.
- Key personnel: Richard Abel (NHMUK), Estelle Bourdon (NHMUK), Stig Walsh (segmentation work and processing), Monja Knoll (segmentation contributions), signatories of endocast and flocculus work.
- Funding and projects: Several specimens linked to NERC Small Grant NE/H012176/1; Intra-European Marie Curie Fellowship 255039; additional grants noted for acquisition and processing.

## Specimen Coverage (Representative Overview)

- The collection spans a wide range of vertebrates (predominantly birds, with multiple mammal and other vertebrate entries) including species such as Acanthorhynchus superciliosus, Alca torda, Alcedo atthis, Amazona aestiva, Apteryx haastii, Aquila chrysaetos, Ara macao, Ardea cineria, Aythya fuligula, Buteo buteo, Casuarius casuarius, Ciconia ciconia, Circus cyaneus, Columba livia, Coracias garrulus, Corvus corax, Creagrus furcatus, Cygnus olor, Diomedea exulans, Dromaius novaehollandiae, Eudyptula sp., Falco spp., Fregata magnificens, Fulmarus glacialis, Gallus gallus, Gavia immer, and many others.
- Catalog and collection identifiers are listed for each entry (e.g., NHMUK S/1966.51.209; NMS Z.2000.08.105; NHMUK A3915; etc.), reflecting the distributed nature of the data across institutions.

## GIS and Data Standards Considerations

- Data custodianship are spread across multiple institutions, highlighting challenges common in GIS-like data integration:
  - Data are held in many places with varying metadata practices.
  - Consistent data standards and metadata schemas are not uniform across entries.
  - Large and complex 3D image datasets require packaging into manageable formats (e.g., standardized 8-bit stacks with clear provenance).
- For GIS-style data products, consider:
  - Adopting a standardized metadata schema capturing: species, taxon, institution, catalog number, scanner, axis, original vs final resolution, voxel size, number of slices, field of view, file formats, segmentation notes, personnel, and funding.
  - Linking specimen metadata to institutional repositories to enable map-based browsing of data availability.
  - Implementing data packaging guidelines to facilitate reuse and integration across collections.

## Notable Methodological Details

- Axial-axis scanning was the standard approach across specimens.
- Endocranial casts and flocculus segmentation were recurring processing steps, with attribution to Stig Walsh and collaborators.
- The overarching aim was to balance data fidelity with processing practicality by down-sampling and cropping while preserving essential segmentation information.