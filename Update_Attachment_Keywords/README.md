# Update attachment keywords (Task)

ArcGIS Survey123 uses attachment [keywords](https://doc.arcgis.com/en/survey123/desktop/create-surveys/xlsformmedia.htm#ESRI_SECTION1_4CD206A4C41D486D945716EB546AA856) to associate an attachment in a feature layer with its corresponding image, file, or audio question in a survey. Attachment keywords are supported for hosted feature layers in ArcGIS Online and ArcGIS Enterprise version 10.8.1 and later.

There are three main reasons you would need to update the keywords for your feature service attachments: 

1. You've exported your Survey123 data as a file geodatabase and want to use that data in Survey123 again
2. You've authored a feature class, enabled attachments, published as an ArcGIS Server feature service, and started collecting data in Survey123
3. You've upgraded your ArcGIS Enterprise organization from a pre-10.8.1 version to a post 10.8.1 version and want to update your existing data to now make use of keywords

**Python notebook** to update attachment keywords for existing attachments. 

### Requirements
- Python 3.6+
- Python IDE (ArcGIS Notebooks, Jupyter Notebook, JupyterLab)
- [ArcGIS API for Python](https://developers.arcgis.com/python/) - this module interacts with your ArcGIS organization

### Usage

**Script requires attachments to be named in one of the two following formats: `<attachmentKeyword>-<timestamp>` or `<attachmentKeyword>_<timestamp>`**

The following variables will need to be updated: 

* **feature_layer_id** - Item ID for the feature service associated with the survey.
* **portal_username** - Organization username.
* **portal_password** - Organization password.
* **portal_url** - The URL for your organization (e.g. www.arcgis.com for ArcGIS Online).
* **multiple_image_questions** - Does your survey have multiple image questions? Accepts `yes` or `no`. `yes` means that your survey contains multiple image questions; `no` means that your survey contains only one image question (this question can use use multiline appearance).
* **attachment_keyword** - Only relevant if there is one image question in your survey. The script will prompt for the keyword, otherwise the script will extract the attachment keyword from the photo name if there are multiple image questions. For more information on how to identify the correct attachment keyword(s) for your survey, see the <a href="https://support.esri.com/en/technical-article/000024606" target="_blank">How To: Update the attachment keywords for existing ArcGIS Survey123 data</a> Knowledge Base article.
