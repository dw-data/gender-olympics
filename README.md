# Tokyo-2021 claims gender-fairness, but equality is not so simple

This repository contains the data and source code behind the analysis for the [story]() published at DW.

It was written by Eva Lopez, Isabela Martel, John Marshall and Rodrigo Menegat.

## Data

The data source for this story is the work of a group of Olympic historians that currrently publish in-detph statistics at [Olympedia](https://www.olympedia.org/static/about) -- and, formerly, at the now inactive [OlympicsReference](https://www.sports-reference.com/olympics.html) website.

It was originally collected by [Randi H. Griffin](https://www.randigriffin.com/) in June 2018 and published as a [Kaggle dataset](https://www.kaggle.com/heesoo37/120-years-of-olympic-history-athletes-and-results). 

The file linked above was the starting point for the analysis. Its accuracy was confirmed by comparing a sample of the data with Olympedia's current website. However, due to the shifting nature of Olympic records, there are some noteworthy exceptions. 

For instance, when the dataset was first collected, a 2008 bronze long jump medal was still awarded to the Russian athlete Tatyana Lebedeva. However, in July 2018, [she had to return her award due to a doping conviction](https://www.espn.com/olympics/story/_/id/24197219/russians-tatyana-lebedeva-maria-abakumova-stripped-2008-olympic-medals). 

The original file won't show this correction, but all the figures mentioned directly in our story take similar cases into account. If a number is mentioned there explicitly, then it was double checked against those changes. This was not done with the entire dataset, though, and one might find similar incosistencies while browsing it. Nevertheless, they are minor exceptions and won't affect the overall conclusions drawn by the text. 

## Methodology

The analysis is based in the following assumption: if women are 50% of a country's Olympic team, then they should also be responsible for nearly as many of this team's Olympic medals. When those two rates are similar, we are seeing a situation of roughly equal performance.

With this is mind, we computed the ratio of athletes of each gender in a team and compared it with the percentage of medals won by either men or women. 

Then, we looked at countries in which this differences were the most significant to find places were men are winning more medals (overperforming) and less medals (underperforming) than their share on the team, as well as nations for which these numbers were even.

Nations with small teams and a small numbers of medals were not highlighted, since a single good result for any gender would skew the metric to one side and wouldn't be representative of a broader pattern.

There are some caveats to this assumption, though. 

First, there's the question of team sports: take football, for instance. Even if an Olympic football team is composed of a total 18 athletes (11 startes and 7 substitutes), the medal count will register a single medal for the winning country. The small amount of team sports medals compared to the individual awards mitigates this issue, but it still has potential to skew the analysis in some cases. Again, the specific examples mentioned on the article were double-checked against this potential issue.

There's also the issue of mixed events, in which men and women compete together. This happens in disciplines such as Sailing, Equestrianism and in some events of Tennis and Badminton. Medals in those categories were excluded from the analysis.

Finally, it's also noteworthy that still today men compete in more events and are awarded more medals than women.


## Interviewees

Apart from the data visualization, the following experts contributed to the article:

| Interviewees | Affiliation |
|--------------|-------------|
| Kristian Butariu | Romanian Olympic Committee |
| Susan Brownell | University of Missouri-St Louis |
| Michelle Donnelly | Brock University |
| Anke Hilbrenne | Georg-August University |

## Repository structure

The files in this repository are divided in the following subdirectories:

- `code`: contains the Jupyter Notebooks in which we conducted our analysis and made the first verstion of the article's charts.
- `data`: contains the raw data used on the data analysis.
- `output`: containts the processed data, summarizing the results of the analysis, which was used for making the data visualizations.