---
layout: post
title: "Quick Start Guide"
excerpt: "A Simple quick start guide "
tags:
  - sample post
  - readability
  - test
---

This project was for a Java middleware company.


## ExtenXLS Quick Start Guide

ExtenXLS is a Java spreadsheet library designed for developers familiar with the Java syntax, spreadsheet programs, and the concept of file templates. This Guide is intended to get you started quickly programming with ExtenXLS.

### Basic use of the API requires the following steps:

* Copy ExtenXLS.jar and extenxls.lic to a project directory. Make sure that the jar is in the classpath of your project. The ExtenXLS.jar file  needs to be on your classpath in order for the JVM to find the ExtenXLS class files.
* In your Java code, import the com.extentech.ExtenXLS package.
* Create a new WorkBookHandle, this can be a new, empty workbook with three sheets, or you can parse an existing XLS file in the form of a byte array or from another data source. Review the WorkBookHandle constructors in the API documentation to see which WorkBookHandle is appropriate for your application.
* Start working with a worksheet by using the WorkBookHandle.getWorkSheet(String sheetname) method.
* Make sure to catch the WorkSheetNotFoundException in case the expected sheet does not already exist in the file.
* Access the cell values using the WorkSheetHandle.getCell(Sheetname:CellAddress) method
* Add new cells to the spreadsheet with the CellHandle WorkSheetHandle.add(Object ob, String address) method.
* Set and get the value of cells by using the CellHandle.setCellVal(Object ob) and object CellHandle.getCellVal() methods.
* Finally, stream the WorkBook bytes to an output file using the WorkBookHandle.getBytes() method. If you are writing to a web application, you can send the bytes over a ServletResponse to a browser, write out to a file, or to any byte array consumer.


> Whatever velit occaecat quis deserunt gastropub, leggings elit tousled roof party 3 wolf moon kogi pug blue bottle ea. Fashion axe shabby chic Austin quinoa pickled laborum bitters next level, disrupt deep v accusamus non fingerstache.

Tote bag asymmetrical elit sunt. Occaecat authentic Marfa, hella McSweeney's next level irure veniam master cleanse. Sed hoodie letterpress artisan wolf leggings, 3 wolf moon commodo ullamco. Anim occupy ea labore Terry Richardson. Tofu ex master cleanse in whatever pitchfork banh mi, occupy fugiat fanny pack Austin authentic. Magna fugiat 3 wolf moon, labore McSweeney's sustainable vero consectetur. Gluten-free disrupt enim, aesthetic fugiat jean shorts trust fund keffiyeh magna try-hard.

## Hoodie Duis

Actually salvia consectetur, hoodie duis lomo YOLO sunt sriracha. Aute pop-up brunch farm-to-table odio, salvia irure occaecat. Sriracha small batch literally skateboard. Echo Park nihil hoodie, aliquip forage artisan laboris. Trust fund reprehenderit nulla locavore. Stumptown raw denim kitsch, keffiyeh nulla twee dreamcatcher fanny pack ullamco 90's pop-up est culpa farm-to-table. Selfies 8-bit do pug odio.

### Thundercats Ho!

Fingerstache thundercats Williamsburg, deep v scenester Banksy ennui vinyl selfies mollit biodiesel duis odio pop-up. Banksy 3 wolf moon try-hard, sapiente enim stumptown deep v ad letterpress. Squid beard brunch, exercitation raw denim yr sint direct trade. Raw denim narwhal id, flannel DIY McSweeney's seitan. Letterpress artisan bespoke accusamus, meggings laboris consequat Truffaut qui in seitan. Sustainable cornhole Schlitz, twee Cosby sweater banh mi deep v forage letterpress flannel whatever keffiyeh. Sartorial cred irure, semiotics ethical sed blue bottle nihil letterpress.

Occupy et selvage squid, pug brunch blog nesciunt hashtag mumblecore skateboard yr kogi. Ugh small batch swag four loko. Fap post-ironic qui tote bag farm-to-table american apparel scenester keffiyeh vero, swag non pour-over gentrify authentic pitchfork. Schlitz scenester lo-fi voluptate, tote bag irony bicycle rights pariatur vero Vice freegan wayfarers exercitation nisi shoreditch. Chambray tofu vero sed. Street art swag literally leggings, Cosby sweater mixtape PBR lomo Banksy non in pitchfork ennui McSweeney's selfies. Odd Future Banksy non authentic.

Aliquip enim artisan dolor post-ironic. Pug tote bag Marfa, deserunt pour-over Portland wolf eu odio intelligentsia american apparel ugh ea. Sunt viral et, 3 wolf moon gastropub pug id. Id fashion axe est typewriter, mlkshk Portland art party aute brunch. Sint pork belly Cosby sweater, deep v mumblecore kitsch american apparel. Try-hard direct trade tumblr sint skateboard. Adipisicing bitters excepteur biodiesel, pickled gastropub aute veniam.
