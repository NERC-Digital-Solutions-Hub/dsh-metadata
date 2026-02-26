# Supporting documentation for Stable_concentration_means.csv

## Overview
- Documents the structure and meaning of columns in the Stable_concentration_means.csv dataset.
- Covers sample identifiers, taxon information, experimental context, and a wide range of elemental concentrations with associated statistics.
- Focuses on fresh weight basis measurements expressed in milligrams per kilogram (mg/kg), with mean type and variability included.

## Data Model and Key Fields
- Sample_Code: unique sample identifier.
- Species: Latin name of the sampled species.
- RAP: ICRP Reference Animals and Plants (RAP) classification to which the species can be attributed.
- Sample_Description: portion of the sample analyzed.
- Mean_Value: indicates whether the reported mean is geometric or arithmetic.
- Element concentration fields (examples): I-127_mg_kg, Li_mg_kg, Be_mg_kg, B_mg_kg, Na_mg_kg, Mg_mg_kg, Al_mg_kg, P_mg_kg, S_mg_kg, K_mg_kg, Ca_mg_kg, Ti_mg_kg, Mn_mg_kg, Fe_mg_kg, Co_mg_kg, Ni_mg_kg, Cu_mg_kg, Zn_mg_kg, As_mg_kg, Se_mg_kg, Rb_mg_kg, Sr_mg_kg, Mo_mg_kg, Ag_mg_kg, Cd_mg_kg, Cs_mg_kg, Ba_mg_kg, Pb_mg_kg, U_mg_kg (and related variants).
- For each element: Standard_Deviation_<element>_mg_kg, denoting the standard deviation on a fresh weight basis.
- Units and notes: Most concentrations and standard deviations are in mg/kg; notes explain mean type and basis where applicable.

## Metadata and Standards
- Units: Milligrams per kilogram (mg/kg) for chemical concentrations; Basis: fresh weight.
- Documentation fields include Explanation, Units, and Notes to clarify the meaning of each column and its calculation basis.
- Mean_Value notes indicate whether the mean is geometric or arithmetic and are intended to align with the corresponding standard deviation reporting.
- Notes contain guidance such as “Geometric or arithmetic mean as identified by Mean_Value” and similar phrasing for standard deviations.

## Data Quality and Governance Considerations
- Ensure consistent interpretation of Mean_Value across all rows and corresponding statistics.
- Validate alignment between mean type (Mean_Value) and its reported statistics (Standard_Deviation_* fields).
- Maintain metadata completeness for Sample_Code, Species, RAP, and Sample_Description to support discoverability.
- Enforce uniform units (mg/kg) and confirm measurements are on a fresh weight basis.
- Document data provenance, any transformations, and the source of RAP classifications.
- Track data availability, including any embargoes or access restrictions.
- Address incomplete records and resolve inconsistent or garbled field descriptions (e.g., typographical inconsistencies).

## Data Availability and Accessibility
- Designed to be uploaded to data portals and catalogues for discoverability and reuse by researchers and stakeholders.
- Comprehensive field-level documentation supports understanding and correct usage of the dataset.

## Practical Challenges Highlighted by the Documentation
- Incomplete picture of user needs and priorities for metadata and dataset structure.
- Timeliness of data provision from data producers and collaborators.
- Ensuring data creators meet standards, including complete metadata for each element.
- Interoperability across many systems and formats and the handling of numerous analytes.
- Working with large datasets and older databases that may require bespoke, non-interoperable solutions.

## Recommendations for Data Stewards
- Standardize column naming for all elements (e.g., <Element>_mg_kg) and ensure consistent naming across the dataset.
- Correct typos and reduce duplication or garbled field descriptions to improve clarity.
- Ensure explicit documentation for high-importance fields like U_mg_kg and other lesser-documented elements.
- Provide a separate, structured data dictionary with clear examples and unit definitions.
- Implement validation checks to ensure that Mean_Value is consistently applied with the corresponding standard deviations.
- Establish data release policies and versioning to manage updates and provenance over time.