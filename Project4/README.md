# Project 4: West Nile Virus Prediction
#### Group 2: Don, Emily, Gabriel, Vincent, Will 
#### 8 June, 2020


## Problem Statement

The deadly, mosquito-borne West Nile Virus has long infested the City of Chicago. It is imperative to develop an accurate predictive model that could identify the key contributing factors that leads to proliferation of the virus. The model and the insights drawn could help the authority to predict future outbreaks of West Nile Virus and thus effectively allocate resources to mitigate it.

The accuracy and recall score from different machine-learning models will be compared and used to evaluate to find the best model for production and prediction.


## Executive Summary

**Exploratory Data Analysis**

It has been found that the 3 main species of WNV-positive mosquitoes are Culex Pipens, Culex Restuans and the Culex Pipens/Restuans Complex. Peak Seasons for Mosquitos has shown to be from around June to September and the optimal temperature range is around 65 to 80 degrees Fahrenheit. 

From the data of mosquito traps collected, the WNV-positive mosquitoes mainly comes from two sources of areas.  the neighbourhoods which have the highest WNV-positive mosquitoes in traps are at O'Hare (Northwest) and South Deering (SouthEast). O'Hare has found to have many retention ponds for airport stormwater control, whereas South Deering is an industrial estate with swamplands. It can be infered as a result, the stagnation of water pool in both neighbourboods provides a habitable breeding spot for these mosquitoes. The districts adjacent to O'Hare, such as Dunning and Norwood Park, has also suffered an outbreak of WNV-positive mosquitoes.


**Modelling**

Logistic Regression, Naive Bayes, Extra Trees and XGboost models are used to model the data. There is a heavy class-imbalance in the data, at 19:1 ratio of WNV-negative against WNV-positive mosquito traps. The Synthetic Minority Over-sampling Technique (SMOTE) was used to adjust for the imbalance. 

Logistic Regression has shown to be the best performing model at an overall accuracy of 70%, with recall and specificity scores of 77% and 70% respectively. 


**Cost Benefit Analysis**  

Vector Controls, which include aerial spraying of pyretherins for six nights, has reported to have benefits in the form of both medical costs reductions as well as productivity increases. The benefit-cost ratio (in US$) has is estimated to be around 3.8.  


## Conclusions & Recommendations

To sum up, the West Nile Virus is a seasonal outbreak which peaks during the summer. Temperature and Rainfall are the main causes for the outbreaks. With this data in mind, the disease control authorities can prepare for these peak periods and mitigate the airborne of the virus through the mosquitoes. 

