# Create reports using the ArcGIS API for Python (Guide)

ArcGIS Survey123 reports are an effective way to quickly visualize, interpret, and share survey responses. Reports use a template you can personalize, that's applied to your survey results and shared as either a Microsoft Word or PDF document.

There are several ways to create reports from your survey data. The most common method is through the Report panel on the Data tab for your survey on the Survey123 website. Here, you can manage report templates and generate reports in PDF and DOCX format.

You can also use a webhook to trigger a process to create and share reports that contain survey results. A webhook is useful if want the report to be triggered by an action. For example, each time a survey is submitted, a webhook can trigger the Create report module in Integromat to generate a report. For more information, see [Webhooks](https://doc.arcgis.com/en/survey123/browser/create-surveys/webhooks.htm).

Another approach is to run an automated reporting process at regular intervals. For example, you might want to produce a report for all surveys submitted in the past week, month, or quarter. This is where the ArcGIS Survey123 module in the ArcGIS API for Python can be useful: you can set up a script and run it periodically as a scheduled task.

This sample notebook demonstrates ways you can use the ArcGIS Survey123 module to work with reports and covers the following functionality:

- Identify report templates associated with a survey
- Generate a default report template
- Check template syntax
- Associate a report template with a survey
- Estimate credits
- Create sample report
- Generate a single report
- Generate a report as a PDF
- Generate multiple reports
- Generate multiple reports and save to your organization
- Generate a report with all possible parameters
- Update report template
- List saved reports

**Python Notebook** that demonstrates how to automate the process of generating reports.  

### Requirements
- Python 3.6+
- Python IDE (ArcGIS Online notebooks, Jupyter notebook, Notebook Server)
- [ArcGIS API for Python](https://developers.arcgis.com/python/) - this module interacts with your ArcGIS organization

### Usage
- Enter your ArcGIS organization credentials in the GIS connection.
- Enter the item ID of a Form item.
- Update the template index with the correct index of your template when generating reports.
