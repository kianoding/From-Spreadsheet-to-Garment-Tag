# From Spreadsheet to Label Generator

Python Automation for Fashion Archives

### Introduction
This tutorial teaches archivists to automate garment label creation using Python. We'll transform a CSV spreadsheet into professional bag tags for fashion collections, processing 30 items into a print-ready Word document in seconds rather than hours.
Our implementation builds on the python-docx library (https://python-docx.readthedocs.io/en/latest/), specifically utilizing table creation, text formatting, and document structure features. This approach makes the code accessible to archivists learning Python while maintaining professional output quality.

##### Before You Start
- *Time Required*: 90 minutes
- *Skill Level*: Beginner (no coding experience needed)
- *Tools*: Google Colab (free, no installation required)
- *Dataset Considerations*: This tutorial handles collections of any size. Small collections under 4 items will have empty label spaces. Medium collections like our 30-item example work perfectly. Large collections of over 100 items should be processed in batches to avoid memory issues.

------
### Chapter 1: Setup
Step 1: Open Google Colab
> Go to https://colab.research.google.com
Sign in with your Google account
Click "New Notebook"

Step 2: Upload Your Data
> Click the folder icon on the left sidebar
Click the upload icon
Upload 'Garment Bag Tag_Dataset.csv'

Step 3: Install Libraries
```ruby
# Run this first
!pip install python-docx pandas
```
You should see installation messages. 
