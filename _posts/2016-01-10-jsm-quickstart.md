---
layout: post
title: "Quick Start Guide"
excerpt: "A Simple quick start guide "
tags:
  - Quickstart
  - readability
  - Java API


---

This project was for a Java spreadsheet tools company.


## ExtenXLS Quickstart Guide

ExtenXLS is a Java spreadsheet library designed for developers familiar with the Java syntax, spreadsheet programs, and the concept of file templates. This guide is intended to get you started quickly programming with ExtenXLS.

### Basic use of the API requires the following steps:

1. Copy ExtenXLS.jar and extenxls.lic to a project directory. Make sure that the jar is in the classpath of your project. The ExtenXLS.jar file  needs to be on your classpath in order for the JVM to find the ExtenXLS class files.
2. In your Java code, import the com.extentech.ExtenXLS package.
3. Create a new WorkBookHandle, this can be a new, empty workbook with three sheets, or you can parse an existing XLS file in the form of a byte array or from another data source.

````
Note: Review the WorkBookHandle constructors in the API documentation

      to see which WorkBookHandle is appropriate for your application.
````
4. Start working with a worksheet by using the `WorkBookHandle.getWorkSheet(String sheetname)` method.
5. Make sure to catch the `WorkSheetNotFoundException` in case the expected sheet does not already exist in the file.
6. Access the cell values using the `WorkSheetHandle.getCell(Sheetname:CellAddress)` method
7. Add new cells to the spreadsheet with the `CellHandle WorkSheetHandle.add(Object ob, String address)` method.
8. Set and get the value of cells by using the `CellHandle.setCellVal(Object ob)` and object `CellHandle.getCellVal()` methods.
9. Finally, stream the WorkBook bytes to an output file using the `WorkBookHandle.getBytes()` method. If you are writing to a web application, you can send the bytes over a ServletResponse to a browser, write out to a file, or to any byte array consumer.
