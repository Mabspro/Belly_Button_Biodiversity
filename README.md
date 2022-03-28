# Belly_Button_Biodiversity
Exploring Belly Button Biodiversity using a web-deployed Interactive Dashboard.

## Summary
The goal of this project was to create an interactive dashboard that allows the user to explore belly button biodiversity dataset, which catalogs the microbes that colonize human navels. 

The dataset reveals that a small handful of microbial species (also called operational taxonomic units, or OTUs, in the study) were present in more than 70% of people, while the rest were relatively rare.

## Tools Used:
D3, Plotly, Bootstrap

Link for interactive dashboard:

Dataset Link: 
http://robdunnlab.com/projects/belly-button-biodiversity/results-and-data/

## Results and Summary:
Drop down and Demographics panel: 
IDs were added to the “Test Subject ID” dropdown so that the user can select which ID they would like to look at. This way we can use that ID to parse out the information that we need from our data json file. The ID is then used to filter out the metadata pertaining to the selected ID and stored it in an object. D3 was then used to select the panel-body class in the index.html where a forEach statement was used to iterate through the object and append the data to the demographics panel.

Horizontal bar chart and Bubble Chart: 
The json data was filtered by the current ID that the user has would select. This then created a trace for the chart with the top 10 sample values as the x and the OTU IDs. Plotly was used to create the bar chart.

Gauge chart: 
The pie chart was created to have the gradient colors and labels from lowest to highest frequency washings per week. Then proceeded to create the needle by created several SVG paths that would draw the needle and that correlate with the washing frequency of a subject. At this point then created a function that would use a switch statement to select the correct path drawing for the needle depending on the number of washing frequency. 
