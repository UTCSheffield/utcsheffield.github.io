# SimpleHTML5

A multipage static site template using semantic HTML5 and responsive CSS3 layouts.

## Features
- Semantic HTML5 structure
- Responsive CSS3 design

## Version 1 (root directory)
- Basic static HTML5 and CSS3 files

## Version 2 (v2 directory)
- Enhanced styling with CSS3 Flexbox and Grid
- Improved accessibility features

## Version 3 (v3-src directory)
- Static site generation using Jinja2 templates
- Automated build process with Python script
- Modular template structure for easy maintenance
- Output static files in build directory  

### Usage
1. Ensure you have Python and Jinja2 installed.
2. Run the build script to generate the static site:
   ```bash
   python build-v3.py
   ```  
3. The generated static files will be available in the `build` directory.

### GitHub Pages deploy workflow (disabled)

A GitHub Actions workflow to build v3 and publish the `build/` directory to GitHub Pages is included at `.github/workflows/deploy-pages.yml`, but it is intentionally disabled.

To activate the deploy workflow:
1. Edit `.github/workflows/deploy-pages.yml` and remove the line `if: false`
 (or change it to the trigger you want).
2. Commit and push the change to the repository's default branch (e.g. `main`).
3. (Optional) In the repository Settings → Actions, ensure Actions are enabled 
for the repository.
4. In the repository Settings → Pages, you can confirm the site is served via 
"GitHub Actions" after the workflow runs successfully.

Once activated, the workflow will:
- Install Python and Jinja2
- Run `python build-v3.py`
- Upload the contents of `build/` and deploy them to GitHub Pages

If you want to test without publishing, keep `if: false`, or change the `on:` 
triggers to a branch you use for testing.


