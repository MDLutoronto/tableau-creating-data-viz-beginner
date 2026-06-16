---
title: "4. Creating a Simple Line Graph"
parent: "Creating Data Visualizations Using Tableau Desktop (Beginner)"
layout: default
created_date: 2019-03-27
staff:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
maintainer:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
nav_order: 4
---

## 4. Creating a Simple Line Graph
    
Okay, let’s create a new visualization: A line graph of average monthly temperature data by country (looking again at the same range of years, 1901-2015). First, we need to load some more data. Go to the top **Data** Menu and select **New Data Source**. Select **Excel** and choose the *2015TemperaturesByMonthByCountry.xls* file.  

    ![Adding a new data source, with "New Data Source" option highlighted. ]({{ '/assets/images/TableauVisualization_3.png' | relative_url }})
    
From this screen, you can see what types of variables Tableau has detected (based on small icons above the variables names).

    ![The image shows the Data Source Page Display. The data table for the loaded data is displayed with the variable types highlighted. ]({{ '/assets/images/tableau_beginner_004a.JPG' | relative_url }})
    
These variables can be changed if you’d like. For example, based on the small "**Abc"** above them, you can see that **Year** and **Month** columns have been identified as a string. If I want to plot data over time using a line graph, it would be best to change **Month** to date format. To do that, I just click on the **Abc icon** above the **Month** column and select **Date** instead.

    ![Image showing the configuration of the variable type in the initial data source view for the variable, 'Month'. A dropdown menu is displayed with a list of variable configuration options: the option 'Date' is highlighted.]({{ '/assets/images/tableau_beginner_004b.JPG' | relative_url }})

You’ll see below that the data has changed format and the icon now looks like a calendar.

    ![Image showing the changed variable type to date from numeric]({{ '/assets/images/tableau_beginner_004c.JPG' | relative_url }})

Once happy with your data, you can create a new worksheet to start building a new visualization by clicking on the tab next to where it says Sheet 1. This is a **new worksheet icon**.

    ![Image showing the new worksheet button]({{ '/assets/images/Tableau_2copy.PNG' | relative_url }})

Let’s drag the **Month** variable to the **Columns** section again. This time it is a date variable, so we have more options in our drop-down menu. We want is to make sure we’re displaying months, not years, so right click on the **Month** pill and select the first option for **Month**.

    ![Image showing the configuration for month. A drop-down menu is displayed with a list of configuration options, the first option 'Month' is highlighted.]({{ '/assets/images/tableau_beginner_004d.jpg' | relative_url }})

Next, drag the **Temperature** variable to the **Rows** section. You’ll notice that our graph is summing the temperatures for all the countries. We can again right-click on the **Temperature** pill, and select **Measure (Sum)**, then pick **Average**.

    ![The initial line graph is displayed]({{ '/assets/images/Capture3_1.JPG' | relative_url }})

We would like to see each country’s data separately, so let’s drag the **Country** variable onto the **Color** box in the **Marks** card. You can see that Tableau has assigned a qualitative colour palette scheme to represent our countries, but we do have a lot of them, so it is a bit overwhelming.

    ![Highlight of the Country variable in the Dimensions section as well as the colour box in the Marks Card.]({{ '/assets/images/tableau_beginner_004e.JPG' | relative_url }})

One way to simplify this would be to show 2 countries to compare their temperature distributions. Drag the **Country** variable over to the **Filters** shelf. Click on the **None** button to first clear the selections. Then select two countries only – let’s pick **Canada** and **Brazil** and click on OK. Now we are just filtering the data to show only Canada and Brazil to tell our visual story.

**Note:** that if you can't see this Country legend on the right, then you need to close the "Show Me" window on the right by clicking on Show Me at the top right.

    ![Line graph shows temperatures for Brazil and Canada, with the Filters and Country boxes highlighted]({{ '/assets/images/BrazilCAN2_0.JPG' | relative_url }}) 

Another way we could do present this visual would be to allow the user to filter it themselves based on what countries they are interested in. To do that, go back to the **Filters** shelf, right-click on the **Country** pill and pick **Edit Filter…** Select the **All** button to re-select all the countries and then click **OK**. Then right-click on the **Country** pill again, but this time select **Show Filter**. Now you can see the filters show up on the right. We can select or deselect as we like and the graph changes.

    ![A line graph displaying temperature for various countries. The ‘Country’ pill in the Filter Shelf as well as the resulting Country Filters are highlighted. ]({{ '/assets/images/Section4%20T6_0.JPG' | relative_url }})

To further help the user read your graph, you could also add a highlighter. Go back to the **Filters** shelf, right click on the **Country** pill, but this time pick **Show Highlighter**. Now the **Highlight Country** box shows up on the right.

    ![Image displaying a dropdown menu emerging from the 'Country' pill in the filters card. In the dropdown menu 'Show Highlighter' is selected.]({{ '/assets/images/tableau_beginner_004f.jpg' | relative_url }})

The user can pick a country and the graph emphasizes that country. To try it out, make sure you aren’t filtering any of the countries first, then click on the **Highlight County** search box to see the list of countries, and then hover over one – try **Canada**. You should see it emphasized in the graph.

Let’s adjust a bit more of the formatting on this graph. For one thing, I don’t like how the months are displayed at the bottom. We can fix that. Right-click on one of the months and select **Format**…

    ![Image displaying a dropdown menu emerging from the Months' axis. In the dropdown menu 'Format...' is selected.]({{ '/assets/images/tableau_beginner_004g.jpg' | relative_url }})

The **Format** pane should show up on the left. From the **Header** tab, under **Default**, where it says **Dates**, select from the drop-down menu, **Abbreviation**. Then click anywhere on the graph to save it. Click on the x at the top right of the Format window to close it so you can see your variables again.

*If you are encountering a problem where the "Dates" option is not showing up under the Default section, you might have the wrong data type selected for your "MONTH(Month)" variable in the Columns section. You can fix this issue by right-clicking the "MONTH(Month)" pill (in the Columns section) and selecting the other "Month" option (i.e., the first Month option). Then try the previous step again.*

    ![Image showing the location of the Dates formatting options in the ‘Format Month’ window. A drop-down menu emerges from it, with the option ‘Abbreviation’ highlighted. ]({{ '/assets/images/tableau_beginner_004h.jpg' | relative_url }})

Finally, let’s say you didn’t like these colours. Click on the **Color** box under **Marks** and select **Edit Colors**…

    ![Highlight of the Colour box in the Marks card. A drop-down menu emerges from it with the 'Edit Colours...' button highlighted.]({{ '/assets/images/tableau_beginner_004i.jpg' | relative_url }})

Here you can pick from a drop-down menu of various qualitative palettes, including a colour blind safe palette. Select one you like and click on **Assign Palette (you must click this option to activate the new colour palette)**. Then click on **OK**.

    ![Pop-up window displaying the Edit Colors options, with the ‘Assign Palette’ button highlighted]({{ '/assets/images/ColourBlind.JPG' | relative_url }})    

Again, we can give our visualization a more meaningful title by double clicking on **Sheet 2** at the top and replacing the text with our title “Average Monthly Temperature for Various Countries” and click **OK**. You have completed a simple line graph in Tableau!

**Technique:** [Data Visualization](https://mdlutoronto.github.io/tutorials-search/?technique=Data+Visualization) \| **Tools:** [Tableau](https://mdlutoronto.github.io/tutorials-search/?tool=Tableau)