# elecprice
Rshiny app to analysis elecprice
------
This R Shiny application is a data analysis tool for the- **Power to Choose (PTC)**, built to
visualize electricity plans and prices in the market.
------
##Background
-----
[Power to Choose](PTC) is a consumer choice website to provide customers a competitive platform to
compare electricity plans and offers in Texas. The general use of PTC is to quickly compare estimated prices at monthly usage thresholds (`500kWh`, `1000kWh`, `2000kWh`). 
The various Electricity Facts Label (EFL) price values corresponds to these usage thresholds.

------
## Data
>   This section provides details on the data source and processes that go towards scraping and munging the initial 
>   unorganized data into a consolidated R dataframe that is used in the Shiny app. The data procesing is in the file "datascraping.R"

### Data Source
The PTC data is conveniently provided as a organized csv download file accessed from
<http://www.powertochoose.org/en-us/Plan/ExportToCsv>
