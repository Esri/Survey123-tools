# Using the Survey Manager (Guide)

As a survey owner, you may want to work with your ArcGIS Survey123 surveys via the ArcGIS API for Python to automate certain tasks, modify your surveys, or work with your surveys' data. This notebook demonstrates the different workflows for connecting to your surveys using the ArcGIS API for Python.

The first way uses the form item's ID which is more precise and allows you to quickly get up and running with a specific survey. The second method shown performs a search against your content to identify form items. This method would be beneficial if you are looking to work with multiple surveys as a list. You can modify the search parameters to refine the list and only work with surveys that meet a specific criteria.

To work with a survey you must define a Survey Manager. The Survey Manager allows survey owners and administrators to analyze, report on, and access the data of multiple surveys.

**Python notebook** that demonstrates how to connect to your ArcGIS Survey123 surveys by using either the form's item ID or by searching for it in the organization.

### Requirements
- Python 3.6+
- Python IDE (ArcGIS Notebooks, Jupyter Notebook, JupyterLab)
- [ArcGIS API for Python](https://developers.arcgis.com/python/) - this module interacts with your ArcGIS organization

### Usage
- Enter your ArcGIS organization credentials in the GIS connection.
- Enter the item ID of a form item.
- Update the form owner to a user in your ArcGIS organization. 
