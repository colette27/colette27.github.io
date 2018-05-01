---
layout: post
title: "ExtenXLS Working With Charts"
excerpt: "Examples and code for displaying images in posts."
image: "http://farm9.staticflickr.com/8426/7758832526_cc8f681e48_c.jpg"
tags:
  - Spreadsheet
  - charts
  - test
---

## Working With Charts

With ChartHandle, you can add cells to a chart, change a chart’s title, axis labels, and copy charts between other worksheets and workbooks.

Begin by retrieving a ChartHandle from an existing chart in a worksheet. To retrieve a ChartHandle, use the ChartHandle WorkSheetHandle.getChart(String chartname) method.

```java
try{        ChartHandle performancechart = mysheet.getChart('Performance');
}catch(ChartNotFoundException e){        
  // oops!
};
```

With a ChartHandle, you can add cells to the chart using the ChartHandle.changeSeriesRange(String originalrange, String newrange) method.

```java
if(performancechart.changeSeriesRange('Sheet1!C23:E23', 'Sheet1!C23:G23')){
System.out.println('Successfully Added Columns F and G to Series Range');
}
```

To change the chart title, use the Charthandle.setTitle(String title) method.

```java
performancechart.setChartTitle('Athletic Performance Results');
```

To change the axis labels, or other text labels in the chart use the ChartHandle.changeTextValue(String originaltext, String newtext) method.

```java
if(ct.changeTextValue('50 Meter Dash Times", "High Jump    Distance')){
System.out.println('Successfully Changed Categories Label');
}
```

To copy a chart into another sheet or workbook, use

```java
book.copyChartToSheet("New Chart Title", "Sheet3");
```
