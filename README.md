# MSFT-Cinema-Venture
## Table of Contents
* [Contextual Information](#contextual-information)
* [Insights and Recommendations](#insights-and-recommendations)
* [Further Analysis Required](#further-analysis-required)

## Contextual Information
The Data Utilized:
* Box Office Mojo "bom_movie_gross"
* The Numbers “movie_budgets"
* Rotten Tomatoes “rt_movies”

Technologies:
* Jupyter Notebooks
* `Python 3`
* `Pandas 1.0.5`
* `Matplotlib 3.2.2`
* `Seaborn 0.10.1`
* `Statistics 3.4`

Objective: Our objective with this analysis is to provide information to Microsoft so they can assess the criteria for a successful entry into the movie production business. 

Topics that we explored: 
* The relationship between the level of investment or production budget and return on investment.  This was an individual effort by David Rasmussen
* The optimal time of year to release a move. This was a group effort.
* The relationship between genres and ratings (ie R, PG-13, etc) and return on investment. This was an individual effort by Blake Tolman.
* Which studios produce the most movies, their corresponding average revenue per move, and which ones are most profitable. This was a group effort.

## Insights and Recommendations

### Investment Amount vs Return on Investment

We think it is important to know if there is an optimal level of investment required to be profitable in the film industry.  There may be a level at which there are diminishing returns on investment for example.

Assumptions:
* We assumed in our analysis that Microsoft should spend at least $30 million.  This level of investment is a lower bound as the average cost of a feature film is estimated to be around $70 million.  We assume Microsoft will invest enough to create a movie worthy of their esteemed brand.
* We assume that extreme outliers are not relevant to this analysis and removed any data further than 2 standard deviations from the median. The median is more appropriate than the mean in this case as a measure of central tendency due to the significant skew to the right side of the distribution.

![Imgur](https://i.imgur.com/m9dRizk.png)
[Imgur](https://i.imgur.com/3rmFEhI.png)

We decided to use a scatter plot here so we could easily see how each variable changes relative to the other variable. 

Insights:
* Per the scatterplot, there does not appear to be a discernible relationship between production budget and ROI.
* The correlation between the two variables is 0.12

Recommendation:
As stated, there does not appear to be a relationship between investment level and return on investment.  We recommend focusing on other criteria when determining an optimal budget for a movie.

## Seasonality

The time of year to release a movie is an easy factor to control.  From a layman's point of view it seems that blockbusters are released only at certain times of the year.  For example, there never appears to be successful movies released in January.  We decided to explore and confirm whether or not there is a seasonal component to profitability.

Assumptions:
* We again removed any films with budgets less than $30 million.   
* We also removed outliers with the same method explained in the preceding analysis. 

![Imgur](https://i.imgur.com/38Fy34P.png)

We decided to use a boxplot because the median and outliers are easy to see. The data is highly skewed to the right due to outliers.  Even after removing 5% of the outliers the data is highly skewed. 

Insights:
* The second and fourth quarter appear to have the highest median return on investment
* The first quarter is not an optimal time to release a movie

Recommendations:
We recommend releasing a move in the May/June/July timeframe or in November/December

### Studio Performance

Studios are recognized by which movies they help produce. The more recognition a studio has the more likely they can make a deal associated with high end companies, and in this case its Microsoft. It comes down to what is the more influential factor to determine a studio's domestic gross. Quantity of films made or quality?

Assumptions:
* It was assumed the Microsoft would pick a studio with an established brand name and history of positive performance 
* The data was reduced to only display the top 10 movies based on number of movies made

![Imgur](https://i.imgur.com/UTlbbAd.png)

Insights:
* Studio BV produces the highest number of films and also has the highest average made per movie. 
* The other studios average gross is more closely distributed to the mean average (100 million) regardless of number of movies made

Recommendations:
It would be recommended to choose a studio who has produced over 40 movies to avoid the possibility of outliers

### Return on Investment per Movie Rating and Genre

Movies are typically tailored to specific audiences. If you can correctly identify your market and advertise to them you have a higher likelihood of having a positive return on investment. An important part of understanding your market is a breakdown of how each movie rating performs within different genres.

Assumptions:
* For simplicity movies were reduced and categorized to only one genre
* It was assumed the first listed genre was the movies primary category

![Imgur](https://i.imgur.com/RcuVqKg.png)

Insights:
* In terms of quantity, the Comedy genre had the highest amount of movies made followed closely by action and adventure.
* Comedy also was the only genre to have movies present in all 6 of the rating classifications (G, PG, PG-13, R, NR, NC17)
* In a general scope of all genres PG-13 had the highest average return on investment

Recommendations:
* For current movies PG is the safest option when making a movie as  is it is present in all but two genre
* If the  rating is still being determined, making the movie into a comedy would be most beneficial
* In terms of ROI the Kids and Family category can yield the highest return 

## Further Analysis Required
What we have provided here is just scratching the surface on the depth of analysis required to assess a strategic shift into the movie production business.  We will list a few topics which should be explored

### Directors and Producers and Return on Investment
Directors and particularly producers have control over how an investment is dispersed during the filmmaking process.  It would be of great interest to determine with director/producer combo yields the highest bang for your buck.  

### Actors
Using a “Moneyball” mentality at assessing each actor on his or her contribution to a movie's return on investment.  Some actors are very expensive to hire and you don’t want to end up like the Chicago Cubs of old and hire overpriced personnel.  The Numbers website has a “Bankability Index” https://www.the-numbers.com/bankability. It would be interesting to try to create a similar measurement of value for each actor.

### Franchises
Microsoft has a very successful video game franchise that began with “Halo: Combat Evolved.”  An analysis into the profitability of movie franchises would help assess the viability of launching a series of Halo related movies.  There is an optionality component to a series of movies, the likelihood of a future movies success is dependent on the success of a preceding movie.
