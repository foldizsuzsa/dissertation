# Religions of Transylvania on Interactive Map
## Master's Thesis

### Religion data (census data from 1850 to 2011)
Data collected form http://nepszamlalas.adatbank.ro/ with webscaping using Python3 BeautifulSoap, Urllib, Request packages.
- removing notes and not numeric data from the tables
- save the data in csv format

### Geolocation
Finding the latitude and longitude coordinates of a particular location using Python's **Geopy** package with **Nominatim** geolocator based on the city/village name and the county. Geopy makes it easy for Python developers to locate the coordinates of addresses, cities, countries, and landmarks across the globe using third-party geocoders and other data sources.

### MapBox GL JS
Now that the GeoJSON is ready, let’s add it to our map.
We use Mapbox GL JS, which is a JavaScript library that uses WebGL to render interactive maps from vector tiles and Mapbox styles.
For every year from the dataset we should add a different layer to the map, which source is a GeoJson file.

To enable clustering on the source, we set the cluster property to true and the clusterRadius property to the desired radius of clustering.
The goal here is to create a visualization showing the distribution of the different religions per cluster. In order to achieve this, we need to add the clusterProperties property and define the categories we want to keep track of.
We will produce an HTML donut chart using three main elements:
- an arc
- an inner circle
- text (number of people)
To complete our visualization, we added interaction to show the exact proportion of each type of religion per cluster.
By clicking on a cluster marker, an additional bar chart appears.

From the menu bar we can choose the year and the religions we are interested in.
