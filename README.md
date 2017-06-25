# Swift-PDF-Form-Fill-from-Numbers
Scripts to import Numbers data to PDF Fillable forms
# Disclaimer
Hey, I’m not the world’s best programmer by any measure. I am writing this project because I want to see this functionality, I know you can do better, please do. If you happen to see value in this or other Projects herein and would like to make them happen, please contact me.
# Known Issues
* Not for lack of trying, but I cannot find a way to set widget checkboxes, the current version only supports text based annotation widgets.  Per the WWDC2017 video on pdfkit, big changes are a coming.
* No user interface, yet
* Files annotated this way to not view properly in Safari, but do show correctly in Chrome.  Preview, Acrobat, etc also seem to display and print correctly.
 
#  Usage
* Create PDF Index, specify the PDF file, the script creates a duplicate in the same folder.  Each text based annotation field is updated with the index number of the annotation.  Use this index to link you Numbers table data to the field.

![](https://github.com/MauiDad/Swift-PDF-Form-Fill-from-Numbers/blob/master/Untitled.png)

* In Numbers, specify a column to the right  of the form data with the name “PDFLink”, format  this column as text, (or enter index numbers in the field as text.  Every table in the sheet is  scanned and the total results are used.
	* The form data can be in the adjacent left column to PDFLink, or several columns to the left.
	* The script skips blank cells in moving to the left.
	* Multiple indices on a single line are separated by commas. “12,13”
	* To skip a cell in Numbers, include a blank . “12,,13”

![](https://github.com/MauiDad/Swift-PDF-Form-Fill-from-Numbers/blob/master/Untitled%202.png)

# WorkFlow:
The workflow for this script will ultimately be:
* Open pdf using file manager, option to create index , or upload data
*  Upload form data to pdf in Preview.
* Create images of filled forms and paste in Numbers Sheet.
