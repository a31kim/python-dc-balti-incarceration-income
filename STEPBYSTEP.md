# Python Process Description

## Importing Libraries/Data
1. Imported plotly (did not use), matplot, seaborn, pandas, and numpy
2. Imported datasets by imbedding GitHub URLs
3. Previewed data using .head

## Merging Data
1. Renamed column names that contained data (incarceration, income) to "Metric"
2. Used pandas to conduct an inner merge, getting rid of values that do not have a match
3. Merge referenced tract number in order to pair the Metric columns
4. Deleted unnecessary columns, and renamed columns for clarity
5. Used this process to merge incarceration and income values for both datasets

## Creating Graphs
1. Created a combination graph using matplot and seaborn
2. Set graph size, color, title, axis labels/colors
3. Removed x-axis labels due to illegibility from overlap
4. Second lineplot was bound to first lineplot using .twinx()
5. Used this process to create combination graphs for both datasets
