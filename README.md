# AI Adoption Survey Analysis - Getting Started Guide

## Overview

This notebook analyzes AI adoption survey data to identify distinct behavioral profiles and provide actionable recommendations. You don't need to be a programmer to run this analysis - just follow the steps below! The data used during the presentation is a fictitious data set to demonstrate the value of the process. Simply replacing it with your data may not result in meaningful insights without proper data preparation and validation.

**What you'll get:**
- Visual charts showing different employee groups and their AI adoption barriers
- Specific recommendations for each group based on research frameworks (MOJO and Self-Determination Theory)
- Professional-quality images you can use in presentations

---

## What You'll Need

### Computer Requirements
- **Operating System**: Windows 10/11, macOS, or Linux
- **RAM**: 4GB minimum (8GB recommended)
- **Disk Space**: ~1GB free space
- **Internet**: Required for initial setup only

### Cost
**Everything is 100% FREE** - all software and tools used are open-source and free to download.

---

## Installation Instructions (First-Time Setup)

### Step 1: Install Python (FREE)

Python is the programming language that runs this analysis. Don't worry - you won't need to write any code!

#### For Windows:
1. Go to [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Click the yellow "Download Python" button (get version 3.10 or newer)
3. **IMPORTANT**: When installing, check the box that says "Add Python to PATH"
4. Click "Install Now"
5. Wait for installation to complete (2-5 minutes)

#### For macOS:
1. Go to [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Download the macOS installer
3. Open the downloaded file and follow the installation wizard
4. Installation takes 2-5 minutes

#### For Linux:
Python is usually pre-installed. Open Terminal and type:
```bash
python3 --version
```
If you see a version number (like 3.10.x), you're good to go!

### Step 2: Extract the Downloaded Files

1. Locate the `guild-webinar.zip` file you downloaded
2. Right-click and select "Extract All" (Windows) or double-click (macOS)
3. Extract to a location you can easily find (e.g., your Desktop or Documents folder)
4. You should now have a folder called `guild-webinar`

### Step 3: Open Command Prompt / Terminal

#### Windows:
1. Press the Windows key
2. Type `cmd` and press Enter
3. A black window will open - this is the Command Prompt

#### macOS:
1. Press `Cmd + Space` to open Spotlight
2. Type `terminal` and press Enter
3. A window will open - this is the Terminal

#### Linux:
1. Press `Ctrl + Alt + T` to open Terminal

### Step 4: Navigate to the Analysis Folder

In the Command Prompt/Terminal window, type the following (adjust the path to where you extracted the files):

**Windows example:**
```bash
cd Desktop\guild-webinar\03-analysis
```

**macOS/Linux example:**
```bash
cd ~/Desktop/guild-webinar/03-analysis
```

**Tip:** You can drag and drop the folder into the Terminal window to auto-fill the path!

### Step 5: Install Required Software Packages (FREE)

Now we'll install the tools needed to run the analysis. Copy and paste this command into your Command Prompt/Terminal:

```bash
pip install scikit-learn nltk spacy matplotlib seaborn pandas numpy scipy jupyter
```

Press Enter and wait. This will take 3-10 minutes depending on your internet speed. You'll see lots of text scrolling - this is normal!

**What if I get an error?**
- If you see "pip is not recognized", try using `pip3` instead of `pip`
- If you see "permission denied", try adding `--user` at the end: `pip install --user scikit-learn nltk spacy matplotlib seaborn pandas numpy scipy jupyter`

### Step 6: Download Language Processing Models (FREE)

The analysis needs some language models to understand text. Run these two commands one at a time:

**First command:**
```bash
python -m spacy download en_core_web_sm
```
Wait for it to finish (1-2 minutes), then run:

**Second command:**
```bash
python -c "import nltk; nltk.download('stopwords'); nltk.download('punkt_tab')"
```

You should see messages saying "Download successful" for both.

---

## Running the Analysis (Every Time You Use It)

### Step 1: Check Your Data File

The analysis needs a CSV file (like an Excel spreadsheet saved as CSV) with your survey data.

**Included sample data:**
- A file called `ai_adoption_survey_data.csv` is already in the `03-analysis` folder
- This is demo data you can use to test the analysis
- To use your own data, replace this file with your survey data (keep the same filename)

**Your data should have these columns:**
- Survey responses on a 1-5 scale (Strongly Disagree to Strongly Agree)
- Open-ended text responses where people describe their challenges and needs
- See the sample file for the exact format

### Step 2: Open the Analysis Notebook

Make sure you're still in the Command Prompt/Terminal from the installation steps. If you closed it, reopen it and navigate back to the folder:

**Windows:**
```bash
cd Desktop\guild-webinar\03-analysis
```

**macOS/Linux:**
```bash
cd ~/Desktop/guild-webinar/03-analysis
```

Now launch Jupyter Notebook by typing:
```bash
jupyter notebook
```

**What happens next:**
- A web browser window will automatically open (this is normal!)
- You'll see a file browser showing the contents of the `03-analysis` folder
- Click on `ai_adoption_analysis.ipynb` to open the notebook

**Note:** Don't close the Command Prompt/Terminal window - keep it running in the background!

### Step 3: Run the Analysis

Once the notebook opens in your browser:

1. Click on the "Cell" menu at the top
2. Select "Run All"
3. Wait 2-5 minutes while the analysis runs
4. You'll see charts and results appear below each section

**What you'll see:**
- Progress messages as each step completes
- Colorful charts showing different employee groups
- Statistical summaries and recommendations
- All charts are automatically saved as PNG image files in the `03-analysis` folder

### Step 4: View Your Results

After the analysis finishes:

1. Look in the `03-analysis` folder on your computer
2. You'll find 9 PNG image files with professional charts
3. These images can be copied into PowerPoint, Word, or any presentation software
4. The notebook itself contains detailed explanations of what each chart means

**To close Jupyter when you're done:**
1. Close the browser window
2. Go back to the Command Prompt/Terminal
3. Press `Ctrl + C` twice
4. You can now close the Command Prompt/Terminal window

---

## Output Files

The notebook generates the following visualizations (saved as PNG files at 300 DPI):

1. `mojo_aggregated_scores.png` - Company-wide MOJO scores
2. `kmeans_hyperparameter_selection.png` - K-Means elbow and silhouette plots
3. `cpa_scatter_plot.png` - PCA scatter plots (ground truth vs discovered clusters)
4. `pca_loadings_plot.png` - PCA component loadings
5. `nmf_hyperparameter_selection.png` - NMF reconstruction error
6. `nmf_topic_modeling.png` - NMF topic word weights
7. `method_alignment_kmeans_nmf.png` - Cross-tabulation heatmap and ARI comparison
8. `mojo_profile_heatmap.png` - MOJO scores by persona
9. `action_priority_matrix.png` - Motivation vs Opportunity scatter plot

All images are saved in the same directory as the notebook.

---

## Troubleshooting Common Issues

### "Python is not recognized" or "pip is not recognized"

**Problem:** You see an error message saying Python or pip is not found.

**Solution:**
1. Make sure you installed Python (Step 1 above)
2. During installation, you must check the box "Add Python to PATH"
3. If you missed this, uninstall Python and reinstall it, making sure to check that box
4. After reinstalling, close and reopen Command Prompt/Terminal

### "Permission denied" errors when installing packages

**Problem:** You get permission errors when running `pip install`.

**Solution:** Add `--user` to the end of the command:
```bash
pip install --user scikit-learn nltk spacy matplotlib seaborn pandas numpy scipy jupyter
```

### Jupyter opens but shows "Kernel error" or won't run cells

**Problem:** The notebook opens but cells won't execute.

**Solution:**
1. Close the browser window
2. In Command Prompt/Terminal, press `Ctrl + C` twice to stop Jupyter
3. Run this command: `pip install --upgrade jupyter`
4. Try launching Jupyter again: `jupyter notebook`

### "File not found: ai_adoption_survey_data.csv"

**Problem:** The notebook can't find your data file.

**Solution:**
1. Make sure your CSV file is in the `guild-webinar/03-analysis` folder
2. The filename must be exactly `ai_adoption_survey_data.csv` (check spelling and capitalization)
3. Make sure it's a CSV file, not an Excel file (.xlsx)

### The analysis runs but produces errors or strange results

**Problem:** You see error messages or unexpected output.

**Solution:**
1. In the Jupyter notebook, click "Kernel" → "Restart & Clear Output"
2. Then click "Cell" → "Run All" to start fresh
3. If errors persist, your data format may not match the expected structure (see sample file)

### Computer runs very slowly or freezes

**Problem:** Your computer becomes unresponsive during analysis.

**Solution:**
1. Close other programs to free up memory
2. If you have a very large dataset (>1000 responses), the analysis may take longer
3. Wait patiently - the analysis can take 5-10 minutes for large datasets

### Need More Help?

If you're still stuck:
1. Check that you completed ALL installation steps (Steps 1-6)
2. Try restarting your computer and starting from "Running the Analysis"
3. Make sure your data file matches the format in the included sample file

---

## Understanding Your Results

The analysis produces 9 professional charts. Here's what each one shows:

### 1. Company-wide MOJO Scores
Shows average scores across all employees for Motivation, Opportunity, Job Capability, and Outcome. This is the "traditional" view that hides important differences.

### 2. K-Means Cluster Selection
Technical chart showing how the analysis chose to divide employees into 5 groups. You can skip this one for presentations.

### 3. PCA Scatter Plots
**This is a key chart!** Shows how employees cluster into distinct groups based on their survey responses. Each color represents a different behavioral profile.

### 4. PCA Loadings
Shows which survey questions drive the differences between groups. Useful for understanding what separates the groups.

### 5. NMF Topic Selection
Technical chart for topic modeling. You can skip this for presentations.

### 6. NMF Topic Themes
Shows the main themes people wrote about in open-ended responses (e.g., "Structural Barriers", "Trust Concerns").

### 7. Method Alignment
Shows how well the quantitative (survey ratings) and qualitative (text responses) analyses agree. Higher agreement = more confidence in the findings.

### 8. MOJO Profile Heatmap
**This is your most important chart!** Shows exactly where each employee group struggles - Motivation, Opportunity, Capability, or Outcomes. Use this to target interventions.

### 9. Action Priority Matrix
**Great for executives!** Shows which groups need what type of intervention (e.g., remove barriers vs. build skills vs. provide evidence).

---

## What the Analysis Tells You

The notebook identifies **5 distinct employee groups**:

1. **Eager Adopters** - High motivation and capability, need organizational support to scale
2. **Willing but Blocked** - Want to use AI but face structural barriers (time, access, approval processes)
3. **Overwhelmed Learners** - Motivated but lack skills and confidence
4. **Skeptical Observers** - Need evidence and trust-building before adopting
5. **Mandated but Disengaged** - Lack intrinsic motivation, need autonomy and meaning

Each group needs **different interventions** - the notebook provides specific recommendations based on Self-Determination Theory.

---

## Using Your Own Survey Data

To analyze your own data instead of the demo data:

1. Export your survey results to CSV format (from Excel, Google Sheets, Qualtrics, etc.)
2. Make sure your CSV has:
   - Survey questions on a 1-5 scale (Strongly Disagree to Strongly Agree)
   - At least 3 open-ended text response columns
   - Column names that match the sample file structure
3. Save it as `ai_adoption_survey_data.csv` in the `guild-webinar/03-analysis` folder
4. Run the analysis following the steps in "Running the Analysis" above

**Tip:** Open the included sample file to see the exact format your data should follow.

---

## Quick Reference: Running the Analysis

**Every time you want to run the analysis:**

1. Open Command Prompt (Windows) or Terminal (macOS/Linux)
2. Navigate to the folder: `cd Desktop\guild-webinar\03-analysis` (adjust path as needed)
3. Launch Jupyter: `jupyter notebook`
4. Click on `ai_adoption_analysis.ipynb` in the browser
5. Click "Cell" → "Run All"
6. Wait 2-5 minutes
7. Find your charts in the `03-analysis` folder
8. Close browser, press `Ctrl + C` twice in Command Prompt/Terminal

---

## About This Analysis

**Methods Used:**
- Component Pattern Analysis (PCA + K-Means clustering)
- Non-negative Matrix Factorization (NMF) for text analysis
- MOJO Framework (Motivation, Opportunity, Job Capability, Outcome)
- Self-Determination Theory (Deci & Ryan, 1985)

**Created for:** L&D professionals, People Analytics teams, and organizational researchers

**Cost:** 100% free and open-source

---

**Questions?** Review the Troubleshooting section or check the detailed explanations in the notebook itself.

**Last Updated:** March 2026 | **Version:** 1.0
