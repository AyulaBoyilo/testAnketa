# testAnketa
Test anketa Google Sheets Apps Script

Test Google Sheet: https://docs.google.com/spreadsheets/d/1wLvGwtzr4QLA6yGP_K45NkPP4G3vEVl0ePYcwZyuZFI/edit?usp=sharing

Apps Script:
function doPost(e) {
  
  const body = e.postData.contents;
  const bodyJSON = JSON.parse(body);
  const ss = SpreadsheetApp.getActiveSpreadsheet();
  const ws = ss.getSheetByName('anketa_test');
  ws.appendRow([bodyJSON.email, bodyJSON.spol, bodyJSON.godine, bodyJSON.regija, bodyJSON.broj_cipela, bodyJSON.poruka, bodyJSON.pravila]);
  
}
