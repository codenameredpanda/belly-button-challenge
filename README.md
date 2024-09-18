# belly-button-challenge

This assignment is meant to show skills using JavaScript and the d3 library. The data in this project originates from an article titled "A Jungle in There: Bacteria in Belly Buttons are Highly Diverse, but Predictable". The article analyses the bacteria in belly buttons. This project takes the data from this article and creates visualizations for the belly button bacteria of each subject examples were taken from.

# Files in this Repository

static
-js
--.gitkeep
--app
index
samples

# Resources:

Hulcr, J. et al. (2012) A Jungle in There: Bacteria in Belly Buttons are Highly Diverse, but Predictable. Retrieved from: http://robdunnlab.com/projects/belly-button-biodiversity/results-and-data/Links to an external site.

# Dependencies

JavaScript
Plotly
d3

# References

https://www.geeksforgeeks.org/how-to-iterate-over-a-javascript-object/
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/entries
https://plot.ly/javascript/bubble-charts/
https://plot.ly/javascript/bar-charts/

# Code

1. Setting up the data.
   a. The index HTML was already set up and imported all necessary libraries. There was an empy <div> for both the bar and bubble charts already created and the <h6> line of text was already set up.
   b. D3 was used to get the data, then the metadata variable was created to get the metadata.
   c. The metadata was filtered to the desired sample.
   d. The panel variable was created and the .html("") was used to clear metadata.
   e. A loop was created using information gathered from mozilla.org and geeksforgeeks.org. It utilizes Object.entries to iterate through the object and append the keys and values to the panel variable.
2. Building the charts
   a. A similar method is used to get data for the charts, however this time the otu_ids, otu_labels, and sample_values are assigned their own variables to be used when constructing the charts.
   b. The charts were created with help from plot.ly library. The previously assigned varables become:
   x: otu_ids,
   y: sample_values,
   text: otu_labels,
   in the buble chart. The layout was created with help from Plot.ly and titles assign based on assignment requirements.
   c. The bar chart is limited to the top ten, so the variables are sliced. In addition, in order for otu_ids to become a ytick on the bar graph, the .map function is used to convert the values to string.
   d. Each chart is rendered respectively.
3. Addining data to dropdown
   a. D3 is used again to get the data, then it is filtered to data.names.
   b. The .forEach function learned from mozilla and geeks for geeks iterates through each object and appends to the dropdown menu each sample subject.
   c. the firstSample variable is created to gather the data from above. It is then applied to the panel function and charts function created above.
   d. The final result is an interactive page with a buble chart and a bar chart. The dropdown menu can be used to examine the belly button bacteria of each subject in the dataset.
