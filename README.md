# How to Push a Local Git Repository to GitHub

## Step 1: Initialize Git (if not already done)
If your local directory isn't a Git repo yet, initialize it:

```bash
git init
```

## Step 2: Add your project files to staging
```bash
git add .
```
This stages all changes in your directory.

## Step 3: Commit the changes
```bash
git commit -m "Initial commit"
```
Provide a meaningful commit message.

## Step 4: Create a GitHub repository
1. Go to [GitHub](https://github.com).
2. Click on **New Repository**.
3. Name your repository and set it as public or private.
4. Don't initialize with a README (since you already have files).
5. Click **Create repository**.

## Step 5: Link your local repo to the remote GitHub repo
Copy the remote URL from the newly created GitHub repo and add it as a remote origin:

```bash
git remote add origin <repository-url>
```
Example:
```bash
git remote add origin https://github.com/username/my-project.git
```

## Step 6: Push your local changes to GitHub
```bash
git branch -M main
git push -u origin main
```

## Step 7: Verify the push
Visit your repository on GitHub to see your uploaded project.

---

### Troubleshooting Tips
- **Authentication Errors:** Ensure you're logged in using `gh auth login` or generate a [personal access token](https://github.com/settings/tokens).
- **Permission Errors:** Double-check the repository URL and your permissions.
- **Branch Conflicts:** Use `git pull origin main --rebase` to sync changes before pushing.
