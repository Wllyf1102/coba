function doPost(e) {
  try {
    var sheet = SpreadsheetApp.getActiveSpreadsheet().getSheetByName("Sheet1");
    var data = JSON.parse(e.postData.contents);

    // Simpan data ke baris baru
    sheet.appendRow([
      data.nama || "",
      data.email || "",
      data.pesan || "",
      new Date()
    ]);

    return ContentService
      .createTextOutput(JSON.stringify({status: "success"}))
      .setMimeType(ContentService.MimeType.JSON);
  } catch(err) {
    return ContentService
      .createTextOutput(JSON.stringify({status: "error", message: err.toString()}))
      .setMimeType(ContentService.MimeType.JSON);
  }
}
