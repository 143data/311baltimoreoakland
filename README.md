# 311baltimoreoakland
## 311 Calls in Baltimore and Oakland from March 1, 2020

I accessed the Baltimore and Oakland datasets via each city's open data repository website. Before downloading each city's data as csv files, I used the filtering tool to keep and export only the 311 calls logged from March 1, 2020, 12:00 AM. Initially, I attempted to filter this manually using R but the complete datasets were too large and crashed R Studio every time.

After importing the filtered data into R Studio, I faced a few design choices regarding which variables were relevant to the task at hand, which was to integrate the datasets of two city's 311 call data with a brief description of the call and the date. Below is a list of attributes for each dataset.

### baltimore Original Dataset Variables
SRRecordID<br /> 
ServiceRequestNum<br /> 
SRType * <br /> 
MethodReceived<br /> 
CreatedDate * <br /> 
SRStatus<br /> 
StatusDate<br /> 
DueDate<br /> 
CloseDate<br />
Agency<br /> 
LastActivity <br /> 
LastActivityDate <br /> 
Outcome <br /> 
Address * <br /> 
ZipCode <br /> 
Neighborhood <br /> 
CouncilDistrict<br /> 
PoliceDistrict<br /> 
PolicePost<br /> 
Latitude<br /> 
Longitude<br /> 
GeoLocation<br /> 
2010 Census Wards Precincts<br /> 
2010 Census Neighborhoods<br /> 
Zip Codes<br /> 

### oakland Original Dataset Variables
REQUESTID<br /> 
DATETIMEINIT * <br /> 
SOURCE<br /> 
DESCRIPTION * <br /> 
REQCATEGORY <br /> 
REQADDRESS<br /> 
STATUS<br /> 
REFERREDTO<br /> 
DATETIMECLOSED<br /> 
SRX<br /> 
SRY<br /> 
COUNCILDISTRICT<br /> 
BEAT<br /> 
PROBADDRESS<br /> 
City * <br /> 
State<br />  

I removed all but three columns (marked with asteriks) for each dataset and renamed them so that the observations could be vertically integrated into one table. The new column names are description, call_date, and city.
