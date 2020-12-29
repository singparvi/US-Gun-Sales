## Topic Selection and the Research Questions

Before the 2020 US election, an article<sup>1</sup> caught my eye. I started to investigate whether the 2020 election has anything to do with gun sales in the US or if this year was any special due to COVID. Or is it anything to do with the sitting president? This got me started in collecting the data on gun sales in the US and analyzing it. 

## Source Dataset

The data for this research is taken from the National Instant Criminal Background Check System (NICS)<sup>2</sup> database maintained by the FBI. NICS system was launched in 1998 and the system allows Federal Firearms Licensee (FFL) (authorized seller in the US) to use the system to run a background check on the buyer. Since its inception, NICS has provided approximately 300 million checks and led to 1.5 million denials. NICS reports the data for each state monthly in a pdf format. Buzzfeednews.com maintain a CSV format of the data from the FBI which was of great help in the data analysis.<sup>3</sup>

In addition to the NICS database, the US population data of each state was also used. For the US population by state, census.gov was used. Census dataset<sup>4</sup> only provided the population data from 2010-2019 while the population for 2020 was projected using 2019 data and 2018-2019 growth. The data from the 2010-2013 population was dropped with this data set as another<sup>5</sup> dataset was used to fill the gap between 2000-2013.

---
## Visualization and Data Interpretation

For data analysis, only the data from 2001-2020 is taken into account. The line plot shown below displays the gun sales month on month across the US from 2001-2020. Major spikes in gun sales are explained by the key events available publically. This line plot also helps conclude that around each election, then be it 2008, 2012, 2016 or 2020, there is an increase in gun sales. 
Generally, the US buys guns mainly in the month of December each year. The trend of these sales can be seen consistent year after year.

![Annual Gun Sales Events](https://github.com/singparvi/singparvi.github.io/raw/8ecf4bc80cf1feceac6fbf9a9699a69799a41335/assets/img/US_Annual_Gun_Sales_Events.jpeg)

### Treemap for Population Change in the US from 2001-2020

A valid argument could be made that states that have more gun sales may have more population. To normalize the gun sales data the population data will be used later. To help graphically the data from 2001-2020 is shown in the treemap below that shows where the population in states has been concentrated over the years.

{% include Treemap_US_Population.html %}

### Total Annual Gun Sales and Population of US States by Year

The choropleth map below shows how gun sales have fared by state each year along with the population data set. The color intensity shows the state that has the maximum gun sales in any time frame.

{% include Choropleth_Annual_Gun_Sales_Population.html %}
### Bar Plot showing Y-o-Y US Gun Sales

2016 and 2020, both election years, made records and there is a significant spike in gun sales in both years. 2020 is on the track to be a record year in gun sales with more than 30 million guns sold.

{% include Barplot_YoY_Gun_Sales_Population.html %}

### Bar Plot of different US states from 2001 to 2020

The bar plot below shows how gun sales pattern has shifted over time. In 2001, California accounted for the most gun sales while for 2020 Illinois has taken the spot.

{% include Barplot_Annual_Gun_Sales_Population.html %}

### Bar chart race for Gun Sales from 2001 to 2020 of top 10 US States

The bar chart race shows how gun sales intensity shifted from California to Illinois in the past two decades. Surprisingly California has seen a consistent decline in gun sales between 2017-2019 with a little increase in 2020.

{% include BarChartRace_Annual_Gun_Sales_Population.html %}

---
### Total Annual Gun Sales per 100k Population of US States by Year

The choropleth map below shows the number of guns per 100k population of any state in any given year. In 2001, Colorado, Montana and West Virginia accounted for most guns sold in the US with 82, 78 and 76 guns per 100k individuals respectively. Fast forward twenty years, Kentucky, Illinois and Utah have taken these spots. Illinois seemed to be a state that is buying a lot of guns based on the total guns sold however the statistics changes with the population considered. Kentucky has approx. 651 guns for every 100,000 individuals while Illinois at 520 guns for every 100,000 individuals. Overall there has been a dramatic shift in gun sales over the years. 

{% include Choropleth_Annual_Gun_Sales_100k.html %}

### Bar plot showing Y-o-Y US Gun Sales with population consideration

The bar plot shows the information in a bar plot setting to give a scale of change in the past twenty years. 

{% include Barplot_Annual_Gun_Sales_100k.html %}

### Bar chart race for Annual Gun Sales per 100k population from 2001 to 2020  of top 10 US States 

Kentucky emerged as the state buying the most guns first in 2006. That year the number of guns purchased per 100k individuals was almost four times compared to a year ago. 2007 was even worse than in 2006 with almost double the number of guns bought a year ago. Kentucky has held the first spot since 2006 for the highest number of guns sold per 100k individuals.

{% include BarChartRace_Annual_Gun_Sales_100k.html %}

---
## Correlation and Linear Regression Fitting

The states that bought the most guns per 100k individuals in 2020 were taken into account for this exercise. The states selected are Kentucky, Illinois and Utah. 

### Kentucky State Correlation and Linear Regression Fitting

The correlation between Kentucky state's guns sold per 100k and its population is approx. 91%. With linear regression, it can be interpreted that the gun sales per 100k in Kentucky can be explained approx. 83% by population only.

![Kentucky OLS Results](https://raw.githubusercontent.com/singparvi/singparvi.github.io/master/assets/img/Kentucky-OLS-Results.png)
### Illinois State Correlation and Linear Regression Fitting

The correlation between Illinois state's guns sold per 100k and its population is approx. 91%. With linear regression, it can be interpreted that the gun sales per 100k in Illinois can be explained approx. 83% by population only.

![Illinois OLS Results](https://raw.githubusercontent.com/singparvi/singparvi.github.io/master/assets/img/Illinois-OLS-Results.png)

### Utah State Correlation and Linear Regression Fitting

The correlation between Utah state's guns sold per 100k and its population is approx. 91%. With linear regression, it can be interpreted that the gun sales per 100k in Utah can be explained approx. 83% by population only.

![Utah OLS Results](https://raw.githubusercontent.com/singparvi/singparvi.github.io/master/assets/img/Utah-OLS-Results.png)
## Sources

<sup>1</sup>[Washington Post News Article](https://www.washingtonpost.com/business/2020/10/29/walmart-guns-civil-unres/)

<sup>2</sup>[FBI NICS](https://www.fbi.gov/services/cjis/nics) 

<sup>3</sup>[BuzzFeedNews](https://github.com/BuzzFeedNews/nics-firearm-background-checks)

<sup>4</sup>[Census U.S.](http://www2.census.gov/programs-surveys/popest/datasets/2010-2019/national/totals/nst-est2019-alldata.csv)

<sup>5</sup>[GitHub Link](https://github.com/jakevdp/data-USstates)

