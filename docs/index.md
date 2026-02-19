---
title: "Creating Data Visualizations Using Tableau Desktop (Beginner)"
layout: "home"
description: ""
permalink: "/"  #! Remove this if not the homepage
---

# Creating Data Visualizations Using Tableau Desktop (Beginner)

This guide is suitable for new Tableau users looking for information on producing popular data visualizations in Tableau, such as bar graphs, line graphs, scatterplots, tree maps, and dashboards. If you are looking for more general data visualization tips, please see the Map and Data Library's [Data Visualization Guide.](https://mdl.library.utoronto.ca/dataviz/getting-started)You can find instructions on installing and acquiring a free academic license for Tableau [here](https://mdl.library.utoronto.ca/technology/tutorials/installing-tableau-desktop). If you are running Tableau on a Mac, please note that there may be some variation between the Windows version used to design this guide and the program as it appears on a Mac.

The data used in this guide are public datasets retrieved from the World Bank’s Open Data repository, the United Nation's Open Data Population Division, and the full text of Shakespeare's Romeo and Juliet available through MIT's website, with a frequency table generated through Voyant Tools. You can find more information regarding the data sources used in this guide in the subsection entitled "10\. Data Sources".

This tutorial was created using Tableau Desktop version 2020\.2\.

 

**Table of Contents**
---------------------

