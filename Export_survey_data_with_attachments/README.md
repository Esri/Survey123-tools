# Export survey data with attachments (Task)

A common ArcGIS Survey123 workflow is to export survey data as a `.xlsx` file and work with that data in other software. A limitation of exporting data from your ArcGIS organization in Microsoft Excel format is that the attachments are not included.

Fortunately, you can use the ArcGIS API for Python to export your survey data in XLSX format and save any attachments to your computer.

**Python notebook** that exports your survey data as an Excel workbook to a local folder and downloads the related attachments to the same location.

### Requirements
- Python 3.6
- Python IDE (ArcGIS Notebooks, Jupyter Notebook, JupyterLab)
- [ArcGIS API for Python](https://developers.arcgis.com/python/) - this module interacts with your ArcGIS organization

### Usage

The following variables will need to be updated:
- **portalURL** - The URL for your ArcGIS organization (e.g. www.arcgis.com)
- **username** - Your ArcGIS organization username (e.g. gisadmin)
- **password** - You ArcGIS organization password (e.g. gisadmin1)
- **survey_item_id** - The item ID for the ArcGIS Survey123 form item in your ArcGIS organization (e.g. 89bc8c7844e548e09baa3aad4695e78b)
- **save_path** - The directory where you would like to save the survey results and attachments (e.g. C:\temp)
- **keep_org_item** - By default, an exported item is added to your content in your ArcGIS organization. This Boolean value allows you to choose if you would like to keep the exported item in your content (`True`), or remove it (`False`).
- **store_csv_w_attachments** - Boolean value that allows you to choose if the `.csv` file that maps each attachment to its parent object ID should be stored in the root folder (with the exported Excel workbook) (`False`), or in each individual layer folder (`True`).