Spraying can be target at high risk zones, identified to be arond the Northwest (O'Hare) and Southeast (South Deering) regions. Major breeding grounds such as O'Hare and South Deering have found often to have stagnant water, especially during summer where there are increased levels in rainfall. Concentrating spraying on these areas can save limited spraying resources and amplify the effectiveness on targeting WNV-positive mosquitoes. 


### Recommendations
  

**Neighbourhood Outbreak Risk Zoning**

The authorities can consider categorizing the different Chicago districts into zones, based on their risk towards a WNV outbreak, as well as the demographics of each district. Some districts have found to have a higher porportion of citizens who can be classified as dependencies (ages under 18 and above 65). These groups of people may have a weaker immune system than an middle-aged adult and it is of importance that the welfare of these dependencies are taken care of. High-risk zones can be demarcated as districts with high WNV-positive moquito count, as well has a high dependencies number. 


### Considerations 

More research can be conducted with regards to larvicide implementation, as well as increased personal protective measures. 

For larvicide implementation, if the disease control authorities are able to halt the life cycle of mosquitoes, this will aid the prevention in mosquitoes being airborne and spreading WNV at a faster rate. 

More data can certainly be gathered about personal protective measures for an added layer of protections. Such measures can include mosquito repellents in the form of sprays, coils and patches. If the denizens of Chicago were to be aware of prevention measures, it maybe even a better solution than chemical fogging of mosquitoes.  

### References

 Data dictionary


|Feature|Type|Description|
| --- | --- | --- |
 |Id  <br/>(train.csv)            |int      | the id of the record
 |Date <br/>(train.csv)          |datetime      |date the WNV test is performed
 |Address <br/>(train.csv)     |datetime | approximate address of the location of trap. This is used to send to the GeoCoder
 |Species  <br/>(train.csv)       |str      | the species of mosquitos
 |Block <br/>(train.csv)        |str      |block number of address
 |Street <br/>(train.csv)       |str      |street name
 |Trap <br/>(train.csv)         |str    |ID  of the trap
 |AddressNumberAndStreet <br/>(train.csv)|str| approximate address returned from GeoCoder
 |Latitude <br/>(train.csv)           |float|latitude and Longitude returned from GeoCoder
 |Longitude <br/>(train.csv)           |float| longitude and Longitude returned from GeoCoder
 |AddressAccuracy <br/>(train.csv)     |int| accuracy returned from GeoCode
 |NumMosquitos <br/>(train.csv)       |int      | number of mosquitoes caught in the specific trap
 |WnvPresent  <br/>(train.csv)         |int      | whether West Nile Virus was present in the mosquitos in the traps. 1 means WNV is present, and 0 means not present
 |Date <br/>(spray.csv)|datetime | date of spray
 |Time <br/>(spray.csv)        |datetime      | time of the spray
 |Latitude <br/>(spray.csv)|float| latitude of spray
 |Longitude <br/>(spray.csv)       |float| longitude of the spray
 |Station <br/>(weather.csv) |int| weather station ID
 |Date  <br/>(weather.csv)   |datetime| date of weather measurement
 |Tmax  <br/>(weather.csv)   |int| maximum temperature (F)
 |Tmin  <br/>(weather.csv)   |int| minimum temperature (F)
 |Tavg  <br/>(weather.csv)|int| average temperature (F)
 |Depart <br/>(weather.csv)    |int| departure from normal temperature (F)
 |Dewpoint <br/>(weather.csv)   |int| average dew point (F)
 |WetBulb <br/>(weather.csv)  |int| average wet bulb (F)
 |Heat <br/>(weather.csv)    |int| degree days of heat (base 65 F)
 |Cool <br/>(weather.csv)  |int| degree days of cool (base 65 F)
 |Sunrise <br/>(weather.csv)    |int| time of sunrise (calculated)
 |Sunset <br/>(weather.csv)    |int| time of sunset (calculated)
 |CodeSum <br/>(weather.csv)    |str| code of weather type
 |Depth <br/>(weather.csv)    |int| snow depth (inch)
 |Water1 <br/>(weather.csv) |int| water equivalent (inch)
 |SnowFall <br/>(weather.csv)    |int|snowfall (inch)
 |PrecipTotal <br/>(weather.csv)    |str|Amount of rainfall (inch)
 |StnPressure <br/>(weather.csv)    |int|average station pressure (inch hg)
 |SeaLevel <br/>(weather.csv)    |int|average sea level pressure (inch hg)
 |ResultSpeed <br/>(weather.csv) |float|wind speed (mph)
 |ResultDir <br/>(weather.csv)    |int|wind direction (degrees)
 |AvgSpeed <br/>(weather.csv)    |int|average wind speed (mph)


Presentation

Bellini, R., Zeller, H. & Van Bortel, W. A review of the vector management methods to prevent and control outbreaks of West Nile virus infection and the challenge for Europe. Parasites Vectors 7, 323 (2014). https://doi.org/10.1186/1756-3305-7-323

Idph.state.il.us. 2020. West Nile Virus In Illinois - Surveillance. [online] http://www.idph.state.il.us/envhealth/wnvsurveillance_humancases_13.htm

Ruktanonchai, Duke J et al. “Effect of aerial insecticide spraying on West Nile virus disease--north-central Texas, 2012.” The American journal of tropical medicine and hygiene vol. 91,2 (2014): 240-5. doi:10.4269/ajtmh.14-0072

Yao, Yi, and Ruth R Montgomery. “Role of Immune Aging in Susceptibility to West Nile Virus.” Methods in molecular biology (Clifton, N.J.) vol. 1435 (2016): 235-47. doi:10.1007/978-1-4939-3670-0_18



