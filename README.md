Factors affecting frequency of Volcanic eruptions
================
x404-pagenotfound

## Summary

We chose to research what factors affect the frequency of volcanic
eruptions.

The data we are analyzing comes from the tidytuesdy package, and was
collected by the Smithsonian’s Global Volcanism Program. To explore the
factors affecting volcanic eruptions, we used 2 data frames, one of
which listed every volcano on the planet, giving its position, name,
number…etc, while the other data set listed every recorded volcanic
eruption. Both dataframes have far too many variables to explore, so we
decided to focus on factors like position, country, crust type, and
tectonic setting.

Now, the easiest visualization to spot trends by location is obviously a
world map, so we will start there. To get an idea of which countries
have had the most volcanic eruptions, we created a choropleth map which
shows number of eruptions by country. Now, this is helpful, but it is
impossible to see any trend, because we can’t see groups of eruptions
within the countries. Also, as you can see from the scale, this map only
gives a rough idea of where the most eruptions happen.

So to solve this, we create a clustered world map. Now the patterns a
becoming a little more apparent. For example, we can now see that most
of the large clusters of eruptions are circled around the pacific ocean.
Our hypothesis as to why these trends exist had to do with tectonic
plates.

So we layered a map of the tectonic borders on to the points, and as you
can see, there is an clear pattern. Most of the eruptions took place
along a tectonic border, which isn’t surprising because volcanoes are
formed by the clashing of two plates. The circle of volcanoes around the
pacific that we saw earlier is a result of the pacific plate, and is
actually called the Pacific Ring of Fire. So just by looking at the
maps, we can see that location has a big effect on the count of
eruptions in a given area.

We then wanted to investigate whether the type of crust and tectonic
setting influenced the number of eruptions. To clarify these variable’s
meaning; the earth’s crust is split into tectonic plates which lie on
top of the mantle. The type of plate is given as the crust variable and
is either: -Continental (thick land plates) -Oceanic (thinner but
heavier sea plates) -Intermediate -And unknown plates. The tectonic
setting is the movement of the plates and mantle that causes the volcano
to form. It is given as the variables: -Subduction zone (an oceanic
plate moves beneath a continental plate) -Rift Zone (two plates move
apart) -Intraplate (a hotter area causes increased magma at the surface)

We investigated these as when comparing the maps of distribution it was
clear that certain areas of the map had higher frequencies of distinct
tectonic settings and crust types in the same areas.

The initial plan was to fit linear models for frequency by crust and
tectonic setting separately. However when evaluating both models, the r
squared value was very low and the residuals were in distinct clusters
by variable category, hence we concluded the linear models weren’t
suitable for the data in hand. We decided our research question could be
answered by visualization and comparisons.

When reviewing the number of eruptions on each crust type it is clear
that continental crust is the crust type with the most eruptions.
Comparing the number of eruptions for each tectonic setting, the
subduction zone has the most eruptions. When referring back to the
distribution maps this connection is shown as all of the subduction
volcanoes are on land, whilst most ocean volcanos appear to be rift
volcanos, a scientific study of why this is the case would be really
interesting if future research occurred.

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.0 ──

    ## ✓ ggplot2 3.3.2     ✓ purrr   0.3.4
    ## ✓ tibble  3.0.4     ✓ dplyr   1.0.2
    ## ✓ tidyr   1.1.2     ✓ stringr 1.4.0
    ## ✓ readr   1.3.1     ✓ forcats 0.5.0

    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

    ## Parsed with column specification:
    ## cols(
    ##   .default = col_character(),
    ##   volcano_number = col_double(),
    ##   latitude = col_double(),
    ##   longitude = col_double(),
    ##   elevation = col_double(),
    ##   population_within_5_km = col_double(),
    ##   population_within_10_km = col_double(),
    ##   population_within_30_km = col_double(),
    ##   population_within_100_km = col_double()
    ## )

    ## See spec(...) for full column specifications.

    ## Parsed with column specification:
    ## cols(
    ##   volcano_number = col_double(),
    ##   volcano_name = col_character(),
    ##   eruption_number = col_double(),
    ##   eruption_category = col_character(),
    ##   area_of_activity = col_character(),
    ##   vei = col_double(),
    ##   start_year = col_double(),
    ##   start_month = col_double(),
    ##   start_day = col_double(),
    ##   evidence_method_dating = col_character(),
    ##   end_year = col_double(),
    ##   end_month = col_double(),
    ##   end_day = col_double(),
    ##   latitude = col_double(),
    ##   longitude = col_double()
    ## )

    ## Parsed with column specification:
    ## cols(
    ##   volcano_number = col_double(),
    ##   volcano_name = col_character(),
    ##   eruption_number = col_double(),
    ##   eruption_start_year = col_double(),
    ##   event_number = col_double(),
    ##   event_type = col_character(),
    ##   event_remarks = col_character(),
    ##   event_date_year = col_double(),
    ##   event_date_month = col_double(),
    ##   event_date_day = col_double()
    ## )

