---
title: "5. Creating a Series of Simple Scatter Plots and Merging Datasets"
parent: "Creating Data Visualizations Using Tableau Desktop (Beginner)"
layout: default
created_date: 2019-03-27
staff:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
maintainer:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
nav_order: 5
---

## 5. Creating a Series of Simple Scatter Plots and Merging Datasets

Sometimes you have to pull data from multiple sources instead of having it all in one Excel file. So, let’s add a couple more datasets, but this time we’re going to match them up, or have Tableau join them together so we will have one large dataset to work from.

Go to the top **Data** Menu and select **New Data Source**. Select **Excel** and choose the *AuthorDataCitationsGrants.xls* file, then click **Open**.

Now click on the **plus sign** next to **Connections** on the top left to add a second dataset . Select **Excel** and then pick the *AuthorDataExperience.xls* file. This dataset has just author names, along with how many years of experience they have as a researcher.

    ![Top left of Data Source Page Display is shown, with the "Add" option highlighted.]({{ '/assets/images/Section5_step1.PNG' | relative_url }})

You can now see the two datasets listed under connections, with AuthorDataExperience highlighted. Under **Sheets", drag its sheet, also named **AuthorDataExperience**, beside AuthorDataMain in the blank space to the right. 

    ![The Data Source Page Display is shown, with the Sheets section and AuthorDataMain section highlighted.]({{ '/assets/images/tableau_beginner_005b.JPG' | relative_url }})

At the top you can now see the two datasets listed and connected together. The bottom window shows us that the data has been related together based on a common column, Author. Now the years of experience data will also be associated with the appropriate authors additional data found in the first table. Tableau performs relates and joins on the fly, as needed. If these terms are new to you, see this [article on relationships & joins](https://help.tableau.com/current/pro/desktop/en-us/datasource_relationships_learnmorepage.htm) for a detailed explanation. 
 
    ![The new connection between datasets is illustrated with a small Venn Diagram]({{ '/assets/images/Section5_step2.PNG' | relative_url }})

Again, once you're happy with your data, you can create a new worksheet to start building a new visualization by clicking on the **new worksheet icon** (at the bottom left of your screen to the right of Sheet 2).

This time, let’s take a look at creating a scatter plot using the **Show Me** feature. To do so, *first* hold down the **CTRL** button on your keyboard (Command key on a Mac) and click on **Grants** and **Years of Experience.** *Secondly*, click on the **Show Me** tab to expand it. We see that a Scatter plot is one of the recommendations (i.e., outlined) – select it. If you’re not sure which one it is, hover over the images and then read the description below to find out which one is the scatter plot. *Thirdly,* observe how Tableau automatically populated your column and row fields once the scatter plot option was selected.   

    ![The screen is pictured with the numbers 1 through 3, corresponding to the instructions above.]({{ '/assets/images/tableau_beginner_005c.JPG' | relative_url }})

Click on **Show Me** again to hide its options panel.

First, instead of summing these variables, let’s take the averages, as we’ve done before. So right click on each pill in the **Rows** and **Columns** sections, and select **Average** from the **Measure (Sum)** menu.

Our next problem is that it is plotting just one x/y pair – the averages of the whole dataset. We need to plot the points either for each author, country, or institution. Let’s do it by author. Drag the **Author** variable over the **Details** box; it explodes out the aggregation to plot it by author. When you hover over each point, you can see the details.  

    ![Image showing the original position of the Author variable in the Dimensions section, the location of the Detail box in the Marks card, as well as the Columns and Rows containing the pills of Average Years of Experience and Average Grants respectively. ]({{ '/assets/images/tableau_beginner_005d.JPG' | relative_url }})

You may notice there is now also another box on the Marks card called Shapes. If you want to add another categorical variable to your scatter plot, you could do so by using different shapes to represent different categories. Drag **Institution** on to the **Shapes** box. Now you should see that there is a legend on the right, using different shapes for different institutions.  

<img src='{{ '/assets/images/TableauBeginnerUpdate-5.7.jpg' | relative_url }}' alt='' title='' width='1896' height='961' />

If you want to add a trend line, right click in the centre of the graph and select **Trend Lines**, and then **Show Trend Lines**.

    ![Image displaying a dropdown menu emerging from the graph. In the master dropdown menu 'Trend Lines' is selected. From this selection a sub-drop down menu is shown with the option 'Show Trend Lines' highlighted.]({{ '/assets/images/tableau_beginner_005g.jpg' | relative_url }})

Hovering over the lines gives you statistical information, such as a p-values.

Finally, one interesting feature of Tableau is that you can create not just one visualization, but a series of them, using the **Pages** shelf. Drag **Year** onto the **Pages** shelf.

    ![Image highlighting the variable 'Year' in the Dimensions section and the Pages card. ]({{ '/assets/images/tableau_beginner_005h.JPG' | relative_url }})

Now you should see some "Year" controls on the right. The user can scroll through three different scatter plots, one for each year, or they can click on the play button to have it animate through the years. Your final graph should resemble the image below (depending on which "page" is currently visualized in Tableau).

<img src='{{ '/assets/images/TableauBeginnerUpdate-5.10.jpg' | relative_url }}' alt='' title='' width='1699' height='964' />

**Technique:** [Data Visualization](https://mdlutoronto.github.io/tutorials-search/?technique=Data+Visualization) \| **Tools:** [Tableau](https://mdlutoronto.github.io/tutorials-search/?tool=Tableau)