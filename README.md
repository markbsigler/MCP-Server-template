# MCP-Server-template
A general purpose template for creating an MCP Server project from a AI prompt

## How to Setup a New Project

If you want to use this template to create a completely new MCP server project (without the original history and disconnected from this template), follow these steps:

### Step 1: Clone and Remove Git History

```bash
git clone https://github.com/markbsigler/MCP-Server-template.git
cd MCP-Server-template
rm -rf .git
```

### Step 2: Initialize as New Git Repository

```bash
git init
git add .
git commit -m "Initial commit"
```

### Step 3: Create New Repository on GitHub

1. Go to GitHub.com and click the **+** icon
2. Select **New repository** 
3. Enter **&lt;newMCPrepo&gt;** as the repository name
4. Choose public/private
5. **Don't** check any initialization options (README, .gitignore, license)
6. Click **Create repository**

### Step 4: Connect to Your New Repository

```bash
git branch -M main
git remote add origin https://github.com/&lt;username&gt;/&lt;newMCPrepo&gt;.git
git push -u origin main
```

### Step 5: Rename the Local Folder

```bash
cd ..
mv MCP-Server-template &lt;newMCPrepo&gt;
cd &lt;newMCPrepo&gt;
```

Now you have your new MCP project ready to go - completely independent from the original template with a fresh git history!
