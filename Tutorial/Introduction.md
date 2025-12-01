# From Spreadsheet to Garment Tag
Python Automation for Fashion Archives

> [!CAUTION]
> **DISCLAIMER OF FACTUAL ACCURACY**
> 
> The dataset provided in this repository is designed purely for **demonstration and practice coding purposes**. While the general scenario and structure may be inspired by real-world experiences of the author, all identifying information, specific details, names, entities, and events have been significantly modified, abstracted, and fictionalized.
> 
> The data does not represent an exact factual account of any specific case, person, or entity. **It has been altered solely to protect privacy and provide a generalized, abstract scenario for educational use.**
> 
> Users should not draw real-world conclusions, apply this data as factual information, or use it for any purpose other than practicing code. We disclaim all liability for any reliance on this information as fact.


### Introduction
This tutorial teaches archivists to automate garment label creation using Python. We'll transform a CSV spreadsheet into professional bag tags for fashion collections, processing 30 items into a print-ready PDF document in seconds rather than hours. You need to have a Google Account to run this on Google Colab/if you have Visual Studio Code, the code should run perfectly fine.

<div align="left">
  <img src="/Tutorial/BeforeAfter.jpg" alt="Before and After: Manual vs Automated Label Creation with no paper errors" width="800">
  <br>
  <i>From hours of manual work to minutes of automation</i>
</div>

##### The Issue
Picture this: You're in a fashion archive storage room with 500 garments in protective bags on racks. A researcher needs "the purple McFadden evening dress from 1989." Without external tags, you'd have to:

The traditional method of creating these tags > typing each row individually in Word, is painfully slow. For 30 garments, this means:
```mermaid
graph LR
    %% Define the Top 3 Steps (Nodes A, B, C)
    A[1. Opening Word] --> B[2. Typing identifier, designer, description];
    B --> C[3. Formatting each label];

    %% Define the Bottom 2 Steps (Nodes D, E)
    D[4. Finding and inserting images] --> E[5. Copying and pasting into a grid];

    %% Connect the steps horizontally
    C --> D;

    %% Create the Cycle (Right to Left) with Annotation
    E -.->|Repeat 30 times...| A;

    %% Adjust styling for the loop annotation (optional: makes the loop line dotted)
    linkStyle 4 stroke-dasharray: 5 5;
```
This tutorial automates the entire process and reduces paper waste from the margin of error we might have. What took 3-4 hours now takes ~15 minutes with a prepared .csv and images.

## Sample Data
Use the included files in the '[Resource](/Resource)' Folder:
- `Garment_Bag_Tag_Dataset.csv` file, which contains garment records.
- 27 image files in .jpg format
- the .ipnyb or The Spreadsheet to Garment Tag automation code

> [!IMPORTANT]
**Please review the [Dataset Usage Rights](Dataset/Dataset%20Usage%20%26%20Rights.md) before using any images.**

> #### A Note About Images
> **Important:** The photos on these tags are for quick identification, not publication. A phone photo taken in storage is perfectly adequate.

## Dataset Considerations
Before starting, consider your collection size:
- **Medium (4-100 items):** Perfect for this tutorial
- **Large (>100 items):** Process in batches

--
### Ready? Let's begin by opening the Google Colab below in a new tab.
> [!IMPORTANT]
> You need a Pratt Gmail account to access this Google Colab!

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1_ZXEGGPbl8gD7UrTQnzXIRVK0BJ6YDlJ?usp=sharing)

📝 **Note:** If you are ready to make your own? Read the [Customization Guide](Customization.md) for data preparation tips.
