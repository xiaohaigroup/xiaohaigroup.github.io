# How to Build Your Own Wiki Page

## Previewing Your Markdown Page

We recommend using the same engine as the site — **MkDocs** — so you can preview and develop your pages locally.

### For Windows:

**1. Open PowerShell and install MkDocs**

```powershell
# Install MkDocs (and pip if needed)
# python -m pip install --upgrade pip
pip install mkdocs
```

**2. Download the site from GitHub and work locally**
```powershell
# Choose a working folder and clone the repo
git clone https://github.com/<xiaohaigroup>/<xiaohaigroup.github.io>.git

# Go into the project
cd <xiaohaigroup>
```

**3. Serve the site locally (hot-reload preview)**

```powershell
mkdocs serve
```

Now open the URL it prints (usually http://127.0.0.1:8000). MkDocs will auto-reload when you edit files.


**4. Add your new wiki page (under `docs/`)**

Prepare your own Markdown file and place it inside the `docs/` folder. If you need a new subdirectory, create it under `docs/` as well.

Examples:
```powershell
# Simple, top-level page
ni .\docs\my-new-page.md

# Or create a new section directory with a page inside it
mkdir .\docs\my-new-dir
ni .\docs\my-new-dir\my-new-page.md
```

Start writing in Markdown, and please follow the syntax of other files.

Assets like images should also live under `docs/images/` and be referenced with relative paths: `![Alt text](images/my-new-plot.png)`.


**5. Add the page to the navigation (`mkdocs.yml`)**

Open `mkdocs.yml` in the repo root and add your new page to the `nav:` section. Match the existing style and indentation (YAML is whitespace-sensitive). Here are common patterns; use the one that matches your current config best.

```yaml
nav:
  - Home: index.md
  - WIKI: my-new-page.md
      - New Name 1: my-new-page.md
      - New Name 2: my-new-dir/my-new-page.md
```
Paths are relative to docs.


**6. Commit → Push a branch → Open a PR**










**4. Add your new wiki page (under `docs/`)**

**4. Add your new wiki page (under `docs/`)**

**4. Add your new wiki page (under `docs/`)**
