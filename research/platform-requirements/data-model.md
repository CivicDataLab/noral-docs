# Data Model

An important step in understanding the requirements of the stakeholders was to decipher their relationship with data and what datasets they use in their decision making process. This information helps us create the most efficient systwem possible to better serve the data to the key stakeholders.

### Data Sources

Access to data is dependent on multiple factors like availability, access, usability, and more. For the state of work during this research, we had limited information around what datasets we will use and the role they will play in the final dashboard.&#x20;

Keeping the following in mind, the data model assumptions were based on the following two sources:

* Research led by University of Strathclyde to identify key datasets that will help resolve the needs of the key stakeholders. The final lists of probable datasets can be found [here](https://github.com/The-Data-for-Children-Collaborative/noral-tech-research/blob/main/information-mapping/DATA%20SOURCES%2006-08.xlsx).
* School level including information around techers, children, familities, communioties and more to identify the the journey of a child through the system.

All the datasets were either agreegate at a geographical granularity like, Data Zone, Regional Parliamentary Constituency, Local Authority, Postcode, Admin Area, National Level or at an Individual or an Individual family level. Alongside all this information, the [Common Education Data Standards](https://ceds.ed.gov/Default.aspx) were also reffered to understand what will be the best way to store data around a child in the education setting.

### Data Types

All the possible data described above can belong to one of the following buckets:

1. **Periodic** : Includes data that is usually changed/updated over a period of time and can contain Personally Identifiable Information (PII). Eg: budget allocation, population, expenses etc.
2. **Seldomly Updated** : Includes data that does not get updated frequently. May contain PII. Eg: highest education qualifications, reasons for dropping out of school etc.
3. **Facts** : Facts are data that remain unchanged. No PII. Eg: address of a school, regions, etc.

### Model

The following information around data sources, standards and data types guide the data model to possibly be in the following structure.

![Suggested Data Model](../../.gitbook/assets/data-model.png)
