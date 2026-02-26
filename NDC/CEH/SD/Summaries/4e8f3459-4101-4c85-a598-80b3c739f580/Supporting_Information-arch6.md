# Introduction

- Purpose: A dataset of IMOGEN (Integrated Model Of Global Effects of climatic anomalies) impact modelling system parameters, used to test new land surface parameterisations before full GCM implementation and to project future emission scenarios.
- Concept: Based on pattern-scaling to emulate Global Circulation Models (GCMs); local monthly meteorological changes scale linearly with global land warming; uses an Energy Balance Model (EBM) to relate evolving atmospheric forcing to land warming with oceanic delays.
- Data scope: Calibration of IMOGEN EBM parameters and patterns against 22 GCMs from the CMIP3 ensemble; patterns are provided for download in ASCII format.
- Key parameters: Five EBM parameters per GCM – climate sensitivity over land λ_l, ocean λ_o (W m^-2 K^-1), ocean effective thermal diffusivity κ (W m^-1 K^-1), ratio ν of mean land and ocean SST warming, and ocean fraction f.
- Data structure and access: For each GCM, a directory pattRelPR_d2_<GCM> contains 12 monthly ASCII files (jan–dec) on a common HadCM3 grid (2.5° x 3.75°, 1631 land points). Each file includes a header and 1631 lines describing per-point data.
- File content: Each point line lists longitude, latitude, and changes per degree of global warming for variables such as temperature, humidity, wind, longwave/shortwave radiation, precipitation, and pressure (with several unused columns).
- Usage with JULES: IMOGEN is routinely coupled to the JULES land surface model; examples of coupling are cited in related publications.
- Data quality and development: Part of a beta program to extend IMOGEN parameterisation beyond UK GCMs (CMIP3); a new version aligned with CMIP5 is under development to enhance traceability and UK ISO standards.
- Acknowledgement and support: Thanks to modelling groups, PCMDI, WGCM, and WCRP/CMIP; data support supported by the U.S. Department of Energy.
- References: Key related works include Huntingford et al. (2010) on IMOGEN, Huntingford & Cox (2000) on pattern analogue methods, Meehl et al. (2007) on CMIP3, and JULES model descriptions (Best et al. 2011; Clark et al. 2011). Zelazowski et al. (2016) notes forthcoming climate pattern scaling work.