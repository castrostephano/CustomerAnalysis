# Tableau Customer Analysis
Tableau Customer Analysis Dashboard

This project was a example of how to create an interactive customer analysis dashboard and the image below is the final product where the various worksheets combine to create the dashboard.

<img width="1280" alt="Screen Shot 2023-10-14 at 12 07 04 PM" src="https://github.com/castrostephano/CustomerAnalysis/assets/52759459/92c60ed7-9fc8-48e2-9be3-982e8a8e1ff4">

Specific steps on how to create charts that are not included in Tableau:

-- Donut Chart --

* Create a Pie chart with Regions in the columns and SUM(Total) in the rows then add the labels
* To get the percentage, go to the SUM(Total) in the Marks section, choose "Quick Table Calculation" then choose "Percent of Total"
* Click on the drop down in the Data pane, then choose "Create Calculated Field" called "Zero Axis" where you only enter "0"
* Drag and drop SUM(Zero Axis) twice on rows, then get rid of all the data from one of the two pie charts
* Increase the size of both charts, but making sure that the first chart with data is bigger
* Click n the left pane of the empty pie chart and choose "Dual Axis"
* Make the inside circle white and the donut chart is complete

-- Butterfly Chart --

* SUM(Total) in Columns, then Gender and Category both on the Rows section
* Click on the drop down in the Data pane, then choose "Create Calculated Field" twice to create Female Revenue and Male Revenue calculations:
  * IF [Gender] = 'M' Then [Total] END for Male Revenue
  * IF [Gender] = 'F' Then [Total] END for Female Revenue
* Remove SUM(Total) in columns and Gender in Rows and replace them with Male Revenue and Female Revenue in the Columns
* Drop the "Zero Axis" in the middle of Male Revenue and Female Revenue
* Click on the SUM(Zero Axis) pane and drag and drop Category onto the label. Then instead of "Automatic", choose "Text" and rename column to "Categories"
* Uncheck show header on Category in Rows section
* Click on Edit Axis one of the chart's header and choose "Reversed" in the Scale section, sort, design and add labels
