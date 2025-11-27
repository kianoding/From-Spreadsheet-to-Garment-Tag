# From Spreadsheet to AdHocDoc
## Label Generator Overview

This workflow creates physical bag tag labels for hanging garments in fashion archives. Our implementation uses the python-docx library, following the official documentation at https://python-docx.readthedocs.io/en/latest/. We specifically utilize three core components:
- [table creation](https://python-docx.readthedocs.io/en/latest/user/tables.html) for the 2x2 label grid 
- [text formatting](https://python-docx.readthedocs.io/en/latest/user/text.html) for proper hierarchy and emphasis 
- [document structure](https://python-docx.readthedocs.io/en/latest/user/documents.html) for page management

We chose the python-docx library because it is easy to use and has clear instructions. This makes it simple for archivists with little programming experience. By following the official tutorials, we keep our code easy to update and change for different collections.

### Working with Different Dataset Sizes
Before running the label generator, think about how many items you have and plan accordingly:
- For <ins>small collections</ins> (fewer than four items): You will see empty spaces on the label sheet. This is normal. You can wait and batch more items together or change the layout to a 1x2 grid.
- For <ins>medium collections</ins> (about 27 items, as in our example): Use the standard 2x2 layout. This will create multiple pages automatically. We recommended having an even number; the sample is within an odd number for example purposes.
- For <ins>large collections</ins> (100 or more items): Process your data in batches of 100 items. Each batch is written to its own output file for printing. This helps avoid memory issues.

This code automatically figures out how many pages are needed and handles cases where the last page isn’t complete. This means you don’t need to change any code to work with different collection sizes.

## 📖 Tutorial
Start here: [Introduction]([tutorial/00-introduction.md](https://github.com/kianoding/FromSpreadsheettoAdHocDoc/blob/main/Introduction.md))
To get started quickly, open Google Colab, upload the CSV file, run the script, and then download your labels.

## 🎯 What This Does
The program reads garment data from a CSV file. It creates four labels on each page. The program outputs a print-ready Word document.

## 📊 Sample Data
Use the included dataset in `Dataset/01_Garment Bag Tag/`.This dataset consists of the `Garment_Bag_Tag_Dataset.csv` file, which contains garment records, 27 sample images, and usage rights documentation.

Please review the [Dataset Usage Rights](Dataset/01_Garment%20Bag%20Tag/Dataset_Usage_Rights.md) before using any images.


## 📝 License
![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)

This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/).

<img src="https://licensebuttons.net/l/by-nc/4.0/88x31.png" alt="CC BY-NC 4.0" style="max-width: 100%;">

---

INFO664: Programming for Cultural Heritage  
Pratt Institute, Fall 2024  
Created by Kelsey Kiantoro
