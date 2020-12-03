Factors affecting frequency of Volcanic eruptions
================
x404-pagenotfound

## Summary

We chose to research what factors affect the frequency of volcanic eruptions.

The data we are analyzing comes from the tidytuesdy package, and was collected by the Smithsonian's Global Volcanism
Program. To explore the factors affecting volcanic eruptions, we used 2 data frames, one of which listed every
volcano on the planet, giving its position, name, number...etc, while the other data set listed every recorded
volcanic eruption, and included name, number, year...etc. Both dataframes have far too many variables to explore,
so we decided to focus on factors like position, country, crust type, and tectonic setting. 




Write-up of your project and findings go here. Think of this as the text
of your presentation. The length should be roughly 5 minutes when read
out loud. Although pacing varies, a 5-minute speech is roughly 750
words. To use the word count addin, select the text you want to count
the words of (probably this is the Summary section of this document, go
to Addins, and select the `Word count` addin). This addin counts words
using two different algorithms, but the results should be similar and as
long as you’re in the ballpark of 750 words, you’re good\! The addin
will ignore code chunks and only count the words in prose.

You can also load your data here and present any analysis results /
plots, but I strongly urge you to keep that to a minimum (maybe only the
most important graphic, if you have one you can choose). And make sure
to hide your code with `echo = FALSE` unless the point you are trying to
make is about the code itself. Your results with proper output and
graphics go in your presentation, this space is for a brief summary of
your project.

## Presentation

Our presentation can be found [here](presentation/presentation.html).

## Data

Mock, T 2020, "Volcano Eruptions", electronic dataset, Global Volcanism Program/Smithsonian Institution, viewed 4 December 2020, <https://github.com/rfordatascience/tidytuesday/blob/master/data/2020/2020-05-12/readme.md>

Include a citation for your data here. See
<http://libraryguides.vu.edu.au/c.php?g=386501&p=4347840> for guidance
on proper citation for datasets. If you got your data off the web, make
sure to note the retrieval date.

<https://www.britannica.com/science/volcano> \<- Volcano types and
explanations

## References

- https://github.com/rfordatascience/tidytuesday/blob/master/data/2020/2020-05-12/readme.md
- https://rstudio.github.io/leaflet/markers.html
- https://arilamstein.com/blog/2016/03/21/mapping-election-results-r-choroplethr/
- 

## Modelling frequency by crust type and frequency by tectonic setting

One of the initial goals was to fit a linear model to frequency by crust
type and tectonic setting separately. When carrying this out the values
given by the output were plausible when viewing the graphs and a small
amount of prior knowledge however the evalutations showed that linear
models were not appropriate. The adjusted r squared values for both sets
of data were very small showing the models were only accurate for a very
small proportion of the data, in addition to this both the residuals
plots showed residuals in distinct clusters that, when coloured by crust
or tectonic settings, showed they were grouped by the categories of
variable. At this point we considered exploring other models however we
decided that the use bar charts and other visualizations to explain the
trends in frequency, tectonic settings and crust types rather than
trying to fit a model that may not cover such a wide range of data
efficiently.

\#\#Number of Volcanos by Crust type. The bar plot shows the number of
eruptions that have been recorded on each separate crust type. The
unknown volcanos where filtered out of the data to try to get a clearer
idea of any relationship displayed. Its clear from the graph that the
majority of eruptions occur on continental plates, being over 4 times
greater than those recorded on oceanic plates and about 10 times greater
than those recorded on intermediate plates. The ambiguity of an
intermediate plate may explain the small number of observations there.
It is also possible that the lower number of eruptions on Oceanic plates
is down to more remote locations of the volcanos. The data set goes back
to very early years so it’s plausible that eruptions recorded at these
times would only have been those where a town or village was impacted by
the volcano directly. Eruptions in the middle of the ocean likely went
unrecorded as there was no way of knowing they were occuring.

The histogram for number of eruptions by start year doesn’t confirm this
theory. Whilst the number of volcanoes recorded in the data increases by
millenium (most significantly in the most recent), the relative
proportion of continental to oceanic crust stays approximately the same.
This confirms the initial graphs projection that, at least in the
dataset, there are significantly more volcanic eruptions on continental
plates than oceanic plates.

## Number of Eruptions by Tectonic Settings

From the plot of frequency of eruptions for different tectonic settings
shows that the majority of eruptions occur as a result of a subduction
zone, about 4 times as many of those that occur as a result of a rift
zone and about 5 times as many of those that occur as a result of an
intraplate. When comparing the maps for eruptions by tectonic setting to
crust type we can see that for the most part, volcanos formed by a
subduction zone are on continental crust referrring back to the earlier
definition this has already been explained. Intraplate formation appears
more randomly distributed however by definition they don’t require the
presence of a plate boundary to form, making them more random in nature.
Most volcanos on oceanic crust appear to be formed by a rift zone
however there are also continental rift zone volcanos which explains the
greater difference in continental and oceanic crust eruptions than in
subduction zone and rift zone eruptions.

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
