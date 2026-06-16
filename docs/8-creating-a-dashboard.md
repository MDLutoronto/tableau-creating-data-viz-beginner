---
title: 8.  Creating a Dashboard
parent: Creating Data Visualizations Using Tableau Desktop (Beginner)
layout: default
created_date: 2019-03-27
staff:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
maintainer:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
nav_order: 8
---

## 8.  Creating a Dashboard

Now so far we’ve been creating visualizations within worksheets. But you can also create dashboards that combine a number of worksheets together. We are now going to create a dashboard capable of displaying the average monthly rainfall and temperature for one country at a time. Let’s click on the **create new dashboard** icon at the bottom, next to the **new worksheet** icon.

    ![Image showing the New Dashboard button, consisting of four small squares]({{ '/assets/images/addingsheets_tabs%20-%20Copy.PNG' | relative_url }})

You then can drag and drop various sheets to layout a dashboard. You can also drag other objects, such as text or images to create your dashboard. 

    ![Image showing sheets and objects highlighted.]({{ '/assets/images/Dashboard_step2.png' | relative_url }})

We can also adjust the size of our dashboard. Under **Size**, select its drop-down menu. Then select the drop-down menu next to Range and change it to **Automatic**, so that the dashboard will re-adjust its size to fit the screen it is viewed on.

    ![Image showing Sheet 1 highlighted at the bottom as well as the annotation and the Remove option.]({{ '/assets/images/Dashboard_step2a.png' | relative_url }})

Before we drag a sheet onto the dashboard, let's also make some adjustments to our Sheet 1. Click on **Sheet 1** at the bottom to go back to your original bar graph. Right click on the **Monsoon Season annotation** and select **Remove** to clean up our visual.

    ![Image showing Sheet 1 highlighted at the bottom as well as the annotation and the Remove option.]({{ '/assets/images/Dashboard_step3.png' | relative_url }})

**Adjust the title**, removing the mention of a particular country. Drag the **Country** pill on the Filters shelf, set to India, back towards the **Dimensions** and **Measures** section to remove it (which you can do with any variables you want to remove from your visualization).

Then go back to the dashboard by clicking on **Dashboard 1** at the bottom. From the left side of your screen, drag **Sheet 1** to the dashboard area.

    ![Image showing Sheet 1 highlighted in the Sidebar as well as the result of dragging the sheet to the dashboard area.]({{ '/assets/images/tableau_beginner_008a.png' | relative_url }})

Next drag **Sheet 2** to the bottom of the dashboard area. As you are dragging each sheet, Tableau will shade in the section of the page the sheet will occupy once you release it, so use this as your guide to the placement of your sheets in the dashboard.

    ![Image showing Sheet 2 highlighted in the Sidebar as well as the bottom of the dashboard area highlighted, where Sheet 2 has been dragged. ]({{ '/assets/images/tableau_beginner_008b.png' | relative_url }})

We can also take the filters we had for one worksheet, in this case the temperature graph, and then apply it to the all the sheets on the dashboard. Right click on the title of the filter, **Country**, select **Apply to Worksheets**, and then pick **All Using Related Data Sources**.

    ![Image displaying a dropdown menu emerging from the Country filter title. In the master dropdown menu ‘Apply to Worksheets' is selected. From this selection a sub-drop down menu is shown with the option ‘All Using Related Data Sources’ highlighted.]({{ '/assets/images/tableau_beginner_008c.jpg' | relative_url }})

Right-click again on the **Country** filter title, but this time select **Single Value (list**). This will make sure that your audience can only view one country at the time. Now you’ll see that when you select one country, both graphs refer to that country.

    ![Image displaying a dropdown menu emerging from the Country filter title. In the dropdown menu ‘Single Value (list)' is selected. ]({{ '/assets/images/tableau_beginner_008d.jpg' | relative_url }})

Now you're done your first dashboard!    

**Technique:** [Data Visualization](https://mdlutoronto.github.io/tutorials-search/?technique=Data+Visualization) \| **Tools:** [Tableau](https://mdlutoronto.github.io/tutorials-search/?tool=Tableau)