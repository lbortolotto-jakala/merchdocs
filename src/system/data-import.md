---
title: Import
redirect_from: 
  - /system/data-import-troubleshooting.html
---

Data for all product types can be imported into the store. In addition, you can import products, advanced pricing data, customer data, customer address data, and product images. Import supports the following operations:

- Add/Update
- Replace
- Delete

The size of the import file is determined by the settings in the `php.ini` file on the server. The system message on the _Import_ page indicates the current size limit. The default size is 2MB.

Special characters—such as the equal sign, greater and less than symbols, single and double quotes, backslash, pipe, and ampersand symbols—can cause problems during data transfer. To ensure that such special characters are correctly interpreted, they can be marked as an “escape sequence.” For example, if the data includes a string of text such as code=”str”, code=”str2”, choosing to enclose the text in double quotes ensures that the original double quotes are understood to be part of the data. When the system encounters a double set of double quotes, it understands that the outer set of double quotes is enclosing the actual data.

When importing product data, new product data is added to existing product data entries in the database. All fields except SKU can be updated through import. All existing product data is replaced with the imported new data. Exercise caution when replacing data. All existing product data will be completely cleared and all references in the system will be lost.

![]({% link images/images/system-import.png %}){: .zoom} 
_Import_

## Step 1: Prepare the Data

1. On the _Admin_ sidebar, click **System**.

1. Under _Data Transfer_, choose **Import**.

1. Under _Import Settings_, set **Entity Type** to one of the following:

    - Advanced Pricing
    - Products
    - Customers and Addresses
    - Customers Main File
    - Customer Addresses

1. Click **Download Sample File**. Then on the download menu in the lower-left corner of your browser window, choose **Open**.

    ![]({% link images/images/data-import-download-sample-file.png %}){: .zoom}
    _Download Sample File_

    The sample file includes column headings with placeholder data for example product types.

    ![]({% link images/images/data-export-sample-data.png %}){: .zoom}
    _Downloaded Sample File_

1. Examine the structure of the sample file. As you prepare your CSV import file, make sure that the column headings are spelled correctly.

1. Verify that the size of your import file does not exceed the limit shown in the message.

    ![]({% link images/images/data-import-size-notification.png %}){: .zoom}

1. If the import data includes paths to product images, make sure that the image files have been uploaded to the appropriate location. The default location on the Magento server is: `pub/media/import`.

    If the images reside on an external server, make sure that you have the full URL to the directory that contains the images.

## Step 2: Choose the Import Behavior

1. Set **Import Behavior** to one of the following:

    * Add/Update—(For products, you can update all fields except SKU through import.)
    * Replace
    * Delete

1. To determine what happens when an error is encountered when importing data, choose one of the following:

    * Stop on Error
    * Skip error entries

1. Then in the **Allowed Errors Count** field, enter the number of errors that can occur before the import is canceled. The default value is 10.

1. Do the following:

    - Accept the default value of a comma (,) for the **Field separator**.

    - Accept the default value of a comma (,) for the **Multiple value separator**.

        In a CSV file, a comma is the default separator. To use a different character, make sure that the data in the CSV file matches the character that you specify.

    - If you want to enclose any special characters that might be found in the data as an “escape sequence,” mark the **Fields Enclosure** checkbox.

    ![]({% link images/images/data-import-import-behavior.png %}){: .zoom} 
    _Import Behavior_

## Step 3: Identify the Import File

1. Click **Choose File** to select the file to import.

1. Find the CSV file that you prepared to import, and click **Open**.

1. In the **Images File Directory** field, enter the relative path to the location on the Magento server where uploaded images are stored. For example: `var/import`.

    To learn more about importing product images, see [Importing Product Images]({% link system/data-import-product-images.md %}).

    ![]({% link images/images/data-import-file-to-import.png %}){: .zoom} 
    _File to Import_

## Step 4: Check the Import Data

1. In the upper-right corner, click **Check Data**.

1. Then, wait a few moments for the validation process to complete. If the import data is valid, the following message appears:

    ![]({% link images/images/data-import-validation-message.png %}){: .zoom}
    _File is Valid!_

1. If the file is valid, click **Import**. Otherwise, correct each problem with the data that is listed in the message, and try to import the file again.

1. The import process continues to the end of the data, unless an error is encountered.

    If an error message appears in the Validation Results, correct the problem in the data, and import the file again.

    ![]({% link images/images/data-import-validation-error-url-key-exists.png %}){: .zoom}
    _URL Key Already Exists_

    A message appears when the import is complete.

## Import Behavior

Operation | Description
--------- | -----------
**Add/Update** | New product data is added to the existing product data for the existing entries in the database. All fields except `sku` can be updated.<br>New tax classes that are specified in the import data are created automatically.<br>New product categories that are specified in the import file are created automatically.<br>New SKUs that are specified in the import file are created automatically<br>**NOTE:** For products, you can update all fields except SKU through import.
**Replace** | The existing product data is replaced with new data.<br>**NOTE:** Exercise caution when replacing data because the existing product data will be completely cleared and all  references in the system will be lost.<br>If a SKU in the import data matches the SKU of an existing entity, all fields, including the SKU are deleted, and a new record is created using the CSV data. An error occurs if the CSV file references a SKU that does not exist in the database. You can Check Data to display error.
**Delete** | Any entities in the import data that already exist in the database are deleted from the database.<br>Delete ignores all columns in the import data, except for SKU. You can disregard all other attributes in the data.<br>An error occurs if the CSV file references a SKU that does not exist in the database. You can Check Data to display error.
{:style="table-layout:auto"}
