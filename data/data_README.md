# Dataset Directory

This directory contains the article classification dataset required for the project.

## Required File

**Filename:** `article_data.csv`  
**Size:** ~4,000 articles (balanced across 4 categories)  
**Format:** CSV with columns:
- `Article` - News article text (title + description)
- `Category` - Label (World, Sports, Business, Sci/Tech)

##  How to Obtain Dataset

### Option 1: Use Your Own Copy (If You Have It)
If you already have `article_data.csv`, simply place it in this directory:
```bash
# Copy your file to this directory
cp /path/to/your/article_data.csv ./data/
```

### Option 2: Download from Original Source
1. Visit [AG News Dataset on Kaggle](https://www.kaggle.com/datasets/amananandrai/ag-news-classification-dataset)
2. Download the AG News dataset
3. Create balanced subset:
   - 1,000 World articles
   - 1,000 Sports articles
   - 1,000 Business articles
   - 1,000 Sci/Tech articles
4. Save as `article_data.csv` in this directory

### Option 3: Request Preprocessed Dataset
Email the project author with subject "Article Dataset Request"

##  Verification

After placing the file, verify:

```bash
# Check file exists
ls -lh data/article_data.csv

# Verify git ignores it (should NOT appear)
git status
```

The file should be **present locally** but **ignored by git**.

##  Important Notes

- This file is **intentionally excluded** from version control via `.gitignore`
- This follows industry best practices (data in storage, code in git)
- The `.gitignore` patterns that exclude this file:
  ```
  data/*.csv
  *.csv
  ```
- Do not commit this file to GitHub

##  Expected Dataset Structure

```csv
Article,Category
"Title: Article headline. Description: Article content...",World
"Title: Sports news. Description: Game summary...",Sports
...
```

##  File Not Included Because

1. **Size considerations** - Keeps repository lightweight
2. **License compliance** - AG News dataset has usage restrictions
3. **Industry standard** - Separation of code and data
4. **Flexibility** - Others can use custom datasets

---

**Once you have the file in place, the notebook will load it automatically using the relative path `data/article_data.csv`**
