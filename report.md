# Portfolio Refactoring Report

## Project: Neural Network Practice Notebook

**Start Time:** 2025-12-26T20:28:06.727Z

---

## Phase 0: Initial Self-Setup

### 0.1 Created Required Files
- Created report.md (this file)
- Will create: suggestion.txt, suggestions_done.txt, project_identity.md

### 0.2 Copilot Guidance Files
- `.github/copilot-instructions.md` already exists - no changes needed

---

## Phase 1: Understanding the Project

### Initial Repository State
- **Main File:** Exercise4.ipynb (Jupyter notebook)
- **Supporting Files:** README.md, requirements.txt
- **Structure:** Single-level, minimal structure

### Project Analysis
The project is a neural network implementation exercise that:
- **Domain:** Machine learning / Deep learning education
- **Method:** Implementation of a two-layer neural network from scratch using NumPy
- **Problem:** MNIST digit classification (handwritten digits 0-9)
- **Approach:** Custom implementation of forward/backward propagation with ReLU and softmax activations
- **Stack:** Python, Jupyter Notebook, NumPy, scikit-learn
- **Inputs:** MNIST dataset (loaded via scikit-learn's fetch_openml)
- **Outputs:** Training loss metrics, test accuracy (~90%)

### Current Issues Identified
1. **Assignment Traces:**
   - README.md: "University Assignment/Task", "NNTI Exercise 4"
   - README.md: "Submission_8_-_7072982_Syed_Rumman_Ali/" folder reference
   - Notebook title: "Exercise 4"
   - Notebook content: "In this exercise..." (assignment language)

2. **Naming Issues:**
   - File: "Exercise4.ipynb" - generic exercise naming
   - No professional project identity

3. **Structure Issues:**
   - No .gitignore file
   - Minimal folder structure (flat)

---

### Naming Alignment Plan

Based on the professional identity defined in project_identity.md, the following changes are planned:

**File Renames:**
1. `Exercise4.ipynb` → `mnist_classifier.ipynb`
   - Reason: Remove "Exercise" assignment framing; use descriptive, professional name
   - Impact: Update README.md references
   - Safety: No import dependencies to update

**Content Updates (not renames):**
1. README.md: Complete rewrite to portfolio-grade format
   - Remove: Course codes (NNTI), assignment language, submission folder references
   - Add: Professional description, setup instructions, reproducibility notes
   
2. Exercise4.ipynb notebook cells:
   - Update title from "Exercise 4" to professional title
   - Remove assignment instructions and grading rubric
   - Convert instructional language to documentation
   
**No Folder Restructuring:**
- Current flat structure is acceptable for this small project
- All files remain at repo root level

**Assessment:** Changes are SAFE - no complex dependency chains, no imports to update, only filename and content updates.

---

## Phase 2: Pre-Change Audit

### Audit Complete
All findings have been logged to `suggestion.txt` with the following breakdown:

**Assignment Traces Found:**
- README.md: 7 instances (title, project type, course description, folder references)
- Exercise4.ipynb: 6 instances (title, instructions, point values)

**Path Issues Found:**
- None (no absolute or brittle paths detected)

**Naming Issues Found:**
- 1 file: Exercise4.ipynb needs professional rename

**Structure Issues Found:**
- Missing .gitignore file

**Total Suggestions Logged:** 15 entries in suggestion.txt

---

