# Setup and Build Instructions for OpenBoardJ

This file contains the instructions to clone, set up the environment, and configure Qt Creator for OpenBoardJ.

---

### 1. Initial Repository Setup (WSL)

Execute these commands in your terminal to clone the repository and enforce LF line endings (for Windows Users):

```bash
# Prevent Windows from adding CR to LF newlines
git config --global core.autocrlf false

# Clone YOUR fork of the repository
# Replace [YOUR_GITHUB_USERNAME] with your actual GitHub username
git clone git@github.com:[YOUR_GITHUB_USERNAME]/OpenBoardJ.git OpenBoardJ
cd OpenBoardJ

# Add the original repository as 'upstream'
git remote add upstream https://github.com/OpenBoard-org/OpenBoard.git
# Verify remotes
git remote -v

# Create and switch to your work branch
git checkout -b wip/analysis
git branch

# Optional
    # Enforce LF line endings across all platforms
    echo "* text=auto eol=lf" > .gitattributes
    git add .gitattributes
    git commit -m "Set LF normalization"
    git push -u origin wip/analysis
```

---

### 2. Workflow: Syncing with Upstream

Use these commands to keep your branch updated with the original repository:

```bash
# 1. Return to master
git checkout master
# 2. Fetch changes from original
git fetch upstream
# 3. Update your local master
git merge upstream/master
# 4. Push updates to your fork
git push origin master
# 5. Return to your analysis branch and merge master
git checkout wip/analysis
git merge master

```

---

### 3. Qt Creator Configuration

To run the project successfully, you need to add the third-party dependencies to your system `Path`.

1. Open **Project** > **Run Settings** > **Environment**.
2. Ensure **"Build Environment"** is selected in the "Base environment for this run configuration" dropdown.
3. Add the following to the `Path` variable. **Important:** Replace `[PATH_TO_THIRDPARTY]` with the actual directory where you have cloned/downloaded the `OpenBoard-ThirdParty` folder:

```text
Path+=[PATH_TO_THIRDPARTY]\quazip\lib\win32\debug;[PATH_TO_THIRDPARTY]\poppler\debug\lib;[PATH_TO_THIRDPARTY]\zlib\1.2.11\lib;[PATH_TO_THIRDPARTY]\poppler\bin;[PATH_TO_THIRDPARTY]\zlib\1.2.11\bin;
```