## Presentation

Our presentation can be found [here](presentation/presentation.html).

## Data

Mock, T 2020, “Volcano Eruptions”, electronic dataset, Global Volcanism
Program/Smithsonian Institution, viewed 4 December 2020,
<https://github.com/rfordatascience/tidytuesday/blob/master/data/2020/2020-05-12/readme.md>

## References

  - <https://github.com/rfordatascience/tidytuesday/blob/master/data/2020/2020-05-12/readme.md>

  - <https://rstudio.github.io/leaflet/markers.html>

  - <https://arilamstein.com/blog/2016/03/21/mapping-election-results-r-choroplethr/>

  - <https://www.britannica.com/science/volcano>

  - 
## Number of Eruptions by Country and Volcano Type

Plot shows the frequency of eruptions in each country, grouped by
volcano type. We choose to only show the top 25 groups of country and
volcano types to avoid overwhelming so this is only a sample of the
data. It can be clearly seen that Japan has the highest number of
eruptions, mainly from strato, caldera and complex volcanoes, closely
followed by Indonesia, and the composition of the eruptions by volcano
type is similar.The US also has a high number of volcanic eruptions,
with eruptions almost evenly split between strato and shield volcanoes.
If we look at the countries of South America; Mexico,Equador,Costa Rica
and Chile, they all have a relatively similar number of eruptions,
solely composed of strato volcanoes. This backs up our conclusion that
tectonic plate type, and crust type affect the number of eruptions, and
also suggests that these factor also affect the volcano type. If we had
more time I think it would be an interesting extension of our project to
investigate the relationship between the factors which affect the number
of volcano eruptions. The majority of this plot if red which indicates
majority of volcanoes with high number of eruptions in our data set are
stratovolcanoes. The variation in number of eruptions as primary volcano
types varies, may lead us to believe that primary volcano type is a
factor which affects the number of eruptions.

# Number of Eruptions by Volcano Type

This can be seen more clearly in this bar plot which shows the number of
eruptions grouped by primary volcano type, in particular it shows 9
primary volcano types with the top 9 number of eruptions. This very
clearly shows that stratovolcanoes are responsible for the greatest
number of eruptions, with nearly 6000 eruptions in the dataset being
eruptions of stratovolcanoes. This is significantly more eruptions than
shield and Caldera volcanoes, which have the second and third highest
number of eruptions, with around 1000 eruptions recorded in the dataset.
We could conclude that volcano type is a factor which affects the number
of eruptions, but I believe to support this conclusion it is important
to take into the consideration the number of each volcano type in the
dataset.

## Number of Volcanoes by Volcano Type

This bar plot shows the number of volcanoes grouped by primary volcano
type. It shows there are 23 different primary volcano types recorded in
the dataset. Stratovolcanoes are the most abundant volcano types,
therefore it makes sense that they cause the most eruptions, however
there are approximately 450 stratovolcanoes, which are responsible for
6000 eruptions in the dataset. Therefore Stratovolcanoes must erupt
several times within there lifetime, approximately 13 times each if we
were to take a raw average. You can also see if we compare the bar plot
of Number of eruptions by volcano type and the bar plot for number of
volcanoes by volcano type, that the plot take a similar shape, which may
be an indicator that the number of eruptions of each volcano type is
proportional to the number of volcanoes of that type.