[1\. Opening Datasets in Tableau](#1)

[2\. Beginning Work](#2)

[3\. Creating a Simple Bar Graph](#3)

[4\. Creating a Simple Line Graph](#4)

[5\. Creating Simple Scatter Plots and Merging Datasets](#5)

[6\. Creating a Tree Map](#6) 

[7\. Creating a Stacked Bar Chart and Using Parameters](#7)

[8\. Creating a Dashboard](#8)

[9\. Publishing Tableau Visualizations and Further Resources](#9)

[10\. Data Sources](#10)

 

**1\. Opening Datasets in Tableau**
-----------------------------------

When you first open Tableau, it looks like this. The main page presents you with several options, such as connecting to a file, to a server, or to save sample data sources. You can also access Tableau’s online training through the “Discover” tab on the right, or access Tableau's help section (with tutorials) [here.](https://www.tableau.com/support/help)

![Initial Tableau start-up page showing connect to file options and sample dataset options]({{ '/assets/images/Tableau_1_0.PNG' | relative_url }})

 

2\. Beginning Work
------------------

In order to begin making visualizations, you must import a dataset into Tableau (such as an Excel spreadsheet) or select a sample dataset from Tableau (such as those located in the bottom left of the page as you open Tableau). For the purposes of this guide, you may download the datasets we will be using for this tutorial in a .Zip file [here](https://maps.library.utoronto.ca/datapub/workshops/TableauDataFiles.zip). You will need to extract the files from the zipped folder using a software such as [7\-Zip](https://www.7-zip.org/).

 

3\. Creating a Simple Bar Graph
-------------------------------

Our first dataset is an Excel file, so in Tableau, click on **Excel** under **Connect To a File**, and select the *2015RainfallByMonthByCountry.xls*file. Click **Open**.  
![Connect to file menu with Microsoft Excel highlighted.]({{ '/assets/images/TableauVisualization_1.png' | relative_url }})

Click on **Sheet 1** (at the bottom, the tab to the right of "Data Source") to open up a worksheet and start creating your visualization.  
![Highlight of Sheet 1 icon]({{ '/assets/images/icon.PNG' | relative_url }})

On the left, you can see our variables listed. Tableau categorized the variables as either **Dimensions** or **Measures**, listing all the Dimensions first above the gray line, and then all the Measures below the grayline.

![Highlight of the Dimensions section at the top and the Measures section directly below it in the Sidebar]({{ '/assets/images/tableau_beginner_003a.JPG' | relative_url }})

The centre area is where you will be dragging and dropping your variables onto different areas, such as rows and columns, or to vary marks like colour or size by your variable, or to filter by a variable. In terms of Tableau terminology, those areas that say filters or pages are called shelves, the marks area is called a card, and when the variables show up in those areas, they are called pills (as they are shaped like a pill).

![The Filters and Marks section is highlighted, located to the left of the sheet. The Columns and Rows sections are also highlighted, located at the top of the sheet.]({{ '/assets/images/tableau_beginner_003b.JPG' | relative_url }})

We loaded in some data that contains average monthly rainfall by country (looking at data from 1901 to 2015\). So let’s create a bar graph with the month along the x\-axis and average rainfall along the y\-axis. Drag the **Month** variable (in the **Dimensions** section on the left) to the **Columns** section and **Rainfall (mm)** (in the **Measures** section on the left) variable to the **Rows** section.

![Highlight of Month and rainfall variables in their original dimensions and measures location as well as in pill form in the Columns and Rows sections respectively]({{ '/assets/images/tableau_beginner_003c.JPG' | relative_url }})

You can see that when we dragged rainfall, it automatically summarized it by adding up all the rainfall averages for all the countries. We can change this to average. Right\-click on the **SUM(Rainfall (mm))** pill in the **Rows** section, go to the **Measure (Sum)** menu and pick **Average**. You will notice that the y\-axis in the resulting graph will have changed.

![SUM(Rainfall (mm)) drop down menu with Measure and Average highlighted,]({{ '/assets/images/Visualization_1.png' | relative_url }})

Right now our graph is showing data combined for all of our countries, but let’s say we just want it to show one of them. Drag the **Country** variable over to the **Filters** shelf and select one country from the list – let’s pick **India.** Click **OK**.

![Filter [Country] menu with India highlighted. ]({{ '/assets/images/Visualization_2.png' | relative_url }})

Now we have a bar graph showing the average rainfall in millimetres for India by month.

![Bar graph is displayed with these initial parameters.]({{ '/assets/images/IndiaBarGraph.JPG' | relative_url }})

Next, let’s look at the **Marks** card. You should see 5 boxes labeled Color, Size, Label, Detail, and Tooltip. You can use these to customize your visualization.

![]({{ '/assets/images/TableauVisualization_2.png' | relative_url }})

Click on **Color**, and change the colour of the bars to a different shade of blue.

![Marks tab with Color highlighted.]({{ '/assets/images/Visualization_3.png' | relative_url }})

Click on **Size**, and use the slider to make the bars wider or narrower.

![Marks tab with Size highlighted. ]({{ '/assets/images/Visualization_4.png' | relative_url }})

Click on **Label**, and select **Show Mark Labels** box to see the values for each bar.

![Marks tab with Label highlighted. ]({{ '/assets/images/Visualization_5.png' | relative_url }})

Click on **Tooltip** to adjust the text that shows up in the pop\-up you get when you hover over the data in your graph. Add to the bottom of the text “Data from WorldBank”. Then click on **OK**. Now hover over the data to see your changes.

![Image displaying the Edit Tooltip pop-up window. 'Data From WB' is written in its textbox, underneath the default text.]({{ '/assets/images/Tableau%20Tool%20Tip%20Edit.JPG' | relative_url }})

You can also customize your axes. Right\-click on your y\-axis title, and select **Edit Title...**

![Right click on y-axis option- with Edit Title highlighted. ]({{ '/assets/images/Visualization_6_0.png' | relative_url }})

Change the title (under **Axis** **Titles** in the **General** tab) to write out the word “Average” instead of “Avg.” Then close the window. The change will be applied automatically, so there is no need to click a “save” button (you will notice there is no "save" button). Click the “x” in the top right\-hand corner to exit the Edit Axis window.

![Image of the edit axis options pop-up window and the lack of an "ok" box to click]({{ '/assets/images/tableau_beginner_003e.JPG' | relative_url }})

You can also annotate your visualization. Perhaps you want to point out that the summer months are Monsoon season for India, which may be why there is such a spike in average rainfall. Right\-click on white space above the graph above those months and select **Annotate** and pick **Area...** Then type in “Monsoon Season”, change its font size to 12, bold it, and click **OK**. Now you can resize and move the box and place it where you want in the graph.

Finally, we can give our visualization a title by double\-clicking on **Sheet 1** at the top and replacing the text with our title “Average Monthly Rainfall for India” and click **OK**. Done! You have created your first visualization on Tableau Desktop.

![Final bar graph is shown with the new text box and new title highlighted.]({{ '/assets/images/tableau_beginner_003f.JPG' | relative_url }})

If you like this visualization and would like to learn how to save, export, or print it at this point in time, you can skip ahead to Section 9:[Publishing Tableau Visualizations and Further Resources](#9). However, you can always come back and save all of your visualizations at the end if you would prefer to proceed to the next section.

 

4\. Creating a Simple Line Graph
--------------------------------

Okay, let’s create a new visualization: A line graph of average monthly temperature data by country (looking again at the same range of years, 1901\-2015\). First, we need to load some more data. Go to the top **Data** Menu and select **New Data Source**. Select **Excel** and choose the *2015TemperaturesByMonthByCountry.xls* file.  
![Adding a new data source, with "New Data Source" option highlighted. ]({{ '/assets/images/TableauVisualization_3.png' | relative_url }})

From this screen, you can see what types of variables Tableau has detected (based on small icons above the variables names).

![The image shows the Data Source Page Display. The data table for the loaded data is displayed with the variable types highlighted. ]({{ '/assets/images/tableau_beginner_004a.JPG' | relative_url }})

These variables can be changed if you’d like. For example, based on the small "**Abc"** above them, you can see that **Year** and **Month** columns have been identified as a string. If I want to plot data over time using a line graph, it would be best to change **Month** to date format. To do that, I just click on the **Abc icon** above the **Month** column and select **Date** instead.

![Image showing the configuration of the variable type in the initial data source view for the variable, 'Month'. A dropdown menu is displayed with a list of variable configuration options: the option 'Date' is highlighted.]({{ '/assets/images/tableau_beginner_004b.JPG' | relative_url }})

You’ll see below that the data has changed format and the icon now looks like a calendar.

![Image showing the changed variable type to date from numeric]({{ '/assets/images/tableau_beginner_004c.JPG' | relative_url }})

Once happy with your data, you can create a new worksheet to start building a new visualization by clicking on the tab next to where it says Sheet 1\. This is a **new worksheet icon**.

![Image showing the new worksheet button]({{ '/assets/images/Tableau_2copy.PNG' | relative_url }})

Let’s drag the **Month** variable to the **Columns** section again. This time it is a date variable, so we have more options in our drop\-down menu. We want is to make sure we’re displaying months, not years, so right click on the **Month** pill and select the first option for **Month**.

![Image showing the configuration for month. A drop-down menu is displayed with a list of configuration options, the first option 'Month' is highlighted.]({{ '/assets/images/tableau_beginner_004d.jpg' | relative_url }})

Next, drag the **Temperature** variable to the **Rows** section. You’ll notice that our graph is summing the temperatures for all the countries. We can again right\-click on the **Temperature** pill, and select **Measure (Sum)**, then pick **Average**. Your "pills" and graph should look like the image below.

![The initial line graph is displayed]({{ '/assets/images/Capture3_1.JPG' | relative_url }})

We would like to see each country’s data separately, so let’s drag the **Country** variable onto the **Color** box in the **Marks** card. You can see that Tableau has assigned a qualitative colour palette scheme to represent our countries, but we do have a lot of them, so it is a bit overwhelming.

![Highlight of the Country variable in the Dimensions section as well as the colour box in the Marks Card.]({{ '/assets/images/tableau_beginner_004e.JPG' | relative_url }})

One way to simplify this would be to show 2 countries to compare their temperature distributions. Drag the **Country** variable over to the **Filters** shelf. Click on the **None** button to first clear the selections. Then select two countries only – let’s pick **Canada** and **Brazil**. Now we are just filtering the data to show only Canada and Brazil.

**Note** that if you can't see this Country legend, then you need to move or close the "Show Me" window, which could be concealing the legend. Go ahead and move or close the window so that you can see the legend.

![Line graph shows temperatures for Brazil and Canada, with the Filters and Country boxes highlighted]({{ '/assets/images/BrazilCAN2_0.JPG' | relative_url }}) 

Another way we could do this would be to allow the user to filter it themselves based on what countries they are interested in. To do that, go back to the **Filters** shelf, right\-click on the **Country** pill and pick **Edit Filter…** Select the **All** button to re\-select all the countries and then click **OK**. Then right\-click on the **Country** pill again, but this time select **Show Filter**. Now you can see the filters show up on the right. We can select or deselect as we like and the graph changes.

![A line graph displaying temperature for various countries. The ‘Country’ pill in the Filter Shelf as well as the resulting Country Filters are highlighted. ]({{ '/assets/images/Section4%20T6_0.JPG' | relative_url }})

To further help the user read your graph, you could also add a highlighter. Go back to the **Filters** shelf, right click on the **Country** pill, but this time pick **Show Highlighter**. Now the **Highlight Country** box shows up on the right.

![Image displaying a dropdown menu emerging from the 'Country' pill in the filters card. In the dropdown menu 'Show Highlighter' is selected.]({{ '/assets/images/tableau_beginner_004f.jpg' | relative_url }})

The user can pick a country and the graph emphasizes that country. To try it out, make sure you aren’t filtering any of the countries first, then click on the **Highlight County** search box to see the list of countries, and then hover over one – try **Canada**. You should see it emphasized in the graph.

Let’s adjust a bit more of the formatting on this graph. For one thing, I don’t like how the months are displayed at the bottom. We can fix that. Right\-click on one of the months and select **Format**…

![Image displaying a dropdown menu emerging from the Months' axis. In the dropdown menu 'Format...' is selected.]({{ '/assets/images/tableau_beginner_004g.jpg' | relative_url }})

The **Format** pane should show up on the left. From the **Header** tab, under **Default**, where it says **Dates**, select from the drop\-down menu, **Abbreviation**.\* Then click anywhere on the graph to save it.

*\*If you are encountering a problem where the "Dates" option is not showing up under the Default section, you might have the wrong data type selected for your "MONTH(Month)" variable. You can rectify this issue by right\-clicking the "MONTH(Month)" pill (selected as your column) and selecting the other "Month" option. Then try the previous step again.*

*![Image showing the location of the Dates formatting options in the ‘Format Month’ window. A drop-down menu emerges from it, with the option ‘Abbreviation’ highlighted. ]({{ '/assets/images/tableau_beginner_004h.jpg' | relative_url }})*

Finally, let’s say you didn’t like these colours. Click on the **Color**box under **Marks** and select **Edit Colors**…

![Highlight of the Colour box in the Marks card. A drop-down menu emerges from it with the 'Edit Colours...' button highlighted.]({{ '/assets/images/tableau_beginner_004i.jpg' | relative_url }})

Here you can pick from a drop\-down menu of various qualitative palettes, including a colour blind safe palette. Select one you like and click on **Assign Palette (you must click this option to activate the new colour palette)**. Then click on **OK**.

![Pop-up window displaying the Edit Colors options, with the ‘Assign Palette’ button highlighted]({{ '/assets/images/ColourBlind.JPG' | relative_url }})

Again, we can give our visualization a more meaningful title by double clicking on **Sheet 2** at the top and replacing the text with our title “Average Monthly Temperature for Various Countries” and click **OK**. You have completed a simple line graph in Tableau Desktop!

 

5\. Creating a Series of Simple Scatter Plots and Merging Datasets
------------------------------------------------------------------

Sometimes you have to pull data from multiple sources instead of having it all in one Excel file. So, let’s add a couple more datasets, but this time we’re going to match them up, or have Tableau join them together so we will have one large dataset to work from.

Go to the top **Data** Menu and select **New Data Source**. Select **Excel** and choose the *AuthorDataCitationsGrants.xls* file, then click **Open**.

Now click on **Add** next to **Connections** on the top left to add a second dataset to ultimately create a database join. Select **Excel** and then pick the *AuthorDataExperience.xls* file. This dataset has just author names, along with how many years of experience they have as a researcher.

![Top left of Data Source Page Display is shown, with the "Add" option highlighted.]({{ '/assets/images/Section5%20T1.PNG' | relative_url }})

You can now see the two datasets listed under connections. In order to relate the two datasets together, double click on **AuthorDataMain** above the table.<img src='{{ '/assets/images/TableauBeginnerUpdate-5.2.jpg' | relative_url }}' alt='' title='' width='1409' height='850' />

 

Ensure the dataset AuthorDataExperience is selected and drag its **sheet**, also named **AuthorDataExperience** beside AuthorDataMain.

![The Data Source Page Display is shown, with the Sheets section and AuthorDataMain section highlighted.]({{ '/assets/images/tableau_beginner_005b.JPG' | relative_url }})

At the top you can now see the two datasets listed, and below you’ll see that Tableau has joined the two together, matching based on the author name. If you want to double check this, click on the **circles** between the two dataset names at the top; this will also provide you with more information about how the join was completed by Tableau. You can see from the icons that Tableau has done an inner join, matching the column Author in one dataset with the Author column in the second dataset. It has copied pasted that information about the author’s years of experience next to that author wherever the author shows up in the first table. The inner join means that it only keeps data on an author if that author shows up in both tables. (Note: If database joins are new to you, see this [resource](https://www.codeproject.com/Articles/33052/Visual-Representation-of-SQL-Joins)for a detailed explanation.)

![The new connection between datasets is illustrated with a small Venn Diagram]({{ '/assets/images/Section5%20T2.PNG' | relative_url }})

Again, once you're happy with your data, you can create a new worksheet to start building a new visualization by clicking on the **new worksheet icon** (at the bottom left of your screen to the right of the Data Source).

This time, let’s take a look at creating a scatter plot using the **Show Me** feature. To do so, *first* hold down the **CTRL** button (on your keyboard) and click on **Grants** and **Years of Experience.** *Secondly*, click on the **Show Me** tab to expand it. We see that a Scatterplot is one of the recommendations (i.e., not greyed out) – select it. If you’re not sure which one it is, hover over the images and then read the description below to find out which one is the scatter plot. *Thirdly,* observe how Tableau automatically populated your column and row fields once the scatter plot option was selected.

![The screen is pictured with the numbers 1 through 3, corresponding to the instructions above.]({{ '/assets/images/tableau_beginner_005c.JPG' | relative_url }})

Click on **Show Me** again to hide its options panel.

First, instead of summing these variables, let’s take the averages, as we’ve done before. So right click on each pill in the **Rows** and **Columns** sections, and select **Average** from the **Measure (Sum)** menu.

Our next problem is that it is plotting just one x/y pair – the averages of the whole dataset. We need to plot the points either for each author, country, or institution. Let’s do it by author. Drag the **Author** variable over the **Details** box; it explodes out the aggregation to plot it by author. When you hover over each point, you can see the details.

![Image showing the original position of the Author variable in the Dimensions section, the location of the Detail box in the Marks card, as well as the Columns and Rows containing the pills of Average Years of Experience and Average Grants respectively. ]({{ '/assets/images/tableau_beginner_005d.JPG' | relative_url }})

You may notice there is now also another box on the Marks card called Shapes. If you want to add another categorical variable to your scatter plot, you could do so by using different shapes to represent different categories. Drag **Institution** on to the **Shapes** box. Now you should see that there is a legend on the right, using different shapes for different institutions.  
<img src='{{ '/assets/images/TableauBeginnerUpdate-5.7.jpg' | relative_url }}' alt='' title='' width='1896' height='961' />

 

If you want to add a trend line, right click in the centre of the graph and select **Trend Lines**, and then **Show Trend Lines**.

![Image displaying a dropdown menu emerging from the graph. In the master dropdown menu 'Trend Lines' is selected. From this selection a sub-drop down menu is shown with the option 'Show Trend Lines' highlighted.]({{ '/assets/images/tableau_beginner_005g.jpg' | relative_url }})

Hovering over the lines gives you statistical information, such as a regression and p\-values.

Finally, one interesting feature of Tableau is that you can create not just one visualization, but a series of them, using the **Pages** shelf. Drag **Year** onto the **Pages** shelf.

![Image highlighting the variable 'Year' in the Dimensions section and the Pages card. ]({{ '/assets/images/tableau_beginner_005h.JPG' | relative_url }})

Now you should see some "Year" controls on the right. The user can scroll through three different scatter plots, one for each year, or they can click on the play button to have it animate through the years. Your final graph should resemble the image below (depending on which "page" is currently visualized in Tableau).

<img src='{{ '/assets/images/TableauBeginnerUpdate-5.10.jpg' | relative_url }}' alt='' title='' width='1699' height='964' />

Again, you may be interested in giving your visualization a name, which you can click and change at the top left of your scatter plot.

 

6\. Creating a Simple Treemap
-----------------------------

Go to the top **Data** Menu and select **New Data Source**. Select **Excel** and choose the *2016PopulationbyRegion.xls* file. This dataset lists population totals for various regions on earth.

Again, once you are happy with your data in the data source view, you can create a new worksheet to start building a new visualization by clicking on the **new worksheet icon** (same as before \- to the right of Sheet 3 at the bottom left\-hand corner).

Treemaps help show hierarchical divisions of parts within a whole. To create a treemap in Tableau, first drag the **Region** variable onto the **Label (text)**box in the **Marks** card, as we’re going to separate and label each box with the Region name.

![Image highlighting the variable 'Region' in the Dimensions section as well as the Text box in the Marks card.]({{ '/assets/images/tableau_beginner_006c.JPG' | relative_url }})

Next drag the **Population** variable onto the **Size** box as we’re going to size these regions blocks by their population.

![Image highlighting the variable '2016Population' in the Measures section as well as the Size box in the Marks card.]({{ '/assets/images/tableau_beginner_006d.JPG' | relative_url }})

Finally, drag the **Continent** onto the **Color** box to colour code the blocks by continent.

![Image highlighting the variable 'Continent' in the Dimensions section as well as the Colour box in the Marks card.]({{ '/assets/images/tableau_beginner_006e.JPG' | relative_url }})

You can hover over the blocks to get more information on the populations, or you could label it as well. Drag the **Population** variable again over the **Label** box to include that information under the region name. You have completed a simple treemap!

![Image highlighting the variable ‘2016Population’ in the Measures section, the location of the Label box in the Marks card, and the resulting tree map with the new labels.]({{ '/assets/images/tableau_beginner_006b.JPG' | relative_url }})

 

7\. Creating a Stacked Bar Chart and Using Parameters
-----------------------------------------------------

Go to the top **Data** Menu and select **New Data Source**. Select **Excel** and choose the *RomeoAndJulietWordFrequenciesByAct.xls* file. This dataset lists word frequencies in Romeo and Juliet by Act. Make sure to check how your variables are classified – note that “Act” is classed as a numeric variable when we know it is a string. You can change this now, as we did before, but we will also show you how to change this later in the guide (in the event you didn't notice this when you initially imported your dataset into Tableau!).

![Image showing the "Act" variable classified as a numeric versus a string variable.]({{ '/assets/images/Section7%20T1.PNG' | relative_url }})

Again, once I’m happy with my data, I can start building a new visualization by clicking on the **new worksheet icon**.

Hold down the **CTRL** button (on your keyboard) and click on the **Term** variable and the **Count** variable, then click on the **Show Me** tab to expand it. I see that a horizontal bar graph is one of the recommendations (i.e., not greyed out) – select it. Your graph should resemble the image below.

![Image displaying the Term variable in the Dimensions section and the Count variable in the Measures section highlighted as well as the horizontal bar graph option highlighted in the ‘Show Me’ menu.  ]({{ '/assets/images/tableau_beginner_007a.JPG' | relative_url }})

Now let’s filter it so we only see the top 10 words mentioned. Drag the **Term** variable to the **Filters** shelf. Go to the **Top** tab, and select **By Field**. By default it is going to use the Count variable and sum up the instances to get the top 10\. Click **OK**.

![The Filter pop-up window is displayed, with the "By field" section and "OK" button highlighted.]({{ '/assets/images/ZZ.JPG' | relative_url }})

Now you will have your top 10 terms, listed in alphabetical order by term. It might be nicer to sort them by count. We can do this by right\-clicking on the **Term** pill in the **Rows** section and select **Sort**. In the **Sort By** section, select **Field.** Under Sort Order, select **Descending.** Leave the rest of the defaults selected, as these will give us the sum of count. You'll notice there is no "OK" or "Apply" option. Changes are applied automatically, so simply click the **X** in the top right of the **Sort** window.

![Image of the Sort pop-up window with "Descending" selected]({{ '/assets/images/zzzx.JPG' | relative_url }})

Result:

![The resulting bar graph is displayed; it has fewer terms in it than the previously.]({{ '/assets/images/AHH.JPG' | relative_url }})

Now suppose I’d like to add information about the Act to make a colour\-coded stacked bar chart. If you did not change the **Act** variable to a string at the beginning of this section, you will notice that when we look at what variable types Tableau has identified, it thinks the **Act** variable is a numeric variable in the measures section, when really it is categorical in this case. If necessary, let’s change it by moving it to our dimensions section. *Firstly,* drag the **Act** variable into the **Dimensions** section.

Now it is a category, so it makes sense to visualize it through colour*. Secondly,* drag the **Act** variable onto the **Color** box in the **Marks** card. Looking better, but the Acts seems to be showing from Act 5 to Act 1\. We can fix that by right\-clicking on the **Act** pill and *thirdly*selecting **Sort**. Select **Descending** and then click the**X**.

![The screen is pictured with the numbers 1 through 3, corresponding to the instructions above.]({{ '/assets/images/tableau_beginner_007b.JPG' | relative_url }})

So now we have our top 10 terms, subdivided by Act; however, what if our audience would rather just see the top 5 terms, or would like to expand it out to the top 20 or 30 terms. We can get an audience’s input into our visualizations using parameters. Right\-click on **Term** in the **Filters** shelf, and select **Edit Filter...** Go to the **Top** tab and click on the drop\-down arrow next to where 10 is specified. Select **Create a New Parameter...** Give it a name, such as **Top Number**. Go down to the **Range of Values** section. Set the minimum to **5,** the maximum to **30**, and the **step size** to **5**. Then click on **OK**, and click **OK** again on the **Filter** window.

![Image showing all the steps described above highlighted on the screen.]({{ '/assets/images/tableau_beginner_007c.JPG' | relative_url }})

Your **Top Number parameter** should show up on the left side, under your variables. Right click on it, and select **Show Parameter**.

Your final product should resemble the image below. Your audience can use the control on the right to adjust how many terms to see in their top terms list.

![Image showing the final product of step number 7, with the Act parameter controls to the right of the Sheet.]({{ '/assets/images/tableau_beginner_007d.JPG' | relative_url }})

 

8\.  Creating a Dashboard
-------------------------

Now so far we’ve been creating visualizations within worksheets. But you can also create dashboards that combine a number of worksheets together. We are now going to create a dashboard capable of displaying the average monthly rainfall and temperature for one country at a time. Let’s click on the **create new dashboard** icon at the bottom, next to the **new worksheet** icon.

![Image showing the New Dashboard button, consisting of four small squares]({{ '/assets/images/addingsheets_tabs%20-%20Copy.PNG' | relative_url }})

You then can drag and drop various sheets to layout a dashboard. You can also drag other objects, such as text or images to create your dashboard. From the left side of your screen, drag **Sheet 1** to the dashboard area.

![Image showing Sheet 1 highlighted in the Sidebar as well as the result of dragging the sheet to the dashboard area.]({{ '/assets/images/tableau_beginner_008a.JPG' | relative_url }})

Next drag **Sheet 2** to the bottom of the dashboard area. As you are dragging each sheet, Tableau will shade in the section of the page the sheet will occupy once you release it, so use this as your guide to the placement of your sheets in the dashboard.

![Image showing Sheet 2 highlighted in the Sidebar as well as the bottom of the dashboard area highlighted, where Sheet 2 has been dragged. ]({{ '/assets/images/tableau_beginner_008b.JPG' | relative_url }})

We can also take the filters we had for one worksheet, in this case the temperature graph, and then apply it to the all the sheets on the dashboard. We can do that in this case, with just a few adjustments to our Sheet 1\. Go back to Sheet 1 by clicking on its tab at the bottom. Select the annotation (your "monsoon season" text) and press the **Delete** key on your keyboard to remove it. **Adjust the title** removing the mention of a particular country. Drag the **Country** filter, set to India, back towards the **Dimensions** and **Measures** section to remove it (which you can do with any variables you want to remove from your visualization).

Go back to the dashboard by selecting its tab at the bottom. Right\-click on the title of the filter, **Country**, select **Apply to Worksheets**, and then pick **All Using Related Data Sources**.

![Image displaying a dropdown menu emerging from the Country filter title. In the master dropdown menu ‘Apply to Worksheets' is selected. From this selection a sub-drop down menu is shown with the option ‘All Using Related Data Sources’ highlighted.]({{ '/assets/images/tableau_beginner_008c.jpg' | relative_url }})

Right\-click again on the **Country** filter title, but this time select **Single Value (list**). This will make sure that your audience can only view one country at the time. Now you’ll see that when you select one country, both graphs refer to that country.

![Image displaying a dropdown menu emerging from the Country filter title. In the dropdown menu ‘Single Value (list)' is selected. ]({{ '/assets/images/tableau_beginner_008d.jpg' | relative_url }})

 

9\. Publishing Tableau Visualizations and Further Resources
-----------------------------------------------------------

If you’re working on some visualizations, like we have been in this guide, you can save work\-in\-progress as a Tableau Workbook file. Go to the **File** menu and click on **Save**. Give it a name and select where you want to save the file. (Note: If you do this, it doesn’t save the underlying data, so you have keep the data file(s) \- such as your Excel worksheets \- and Tableau workbook together).

![How to save workbook by using the file tab, with save highlighted.]({{ '/assets/images/Visualization_9.png' | relative_url }})

Or you can **Export Packaged Workbook…** (also from the **File** menu). Then you could share that file with others who have Tableau (and this time it would include the data). In both cases, you can always come back later to revisit your work by reopening it on Tableau Desktop.

![How to Export Package Workbook using the File tab. Export Package Workbook highlighted.]({{ '/assets/images/Visualization_10.png' | relative_url }})

If you want to export one of your worksheets to an image you can use in a report or article, you can do so from the **Worksheet** menu. First, go to the worksheet tab you want to save. Then, open the **Worksheet** menu and use the **Copy**or **Export**options to copy/ paste your visualization into a document/ image editing software or export it directly.

![Worksheet tab with Copy and Export highlighted.]({{ '/assets/images/Visualization_7.png' | relative_url }})

You can do the same thing for your whole Dashboard from the **Dashboard** menu(“Copy” or “Export” image). Try it out! **Note:** these options only share a static image, without the filter capabilities we added to the dashboard in the previous section. If you want your users to interact with your visualization, continue reading below.

![Dashboard tab with Copy and Export image options highlighted. ]({{ '/assets/images/Visualization_8.png' | relative_url }})

Finally, you can publish your worksheets and dashboards so that readers can interact with them. Your free option is to create a [Tableau Public](https://public.tableau.com/s/) account and publish it there using the**Publish Workbook**option in the **Server** menu (but note it is public; however, you can adjust the settings, if you don’t want readers to download the underlying data and/or workbook). Once it is uploaded to Tableau Public, there is also functionality built\-in for you to embed your visualization on a website. Using the "share" option at the bottom of a published visualization on Tableau Public, you can copy and paste the HTML code for embedding the visualization in a website. There are also paid options ([Tableau Online](https://www.tableau.com/products/cloud-bi?ab=1) and [Tableau Server](https://www.tableau.com/products/server)), if you want to be able to limit permissions on who can view your visualizations or to publish to your own server; use the **Publish Workbook** option from the **Server** menu to access these options.

You can also get inspiration for future visualizations and dashboards by browsing Tableau Public's online [gallery](https://public.tableau.com/en-us/s/gallery)

![Image showing the Tableau Public gallery page]({{ '/assets/images/tableaupublicgallery.PNG' | relative_url }})

In some cases, you may download the workbooks these visualizations were created in (and study them to recreate your own visualizations!).  You can see how to download or explore these Tableau Public visualizations by clicking the download button, which will prompt a pop\-up window with the options set up by the user who published the visualization.

![Image showing a sample Tableau Public dashboard and the download options for this dashboard, including Image, PDF, Powerpoint, and Workbook]({{ '/assets/images/sharingtableau%20workbooks.PNG' | relative_url }})

For further learning, training videos, and tutorials, please explore the many resources available on the[Tableau Help page](https://www.tableau.com/support/help).

10\. Data sources
-----------------

**2015RainfallByMonthByCountry.xls** \& **2015TemperaturesByMonthByCountry.xls** files:

[http://sdwebx.worldbank.org/climateportal/index.cfm?page\=downscaled\_data\_download\&menu\=historical](http://sdwebx.worldbank.org/climateportal/index.cfm?page=downscaled_data_download&menu=historical) (average monthly rainfall or temperature from 1901\-2015\)

**2016PopulationByRegion.xls**: United Nations, Department of Economic and Social Affairs, Population Division (20170\. World Population Prospects: The 2017 Revision, custom data acquired via website: <https://esa.un.org/unpd/wpp/DataQuery/>

**RomeoAndJulietWordFrequenciesByAct.xls** file from the play Romeo and Juliet by William Shakespeare full text: acquired via

<http://shakespeare.mit.edu/romeo_juliet/full.html> and then split into a document per act and run through Voyant tools: [https://voyant\-tools.org](https://voyant-tools.org)

 

 

 

Technique: [Data Visualization](/technique/data-visualization) \| Tools: [Excel](/tools/excel-0), [Tableau](/tools/tableau)**Date Created:** 2019\-03\-27**Updated:** 2022\-12\-15
