# Create reports using the ArcGIS API for Python (Guide)

ArcGIS Survey123 reports are an effective way to quickly visualize, interpret, and share survey responses. Reports use a template you can personalize, that's applied to your survey results and shared as either a Microsoft Word or PDF document.

It's common to deploy a [webhook](https://doc.arcgis.com/en/survey123/browser/create-surveys/webhooks.htm) as an automated process to create and share reports with survey results. Although, using a third party webhook provider may not be a feasible workflow due to organizational or security policies. This is where the ArcGIS Survey123 module in the ArcGIS API for Python can be used to acheive a similar goal.

This sample notebook demonstrates the following functionality:

- Generate a default report template
- Identify report templates associated with a survey
- Generate a single report
- Generate multiple reports
- Generate multiple reports and save to your organization
- List saved reports 

**Python notebook** that demonstrates how to automate the process of generating reports.  

### Requirements
- Python 3.6+
- Python IDE (ArcGIS Notebooks, Jupyter Notebook, JupyterLab)
- [ArcGIS API for Python](https://developers.arcgis.com/python/) - this module interacts with your ArcGIS organization

### Usage
- Enter your ArcGIS organization credentials in the GIS connection.
- Enter the item ID of a form item.
- Update the template index with the correct index of your template when generating reports.
