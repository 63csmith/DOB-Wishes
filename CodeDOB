// Function to send Birthday emails to clients

function birthdayWishes() {
  var spreadsheet = SpreadsheetApp.getActiveSpreadsheet();
  SpreadsheetApp.setActiveSheet(spreadsheet.getSheets()[0]);
  var sheet = spreadsheet.getActiveSheet();
 
  var lastRow = sheet.getLastRow();
  var startRow = 3;

  var templ = HtmlService
    .createTemplateFromFile('Birthday Email');

  var message = templ.evaluate().getContent();
 
  for (var i =startRow ; i <= lastRow; i++) {
    if(sheet.getRange(i, 4).getValue()==true) {
       MailApp.sendEmail({
         to: sheet.getRange(i, 3).getValue(),
         subject: "Happy Birthday!!!",
         htmlBody: message
       });
    }
  } 
  
}
