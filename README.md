# From Spreadsheet to AdHocDoc
## Label Generator Overview

This workflow creates physical bag tag labels for hanging garments in fashion archives. Our implementation uses the python-docx library, following the official documentation at https://python-docx.readthedocs.io/en/latest/. We specifically utilize three core components:
- [table creation](https://python-docx.readthedocs.io/en/latest/user/tables.html) for the 2x2 label grid 
- [text formatting](https://python-docx.readthedocs.io/en/latest/user/text.html) for proper hierarchy and emphasis 
- [document structure](https://python-docx.readthedocs.io/en/latest/user/documents.html) for page management

The python-docx library was chosen for its straightforward API and excellent documentation, making it accessible for archivists who are new to programming. By following established patterns from the official tutorials, we ensure our code remains maintainable and adaptable for different collections.

### Working with Different Dataset Sizes
Before running the label generator, think about how many items you have and plan accordingly:
- For <ins>small collections</ins> (fewer than four items): You will see empty spaces on the label sheet. This is normal. You can wait and batch more items together or change the layout to a 1x2 grid.
- For <ins>medium collections</ins> (about 30 items, as in our example): Use the standard 2x2 layout. This will create multiple pages automatically.
- For <ins>large collections</ins> (100 or more items): Process your data in batches of 100 items. Each batch goes into its own output file for printing. This helps avoid memory issues.

This code automatically figures out how many pages are needed and handles cases where the last page isn’t full. This means you don’t need to change any code to work with different collection sizes.

## 📖 Tutorial
Start here: [Introduction]([tutorial/00-introduction.md](https://github.com/kianoding/FromSpreadsheettoAdHocDoc/blob/main/Introduction.md))

## 🎯 What This Does
- Reads garment data from CSV
- Creates 4 labels per page
- Outputs print-ready Word document

## 📊 Sample Data
Use the included dataset in [Dataset/01_Garment Bag Tag/](Dataset/01_Garment%20Bag%20Tag/) containing:
- `Garment_Bag_Tag_Dataset.csv` with 30 garment records
- 27 sample images
- Usage rights documentation

Please review the [Dataset Usage Rights](Dataset/01_Garment%20Bag%20Tag/Dataset_Usage_Rights.md) before using any images.

## 🚀 Quick Start
1. Open Google Colab
2. Upload the CSV
3. Run the script
4. Download your labels

## 📝 License

![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)

This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/).

<img src="https://licensebuttons.net/l/by-nc/4.0/88x31.png" alt="CC BY-NC 4.0" style="max-width: 100%;">

---

INFO664: Programming for Cultural Heritage  
Pratt Institute, Fall 2024  
Created by Kelsey Kiantoro
