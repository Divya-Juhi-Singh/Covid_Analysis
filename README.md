# Real Time Covid Data Analysis
------------------------------------------------------------
## About
A tiny project on 'Real Time Covid Data Analysis' is about exploring, visualising and plotting the covid dataset on map using a powerful 
Data Mining tool [Orange](https://orangedatamining.com/). In this project, a real time covid dataset is used provided by CSSE at Johns Hopkins University, Baltimore, MD
on their [github page](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data).

## Requirements
Get Orange installed on your system from the [download link](https://orangedatamining.com/download/).

## Add-ons Required
After the successful set up, start the Orange and navigate through "Options" on the top left corner and click on "Add-ons..." under it. A pop up 
window "Installer - Orange" appears, add the required packages "Geo" and "TimeSeries" and then restart Orange.

## Walkthrough the Project
----------------------------------------------------

## 1. Import dataset into File widget
- From the "Data" section, either click on or drag the "File" widget to the white Canvas on right.
- Double-click the File widget, File window will pop out select "url" and enter the [url](https://github.com/Divya-Juhi-Singh/Covid_Analysis/blob/main/covid_dataset.md) for the file (file to be either excel, csv or tab).
![File]()

## 2. Preprocess the data
- Use the "Preprocess" widget to remove missing values if any, by drawing a line between File and Preprocess.
- Use "Select Columns" widget to remove the "Province/ Region" field as it contains too many missing values moreover removing it won't affect our results. Similar to the previous act of join two widgets, join Preprocess to Select Columns.
![Preprocess]()
![Select Columns]()

## 3. Exploring the data using Line Plot
- Place the "Line Plot" on canvas and join it to the right of Select Columns.
- For exploring covid data, sketch a line over the Line Plot to select few lines of the plot.
- To see the results of selected lines in tabular format join Data Table to the right of Line Plot.
![Line Plot]()
![Data Table]()

## 4. Visualising covid dataset using Geo Map
- Place the "Geo Map" on canvas and join it to the right of Select Columns.
- For visualising the covid data on map, double-click the Geo Map which pops out a Geo Map window.
- Hover over any region on the map, all details including meta datas and features will be displayed to you.

## 5. Transpose the data for visualisation using Time Slice or Timeseries
- For using Time Slice or Timeseries, we need to get Date/ Time in one column which is provided as day on incrementing feature in the covid dataset, a new column for each day covid cases in the World.
- To achieve this, apply "Transpose" to the dataset from variable "Country/Region" and then use "Edit Domain" to edit the new feature as "Time".
- To check what has been achieved in a better way,if interested, join the "Data Table" to the next of Edit Domain.

## 6. Visualisation using Time Slice over Choropleth Map
- Next to the widget's arrangement uptill step 5, join "Time Slice" widget, double-click to open it and then select a time period you want to analyse the covid cases of.
- Again apply the Transpose this time select Generic and Edit Domain and check the result on Data Table
-  Retransposing of the data is to get our data as before so that it can be plot over "Choropleth Map".
-  Open the windows of both Time Slice and Choropleth Map side-by-side and play the Time Slice
-  Thereover, you will see amazing results over Choropleth Map, visualising the changes in the covid cases over the time selected for whole of the World, a perfect way of analysing the covid scenario by changes in colour over time and globe with a legend.

## 7. Visualisation using Timeseries and Line Chart
- Same as 6th step follows here, next to the widget's arrangement uptill step 5, join "Timeseries" widget, double-click to open it and then select the option "Sequence is implied by instance order" and close the window.
- Next to Timeseries, join Line Chart and open it to have a analysis by the graph
- The x-axis of the graph shows the Time while on y-axis it shows the number of covid cases. The chart for the rise and fall in the covid cases for respective countries is shown by different colours.
- Select a few countries from the country list on left. The graph for analysis will be shown on the rightside. 
- You can place the pointer at any point of time, the number of cases will be displayed over to you for the countries have been selected earlier.



