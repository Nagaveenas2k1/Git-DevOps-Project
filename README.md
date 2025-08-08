# Git-branch DevOps Project

## Project Overview

This project demonstrates a standard DevOps Git workflow, including creation and management of `main`, `dev`, and `feature branches`. It covers file additions, branching, merging, tagging, and documentation—all using best practices.

---

## Table of Contents

- [Project Setup](#project-setup)
- [Branching Workflow](#branching-workflow)
- [Adding and Committing Files](#adding-and-committing-files)
- [Feature Development](#feature-development)
- [Pull Request & Merging Process](#pull-request--merging-process)
- [Tagging Releases](#tagging-releases)
- [Frequently Used Git Commands](#frequently-used-git-commands)
- [File Descriptions](#file-descriptions)

---

## Project Setup

1. **Initialize the repository**
    ```
    git init
    ```

2. **Create basic files**
    - `README.md` (this file)
    - `.gitignore`
    - `sample.py` (basic practice script)

3. **Add and commit files**
    ```
    git add .
    git commit -m "Initial commit: add README, .gitignore, sample.py"
    ```

4. **Rename default branch (if needed):**
    ```
    git branch -m master main
    ```

5. **Connect to GitHub and push main**
    ```
    git remote add origin https://github.com/<your-username>/<your-repo>.git
    git push -u origin main
    ```

---

## Branching Workflow

1. **Create dev branch from main**
    ```
    git checkout -b dev
    git push -u origin dev
    ```

2. **Create a feature branch from dev**  
   (Example: practice script)
    ```
    git checkout dev
    git checkout -b feature/practice-script
    git push -u origin feature/practice-script
    ```

---

## Adding and Committing Files

1. **Edit or add files in the feature branch**
    - Example content for `sample.py`:
        ```
        def main():
            print("Hello, DevOps Intern! This is a practice script.")

        if __name__ == "__main__":
            main()
        ```

2. **Stage and commit changes**
    ```
    git add sample.py
    git commit -m "Added practice Python script"
    git push
    ```

---

## Feature Development

- All new features **must be created in a new feature branch from dev**.
- Make all edits and commits in the feature branch first.

---

## Pull Request & Merging Process

**On GitHub:**

1. **Merge feature branch into dev**
    - Go to Pull Requests tab.
    - Click "New Pull Request".
    - Base branch: `dev`
    - Compare branch: `feature/practice-script`
    - Add a title and description:
        ```
        Merge feature/practice-script into dev: add basic practice script.
        ```
    - Submit and merge pull request.

2. **Test in dev**  
   Pull the latest changes into your local dev branch if needed:
    ```
    git checkout dev
    git pull origin dev
    ```

3. **Merge dev into main (for release)**
    - On GitHub, create a new Pull Request:
   
        - Base branch: `main`
        - Compare branch: `dev`
        - Add a message:
            ```
            Merge dev into main: integrate tested development changes for release.
            ```
    - Submit and merge pull request.

---

## Tagging Releases

**Tag the release on main:**

1. **Create a tag**
    ```
    git tag -a v1.0.0 -m "Release version 1.0.0"
    ```

2. **Push the tag to GitHub**
    ```
    git push origin v1.0.0
    ```

---

## Frequently Used Git Commands

### 1.Create a new branch from current branch

- git checkout -b branch-name

### 2.Switch branches

- git checkout branch-name

### 3.Add all changes

- git add .

### 4.Commit changes

- git commit -m "Commit message"

### 5.Push changes to remote

- git push origin branch-name

### 6.Merge branches (locally)

- git checkout dev
- git merge feature/practice-script

### 7.Tag a commit

- git tag -a v1.0.0 -m "Release notes"
- git push origin v1.0.0

---

## File Descriptions

| File Name     | Purpose                               |
|---------------|---------------------------------------|
| README.md     | Project instructions & documentation  |
| .gitignore    | Specifies files ignored by Git        |
| sample.py     | Practice Python script                |

---

## Conclusion

This project follows DevOps best practices for version control and collaboration. All steps are clearly documented.  

## Author
S Nagaveena

