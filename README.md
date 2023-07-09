# Event-Based-Contagion-Forecasting
@sieverett

## Background
> We propose an event-based contagion forecasting model that considers the social dimensions of spread. <br>
The model proposes consideration of the aggregated behavior among groups, information asymettries and <br>
diversity in risk tolerance. <br>
Few models incorporate the rise in the politization of information that confirms or rejects potential <br>
risk factors for the spread of disease. This analysis looks specific cases of large scale events asseses <br>
the potential for spread, and weighs the event against the information about potential health risks <br>
that precedes these events.

# Notebook
> The following analysis seeks to determine if there is a correlation between the information on Covid-19, <br>
number of Covid-19 cases and the number of attributed deaths in relation to the timing and location of <br>
Trump's 2020 campaign rallies for U.S. President. The analysis assumes that the covid statistics will be <br>
captured for each city in which a rally occured.
> The rally schedule @ 'https://ballotpedia.org/Donald_Trump_presidential_campaign,_2020#Campaign_rallies' <br>
is listed by city and New York Times Covid-19 @ 'https://raw.githubusercontent.com/nytimes/covid-19-data/master/us-counties.csv' <br>
is by county, therefore the table is joined first by looking up the county for each city, and getting the fips coded geographic boundaries.
