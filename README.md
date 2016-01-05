# GS3
A quick Google app script to add an export facility from Google Sheets to an Amazon Web Services S3 bucket. 

The script turns a Google spreadsheet into JSON data and exports it to a bucket in your S3 account using a [library](https://script.google.com/a/dallasnews.com/d/1Qx-smYQLJ2B6ae7Pncbf_8QdFaNm0f-br4pbDg0DXsJ9mZJPdFcIEkw_/edit?usp=drive_web) built by [Erik Schultink](http://engetc.com/projects/amazon-s3-api-binding-for-google-apps-script/). 


#Here's how to use it:

1. On a spreadsheet, go to "Tools" and select "Script editor..."
2. In the new window, save your script as whatever name.
3. Click "Resources" and select "Libraries..."
4. Enter the following library code for Schultink's S3 binding in "Find a Library" and click "Select".
  - MB4837UymyETXyn8cv3fNXZc9ncYTrHL9
5. Select the most recent version from the dropdown for the S3 library and click "Save".
6. Paste the gs3.gs code into you script window, replace the AccessKey and SecretKey placeholders with you AWS credentials and save, and set the "year" variable to the current year.
7. You may edit the `s3.putObject(...);` statement to customize the directory you will write your spreadsheet to.
8. Refresh your spreadsheet and the "Publish Data" button should appear.
9. Export your data (may have to authorize the app) and a dialog box will appear with the address where you can retrieve your JSON.


### Important:
- Make sure to freeze your first row with column headers. (Highlight the row, select VIEW > FREEZE > 1 ROW.)
- Name your spreadsheet something unique with no spaces or special characters and beginning with a lowercase letter.
