# Swift-PDF-Form-Fill-from-Numbers
Scripts to import Numbers data to PDF Fillable forms
# Disclaimer
Hey, I’m not the world’s best programmer by any measure. I am writing this project because I want to see this functionality, I know you can do better, please do. If you happen to see value in this or other Projects herein and would like to make them happen, please contact me.  Some of the stuff I programmed was hard to find how to do using a web search, maybe this makes it easier for some.
# Known Issues
* none at this time
* tested on 2016 Form 1040, from IRS.gov
 
#  Usage
This is a Script written in Swift 4.0 and High Sierra (10.13), using Apples new PDFKit, and the Scripting Bridge to access iWork Numbers.  The Script has 2 functions.

* Create an indexed pdf for fillable forms, such as IRS.gov tax forms.  The indexed form lets you map the fillable form fields to your Numbers spreadsheet.
* Upload values from a Numbers spreadsheet and enter them onto the pdf forms as Text and Check Boxes.  Open the filled form in Preview.  Save each page of the filled form as a "Save as PDF" file from Preview (These files are "flattened and no longer fillable".  Import the images of the pdf pages into the Numbers sheet. 

* An example of the PDF Index is:

![](https://github.com/MauiDad/Swift-PDF-Form-Fill-from-Numbers/blob/master/Untitled.png)

* In Numbers, specify a column to the right  of the form data with the name “PDFLink”, format  this column as text, (or enter index numbers in the field as text.  Every table in the sheet is scanned for "PDFLink" and the result from all tables are used.
	* The form data can be in the adjacent left column to PDFLink, or several columns to the left.
	* The script skips blank cells in moving to the left.
	* Multiple indices on a single line are separated by commas. “12,13”
	* To skip a cell in Numbers, include a blank . “12,,13”
	* The formatted value in Numbers, including custom formats, are imported.
	* A checkbox may use the Numbers CheckBox format, a formula evaluating to true/false, or any of the values: "true", 1, or -1 

![](https://github.com/MauiDad/Swift-PDF-Form-Fill-from-Numbers/blob/master/Untitled%202.png)

# Code Samples:
Sample code you might be interested in:
* Printing a PDF as a PDF (flatten) - can be easily changed to print.
* Get text values from Numbers as an array of arrays [[String]].
* Check the format of a cell or range.
* Create and delete Objects (Images) in Numbers
* Script through all tables on a sheet, also Images.  
* Look for a named range in a table.
* Create images of filled forms and paste in Numbers Sheet.
* Setting values for text widgets, checking boxes for btn widgets using PDFKit
* Save a PDF document
* rename files, check if files exist
