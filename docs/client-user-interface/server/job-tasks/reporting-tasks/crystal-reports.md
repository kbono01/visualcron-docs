---
sidebar_label: 'Task Reporting - Crystal Reports'
hide_title: 'true'
---

## Task Reporting - Crystal Reports

The Crystal Reports Task allows you to output Crystal reports in various formats like PDF, Excel and to printer. With this Task you can specify in-parameters and record filter. The record filter can further narrow down the report query.
 
This Task uses the [Crystal Reports Connection](../../../server/connection-crystalreports). It requires runtime files to be installed on the Server. You can find this in the Connection.
 
**Crystal reports > Main settings** sub tab

![](../../../../../static/img/Client%20User%20Interface/Main%20Menu/Server/Jobs/Job%20Tasks/Tasks/Reporting%20Tasks/Reports%20settings.png)

**Report file**

The file path to the Crystal Reports report file (.rpt). Click the File icon to browse for the file.
 
**Source Credential**

If the report file is located on a network drive, select a Credential to access it.
 
**Connection details**

Select one or more Connections here depending on how many database connections your report uses. The following additional options are available:

* _Override default database in DSN_ - when checked, enables the text field below to specify a different database name to override the one defined in the DSN
* _Refresh report's data_ - when checked, forces the report to refresh its data from the database when running

**Destination type**

Select the output destination for the report:

* _File_ - exports the report to a file; the Printer tab is disabled
* _Printer_ - sends the report to a printer; the Printer tab is enabled
 
**Output format**

The file format to use when the destination type is _File_. Available formats:

* _No format_
* _Crystal report_
* _Rich text_
* _Word_
* _Excel_
* _PDF_
* _HTML 3.2_
* _HTML 4.0_
* _Excel record_
* _Text_
* _CSV_
* _Tab separated text_
* _Editable RTF_
* _XML_
* _RPTR_
* _Excel Workbook_

When _Text_, _Rich text_, or _Tab separated text_ is selected, the Export settings tab is enabled.

**Destination file**

The file path where the exported report will be saved. Required when the destination type is _File_.
 
**Destination Credential**

If the output file is on a network drive, select a Credential to access it.

**Required 32 bit runtime library / Required 64 bit runtime library**

Links to download the Crystal Reports runtime libraries required by the server.
 
**Crystal reports > Parameters** sub tab

![](../../../../../static/img/Client%20User%20Interface/Main%20Menu/Server/Jobs/Job%20Tasks/Tasks/Reporting%20Tasks/Parameters.png)

Your report might include required or optional parameters. If parameters are already defined you can click on "Import parameters". This will import and list your parameters. You can then edit any parameter by double clicking on it (or press Edit). Import parameters button require that you have setup your Connection settings in the Task before pressing - otherwise VisualCron will not be able to query for parameters.
 
**Crystal reports > Record filter** sub tab

![](../../../../../static/img/Client%20User%20Interface/Main%20Menu/Server/Jobs/Job%20Tasks/Tasks/Reporting%20Tasks/Record%20Filter.png)

The record filter allows you to choose from existing columns in the report and specify filters - similar like WHERE in a SQL query. This way you can filter the report.
 
You can manually write the query in the Record filter text box or click "Reload" to load all existing columns, choose a condition, write a value and then press Add.
 
**Crystal reports > Printer** sub tab

The Printer tab is only enabled when _Printer_ is selected as the destination type.

**Select printer**

Select the printer to use from the dropdown list of available printers.

**Page range**

Select which pages to print:

* _All pages_ - prints all pages of the report
* _Pages_ - prints the specified page range; enter a page number or range in the text field (e.g. 2-4)

**Number of copies**

The number of copies to print. Minimum is 1, maximum is 1000, default is 1.

**Collated**

When checked, multiple copies are printed in collated order.

**Orientation**

Select the print orientation:

* _Portrait_
* _Landscape_

**Crystal reports > Export settings** sub tab

The Export settings tab is only enabled when the output format is _Text_, _Rich text_, or _Tab separated text_.

**Characters per inch**

The number of characters per inch for the text export.

**Lines per page**

The number of lines per page for the text export.

**The Crystal Reports Connection**
 
### Troubleshooting
 
*Could not load file or assembly 'CrystalDecisions.ReportAppServer.DataDefModel, Version=13.0.3500.0*

Make sure you installed the Crystal Reports runtime 13.0.24.
