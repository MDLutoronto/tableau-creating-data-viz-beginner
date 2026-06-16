---
title: "6. Creating a Simple Treemap"
parent: "Creating Data Visualizations Using Tableau (Beginner)"
layout: default
created_date: 2019-03-27
staff:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
maintainer:
    - name: Kelly Schultz
      link: https://library.utoronto.ca/staff/kelly-schultz
nav_order: 6
---

## 6. Creating a Simple Treemap

Go to the top **Data** Menu and select **New Data Source**. Select **Excel** and choose the *2016PopulationbyRegion.xls* file. This dataset lists population totals for various regions on earth.

Again, once you are happy with your data in the data source view, you can create a new worksheet to start building a new visualization by clicking on the **new worksheet icon** (to the right of Sheet 3 at the bottom left corner).

Treemaps help show hierarchical divisions of parts within a whole. To create a treemap in Tableau, first drag the **Region** variable onto the **Label (text)** box in the **Marks** card, as we’re going to separate and label each box with the Region name.

   ![Image highlighting the variable 'Region' in the Dimensions section as well as the Text box in the Marks card.]({{ '/assets/images/tableau_beginner_006c.JPG' | relative_url }})

Next drag the **Population** variable onto the **Size** box as we’re going to size these regions blocks by their population.

   ![Image highlighting the variable '2016Population' in the Measures section as well as the Size box in the Marks card.]({{ '/assets/images/tableau_beginner_006d.JPG' | relative_url }})

Finally, drag the **Continent** onto the **Color** box to colour code the blocks by continent.

   ![Image highlighting the variable 'Continent' in the Dimensions section as well as the Colour box in the Marks card.]({{ '/assets/images/tableau_beginner_006e.JPG' | relative_url }})

You can hover over the blocks to get more information on the populations, or you could label it as well. Drag the **Population** variable again over the **Label** box to include that information under the region name. You have completed a simple treemap!

   ![Image highlighting the variable ‘2016Population’ in the Measures section, the location of the Label box in the Marks card, and the resulting tree map with the new labels.]({{ '/assets/images/tableau_beginner_006b.JPG' | relative_url }})

**Technique:** [Data Visualization](https://mdlutoronto.github.io/tutorials-search/?technique=Data+Visualization) \| **Tools:** [Tableau](https://mdlutoronto.github.io/tutorials-search/?tool=Tableau)