# Update CSV item in ArcGIS (Sample)

ArcGIS Survey123 utilizes CSV data in several workflows, including external choice lists, the search() appearance, and pulldata() calculations. When you need to periodically update the CSV content used in a survey, a useful method is to upload the CSV files to your ArcGIS organization and link the CSV items to your survey. Once linked, any updates to the CSV items will automatically pull through to your survey without the need to republish the survey. To learn more about linking items to a survey, see <a href="https://doc.arcgis.com/en/survey123/desktop/create-surveys/publishsurvey.htm#ESRI_SECTION1_90818E24DF84492CBA5A35D5F0CC3AAE" target="_blank">Linked content</a>.

This notebook demonstrates how to automate updating a CSV item in your ArcGIS organization.

**Note:** It is recommended to run this notebook on your computer in Jupyter Notebook or ArcGIS Pro, as that will provide the best experience when reading locally stored CSV files. If you intend to schedule this notebook in ArcGIS Online or ArcGIS Notebook Server, additional configuration may be required to read CSV files from online file storage, such as Microsoft OneDrive or Google Drive.

### Requirements
- Python 3.6+
- Python IDE (ArcGIS Notebooks, Jupyter Notebook, JupyterLab)
- [ArcGIS API for Python](https://developers.arcgis.com/python/) - this module interacts with your ArcGIS organization

### Usage
- Specify the directory path and file name for each CSV file stored locally.
- Specify the credentials for the ArcGIS account that owns the CSV items in your ArcGIS organization.
