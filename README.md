# Form-to-Email

Send custom emails containing feedback collected via Google Forms to target audience in real time.
This code snippet is designed to automate the process of sending emails with data from a Google Sheets spreadsheet. It uses Google Apps Script, specifically the Spreadsheet service and Gmail service, to retrieve data from the spreadsheet and send an email with the extracted data.

# Prerequisites
To use this code, you need the following:

A Google Sheets spreadsheet with the data you want to retrieve and send via email.
Google Apps Script environment.

# Usage
Follow the steps below to use this code:

Open the Google Sheets spreadsheet that contains the data.

In the menu, click on "Extensions" and select "Apps Script."

In the Apps Script editor, replace the placeholders with your own values:

Replace Add your Email body (header) with the desired email body header.

Replace Add your target email address with the email address where you want to send the data.

Replace Subject in GmailApp.sendEmail(naEmail, 'Subject'+" "+rowData.fullName, '', { with the desired subject line for the email.

Customize the email body by modifying the HTML structure within the for loop.

Add your desired email body footer before htmlBody += '</ul><p> </p>'.

Save the script.

Run the onFormSubmit function manually or set up a trigger to automatically run it whenever a form submission is made in the spreadsheet.

# Explanation of the Code
The code consists of two main functions:

1. onFormSubmit(e)
This function is triggered when a form submission event occurs. It retrieves the active spreadsheet, selects the first sheet, and retrieves the submitted values. It then iterates over the values and creates an HTML string to construct the email body. After that, it retrieves additional data from the spreadsheet using the getRowsData function. Finally, it sends an email with the constructed email body using the Gmail service.

2. getRowsData(sheet, range, columnHeadersRowIndex)
This function retrieves the data from the specified sheet and range and returns an array of objects. Each object represents a row of data, with keys being the column headers and values being the corresponding data values.

# Important Note
The code includes a section at the end with a comment that says "DO NOT ALTER THE BELOW CODE AT ALL." This comment is a reminder not to modify the code below that point, as it is a reused code block from a different script.

Make sure to review the code and adjust it according to your specific requirements before running it.
