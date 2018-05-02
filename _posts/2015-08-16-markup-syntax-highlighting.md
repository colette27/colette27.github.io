---
layout: post
title: "Java Spreadsheet User Guide & Manual "
excerpt: "This section documents the WorkSheetHandle of the API.
"
tags:
  - code
  - Java Spreadsheet
---

## Worksheet Functions

The WorkSheetHandle provides a handle to a worksheet within an XLS file, and includes convenience methods for working with the cell values within a sheet. The WorkSheetHandle allows access to a particular worksheet within your WorkBookHandle.

### Instantiating the WorksheetHandle

To gain access to the handle, use the getWorkSheet(String sheetName) method within the WorkBookHandle object:

```java
WorkBook mybook = new WorkBook();
WorkSheetHandle sheet = mybook.getWorkSheet(Sheet1);
```

You can get an array of handles to all of the worksheets in a workbook by using the getWorkSheets() method:

```java
WorkSheetHandle[] sheets = book.getWorkSheets();
```

This will return an array of handles to all of the worksheets in a workbook, giving flexibility to work with each one individually.

### Creating, Copying, and Deleting Worksheets

To create a new worksheet, use the createWorkSheet(String newSheet) method. This will insert a new worksheet and place it at the end of the workbook.

```java
createWorkSheet('mysheet');
WorkSheetHandle mysheet = new WorkSheet();
```

To delete any number of worksheets, use the remove method. To delete all worksheets in a workbook, use the removeAllWorkSheets() method.

```java
sheet.remove('mysheet');
sheet.removeAllWorkSheets('mybook');
```

To copy an existing worksheet to your workbook, use the copyWorkSheet(String SourceSheetName NewSheetName) method. This will duplicate a worksheet in the workbook and add it to the end of the workbook with a new name.

```java
WorkBook thisbook = new WorkBook(); WorkSheetHandle sheet = thisbook.getWorkSheet(sheet1);
createWorkSheet('newsheet');
copyWorkSheet('WorkSheet1', 'WorkSheet4');
```

### Editing Sheet Names

The setSheetName(String newName) method can be used to modify or rename your worksheet.
This method will change the name on the worksheet’s tab as well as all programmatic and internal references to that name.

```java
setSheetName('sheet1', 'Records');
```

### Getting, Setting and Reordering Tabs

Sheet tab names can be set and retrieved. To get the name of a worksheet, use the getSheetName() method.

```java
String sheetname = mysheet.getSheetName();
```

To set the tab name, use the WorkSheetHandle.setSheetName(String NewName) method.

```java
mysheet.setSheetName('CreditTracking');
```

Sheets can be selected so they appear as the first visible sheet when the output file is opened. You can also reorder sheets to your specifications. To select a worksheet and set it to the first visible tab in the workbook use the setFirstVisibleTab(int x) method.

```java
WorkSheetHandle WorkSheet4 = new WorkSheet();
setTabIndex('0', 'WorkSheet4');
```

To reorder the display of the worksheet tabs, use the setTabIndex(int idx) method. This is a zero-based index. Thus, the first tab you will see displayed in your WorkBook will be 0.

```java
setTabIndex('1','WorkSheet1');
```

### Protect and Unprotect Worksheets

Worksheet protection can be set or removed to control any modifications in the output file. To lock the values of a worksheet, you can set the worksheet to “protect,” by using the setProtected(boolean b) method

```java
mysheet.setProtected(true);
```

To unlock protected worksheets, use the setProtected(boolean b) method.

```java
mysheet.setProtected(false)
```
