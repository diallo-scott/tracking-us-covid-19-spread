# Tracking the Spread of Covid-19 in US Counties
Covid-19 is a global pandemic that has had a marked impact on the physical and economic health of communities across the United States and the rest of the world.  Tracking the spread of the virus has been key to minimizing the impacts as communites are able to make more informed, data-driven decisions to protect their citizens.  By tracking the spread and being able to anticipate tthe possible impact of Covid-19 on their communities, leaders are able to miplement new guidlines and make public and private partnerships to secure critical supplies and resources for healthcare.  Therefore, having an animated map to track the spread ans show which counties have been most impacted and are in most need of support would be a useful tool for determining which states, counties, and communities are in need of the most support.

## Business Question: How can we visualize and better understand the overall toll of the COVID-19 pandemic on US counties or county equivalents?
These visualizations could be helpful in guiding tthe distribution of resources to the communities most impacted and revising policies to keep heavily impacted communities safer.

## Data Question: Which data and metrics can we use to answer our question? 
Using plotly express we can build an animated choropleth map to demostrate the number cumulative confirmed COVID-19 cases per 100,000 residents in US counties.  We can also review some geospatial data analysis in Python by making a bubble map and a density heat map to showcase the number of cumulative COVID-19 confirmed cases in each US county.

We'll use data from the following sources for our analysis:

• [JHU CSSE COVID-19 Case Data](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports)

• [New York Times COVID-19 Data](https://github.com/nytimes/covid-19-data/blob/master/us-counties.csv)

• [US County Geospatial Data](https://raw.githubusercontent.com/plotly/datasets/master/geojson-counties-fips.json)

## Data Answer
We are able to create a bubble map, where the size of the bubbles is the number of confirmed cases in a county.  This map is great at showing us where the hotspots are, because we can quickly identify those regions that have large bubbles.  This map is displayed below.

This is not sufficient, however, when trying to analyze the impact of covid-19 on a community since the data is not standardized.  The map only shows us what is intuitive– larger cities have larger numbers of confirmed cases.  To understand the impact on a county we need to better show how that county is being affected, given the difference in its population relative to other cities.  We would also 
