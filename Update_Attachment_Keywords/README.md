# Update attachment keywords in ArcGIS Enterprise (Task)

ArcGIS Survey123 uses attachment keywords to associate an attachment in a feature layer with its corresponding image, file, or audio question in a survey. Attachment keywords are supported for hosted feature layers in ArcGIS Online and ArcGIS Enterprise version 10.8.1 and later.

As noted in the <a href="https://community.esri.com/t5/arcgis-survey123-blog/understanding-survey123-feature-reports/ba-p/897659" target="_blank">Understanding Survey123 Feature Reports</a> blog post, attachments such as photos, signatures, and annotated images are not supported in reports when using ArcGIS Enterprise version 10.8 or earlier. This is because report templates rely on attachment keywords to place image questions in the report.

An issue you may run into when upgrading your ArcGIS Enterprise deployment to 10.8.1 or later is that attachments still do not print in reports. The reason for this is that even though the environment is upgraded, the upgrade process does not automatically associate attachments with Survey123 questions, nor does it automatically enable keywords in the attachment table. 

The goal of this **Python notebook** is to automate the workflow for updating attachment keywords after upgrading to ArcGIS Enterprise version 10.8.1 or later.

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
