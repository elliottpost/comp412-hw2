# comp412
LUC Summer '15 COMP 412 - Open Source

## Original Data Sources
Food Inspections <https://data.cityofchicago.org/Health-Human-Services/Food-Inspections/4ijn-s7e5>  
Census Data <https://data.cityofchicago.org/Health-Human-Services/Census-Data-Selected-socioeconomic-indicators-in-C/kn9c-c2s2>  

## Notes about data cleaning
### Food Inspections
Fields used: {Inspection Date, Results, Latitude, Longitude, Location }  
Records used: June 9, 2015 through Jan 1, 2013  
Results standardized:  
* Fail -> fail
* Out Of Business -> record ignored
* Pass -> pass
* Pass W/ Conditions -> pass
* Not ready -> record ignored
* No Entry -> record ignored
* Business Not Located -> record ignored

Ignored records and records without a valid lat/long were removed from data set.

### Census Data
Fields Used: {Community ID, COMMUNITY AREA NAME, PERCENT HOUSEHOLDS BELOW POVERTY, PER CAPITA INCOME }  
Records Used: all records except for aggregated "CHICAGO" record at end of original data set.  
Results standardized:


## Known issues with data and processor
* The census data stops at 2010, but records for food inspections are from 2013-2015. We assume the income data can be extrapolated from census data and is unchanged in any significant manor in 5 years.   
* Chicago neighborhood boundaries seem to vary by map. Some maps do not have all the neighboorhoods, some maps (such as the one we are using) have more neighborhoods than the Chicago census data records.