# **belly-button-challenge**
This project is a dashboard that visualizes bacteria culture data from different human belly button samples. The dashboard consists of interactive charts that allow users to explore and analyze the distribution and abundance of various bacteria present in the samples.

## **Overview**
This JavaScript code builds a dynamic dashboard that visualizes microbiome data using D3.js and Plotly.js.

The dashboard has the following features:
- **Test Subject ID Selection**: Users can select a test subject ID from a dropdown menu.
- **Demographic Information**: Displays demographic information about the selected test subject.
- **Bar Chart**: Shows the top 10 operational taxonomic units (OTUs) found in the selected subject's belly button.
- **Bubble Chart**: Displays all OTUs found in the selected subject's belly button.

The dataset is fetched from a remote URL in JSON format.

## **Dependencies**
- **D3.js**: A JavaScript library for producing dynamic, interactive data visualizations in web browsers.
- **Plotly.js**: A graphing library that makes interactive, publication-quality graphs online.
- **JSON data**: The data is fetched from a provided URL in JSON format.

## **Files**
- **index.html**: The main HTML file that sets up the structure of the dashboard.
- **static/app.js**: Contains the JavaScript code for fetching data, building charts, and handling user interactions.
- **samples.json**: Reference data file hosted online that provides the sample data for the dashboard.

## **Logic (app.js)**
The page creates a drop-down box which can be used to observe information on any specific sample from the given dataset.

### **Metadata Panel**
- The metadata panel displays demographic information for the selected sample.
- It retrieves data from a JSON file and populates the panel with demographic information pairs representing various metadata fields.

### **Charts**
Two types of charts are used to visualize the data:
- **Bubble Chart**: Displays the abundance of bacteria cultures per sample.
- **Bar Chart**: Shows the top 10 most common bacteria cultures found in the selected sample.

### **Data Handling**
- The data for the dashboard is fetched from a remote JSON file hosted at a specified URL.
- The data is then filtered and processed to extract relevant information for the charts and metadata panel.

### **Functions**
- **buildMetadata(sample)**: Fetches and displays the metadata for the selected sample.
- **buildCharts(sample)**: Creates and updates the bubble and bar charts based on the selected sample.
- **init()**: Initializes the dashboard by populating the dropdown menu with sample names and displaying the default sample's data.
- **optionChanged(newSample)**: Event handler that updates the charts and metadata panel when a new sample is selected from the dropdown menu.
