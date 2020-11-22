# Analyzing the Relationship Between Incarceration Rate and Household Income

## Background

Over the past few decades, America's prisoner population has skyrocketed to over [2.2 million inmates](https://www.prisonpolicy.org/reports/pie2020.html), contributing to the U.S.'s achievement of the highest per capita imprisonment rate in the entire world. This trend of mass incarceration, which began in the 1970s, has disprortionately affected poor, black communities such as the Fairfield Area in Baltimore, and the housing projects of Southeast D.C. Many of these areas already face the obstacles of an underprivileged schooling system and high-risk neighborhoods - higher incarceration rates serve to further perpetuate the lack of social mobility experienced by these communities.

The cities of Baltimore, Maryland and Washington, D.C. present similar examples of underprivileged, metropolitan communities. Using data provided by [The Opportunity Atlas](https://www.opportunityatlas.org/), this project will analyze the relationship between incarceration rates and household incomes in different areas in both cities, and compare the resulting data. In particular, I'll be examining whether the expected negative relationship is visibile in the data, and if there are any noticable similarities or differences between the two analyzed cities.

I chose to examine this particular metric because I recently finished Michelle Alexander's _The New Jim Crow_, which provides a detailed recount of the caste-like imprisonment system instituted by the U.S. Government over the last few decades. My hometown is technically Potomac, MD, but the data from my area wasn't significant enough to compare with Baltimore, so I decided to use D.C. instead since I only live 15 minutes away.

## Business Question
What is the relationship between incarceration rates and household incomes in Baltimore and D.C., and how does the data from the two cities compare? What does this information tell us about the characteristics of these two cities?

## Data Question - Open Data

All of the data used in this project was gathered from [The Opportunity Atlas](https://www.opportunityatlas.org/).
The original data files can be found in the repository [here](https://github.com/a31kim/python-dc-balti-incarceration-income/tree/main/original%20datasets).

1. [balti_jail](https://github.com/a31kim/python-dc-balti-incarceration-income/blob/main/original%20datasets/balti_jail.csv) contains the data for incarceration rates in various communities within Baltimore city.
2. [balti_income](https://github.com/a31kim/python-dc-balti-incarceration-income/blob/main/original%20datasets/balti_income.csv) contains the data for average household incomes in various communities within Batlimore city.
3. [dc_jail](https://github.com/a31kim/python-dc-balti-incarceration-income/blob/main/original%20datasets/dc_jail.csv) contains the data for incarceration rates in various communities within Washington, D.C.
4. [dc_income](https://github.com/a31kim/python-dc-balti-incarceration-income/blob/main/original%20datasets/dc_income.csv) contains the data for average household incomes in various communities within Washington, D.C.

## Data Question - Analysis

Python (Google Colaboratory Notebooks) was used to answer:
* **What is the relationship between household income and incarceration rates in Baltimore and D.C.?** Cleaning the data to effectively merge the incarceration and household income data into an aggregate chart
* **Do Baltimore and D.C. demonstrate similar characteristics regarding the income/incarceration relationship?** Comparing the data between the two cities to determine if there is a noticable difference between the two


## Data Answer

I chose to summarize my anaylsis with a combination graph that displays the relationship between both metrics. I imported matplot and seaborn into my Python notebook in order to create these graphics. The code for these graphs can be found in my Google Colaboratory Notebook.

### Baltimore, MD Graph

![](.gitbook/assets/balti_graph.png)

This combination graph clearly shows a negative relationship between incarceration rates and household income. As incarceration rates decrease (red), household income (blue) noticeably trends upwards. I removed the labels from the x-axis, since it was illegible due to font overlap. The full dataset used to generate this graph can be found in my Google Colaboratory Notebook.

Examples of the statistical relationship described above:
* Greenmount West face incarceration rates as high as 25%, with household incomes barely reaching $15,000
* Comparatively, Mount Washington experiences incarceration rates as low as 0.05%, while benefitting from household incomes in the range of $70,000 a year

### Washington, D.C. Graph

![](.gitbook/assets/dc_graph.png)

This combination graph displays a similarly negative relationship between incarceration rates and household income, although the graphical representation is not as clear. As incarceration rates decrease (orange), household income (green) appears to follow an upwards trend. I believe that this data is much less inclusive due to the much lower rates of incarceration in D.C. (<4%), and the decreased variance of the household income metric.

I removed the labels from this x-axis as well, due to the same reasons (font overlap, illegibility) as the Baltimore graph.

Examples of the statistical relationship described above:
* The Georgetown and Naval Observatory areas have incarceration rates below 1%, with average household incomes greater than $60,000
* Comparatively, Columbia Heights and Southwest Washington have incarceration rates larger than 2%, with average houeshold incomes lower than $40,000
* Clearly, the variance in metrics is not as substantial in the D.C. dataset


## Data Application

The data analysis presented in this project seeks to demonstrate the widely assumed negative relationship between household income and incarceration rates. This presumed relationship is most visible in the Baltimore dataset, as the two plot lines are clearly inversely related to each other. The D.C. dataset is a little less conclusive, but the inverse relationship between the two is still noticable in the graphical representation.

The two cities displayed very similar relationships, but the observed variance of the datasets was very different.
* The variance of the Baltimore dataset is much larger for incarceration, with rates ranging from 3% to 25%. This is a substantially wider margin than the D.C. dataset, with incarceration rates ranging from 0% to 4%. 
* Meanwhile, household incomes in Baltimore range from $39,000 to $12,000, while household incomes in D.C. range from $85,000 to $32,000.
These discrepancies in the dataset may be a possible explanation for the less consistent results generated by the D.C. graph. I suspect that the much lower variance in incarceration rates is at least partially responsible.

Regardless, the data analysis serves to demonstrate a distinct relationship between incarceration rates and household incomes in these two urban areas. Although this observed linkage does not necessarily imply causation, it is worth noting that many studies have linked lessened economic opportunities to higher rates of incarceration in urban communities. This dataset can be used to demonstrate the possiblity of this causal relationship, and supports greater economic support in less wealthy communities. This support can come in the form of public-sponsored employment opportunities, better access to education, and effective social support for communities that are in need.

In order to further develop this analysis, it may have been helpful to have some additional data on the number of crimes committed annually in each area. This would enable me to determine the crime rates in each community as context for the incarceration data. It would also be interesting to compare this data analysis with the relative primary/secondary education opportunities provided in each area.
