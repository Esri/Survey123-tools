# Update Form Resources (Task)

The media folder for a survey contains items used in various ArcGIS Survey123 questions and workflows. A survey's media folder can contain the following:
- Offline basemaps for use in the ArcGIS Survey123 field app.
- CSV files for use in `pulldata()` functions or for use as choice lists.
- Image and audio files for use in various question types.

This notebook demonstrates how you can automate the task of updating the contents of the media folder for a published survey without having to republish it in Survey123 Connect. This is useful when the items in the media folder need to be updated regularly. 

**Python notebook** that automates the task of updating content in the media folder of a published survey.

### Requirements
- Python 3.6+
- Python IDE (ArcGIS Notebooks, Jupyter Notebook, JupyterLab)
- [ArcGIS API for Python](https://developers.arcgis.com/python/) - this module interacts with your ArcGIS organization

### Usage

The following variables will need to be updated: 

- portalURL - The URL for your ArcGIS organization (e.g. www.arcgis.com)
- username - Your ArcGIS organization username (e.g. gisadmin)
- password - You ArcGIS organization password (e.g. gisadmin1)
- itemID - The item ID for the ArcGIS Survey123 form item in your ArcGIS organization (e.g. 89bc8c7844e548e09baa3aad4695e78b)
- updated_files - The updated file name containing the extension (e.g. myphoto.png)
- source_loc - Folder directory where the updated file is located (e.g. C:/Users/username/ArcGIS/My Survey Designs/...)
