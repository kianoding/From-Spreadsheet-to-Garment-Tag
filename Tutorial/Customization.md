# Customization Guide
This design and layout descisions are based on the manual 8.5x1" Letter size paper we used for the garment tag.
Which will be easier to be cut toegther with paper timmer. If you do have different preferences, feel free to duplicate and customize your own.

##Before You Start
### Step 1: Data Preparation

**Your CSV Must Have These Columns:**
| Column | Description | Example |
|--------|-------------|---------|
| `identifier` | Unique catalog number | C2025-0169-LL |
| `designer` | Designer name | Mary McFadden |
| `description` | Item description (max 200 chars) | Purple charmeuse evening gown... |
| `item_type` | Garment category | Evening Dress |
| `image_URL` | Image filename | C2025-0169-LL.jpg |


**Your Images:**
- **Format:** `.jpg` only (not .jpeg or .png)
- **Location:** Upload to `images/` folder
- **Naming:** Must match CSV exactly (case-sensitive)
- **Quality:** Phone photos are fine (for ID, not publication)

##### 💡 Pro Tips: Bulk format your images before hand using Adobe Bridge
---

##Step 2: Customization
In the Chapter 3 - Step 1.
### Change Your Institution Name:
```python
institution = "Pratt"  # ← Change to your institution

# Examples:
institution = "MET"
institution = "Brooklyn_Museum"
institution = "FIT"
```

In the Chapter 3 - Step 1, Code Line 84.
### Adjust Footer Text (Optional):
```python
# Find these lines:
pdf.drawCentredString(center_x, y + 30, f"{institution} Fashion Design")
pdf.drawCentredString(center_x, y + 15, "STUDY COLLECTION")

# Change to:
pdf.drawCentredString(center_x, y + 30, f"{institution} Costume Collection")
pdf.drawCentredString(center_x, y + 15, "PERMANENT COLLECTION")
```

---

# Troubleshooting Guide

### Common Issues & Quick Fixes

| Problem | Solution |
|---------|----------|
| **Images not appearing** | Check filename matches exactly: `C2025-0169-LL.jpg` ≠ `c2025-0169-ll.jpg` |
| **"NameError: total_pages not defined"** | Run the complete code block from start, not just parts |
| **Description text cut off** | Shorten to under 200 characters in your CSV |
| **PDF over 10MB** | Images too large - resize to under 1MB each before uploading |
| **Labels appear on 2 pages** | Normal in preview - will print correctly on letter paper |
| **"No module named reportlab"** | Run the installation cell: `!pip install reportlab pandas pillow` |


### Still Having Issues?
**Before asking for help, check:**
1. Did you run ALL cells in order?
2. Is your CSV named exactly `Garment_Bag_Tag_Dataset.csv`?
3. Are ALL images in `.jpg` format (not .jpeg or .JPG)?
4. Did you create the `images/` folder?

**File Structure Should Be:**
```
Google Colab Environment/
├── Garment_Bag_Tag_Dataset.csv
└── images/
    ├── C2025-0169-LL.jpg
    ├── C2025-0170-LL.jpg
    └── (other .jpg files)
```

---

##Final Thoughts
- **Batch Large Collections:** Process 100 items at a time
- **Missing Images OK:** Script continues with placeholder text
- **Multiple Runs:** Files auto-number (Label.pdf, Label_1.pdf, Label_2.pdf)

---

  <b>Ready to generate labels?</b><br><br>
  <a href="[https://colab.research.google.com/github/YOUR_USERNAME/FromSpreadsheettoAdHocDoc/blob/main/garment_label_generator.ipynb](https://colab.research.google.com/drive/1_ZXEGGPbl8gD7UrTQnzXIRVK0BJ6YDlJ?usp=sharing)"> Open Colab Notebook</a> • 
  <a href="/Tutorial/Introduction.md"> Back to __Introduction__ </a>
</p>

---
