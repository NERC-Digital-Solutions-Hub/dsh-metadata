### Income deprived older people in an area (% of people 60 or over)

**Description:**
This field (identified internally as `OlderAdultIncomeDeprivation` in the spatial dataset) represents the percentage of the population aged 60 or over who are experiencing income deprivation within a given Lower Super Output Area (LSOA). It serves as a focused proxy for financial disadvantage among a community's older population.

**Vulnerability Rationale:**
This metric is a core indicator within the "Income" domain, which is utilized to evaluate a community's "(In)ability to Prepare", "(In)ability to Respond", and "(In)ability to Recover" from extreme climate events, such as floods and heatwaves. 

Higher proportions of people on low incomes indicate a higher level of social vulnerability. A lack of financial resources significantly restricts an older person's adaptive capacity during an extreme weather event for several reasons:
*   **Preparation:** Low-income households are significantly less likely to have the financial capacity to fully prepare for future hazards, such as by affording property-level protection measures, cooling systems, or adequate home insurance.
*   **Housing Tenure:** Low-income households are less likely to own their own homes. The combination of living in rented accommodation and having a low income severely restricts a person's ability to make physical modifications or adaptations to the property.
*   **Response and Recovery:** A lack of savings restricts the ability of households to respond immediately to flood or heatwave damage, making it much harder to recover from impacts and kick-start the recovery process. 

**Interpretation:**
When used to calculate the final vulnerability indices, this raw percentage is standardized (often represented as a Z-score, `Z_OlderAdultIncomeDeprivation`) to allow for direct relative comparisons across different geographic areas:
*   **Higher percentages** denote a higher concentration of income-deprived older individuals, indicating lower average wealth and a higher level of social vulnerability.
*   **Lower percentages** signify lower rates of income deprivation among older people, indicating greater financial capacity to adapt and lower relative vulnerability.

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying data for this indicator is derived from the English Indices of Deprivation 2019 (IMD 2019). Specifically, it utilizes the "Income Deprivation Affecting Older People" sub-domain (often referred to as IDAOPI), which measures the number of income-deprived older people in an area, converted into a percentage of people aged 60 or over, and is sourced via the Department for Work and Pensions. It carries a weight of 0.333 within the broader "Income" domain, sharing this dimension equally with the indicators for overall income deprivation and employment deprivation.