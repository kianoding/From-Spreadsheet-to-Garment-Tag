# From Spreadsheet to AdHocDoc
## Label Generator Overview

This workflow creates physical bag tag labels for hanging garments in fashion archives. Our implementation is built using the python-docx library, following the official documentation at https://python-docx.readthedocs.io/en/latest/. We specifically utilize three core components: table creation for the 2x2 label grid (https://python-docx.readthedocs.io/en/latest/user/tables.html), text formatting for proper hierarchy and emphasis (https://python-docx.readthedocs.io/en/latest/user/text.html), and document structure for page management (https://python-docx.readthedocs.io/en/latest/user/documents.html).

The python-docx library was chosen for its straightforward API and excellent documentation, making it accessible for archivists who are new to programming. By following established patterns from the official tutorials, we ensure our code remains maintainable and adaptable for different collections.

### Working with Different Dataset Sizes

Before running the label generator, it's essential to consider your dataset size and adjust accordingly. For small collections with fewer than four items, you'll have empty spaces on your label sheet—this is normal and expected. Consider waiting to batch items together or adjusting the layout to a 1x2 grid instead. For medium-sized collections like our example of 30 garments, the standard 2x2 layout works perfectly, generating multiple pages as needed.

However, if you're working with collections of 100 or more items, we recommend processing in batches to avoid memory issues. Split your dataset into manageable chunks of 100 items each, creating separate output files that can be printed sequentially. For very large collections with thousands of items, consider transitioning to a database system rather than CSV files, as this will provide better performance and data management capabilities.

The code we provide handles all these scenarios gracefully, automatically calculating the number of pages needed and managing partial pages when your item count isn't divisible by four. This flexibility ensures the workflow adapts to real-world collection sizes without requiring code modifications.

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
