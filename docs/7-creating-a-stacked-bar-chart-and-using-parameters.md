---
title: "7. Creating a Stacked Bar Chart and Using Parameters"
parent: "Creating Data Visualizations Using Tableau (Beginner)"
layout: default
created_date: 2019-03-27
staff:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
maintainer:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
nav_order: 7
---

## 7. Creating a Stacked Bar Chart and Using Parameters

Go to the top **Data** Menu and select **New Data Source**. Select **Excel** and choose the *RomeoAndJulietWordFrequenciesByAct.xls* file. This dataset lists word frequencies in Romeo and Juliet by Act (the play is subdivided into 5 acts/parts).

Again, I can start building a new visualization by clicking on the **new worksheet icon**.

Hold down the **CTRL** button on your keyboard (Command on a Mac) and click on the **Term** variable and the **Count** variable, then click on the **Show Me** tab to expand it. I see that a horizontal bar graph is one of the recommendations (i.e., outlined) – select it. Your graph should resemble the image below.

   ![Image displaying the Term variable in the Dimensions section and the Count variable in the Measures section highlighted as well as the horizontal bar graph option highlighted in the ‘Show Me’ menu.  ]({{ '/assets/images/tableau_beginner_007a.JPG' | relative_url }})

Now let’s filter it so we only see the top 10 words mentioned. Drag the **Term** variable to the **Filters** shelf. Go to the **Top** tab, and select **By Field**. By default it is going to use the Count variable and sum up the instances to get the top 10. Click **OK**.

   ![The Filter pop-up window is displayed, with the "By field" section and "OK" button highlighted.]({{ '/assets/images/ZZ.JPG' | relative_url }})

Now you will have your top 10 terms, listed in alphabetical order by term. It might be nicer to sort them by count. We can do this by right clicking on the **Term** pill in the **Rows** section and select **Sort**. 

   ![Right clicking on the Term pill in the Rows section and highlighting Sort in the menu]({{ '/assets/images/ZZa.png' | relative_url }})

In the **Sort By** section, select **Field.** Under Sort Order, select **Descending.** Leave the rest of the defaults selected, as these will give us the sum of count. You'll notice there is no "OK" or "Apply" option. Changes are applied automatically, so simply click the **X** in the top right of the **Sort** window.

   ![Image of the Sort pop-up window with "Descending" selected]({{ '/assets/images/zzzx.JPG' | relative_url }})

Result:

   ![The resulting bar graph is displayed; it has fewer terms in it than the previously.]({{ '/assets/images/AHH.JPG' | relative_url }})

Now suppose I’d like to add information about the Act to make a colour-coded stacked bar chart. You will notice that when we look at what variable types Tableau has identified, it thinks the **Act** variable is a numeric variable in the measures section (meaning you could do math with it), when really it is categorical in this case. Let’s fix it by moving it to our dimensions section. *First,* drag the **Act** variable into the **Dimensions** section.

Now it is a category, so it makes sense to visualize it through colour*. Second,* drag the **Act** variable onto the **Color** box in the **Marks** card. Looking better, but the Acts seem to be showing from Act 5 to Act 1. We can fix that by right-clicking on the **Act** pill and *third* selecting **Sort**. Select **Descending** and then click the **X**.

   ![The screen is pictured with the numbers 1 through 3, corresponding to the instructions above.]({{ '/assets/images/tableau_beginner_007b.JPG' | relative_url }})

So now we have our top 10 terms, subdivided by Act; however, what if our audience would rather just see the top 5 terms, or would like to expand it out to the top 20 or 30 terms. We can get an audience’s input into our visualizations using parameters. Right click on **Term** in the **Filters** shelf, and select **Edit Filter...** Go to the **Top** tab and click on the drop-down arrow next to where 10 is specified. Select **Create a New Parameter...** Give it a name, such as **Top Number**. Go down to the **Range of Values** section. Set the minimum to **5,** the maximum to **30**, and the **step size** to **5**. Then click on **OK**, and click **OK** again on the **Filter** window.

   ![Image showing all the steps described above highlighted on the screen.]({{ '/assets/images/tableau_beginner_007c.JPG' | relative_url }})

Your **Top Number parameter** should show up on the left side, under your variables, at the bottom. Right click on it, and select **Show Parameter**.

   ![Image showing right clicking on the parameter and selecting Show Parameter.]({{ '/assets/images/tableau_beginner_007cc.png' | relative_url }})

Your final product should resemble the image below. Your audience can use the control on the right to adjust how many terms to see in their top terms list.

   ![Image showing the final product of step number 7, with the Act parameter controls to the right of the Sheet.]({{ '/assets/images/tableau_beginner_007d.JPG' | relative_url }})

**Technique:** [Data Visualization](https://mdlutoronto.github.io/tutorials-search/?technique=Data+Visualization) \| **Tools:** [Tableau](https://mdlutoronto.github.io/tutorials-search/?tool=Tableau)