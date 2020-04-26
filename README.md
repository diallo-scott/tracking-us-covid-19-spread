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
![covid bubble](https://github.com/diallo-scott/tracking-us-covid-19-spread/blob/master/Covid-19%20US%20Bubble.png)

This is not sufficient, however, when trying to analyze the impact of covid-19 on a community since the data is not standardized.  The map only shows us what is intuitive– larger cities have larger numbers of confirmed cases.  To understand the impact on a county we need to better show how that county is being affected, given the difference in its population relative to other cities.  We would also like to show when the virus was spread to that community and how quickly has this standardized count of cases and deaths have grown. Two animated choropleth maps (displayed below), which show the spread of the virus and the number of cases per 100,000 citizens and the number of deaths per 100,000 citizens are able to show these characteristics.

This animation show the number of cumulative cases:

![covid spread](https://github.com/diallo-scott/tracking-us-covid-19-spread/blob/master/Covid-19%20Spread.gif)

This animation shows the number of cumulative deaths:



## Business Answer
Our above visualizations can allow state and local leaders to visualize the spread within their communites and implement various policy responses.  

One takeway could be to ramp up testing efforts in their county.  The map shows that there are some counties that have been impacted much more than a neighboring county.  The isolation of the virus to one county is very unlikely, given how fluidly people travel between county lines.  Thus, if one county's incidence of the virus is dramatically less than that of a neighobring county, then leaders know that they should attempt to ramp up testing in that county and begin offering more support to their community.  

The animations also shows how quickly the prevalence of the virus has increased in a county, which could lead policymakers to alter social distancing guidelines and provide more resources to the healthcare system.  If the virus has recently become much more severe in a short period of time, then the county may want to strengthen social distancing through more stringent policies, such as closing parks or beaches and re-evaluating which businesses are considered to be essential.  Businesses, such as grocery stores, may also want to re-evaluate company policy and consider policies to increase employee and customer safety, such as requiring face coverings and limiting the number of customers and employees in their locations.   On the flipside, if the incidence of Covid-19 has remained relatively stable in a community, this is a sign that local leaders may have been successful at minimizing the impact of the virus and should stay the course until it has been deemed safe to ease their guidlines.

Any entity looking to use this animation and the information it contains, however, should note a few of its shortcomings. First, this animation and the accuracy of the case count is a function of the amount of testing being done in that county.  Hence, it may be helpful to include their own statistics on the number of tests that have been done in their county.  Another area for improvement would be to only track to number of active cases.  This map shows cumulative cases, so some of the cases depicted may no longer exist in that community.  If our dataset only tracked active cases, then it may be better at revealing how successful a county has been a minimizing community infection.  This change could also allow the map to provide insights on how close a county is to being able to reopen.  We may also come up with a way to more accurately track the growth rates of cases and deaths in a community.
