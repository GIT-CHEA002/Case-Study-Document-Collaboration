# Case Study Document Collaboration

This repository is used for **team collaboration and version control of project documents**, including:

* Markdown (`.md`) files
* Microsoft Word (`.docx`) files
* PowerPoint (`.pptx`) files
* Excel (`.xlsx`) files

> **Recommendation:** Use Markdown (`.md`) whenever possible because Git can track changes and merge text files effectively. For Microsoft Office documents, use **Git LFS**.

---

## 1. Join the Collaboration Repository

### Step 1: Send Your GitHub Username

Send your GitHub username to the repository administrator.

**Example:**

```text
git-chea002
```

The administrator will add you as a collaborator to the repository.

> ⚠️ You must accept the GitHub collaboration invitation before you can push changes.

---

## 2. Clone the Repository

After being added to the repository, clone it to your computer:

```bash
git clone https://github.com/YOUR-USERNAME/Case-Study-Document-Collaboration.git
```

Replace `YOUR-USERNAME` with the correct GitHub organization or repository owner.

---

## 3. Change to the Repository Directory

After cloning, move into the repository:

```bash
cd Case-Study-Document-Collaboration
```

You can check the repository files with:

```bash
ls
```

On Windows Command Prompt:

```bash
dir
```

---

# Working with Documents

## Option 1: Using Markdown (`.md`) — Recommended

Markdown files are recommended for documents that mainly contain text because Git can easily:

* Track changes
* Compare versions
* Merge changes from multiple team members
* Review changes through Pull Requests

### Create a Markdown File

Create a new file with the `.md` extension.

Example:

```text
introduction.md
```

You can also create it using the terminal:

```bash
touch introduction.md
```

Then edit the file using VS Code or another text editor.

### Example Markdown Structure

```md
# Project Title

## Introduction

Write your introduction here.

## Objectives

- Objective 1
- Objective 2

## Conclusion

Write your conclusion here.
```

After making changes:

```bash
git add .
git commit -m "Add introduction document"
git push
```

---

# Option 2: Using Microsoft Word and Office Documents

Microsoft Word files such as `.docx` are **binary files**. Git cannot easily compare or automatically merge their content.

Therefore, we recommend using **Git LFS (Large File Storage)** for Office documents.

Git LFS can be used for:

* `.docx` — Microsoft Word
* `.pptx` — Microsoft PowerPoint
* `.xlsx` — Microsoft Excel

---

## Step 1: Check Git LFS Installation

Check whether Git LFS is installed:

```bash
git lfs version
```

If Git LFS is installed, you should see a version number.

Initialize Git LFS:

```bash
git lfs install
```

> If the command is not recognized, install Git LFS first, then run the command again.

---

## Step 2: Configure Git LFS to Track Office Files

Run the following commands:

```bash
git lfs track "*.docx"
git lfs track "*.pptx"
git lfs track "*.xlsx"
```

This will create or update a file called:

```text
.gitattributes
```

---

## Step 3: Commit the Git LFS Configuration

After configuring Git LFS, commit the `.gitattributes` file:

```bash
git add .gitattributes
git commit -m "Configure Git LFS for Office documents"
git push
```

> ⚠️ Normally, this configuration only needs to be committed once to the repository. After pulling the latest repository, other collaborators will receive the `.gitattributes` configuration.

---

## Step 4: Add or Update Office Documents

Place your document inside the appropriate repository folder.

Example:

```text
Case-Study-Document-Collaboration/
│
├── README.md
├── .gitattributes
│
├── Documents/
│   ├── Requirements/
│   │   └── requirements.docx
│   │
│   ├── Design/
│   │   └── system-design.docx
│   │
│   └── Reports/
│       └── final-report.docx
│
└── Meeting-Notes/
```

After editing and saving your document:

```bash
git add .
git commit -m "Update project document"
git push
```

---

# Recommended Team Workflow

Before starting your work, always get the latest changes:

```bash
git pull origin main
```

Then follow this workflow:

```text
1. Pull the latest changes
        ↓
2. Edit or create your document
        ↓
3. Save your changes
        ↓
4. git add .
        ↓
5. git commit -m "Describe your changes"
        ↓
6. git push
```

Example:

```bash
git pull origin main
git add .
git commit -m "Update case study requirements"
git push origin main
```

---

# ⚠️ Important Rules for Microsoft Word Documents

## Do Not Edit the Same Word File at the Same Time

Avoid this situation:

```text
Member A → Editing report.docx
Member B → Editing report.docx at the same time
```

Git cannot automatically merge Microsoft Word files properly.

### Recommended Solution

Assign different documents or sections to different team members.

Example:

```text
Member A → Introduction.md
Member B → Requirements.md
Member C → System Design.md
Member D → Testing.md
```

Alternatively, use separate Word documents:

```text
Member A → introduction.docx
Member B → requirements.docx
Member C → system-design.docx
```

---

# Best Practice Recommendations

## For Markdown Documents

Use `.md` files when:

* Multiple people need to collaborate
* You want Git to track line-by-line changes
* You want to resolve merge conflicts
* You want to review changes using Pull Requests

## For Microsoft Office Documents

Use Git LFS when:

* The document requires Microsoft Word formatting
* You need `.docx`, `.pptx`, or `.xlsx` files
* The file is large or binary

> **Important:** Avoid multiple people editing the same Office document simultaneously.

---

# Quick Commands Reference

### Clone the Repository

```bash
git clone https://github.com/GIT-chea002/Case-Study-Document-Collaboration.git
```

### Enter the Repository

```bash
cd Case-Study-Document-Collaboration
```

### Get the Latest Changes

```bash
git pull origin main
```

### Check Repository Status

```bash
git status
```

### Add Changes

```bash
git add .
```

### Commit Changes

```bash
git commit -m "Describe your changes"
```

### Push Changes

```bash
git push origin main
```

---

# Final Recommendation

For the best collaboration experience:

* ✅ Use **Markdown (`.md`)** for documents whenever possible.
* ✅ Use **Git LFS** for Microsoft Office documents.
* ✅ Always run `git pull` before starting work.
* ✅ Commit changes with clear messages.
* ❌ Avoid editing the same `.docx` file simultaneously.
* ❌ Do not force-push (`git push --force`) to the shared `main` branch.

**Happy collaborating! 🚀**
