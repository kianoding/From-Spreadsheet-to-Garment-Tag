# FromSpreadsheettoAdHocDoc

## Label Generator Overview

This workflow creates physical bag tag labels for hanging garments in fashion archives. Our implementation is built using the python-docx library, following the official documentation at https://python-docx.readthedocs.io/en/latest/. We specifically utilize three core components: table creation for the 2x2 label grid (https://python-docx.readthedocs.io/en/latest/user/tables.html), text formatting for proper hierarchy and emphasis (https://python-docx.readthedocs.io/en/latest/user/text.html), and document structure for page management (https://python-docx.readthedocs.io/en/latest/user/documents.html). 

The python-docx library was chosen for its straightforward API and excellent documentation, making it accessible for archivists who are new to programming. By following established patterns from the official tutorials, we ensure our code remains maintainable and adaptable for different collections.
----
### Working with Different Dataset Sizes

Before running the label generator, it's essential to consider your dataset size and adjust accordingly. For small collections with fewer than four items, you'll have empty spaces on your label sheet—this is normal and expected. Consider waiting to batch items together or adjusting the layout to a 1x2 grid instead. For medium-sized collections like our example of 28 garments, the standard 2x2 layout works perfectly, generating multiple pages as needed.

However, if you're working with collections of 100 or more items, we recommend processing in batches to avoid memory issues. Split your dataset into manageable chunks of 100 items each, creating separate output files that can be printed sequentially. For very large collections with thousands of items, consider transitioning to a database system rather than CSV files, as this will provide better performance and data management capabilities.

The code we provide handles all these scenarios gracefully, automatically calculating the number of pages needed and managing partial pages when your item count isn't divisible by four. This flexibility ensures the workflow adapts to real-world collection sizes without requiring code modifications.


Shield: ![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)

This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License](https://camo.githubusercontent.com/7c5a351792d77b3e4294b5b9a41d6b01e8dd69a2a00ef0437b806dcbef151656/68747470733a2f2f6c6963656e7365627574746f6e732e6e65742f6c2f62792d6e632f342e302f38387833312e706e67).

<img src="https://camo.githubusercontent.com/7c5a351792d77b3e4294b5b9a41d6b01e8dd69a2a00ef0437b806dcbef151656/68747470733a2f2f6c6963656e7365627574746f6e732e6e65742f6c2f62792d6e632f342e302f38387833312e706e67" alt="CC BY-NC 4.0" data-canonical-src="https://licensebuttons.net/l/by-nc/4.0/88x31.png" style="max-width: 100%;">

