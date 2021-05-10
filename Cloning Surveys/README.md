# Clone survey content (Task)

A common question the Survey123 team has received from organization administrators is, "What's the best way to clone my surveys from one organization to another?"

There are two common use cases for cloning surveys:
1. Create a copy of a survey in another ArcGIS organization. For example, a city's transportation and water departments have different ArcGIS Online organizations and the water department would benefit from having a copy of one of the transportation department's surveys as well as its associated web map and dashboard.
2. Clone a survey from a development organization in ArcGIS Enterprise to staging and production organizations.

This sample Python notebook demonstrates how to clone surveys and associated content from one organization to another. This workflow can be used to clone surveys from ArcGIS Online to ArcGIS Online, ArcGIS Online to ArcGIS Enterprise, or ArcGIS Enterprise to ArcGIS Enterprise. The direction of cloning does not matter.

This notebook demonstrates two cloning methods:

- Clone related items
- Clone survey folder

**Python notebook** that demonstrates how to clone survey content between organizations.

### Requirements
- Python 3.6
- Python IDE (ArcGIS Notebooks, Jupyter Notebook, JupyterLab)
- [ArcGIS API for Python](https://developers.arcgis.com/python/) - this module interacts with your ArcGIS organization

### Usage

This notebook is intended to be used as a guide; you can take what's here and incorporate it into your own workflows, or run the notebook as is if desired. 

To run as is, update the following:

- Source and target GIS connections (code cell 1)
- Specify your own group ID (code cell 2)
- Specify your own save path for the `outpath` variable (code cell 3)
- Update the folder name and tags as desired (code cell 4)
- Update the survey that is obtained and used to clone all folder content (code cell 6)
