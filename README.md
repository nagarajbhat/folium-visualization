# Using python's Folium to create interactive maps

The blog post for this notebook can be found [here]().

Folium is a python library built on top of leaflet.js. It is used to visualize data through interactive maps, choropleth visualization, as well as parsing markers on data. 

### What will be covered in this notebook?

- data preparation - merging,sorting, grouping using pandas. (step 1-5)
- barplot visualization using seaborn (step 6)
- creating maps using python's folium - tiles, circle marker, choropleth map, and geojson. (step7-9)
- creating labels on the choropleth map using geojsontooltip. (step 10)
- Displaying multiple data views on the same map using the "feature group" and control layer. (step 11)
- Calculate market share(step 12)
- Calculate the largest commodity in each district(step 13)
- Create markers and use custom icons. (step 14)


### Pitfalls to avoid
I broke my head for several hours so that you don't have to.
- Avoid using jupyter lab in chrome, use firefox instead. Chrome did not render large maps. This will be useful in step 11.
- While creating a choropleth map we will be using geojson data. Make sure the values in the key column (district name, or state) is the same across this file and the original data.
- folium.Choropleth() doesn't provide an option for creating labels on top, use geojsontooltip along with it to create labels.

#### Data
- You can find the data used in this notebook in the "data" folder.
- **References**:
    1. "CommMktArrivals2012.xls" - Karnataka Agriculture market data by [data.gov.in](https://data.gov.in/resources/karnataka-agricultural-market-data-2012) 
    2. "kar.json" - Geojson map data for karnakata by [Kenneth Mark Dsouza](https://github.com/inosaint) from [here](https://github.com/inosaint/StatesOfIndia/blob/master/karnataka.geojson).
        Some of the districts name were corrected to suit "CommMktArrivals2012.xls".
    3. "kar_latlong.xlsx" - Latitude and longitude for each district in karnataka. This file was created by me.



